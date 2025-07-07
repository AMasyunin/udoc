
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Safety](..\Safety.md)

# ADAS warnings

## Overview

Advanced Driver Assistance Systems (ADAS) are engineered to elevate driver safety by delivering real-time alerts and monitoring while on the road. ADAS utilizes advanced algorithms and machine vision technologies, powered by AI, to analyze data from video cameras and lidar sensors. This enables the system to accurately detect potential hazards and unsafe driving behaviors, ensuring a proactive approach to road safety in line with the latest advancements in vehicle telematics.

The Navixy platform logs and can alert users to the following events:

|  **Event**                             |  **Description**                                                                                                                              |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| **Lane departure warning (LDW)**       | Alerts the driver when the vehicle unintentionally drifts out of its lane, helping to prevent potential collisions due to driver inattention. |
| **Forward collision warning (FCW)**    | Warns the driver of an imminent collision with a vehicle or object ahead, allowing for timely braking or evasive action to avoid an accident. |
| **Headway monitoring warning (HMW)**   | Monitors the distance to the vehicle ahead and alerts the driver if the following distance becomes unsafe, promoting safer driving habits.    |
| **Pedestrian in Danger Zone (PDZ)**    | Detects when a pedestrian is in close proximity to the vehicle, particularly in blind spots, to prevent accidents and enhance road safety.    |
| **Pedestrian Collision Warning (PCW)** | Issues a warning when a potential collision with a pedestrian is detected, giving the driver time to react and prevent an incident.           |
| **Traffic Sign Recognition (TSR)**     | Identifies and alerts the driver to important traffic signs, such as speed limits or stop signs, to ensure compliance with road regulations.  |

Monitoring these events helps improve driver awareness, reduce the risk of accidents, and ensure adherence to traffic regulations. This, in turn, supports efforts to enhance driver performance, mitigate liability, and prevent costly fines or vehicle repairs.

## Rule settings

### Event selection

As ADAS events are processed on the Video telematics device side rather than in the cloud, no additional settings are required. Simply select the events you want to monitor to ensure comprehensive driver behavior tracking.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **No reset timer:** The "ADAS" alert does not have a reset timer, meaning an alert will be triggered every time an ADAS event is detected.
- **Multiple Devices:** Users can select multiple trackers to receive ADAS notifications. The only requirement is that the chosen trackers must support ADAS events, and this feature must be integrated into the platform. This allows for efficient monitoring of driving behaviors across a fleet of vehicles.
- **GPS-Independent Event Alert:** The platform will recognize and display ADAS events even if the data packet from the tracker lacks valid GPS coordinates. In these cases, the Inside/Outside geofence settings are ignored, ensuring that critical events are not missed.
