
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Device positioning](..\Device%20positioning.md)

# Location report on demand

## Overview

The **Location report on demand via SMS** feature allows users to manually request the current location of a GPS device by sending an SMS command. This feature is particularly useful in situations where the device cannot establish a cellular connection with the platform over IP, such as when it is in a roaming area with limited or no data coverage.

When the device is unable to transmit its location data through the usual channels (like GPRS or 3G/4G networks), the **Location update on demand via SMS** feature provides a reliable alternative. By sending an SMS command from the platform to the device, users can still retrieve the device's position. The device responds with its GPS coordinates via SMS to the platform, ensuring location tracking even when standard data connections are unavailable.

To further enhance convenience, Navixy offers a **Location Update via SMS Rule**. This rule notifies users as soon as a GPS location update is received via SMS. Given that SMS-based location updates can take anywhere from minutes to hours, depending on network availability and device status, this rule ensures users are promptly alerted when the update occurs. This notification feature streamlines the process, allowing users to focus on other tasks without needing to manually check for the update's arrival.

## Rule settings

There are no specific rule settings. For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Reset timer.** The "Location report on demand" alert has a 1-minute reset timer, meaning the alert event will not occur more often than once every 1 minute. If this type of event occurs in time the rule has been waiting for the reset, this event will be omitted by the platform, including the reports.
- **Multiple devices.** In this rule type, users have the flexibility to select multiple trackers which they wish to receive notifications from. The only requirement is that the selected trackers must support Location report on demand events and the feature must be integrated on the platform for given trackers. This means that users can choose multiple compatible trackers to receive notifications from, allowing them to monitor harsh driving events across various vehicles or devices in a convenient way.
