
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Safety](..\Safety.md)

# Call Button Pressed

## Overview

The "Call Button Pressed" rule is designed for GPS devices equipped with a built-in call function, typically found in devices capable of voice calls or radio communication.

This rule triggers notifications whenever the device's phone call function is activated, providing a quick way to initiate real-time communication. This feature enhances safety, security, and operational efficiency by ensuring rapid responses in critical situations and contributing to smoother operations.

## Rule settings

The functionality of this rule depends on the device's capabilities and configuration, so no specific rule settings are required.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Reset timer:** The “Call Button Pressed" alert has a 1-minute reset timer, meaning the alert will not trigger more than once per minute. If an event occurs while the rule is waiting for the reset, the platform will omit the event, including in reports.
- **Multiple devices:** This rule allows users to select multiple trackers from which they wish to receive notifications. The selected trackers must support the "Call Button Pressed" event, and this feature must be integrated on the platform for those trackers. This enables users to monitor events across various devices conveniently.
- **GPS-independent event alert:** The platform recognizes and counts this type of hardware event even if the data packet lacks valid GPS coordinates. The event will be displayed regardless of whether it occurred within or outside the defined geofences. The Inside/Outside geofence settings are ignored in this case, ensuring that no critical event is omitted.
