
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Safety](..\Safety.md)

# Pressing SOS Button

## Overview

The “Pressing SOS Button” feature, commonly referred to as the “SOS button,” is an essential safety function designed for GPS devices equipped with an emergency button. This button can be either an external component or integrated within a personal tracker device. It serves as a vital lifeline in critical situations, enabling employees and individuals to swiftly request assistance when it’s needed most.

## Rule settings

The functionality of this rule depends on the device's capabilities and configuration, so no specific rule settings are required.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

<details>
<summary>Connecting external button to a vehicle’s GPS device input</summary>

Depending on the device, the SOS button can be connected to either a dedicated input, specifically designed for this function, or to a general discrete input. If connected to a discrete input, you should create the input within the Devices and Settings menu under the Sensors and Buttons section. In this case, select the “Input Triggering” rule type for proper configuration.

</details>

## System operation details

- **Reset timer:** The “Pressing SOS Button” alert has a 30-second reset timer, meaning the alert will not trigger more than once every 30 seconds. If an event occurs while the rule is waiting for the reset, the platform will omit the event, including in reports.
- **Multiple devices:** This rule allows users to select multiple trackers from which they wish to receive notifications. The selected trackers must support the “Pressing SOS Button” event, and this feature must be integrated on the platform for those trackers. This enables users to monitor emergency signals across various devices conveniently.
- **GPS-independent event alert:** The platform recognizes and counts this type of hardware event even if the data packet lacks valid GPS coordinates. The event will be displayed regardless of whether it occurred within or outside the defined geofences. The Inside/Outside geofence settings are ignored in this case, ensuring that no critical event is omitted.
