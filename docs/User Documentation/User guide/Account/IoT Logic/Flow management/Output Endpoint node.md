
[Account](..\..\..\Account.md) > [IoT Logic](..\..\IoT%20Logic.md) > [Flow management](..\Flow%20management.md)

# Output Endpoint node

## Technical overview and capabilities

![image-20250407-210332.png](..\..\..\..\attachments\b25a3327-9103-4182-9bfb-ba6d317b2f70.png)

**Output Endpoint node** serves as the data transmission component within IoT Logic flows, defining where processed device data is sent. Its primary function is to standardize heterogeneous device data into a consistent format before transmitting it to external systems or services. All data is transferred in a unified format, enabled by [Navixy Generic Protocol](..\..\..\..\..\IoT%20Logic\Navixy%20IoT%20Logic\Navixy%20Generic%20Protocol.md).

For details on the format in which data is transmitted, see [Output Endpoint node](Output Endpoint node.md).

### Flow architecture integration

![Output Endpoint node in the flow workspace](..\..\..\..\attachments\696d6abd-7b47-4a76-a7b1-6f186fa90db7.webp)

A single IoT Logic flow can contain multiple output nodes, each with independent configurations. This architecture enables:

- Multi-destination data transmitting to different external systems simultaneously
- Multiple data sources handling with different incoming data formats
- Selective data routing that enables flexible data flow scenarios

> [!IMPORTANT]
> Each flow includes a default Navixy endpoint node. It is recommended to maintain connections between your **Data Source** nodes and this output. The connection ensures device data is sent to the platform, enabling monitoring capabilities using Navixy tools. If the Navixy output is removed, data from the devices involved in the flow will no longer reach the platform.

### Node capabilities

The **Output Endpoint** nodeby itself offers:

- **Secure transmission**: Implements SSL encryption and authentication mechanisms for data protection during transit
- **Configurable delivery assurance**: Provides MQTT QoS level selection to balance between delivery guarantees and network overhead
- **Configuration reusability**: Supports creating endpoint profiles that can be reused across multiple flows, ensuring configuration consistency
- **Concurrent processing**: Accepts inputs from multiple data sources within a flow, allowing consolidated data transmission
- **Transport protocol version selection**: Supports both MQTT 3.1.1 and 5.0 to accommodate various broker implementations

## Configuration options

Setting up an **Output endpoint node** determines how and where data will be delivered from a particular flow. Each configuration option serves a specific purpose in establishing reliable data transmission.

![Output Endpoint node configuration panel in its default appearance](..\..\..\..\attachments\4acca997-f1a5-4343-96c6-badda4d6059b.png)

Let's see what elements this node uses and what you can configure when working with it:

### Configuration steps

1. Select **Endpoint type**: Choose what type of transmitting to use for this endpoint

   - **Default endpoint** - standard configuration for sending flow data to the Navixy platform that cannot be edited
   - **MQTT endpoint** - custom configuration that uses MQTT as transport for sending flow data to 3rd-party systems.
2. Select a **Preset** (optional): Open the **Preset** dropdown and select a template that fits your needs. Several ready-made configurations are available for common destinations, like Navixy servers.  
   **Note:** After an endpoint is saved, it can be used as a preset for creating new outputs.

2. **Specify Endpoint Name**: Enter a unique, descriptive name for this endpoint configuration

   - Use a name that helps you identify the destination the data is sent to
   - This name will be displayed in the flow diagram for easy identification
3. **Select protocols**:

   - **Protocol** – select a protocol for data transmission to third-party services from a dropdown list. Currently, only the **Navixy Generic Protocol (JSON)** is supported. In the future, other formats can be considered as additional options for data transmission.
4. **Configure connection parameters**:

   - Enter the target **IP/Domain** in the format: *123.123.123.123* or *example.example.com*.
   - Specify the **Port** number. By default, *1883* is used for standard MQTT, *8883* – for SSL).
   - Toggle **Enable SSL** for secure connections. This action automatically sets the port to *8883* if it wasn’t changed manually.
5. **Set MQTT parameters**:

   - Enter **Client ID**. The receiving side has a fixed list of clients. In this field, the correct value must be specified so that the data is not rejected.
   - Select **MQTT Version**: 3.1.1 or 5.0.
   - Specify **Topics** in the form of tags that will be used for data transmission.
   - Choose **QoS** level that determines the logic of data transmission:

     - **QoS 0** – no delivery confirmation.
     - **QoS 1** – guaranteed delivery with possible duplication.
     - **QoS 2** – guaranteed delivery without duplication.
6. **Configure MQTT authentication** (optional):

   - Toggle **MQTT Authentication** on.
   - Enter **MQTT Login** and **MQTT Password** for the receiving party in the appeared fields.
7. **Save** your configuration.

> [!NOTE]
> Make sure to connect the relevant data nodes to your new output; otherwise, it won’t receive any data.

## Output data format

The node's primary capability is data format standardization through [Navixy Generic Protocol](..\..\..\..\..\IoT%20Logic\Navixy%20IoT%20Logic\Navixy%20Generic%20Protocol.md). This standardization solves a fundamental challenge in IoT implementations - the diversity of device-specific protocols that require custom integration work.

Usually, each device type uses its own data format, requiring dedicated protocol handlers on receiving systems. This approach increases development and maintenance overhead exponentially as device fleets expand. IoT Logic addresses this by normalizing all device data into a standardized JSON structure, regardless of the original manufacturer or protocol.

The [Navixy Generic Protocol](..\..\..\..\..\IoT%20Logic\Navixy%20IoT%20Logic\Navixy%20Generic%20Protocol.md) specification includes standardized fields for device identification, location data, telemetry values, and metadata. This format supports bidirectional communication, allowing both data transmission from IoT Logic to external systems and data ingestion from external sources into the platform.

By implementing a single protocol, the **Output Endpoint** node enables:

- A single integration pattern for receiving systems instead of multiple device-specific handlers
- Consistent data structure that remains uniform across all connected devices
- Reduced server-side processing overhead through protocol normalization
- Simplified scaling when adding new device types to existing deployments
- Bidirectional data exchange capabilities with external systems

The node implements MQTT as the transport protocol for this standardized JSON payload, providing a reliable, lightweight transmission mechanism suitable for IoT deployments.

## Frequently asked questions

### Can I connect multiple data sources to a single Output Endpoint node?

Yes. The **Output Endpoint** node accepts inputs from multiple **Data Source** nodes simultaneously. All processed data, including location coordinates, device identifiers, telemetry parameters, and calculated attributes, is serialized according to the [Navixy Generic Protocol](..\..\..\..\..\IoT%20Logic\Navixy%20IoT%20Logic\Navixy%20Generic%20Protocol.md) specification before transmission.

![Example flow showing multiple Data Sources connected to a single Output Endpoint](..\..\..\..\attachments\ec7c68d9-3ac7-427c-9ce3-2df69a8a0a88.png)

### What happens if I modify an endpoint that's used in multiple flows?

Endpoint configurations are stored as reusable resources across the entire client account. Modifications to an existing endpoint configuration will affect all nodes referencing that endpoint across all flows. This behavior facilitates configuration standardization but requires careful change management when updating endpoint parameters.

### What security practices are recommended for production deployments?

For implementations requiring high security standards (healthcare, financial, etc.), enable SSL and implement MQTT authentication. While this increases protocol overhead slightly, it provides necessary data protection during transmission. Standard implementations should use at minimum QoS level 1 to ensure delivery confirmation.
