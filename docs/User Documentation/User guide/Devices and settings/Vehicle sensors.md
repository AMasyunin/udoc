
[Devices and settings](..\Devices%20and%20settings.md)

# Vehicle sensors

The **Sensors and buttons** widget in Navixy allows you to manage and configure various sensors connected to your GPS devices from the platform standpoint. This feature is essential for monitoring various vehicle parameters, such as fuel levels, temperature, and engine diagnostics, directly through the platform.

## Overview

The **Sensors and buttons** widget is located in the **Devices and settings** section, which you can access by clicking the corresponded item in main menu of the web interface.

The widget provides an overview of the number of sensors already connected to the selected device. Expanding the panel lets you add new sensors or edit existing ones.

![image-20240815-205217.png](..\..\attachments\003e2f47-dde3-4653-a052-3516ad95cf76.png)

The number and type of sensors you can connect depend on the GPS device model. For example, certain devices allow you to configure data parameters transmitted via the CAN bus or OBDII diagnostic connector.

## Adding and editing sensors

To manage your sensors, you can use the following buttons:

- **Add**: Allows you to add a new sensor.
- **Edit**: Lets you modify the parameters of an existing sensor.
- **Delete**: Removes the selected sensor from the system.

### Sensor types

Navixy supports various sensor types, including:

- [Discrete sensors](Vehicle%20sensors\Discrete%20sensors.md): Used for binary inputs like ignition status, door open/close, etc.
- [Measurement sensors](Vehicle%20sensors\Measurement%20sensors.md): These sensors measure and report continuous values like temperature, fuel level, or engine RPM.
- [Aggregation sensors](Vehicle%20sensors\Aggregation%20sensors.md): Combine data from multiple sources into a single reportable value.
- [Virtual sensors](Vehicle%20sensors\Virtual%20sensors.md): Derived from calculated data or combined sensor values.

### Copying sensor settings

To streamline configuration, you can copy sensor settings from one device to another, provided the devices are of the same model. This is particularly useful when managing large fleets with similar vehicle types.

**Steps to copy sensor settings:**

1. Click the copy button (📋).
2. Select the devices to which you want to apply the copied settings.
3. Click **Apply**.

**Note:** Copying sensor settings will overwrite the current settings on the selected devices. Ensure that you only select the devices you intend to update.
