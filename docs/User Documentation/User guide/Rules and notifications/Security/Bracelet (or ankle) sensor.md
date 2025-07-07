
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Security](..\Security.md)

# Bracelet (or ankle) sensor

The “Bracelet sensor” (or “Ankle sensor”) rule is specifically designed for legal monitoring applications involving specialized GPS trackers. It is an essential tool for security in contexts such as house arrest or parole.

This rule is designed to immediately notify security personnel if a GPS device is removed without authorization. In these situations, the rule triggers an instant alert to the relevant authorities, allowing for quick action to prevent any unauthorized movement or breach of legal conditions.

## Rule settings

This rule is entirely dependent on the device's capabilities and hardware configuration. There are no specific settings to configure within the rule itself.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Reset timer.** The "Bracelet sensor" alert has a 3-minute reset timer, meaning the alert event will not occur more often than once every 3 minutes. If this type of event occurs in time the rule has been waiting for the reset, this event will be omitted by the platform, including the reports.
- **Multiple devices:** With this rule, you have the flexibility to select multiple trackers for receiving notifications. The only requirement is that the selected trackers must support Bracelet sensor events and have this feature integrated into the platform. This allows you to monitor multiple compatible trackers simultaneously, ensuring you receive notifications for the relevant events across various vehicles or devices efficiently.
- **GPS-independent event alert:** When the platform detects this type of hardware event from tracker data that lacks valid coordinates, it will still register and display the event as valid. This applies regardless of whether the event took place inside or outside of the designated geofences. In such cases, the platform disregards the Inside/Outside geofence logic to ensure the event is captured and reported.
