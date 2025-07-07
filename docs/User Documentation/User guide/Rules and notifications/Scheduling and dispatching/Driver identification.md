
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Scheduling and dispatching](..\Scheduling%20and%20dispatching.md)

# Driver identification

## Overview

The “Driver identification” rule is designed to help fleet managers monitor and control vehicle usage by accurately identifying drivers. This rule ensures that only authorized drivers can operate vehicles, tracks which driver is behind the wheel, and records the duration and conditions of each driving session. It enhances operational efficiency, improves accountability, and supports compliance with safety protocols.

The rule operates using the device’s built-in capabilities to verify driver identity directly at the source. Authorized driver information is stored within the device’s internal memory. When a driver uses an iButton, RFID key, or facial recognition through a smart camera to authenticate, the device verifies their identity on the spot. The platform then records these identification events, generating real-time alerts, detailed reports, and notifications as needed.

**Application use cases:**

- **Shared vehicles:** Track and manage multiple drivers using the same vehicle.
- **Security:** Restrict vehicle operation to authorized personnel only, with real-time alerts for unauthorized attempts.
- **Compliance:** Ensure that vehicle operation complies with company policies and regulations.
- **Efficiency:** Reduce errors and streamline the driver identification process, especially in high-pressure environments with camera-based recognition.

## Rule settings

No other specific Rule settings are required.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System Operation Details

- **Reset timer:** The “Driver Identification” alert has a 5-second reset timer, meaning the alert will not trigger more frequently than once every 5 seconds. If an event occurs while the rule is in the reset period, the platform will omit the alert, ensuring that notifications and reports remain clear and manageable.
- **Multiple devices:** Users can apply this rule to multiple trackers, as long as they support “Driver Identification” via RFID, iButton, or Camera events. This allows you to monitor driver identification events across various vehicles or devices, ensuring comprehensive coverage.
- **GPS-independent event processing:** The platform will process and display driver identification events even if the data packet lacks valid GPS coordinates. These events are recorded regardless of whether they occur within a defined geofence. In this case, the Inside/Outside geofence settings are bypassed to ensure no critical event is missed.

## See also

- [Driver change](Driver change.md) — the rule is focused on logging when a different driver takes control of the vehicle, with the platform comparing current and previous driver data to detect changes and generate reports after the fact.
