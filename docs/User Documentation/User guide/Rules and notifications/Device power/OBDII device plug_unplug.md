
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Device power](..\Device%20power.md)

# OBDII device plug/unplug

## Overview

The “OBDII Device Plug / Unplug” rule is designed to provide immediate alerts whenever an OBDII GPS tracker is connected or disconnected from the vehicle’s OBDII port. This rule ensures that users can take prompt action to maintain continuous tracking and device functionality.

For instance, when the tracker is unplugged, it switches to its internal battery, which has a limited lifespan. Immediate notifications upon disconnection allow users to respond quickly, ensuring uninterrupted tracking and data transmission.

## Rule settings

This rule is entirely dependent on the device's capabilities and hardware configuration. There are no specific settings to configure within the rule itself.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Reset timer.** The “OBDII Device Plug/Unplug” alert has a 5-minute reset timer, meaning the alert will not trigger more frequently than once every 5 minutes. If the event occurs while the rule is in the reset period, it will be omitted by the platform, including in reports.
- **Multiple devices.** **Multiple devices:** Users can select multiple trackers to monitor under this rule. The only requirement is that the selected devices must support OBDII port plug / unplug events. This flexibility allows users to monitor this event type across various vehicles or devices conveniently.
- **GPS-independent event alert.** The system processes these events regardless of whether GPS data is available. The event will still be logged and displayed, even if it occurs outside defined geofences.
