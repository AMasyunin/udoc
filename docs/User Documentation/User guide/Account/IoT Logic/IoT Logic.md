
[Account](..\Account.md)

# IoT Logic

## Your complete data management solution

**IoT Logic** is a no-code/low-code tool integrated into Navixy platform, designed to simplify telematics data management. It combines a visual flow system with a JEXL-based expression language, enabling efficient data transformation without requiring coding expertise. Acting as a data traffic manager, it processes raw input from GPS devices, dash cams, and IoT sensors, converting it into actionable insights through custom data pipelines.

![IoT_Logic_schema.jpg](..\..\attachments\40b31385-9e0c-49a2-afe9-b49dc0e49ada.jpg)
> [!NOTE]
> **Navigation**
>
> IoT logic is accessible to account **Owners** in the **Account Settings** section. To find it:
>
> 1. Click the profile icon in the top-left corner of the screen to open your account settings
> 2. In the settings sidebar, select **IoT Logic**

## IoT Logic components

**IoT Logic** leverages its components to process, decode, enrich, and convert incoming data in real time, ensuring compatibility with various platforms and services. By optimizing data flow management, the solution enhances accuracy and customization of your data-related activities and offers more control over the data involved in your processes in general.

### Navixy Generic Protocol

Navixy Generic Protocol (NGP) creates the foundation for IoT Logic data handling. It is a flexible communication mechanism designed to standardize data flows from diverse GPS devices and sensors connected to them, enabling seamless integration into a single system. Regardless of the original data format, NGP unifies device communications by converting all incoming data into a common standard, therefore reducing compatibility issues. The protocol ensures reliable, scalable, and secure data transmission, making it ideal for complex fleet management and asset tracking tasks.

For technical details and implementation guidance, see the focused [Navixy Generic Protocol](..\..\..\IoT%20Logic\Navixy%20IoT%20Logic\Navixy%20Generic%20Protocol.md).

### Flow

Flow is the central functional element of IoT Logic, providing a structured framework for designing, customizing, and managing data processing. It introduces an intuitive drag-and-drop workspace that simplifies the creation of data pipelines. The process is built around three key stages of data interaction, each handled by specific nodes:

- **Data reception**  
  [Data Source node](IoT%20Logic\Flow%20management\Data%20Source%20node.md)manages data reception by connecting trackers to the Navixy platform for seamless input.
- **Data enrichment**  
  [Initiate Attribute node](IoT%20Logic\Flow%20management\Initiate%20Attribute%20node.md)enables data enrichment by renaming and customizing incoming parameters to meet various application requirements.
- **Data transmitting**  
  [Output Endpoint node](IoT%20Logic\Flow%20management\Output%20Endpoint%20node.md)handles data transmission by forwarding processed data to third-party servers and applications, ensuring efficient delivery.

> [!NOTE]
> These nodes can be interacted with directly from Navixy’s interface. For a detailed breakdown of each node and usage instructions within the UI, redirect to the dedicated descriptions by clicking on data operations in the list.

### Data Stream Analyzer

Data Stream Analyzer is a monitoring tool offering real-time troubleshooting capabilities for your data flow. The Analyzer provides a detailed view of incoming device data, making it the primary instrument to assess data integrity. On top of that, it has the potential to minimize operational risks, enhance decision-making, and improve service quality by allowing you to quickly identify data inconsistencies, optimize device performance, and maintain seamless operations.

For more details and usage instructions, see [Data Stream Analyzer](IoT%20Logic\Data%20Stream%20Analyzer.md).

## API access

IoT Logic functionality can also be accessed programmatically through the Navixy API. This allows developers to automate flow creation, management, and monitoring.

> [!IMPORTANT]
> For security reasons, API access requires appropriate permissions. Contact your account administrator to ensure you have the necessary access rights.

For complete API documentation, parameters, request/response formats, and code examples, refer to the [IoT Logic API documentation](https://navixy.com/docs/iot-logic-api).

## Section content

- [Workspace and default flow](IoT%20Logic\Workspace%20and%20default%20flow.md)
- [Quick start guide](IoT%20Logic\Quick%20start%20guide.md)
- [Flow management](IoT%20Logic\Flow%20management.md)
  - [Data Source node](IoT%20Logic\Flow%20management\Data%20Source%20node.md)
  - [Initiate Attribute node](IoT%20Logic\Flow%20management\Initiate%20Attribute%20node.md)
    - [Managing attributes](IoT%20Logic\Flow%20management\Initiate%20Attribute%20node\Managing%20attributes.md)
    - [Calculation examples](IoT%20Logic\Flow%20management\Initiate%20Attribute%20node\Calculation%20examples.md)
    - [Displaying new calculated attributes on the Navixy platform](IoT%20Logic\Flow%20management\Initiate%20Attribute%20node\Displaying%20new%20calculated%20attributes%20on%20the%20Navixy%20platform.md)
  - [Output Endpoint node](IoT%20Logic\Flow%20management\Output%20Endpoint%20node.md)
  - [Flow configuration example](IoT%20Logic\Flow%20management\Flow%20configuration%20example.md)
- [Data Stream Analyzer](IoT%20Logic\Data%20Stream%20Analyzer.md)
