
[GPS Tracking](..\..\GPS%20Tracking.md) > [Objects list](..\Objects%20list.md)

# Object widget

In Navixy, **Object widget** serves as a comprehensive collection of telematics data blocks for monitoring and managing your fleet. It provides an in-depth look at your business assets, GPS devices, and the sensors connected to them.

> [!NOTE]
> **Navigation**
>
> - By default, to access the detailed view of a specific object, either click the object’s icon on the map or hover your mouse over it and click the appearing ![Info_Icon.png](..\..\..\attachments\cbf4aec3-63ea-4b47-8292-e8fad009dd2d.png) button.
> - If the **Show info by click** option is enabled in the [Additional settings](https://squaregps.atlassian.net/wiki/spaces/USERDOCSOLD/pages/edit-v2/2909015397#Additional-settings), clicking on an object also opens the **Object widget**.

Once opened, the panel displays extensive information about the selected object, including current status, GPS location, and further telematics data. All operational management tools are conveniently located in one place, allowing for efficient fleet management and quick response to any arising issues.

![Object_widget_big.png](..\..\..\attachments\1cb4ba10-1841-4baf-9068-11f3d1f68a08.png)

## Structure

The top section of the widget panel contains essential details about the object, including its name, movement status, and connection status. It also includes the following options:

- **Customization options**    
  The widget layout provides robust customization capabilities to help you organize information according to your needs:

  - **Data blocks**: Click ![Cogwheel](..\..\..\attachments\b6d9a227-186d-4a35-afd7-7cc1085380bc.png) to open widget settings and select which data blocks you want to display. By default, all blocks available to the objects are selected. This menu also enables the display of the update time below each sensor.
  - **Layout management**: Click ![Lock](..\..\..\attachments\0b2f33b8-3c5f-4d0b-ac41-faa17666738b.png) to switch into layout management mode. When it’s enabled, you can drag data blocks to your preferred positions. In this mode, you can also change the order of information inside the blocks manually in the same drag-and-drop manner.
- **Street view access**  
  Clicking the widget enables **Street view**, displaying the real-world imagery of the object’s position on the map for improved context and navigation.
- **Video monitoring**  
  The ![Video](..\..\..\attachments\145af26f-7148-459c-81dd-9bcbffc11b5d.png) button, available only for GPS devices with this functionality, opens the **Video monitoring** window. Here, you can watch a live stream from your camera or review past recordings stored in the device’s memory or the cloud. To learn more about this feature, see [Video monitoring](#video-monitoring).
- **Apply pins to all vehicles**  
  The ![Apply pins to all vehicles](..\..\..\attachments\303d9a01-ac97-4454-ad5c-303228fda49f.png) button allows you to instantly mark all data blocks as **Favorites**, ensuring their information is shown under the object’s name in the **Objects list**. For details on this feature, see [Favorites](#favorites).

## Data blocks

The **Object widget** organizes crucial information through specialized data blocks. Each component serves a specific purpose in providing comprehensive monitoring and management capabilities.

> [!IMPORTANT]
> The blocks' availability and content depend on the GPS device assigned to the selected object. They display only the information transmitted by the device or sensors connected to it. You can also customize their appearance. For details, see [Customization options](#customization-options) above.

Here's a detailed overview of the available blocks:

|  **Block**             |  **Description**                                                                                                                                                                                                                                         |
|:-----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Location**           | Delivers precise positioning data, including the latest known location with either a street address or GPS coordinates, accompanied by timestamps. The widget also tracks current speed and altitude measurements.                                       |
| **GPS device**         | Provides basic information about the GPS device, including its connection status, GPS/GSM signal level, and subscription plan.                                                                                                                           |
| **Status**             | Provides movement status, speed, and direction.                                                                                                                                                                                                          |
| **OBD2 & CAN**         | Connects to the vehicle's onboard systems to provide real-time diagnostic data, such as fuel level, engine speed, coolant temperature, and any diagnostic trouble codes when the GPS device is properly connected to the vehicle's CAN bus or OBD2 port. |
| **Sensor readings**    | Monitors and displays data from all configured device sensors, providing recent readings with timestamps. Separate sensors can be marked as **Favorites** for quick access to critical measurements.                                                     |
| **Odometer**           | Tracks the device's total mileage. This data can be adjusted manually via the ![Edit](..\..\..\attachments\b1fec213-7fd4-4b77-a80f-651e46d18d42.png) button, ensuring accurate distance records.                                                         |
| **Engine hours**       | Monitors the total running time of the engine. This data can be adjusted manually via the ![Edit](..\..\..\attachments\b1fec213-7fd4-4b77-a80f-651e46d18d42.png) button for accurate usage tracking.                                                     |
| **Inputs**             | Monitors the current state of various connected sensors, including the ignition status and other vehicle sensors such as door sensors, providing real-time feedback on vehicle status.                                                                   |
| **Outputs**            | Enables active control over devices connected to the GPS device, including features such as remote vehicle immobilization, allowing for direct intervention when necessary.                                                                              |
| **Driver**             | Displays the vehicle’s driver and allows you to assign them directly through the widget. Also displays their phone number, key, and the time the driver was assigned.                                                                                    |
| **Working statuses**   | Manages operational states by displaying and enabling changes to the object's current status, helping track its working history.                                                                                                                         |
| **Recent events**      | Tracks and displays alerts related to the object. By default, you can see three recent events with an option to view all of them. Click ![View](..\..\..\attachments\d5768267-d241-424b-94de-41676b1a07c5.png) next to the event to open its details.    |
| **Electronic padlock** | Provides security management for devices equipped with smart lock features, enabling remote control over the lock state, including both locking and unlocking capabilities.                                                                              |

## Favorites

The **Object list** can display not only the objects' names and connection status but also specific telematics data from GPS devices and connected sensors. To achieve that, you need to mark the data blocks as **Favorites** by following these steps:

1. Hover the cursor over the desired data block inside the **Object widget**.
2. Click the appearing ![image-20250129-163848.png](..\..\..\attachments\9853d939-1cbb-4f1e-9c1a-1b86faf97b81.png) button to mark it as **Favorite**.

Once marked as **Favorite**, the selected data entry will appear under the corresponding object in the **Object list**, ensuring quick and easy access. To remove a block from the list display, click ![image-20250129-163848.png](..\..\..\attachments\9853d939-1cbb-4f1e-9c1a-1b86faf97b81.png) again.

## Video monitoring

The **Video monitoring** window provides real-time and historical video access for GPS devices with camera support. This feature enables visual monitoring capabilities through a dedicated interface accessible from the **Object widget**. The system supports both live streaming and recorded video playback from multiple camera sources.

### Live stream monitoring

The live stream functionality delivers real-time video feeds from installed dash cams or MDVR devices directly to your monitoring interface.

To use the live stream feature, follow these steps:

1. Click ![image-20250522-120053.png](..\..\..\attachments\d8e75c2a-6f9e-4458-97b1-0855725ee441.png) to initiate the live stream.
2. Use the player controls to navigate through the recent footage.
3. Select the **Live** button to return to real-time viewing.

> [!WARNING]
> Video streaming consumes significant data traffic. To conserve bandwidth, the platform automatically stops the stream when you close the video window or navigate to another module. For most browsers, closing the tab will also stop the stream, though some browser extensions may interfere with this function.

### Video playback

The playback functionality enables review of historical video footage stored either on the device or in the cloud platform. This capability supports event analysis, driver behavior monitoring, and incident investigation.

To use the playback feature, follow these steps:

1. Open the date selection menu to choose the date for the video you want to watch.
2. Depending on your history, the following icons will be displayed under the date:

   - **Gray dot**: Information is stored in the device's memory. Viewing it requires uploading it from the device to the cloud. This is done while you’re playing the video.
   - **Blue dot**: Content already available in cloud storage.
   - **No dot**: No video content available for selected date
3. Select your desired date to access the hourly timeline.
4. Choose specific time segments from the fragment line for playback

> [!WARNING]
> Consider data usage implications when downloading multiple fragments
