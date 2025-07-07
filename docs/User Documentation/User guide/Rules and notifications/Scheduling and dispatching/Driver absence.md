
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Scheduling and dispatching](..\Scheduling%20and%20dispatching.md)

# Driver absence

## Overview

The "Driver Absence" event is designed to monitor and ensure the presence of the driver in the vehicle's seat. This feature is particularly important for preventing the vehicle from being left unattended in situations where it could pose a security risk or violate company policies.

### How it works

This feature typically relies on in-vehicle video systems equipped with AI and sensors to continuously monitor the driver's seat. These systems use a combination of visual recognition (via cameras) and sensor data to detect the presence or absence of a driver. If the system detects that the driver's seat is unoccupied when the vehicle is in operation or when it should be attended, it triggers a "Driver Absence" event.

This event is then communicated to the Navixy telematics platform, which can generate alerts, record the event, and notify the appropriate personnel. An alert might be triggered, for example, if the vehicle is in motion and the system detects that there is no driver in the seat, or if the driver leaves the seat without properly securing the vehicle.

### Applications

- **Fleet Safety:** Ensuring that vehicles are not operated without a driver, preventing accidents and unauthorized use.
- **Security:** Alerting fleet managers if a vehicle is left unattended in a potentially dangerous or high-risk area.
- **Compliance:** Helping fleets comply with safety regulations that require a driver to be present during vehicle operation.
- **Insurance:** Providing evidence in case of incidents where driver absence could be a factor, which may be required for insurance claims or legal purposes.

The "Driver Absence" event is a critical component in enhancing fleet safety and security, providing fleet managers with the tools needed to monitor and respond to situations where driver presence is required.

## Rule settings

No specific settings are required for this rule.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- **Reset timer:** The “Driver Absence” alert has a 10-second reset timer, meaning the alert will not trigger more frequently than once every 10 seconds. If an event occurs while the rule is in the reset period, the platform will suppress the alert, keeping notifications and reports clear and manageable.

- **Multiple devices:** This rule can be applied to multiple trackers, as long as they support “Driver Absence” events and have this feature integrated into the platform. This allows users to monitor these events across various vehicles or devices conveniently.

- **GPS-independent event processing:** The platform processes and displays driver absence events even if the data packet lacks valid GPS coordinates. These events are recorded regardless of whether they occur inside or outside a designated geofence. The Inside/Outside geofence settings are bypassed in this case, ensuring that no critical event is missed.
