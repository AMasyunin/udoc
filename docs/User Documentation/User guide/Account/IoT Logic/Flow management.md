
[Account](..\..\Account.md) > [IoT Logic](..\IoT%20Logic.md)

# Flow management

IoT Logic provides a flexible canvas environment where you can build custom data flows to process, transform, and route device telemetry. Each flow consists of interconnected nodes that perform specific functions within your data processing pipeline, from receiving raw device data to forwarding enriched information to external systems.

## Creating a new flow

IoT Logic starts with an empty workspace where you can design your data processing flow.

![Create flow dialog showing name field, description field, and enabled toggle](..\..\..\attachments\869344c4-776f-4104-aa8e-d4c90a11d13f.png)

Follow these simple steps to create a flow:

1. Click the **New flow** button at the top of the screen to open the flow creation dialog.
2. Enter a **Flow name** and provide an optional **Description** to clearly show specific details about this flow's functionality or purpose.
3. Ensure the **Flow enabled** toggle is switched on (unless you're creating a flow that should initially remain inactive).
4. Click **Save** to create your flow and access the flow workspace.

The flow name and description help you identify each flow when you have multiple configurations. The enabled/disabled toggle provides a convenient way to temporarily stop data processing without deleting the entire flow configuration.

> [!WARNING]
> Disabled flows don't send any data! The readings from the devices involved in a disabled flow do not reach any destination, including the Navixy platform. This means that disabling a flow can interrupt your monitoring capabilities and data collection for the affected devices. Only disable flows when you deliberately want to stop data transmission completely.

After saving, your new flow appears in the workspace, and you can begin adding processing nodes from the left menu panel.

## Configuring flow components

Each flow consists of interconnected nodes that define how data moves through your system. The basic components available in the **Nodes** pane include:

### Data Source node

|                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| This node establishes the entry point for device data in your flow. It processes specific devices from your Navixy account that you can: <br/><ul><li><p>Filter by manufacturer and model</p></li><li><p>Specify the communication protocol</p></li><li><p>Select from one to an unlimited number of devices to send data into the flow</p></li><li><p>Easily select the whole device groups</p></li></ul>  <br/> | ![Data Source node configuration panel showing manufacturer, model, and device selection options](..\..\..\attachments\c4233aba-c0bd-4ab9-acfc-5b498acb2ebe.png) |

For detailed configuration options, see [Data Source node](Flow%20management\Data%20Source%20node.md).

### Initiate Attribute node

|                                                                                                                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| This node enables data transformation through the [Navixy IoT Logic Expression Language](..\..\..\..\IoT%20Logic\Navixy%20IoT%20Logic\Nodes\Data%20enrichment\Navixy%20IoT%20Logic%20Expression%20Language.md). It allows you to: <br/><ul><li><p>Create new calculated attributes based on device parameters </p></li><li><p>Perform unit conversions and mathematical operations</p></li><li><p>Apply time-based calculations</p></li></ul> | ![Initiate Attribute node configuration panel showing attribute creation interface](..\..\..\attachments\e2318af0-59ce-4e18-a383-a7d91f95fc99.png)  <br/> |

For detailed configuration options, syntax, and expression examples, see the [Initiate Attribute node](Flow%20management\Initiate%20Attribute%20node.md).

### Output Endpoint node

|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| This node defines where and how your processed data is transmitted. In its configuration, you can: <br/><ul><li><p>Specify destination connection details (IP/domain, port)</p></li><li><p>Select transport protocols and protocol versions</p></li><li><p>Set up security measures including SSL and authentication</p></li><li><p>Configure MQTT parameters like client ID, topics, and QoS levels</p></li><li><p>Create reusable endpoint profiles for consistent configurations</p></li></ul> | ![Output Endpoint node configuration panel showing connection settings and MQTT parameters](..\..\..\attachments\fef3ce39-ff37-4edb-9a18-c821f5ad1278.png) |

For complete details on data transmission options, see the [Output Endpoint node](Flow%20management\Output%20Endpoint%20node.md).

> [!IMPORTANT]
> Your flow should include a **Default Output Endpoint** to send data to the platform. Maintaining this connection ensures your device data remains available for visualization and management in the Navixy interface.

## Building your flow

To assemble your data processing sequence:

1. Drag nodes from the left menu and drop them onto the workspace.
2. Click on each node to open its configuration panel and set up the required parameters.
3. Connect nodes by clicking on a node's output connector and dragging it to the input connector of the destination node.

![Flow workspace showing connected nodes with visible connectors between them](..\..\..\attachments\d2da4711-a384-42da-b9e7-0fd7bae63e78.png)

Your flow must begin with at least one **Data Source** node and end with one or more **Output Endpoint** nodes. Between these, you can add transformation nodes to manipulate the data according to your requirements.

Nodes can be connected in various configurations:

- A single **Data source node** can feed multiple nodes for parallel processing
- Multiple **Data source nodes** can connect to a single **Output endpoint node** to consolidate data streams
- **Initiate attribute nodes** can be chained sequentially for multi-stage calculations

## Editing existing flows

After creating a flow, you can modify its configuration as your requirements evolve.

### Modifying flow details

To change the flow name, description, or enabled status:

1. Click ![image-20250403-161404.png](..\..\..\attachments\f65fce35-c378-437b-8a56-b7bee57d5e00.png) next to the flow name
2. Update the desired fields
3. Save your changes

### Removing elements

When you need to restructure your flow, you can remove nodes or connections:

![Node with delete icon](..\..\..\attachments\991f3795-ed0b-4c0c-b026-f043f6ffb15b.png)

**Deleting a node:**

1. Hover your cursor over the node you want to remove
2. Click the delete icon that appears in the top right corner of the node

> [!IMPORTANT]
> When you delete a node, all of its connections will also be removed.

**Deleting a connection:**

![Selected connection highlighted for deletion](..\..\..\attachments\640ffaee-0c6f-42a7-8f1d-6e375340357e.png)

1. Click on the connection line you want to remove
2. Click **Unlink** or press the backspace key on your keyboard

### Managing multiple flows

To switch between different flows:

1. Click the **Data flow** dropdown
2. Select the flow you want to view or edit, it opens on the workspace

> [!IMPORTANT]
> Any unsaved changes in the current flow will be lost when switching, you will be asked to confirm the action.

## Saving and activating flows

After configuring your flow:

1. Click the **Save flow** button to store your flow configuration
2. Ensure the flow is enabled for it to begin processing data

Once activated, your flow will:

- Receive real-time data from the configured devices
- Apply any defined transformations through Initiate attribute nodes
- Forward the processed data to your specified endpoints in the [Navixy Generic Protocol](..\..\..\..\IoT%20Logic\Navixy%20IoT%20Logic\Navixy%20Generic%20Protocol.md)format

If you need to temporarily disable data processing, you can toggle the flow's enabled status without losing your configuration.

## Example configurations

You can find detailed step-by-step descriptions of an example flow creation in [Flow configuration example](Flow%20management\Flow%20configuration%20example.md). The example also contains explanations on some common data enrichment options. Feel free to use this example as a template for your custom flows.
