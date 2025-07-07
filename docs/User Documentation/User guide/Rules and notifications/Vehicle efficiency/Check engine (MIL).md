
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Vehicle efficiency](..\Vehicle%20efficiency.md)

# Check engine (MIL)

## Overview

The "Check engine (MIL)" rule is designed to monitor the status of the Malfunction Indicator Lamp (MIL), commonly known as the "Check Engine" light, in vehicles. This rule is crucial for vehicle maintenance and fleet management, as it promptly alerts users when the MIL is activated.

The MIL typically illuminates when the vehicle's onboard diagnostic system detects an issue with the engine, emissions, or other critical systems. By receiving timely notifications, users can take immediate action to address potential problems, preventing further damage and ensuring vehicle safety and compliance.

> [!IMPORTANT]
> To monitor specific DTC codes, you can set up a [State field value](..\Inputs%20and%20outputs\State%20field%20value.md) rule.

## Rule settings

This rule is entirely dependent on the device's capabilities and configuration. There are no specific settings to configure within the rule itself.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Reset timer.** The "Check engine (MIL)" alert has a 24-hour reset timer, meaning it will not trigger more frequently than once every 24 hours. If the event occurs during the reset period, it will be omitted from the platform and reports.
- **Multiple devices.** This rule can be applied to multiple GPS devices, provided they support the Check Engine (MIL) event and have the feature integrated into the platform.
- **GPS-independent event alert.** The platform will log the event and trigger notifications regardless of whether the vehicle is inside or outside a geofence, even if the data packet lacks valid GPS coordinates. The platform prioritizes capturing and displaying these critical events to ensure they are not missed.
