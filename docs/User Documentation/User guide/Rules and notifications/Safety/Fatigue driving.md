
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Safety](..\Safety.md)

# Fatigue driving

## Overview

The Fatigue Driving rule is a critical feature within the telematics platform, designed to enhance road safety by detecting and alerting dispatch teams when signs of driver fatigue are identified. Utilizing advanced tracker cameras, the system continuously monitors drivers for indicators of drowsiness or fatigue, which are key contributors to road accidents.

When fatigue is detected, an immediate alert is sent to dispatch, allowing for prompt intervention—such as arranging rest breaks or providing necessary support. Implementing this rule not only helps in preventing accidents and reducing operational losses but also prioritizes driver well-being and promotes safe driving practices.

## Rule settings

Since this rule is hardware-dependent, configuration is minimal within the platform itself. The primary requirement is ensuring that the selected trackers are equipped to support and detect Fatigue Driving events.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Reset timer:** The “Fatigue Driving” alert is governed by a 5-second reset timer, ensuring that alerts do not trigger more frequently than once every 5 seconds. If a fatigue event is detected during this reset period, it will be omitted from the platform and reports.

- **Multiple devices:** This rule allows the selection of multiple device for monitoring. The selected devices must support Fatigue Driving events and have this feature integrated into the platform. This enables comprehensive monitoring across various vehicles or devices, ensuring that driver fatigue is consistently tracked and managed.

- **GPS-independent event alert:** The platform will register and display Fatigue Driving events even if the data packet lacks valid GPS coordinates. In such cases, the Inside/Outside geofence settings are ignored, as the system prioritizes the display of critical events, ensuring that no crucial information is overlooked.
