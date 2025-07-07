
[Rules and notifications](..\..\Rules%20and%20notifications.md) > [Movement monitoring](..\Movement%20monitoring.md)

# Parking state detection

## Overview

This rule allows users to receive notifications when a device starts or ends parking. For example, organizations that want to control the driving time of their vehicles can use this rule to ensure vehicles aren’t used off-duty. This rule provides notifications to the user interface, email address, or phone number about the parking states of selected objects.

Setting up this rule helps users stay informed about the beginning and end of trips, as well as changes in the parking status of their vehicles. This enhances control, security, and efficiency in fleet management operations.

## Rule settings

**Parking detection configurations**

The settings for a parking detection rule are managed exclusively within the Parking Detection widget. For detailed information on configuring parking detection, please refer to the Parking Detection article.

For common settings, please refer to [Rules and notifications](..\..\Rules%20and%20notifications.md).

## System operation details

- The "Parking state detection" alert has a 10-second reset timer, which means the alert event will not occur more often than once every 10 seconds. If an event occurs while the rule is waiting for the reset, the platform will omit the event, including in reports.
- This rule is detected on the server side and is not tied to any specific hardware, allowing it to be applied to multiple trackers simultaneously. This flexibility enables you to manage several trackers within a single rule.
