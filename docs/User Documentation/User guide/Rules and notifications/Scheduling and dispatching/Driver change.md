
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Scheduling and dispatching](..\Scheduling%20and%20dispatching.md)

# Driver change

## Overview

The “Driver change” rule helps fleet managers track which driver is operating a vehicle, especially when multiple drivers share the same vehicle. This feature works with driver identification technologies like iButton, RFID readers, or BLE hardware keys.

## Rule settings

To use this rule, start by adding all your drivers to the **Fleet Management** → **Drivers section**. Assign each driver their unique hardware key, such as an iButton or RFID tag. When a driver change is detected, the platform matches the event to the correct driver, ensuring accurate reports and alerts.

No other specific Rule settings are required. For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Driver Change Detection:** The platform identifies a driver change by checking if the latest hardware key data received from the tracker differs from the previous data. If the key has changed, it records this as a driver change event. This differs from the [Driver identification](Driver identification.md) rule where the alert is triggered directly by the hardware upon successful driver authentication, and the platform simply displays the event.
- **Manual overrides:** Manual driver changes made through the user interface (i.e. in widgets) do not trigger a driver change event. These changes are also not included in the “Report on all events.” However, all manual and automatic driver changes can be reviewed in detail through the “Driver shift change” report.
- **Alert reset timer:** The “Driver Change” alert has a 10-second reset timer, preventing it from triggering more than once every 10 seconds. If a driver change event occurs during this period, the platform will suppress the alert, keeping notifications and reports accurate and concise.
- **Support for multiple devices:** This rule can be applied to multiple trackers, allowing fleet managers to monitor driver changes across various vehicles. The trackers must be compatible with the Driver Change event and have this feature integrated into the platform.
- **GPS-independent event processing:** The platform processes driver change events even if GPS data is missing or invalid. These events will still be recorded and displayed, regardless of whether they occurred inside or outside a geofence. This ensures that all critical driver change events are captured and accurately reported.

## See also

- [Driver identification](Driver identification.md) — the rule used for verifying and authorizing the driver before or during vehicle operation, providing immediate alerts and ensuring that only authorized drivers can operate the vehicle.
