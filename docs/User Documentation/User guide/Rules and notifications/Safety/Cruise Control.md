
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Safety](..\Safety.md)

# Cruise Control

## Overview

Receiving notifications when Cruise Control is enabled or disabled in a vehicle provides valuable insights for monitoring and managing vehicle performance. Here are some key benefits:

- **Fuel efficiency monitoring:** Cruise Control helps maintain a consistent speed, which can improve fuel efficiency. Notifications allow users to track Cruise Control usage and assess its impact on fuel consumption.
- **Battery management:** For electric or hybrid vehicles, Cruise Control usage can affect battery life and range. Notifications help users monitor its impact on battery usage, enabling better management of the vehicle's electric power.
- **Driving behavior analysis:** Tracking when and where Cruise Control is used offers insights into driver behavior. This data can be used to analyze driving habits and identify opportunities for improvement, such as reducing excessive or increasing underutilized Cruise Control usage.
- **Performance evaluation:** Monitoring Cruise Control usage can aid in evaluating vehicle performance. Users can compare Cruise Control with other driving modes to assess efficiency across different routes and driving conditions.
- **Safety and comfort:** Cruise Control enhances comfort and safety during long journeys. Notifications ensure users are aware of whether Cruise Control is active, allowing them to adjust their driving style as needed.

These benefits may vary depending on the vehicle's make, model, and additional features.

## Rule settings

This rule does not require any specific settings.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Reset timer:** The "Cruise Control Switched ON/OFF" alert has a 10-minute reset timer, preventing the alert from triggering more than once every 10 minutes. If another event occurs within this reset period, it will be omitted from the platform and reports.
- **Multiple devices:** Users can select multiple trackers to receive notifications. The selected trackers must support Cruise Control Switched ON/OFF events and have this feature integrated into the platform. This allows monitoring of Cruise Control events across various vehicles.
- **GPS-independent event alert:** The platform registers and displays Cruise Control events even if the data packet lacks valid GPS coordinates. The Inside/Outside geofence settings are ignored for this rule, ensuring that critical events are not missed.
