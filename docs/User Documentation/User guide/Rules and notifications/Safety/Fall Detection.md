
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Safety](..\Safety.md)

# Fall Detection

## Overview

The "Fall Detection" rule is designed to ensure the safety and well-being of individuals by detecting and notifying users of potential falls or accidents.

This rule uses advanced sensors and algorithms to monitor the movement patterns and orientation of personal GPS devices. If the system detects a sudden and significant change in position or acceleration, it identifies this as a potential fall and triggers a notification.

This functionality is especially valuable for monitoring elderly individuals, lone workers, or others who may be vulnerable to falls. By providing real-time alerts, the system enables immediate response and assistance, enhancing overall safety and offering peace of mind to caregivers and loved ones.

## Rule settings

The functionality of this rule depends on the device's capabilities and configuration, so no specific rule settings are required.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Reset timer:** The "Fall Detection" alert has a 30-second reset timer, meaning the alert will not trigger more frequently than once every 30 seconds. If an event occurs while the rule is in the reset period, the platform will suppress the alert, ensuring that notifications and reports remain clear and manageable.
- **Multiple devices:** This rule can be applied to multiple personal GPS trackers, provided they support "Fall Detection" events and have this feature integrated into the platform. This allows users to monitor fall detection events across various devices, ensuring comprehensive coverage.
- **GPS-independent event processing:** The platform processes and displays fall detection events even if the data packet lacks valid GPS coordinates. These events are recorded regardless of whether they occur inside or outside a designated geofence. The Inside/Outside geofence settings are bypassed in this case, ensuring that no critical event is missed.
