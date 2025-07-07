
[Geo links](..\Geo%20links.md)

# Creating geo links

To create a geo link, simply click on the "+" button, and the creation dialogue will appear:

The dialogue provides a couple of options to be configured or filled in:

1. **Description (Optional)**

Information field which serves for specifying additional custom information about the link. The maximum length is 100 characters.

2. **Select objects and data**

The list of objects available by the link. Each object has the following list of options to be specified upon adding the object:

*Object* - The beacon to be tracked.

*Label* - The specific label that will be displayed in the geo link interface overwriting the currently set label in the cabinet.

*Attributes* - The attributes of the tracker to be displayed in the geo link interface. The attributes include:

- Speed
- Address
- Movement status
- Driver name
- Phone number
- Vehicle name
- License plate
- Connection status

Use the copy button to apply the same attribute list to all other objects in the geo link. This function may save a significant amount of time when configuring attributes for multiple objects.

3. **Map settings**

*Map provider* - Select the map which you want your geo link end users to see by the generated geo link. The list of maps is specified by the platform service provider.

*Trace duration* - The tracking trace.

This is what a trace might look like if set for 5 minutes:

*Autoscale* - The map zoom and position auto adjustment on the multiple tracker movement.

*Geofence* *settings* - Selection can be made to either show or hide tracker locations based on the geofence position. For instance, by selecting the "Track outside geofence" option, trackers will be shown on the map only when they are outside of the selected geofences. This function may be useful for scenarios such as shipping or delivery, where the end-user should not see the tracker being loaded with goods before departure. Respectively, the "Track inside geofences" will show trackers only when they are inside the selected geofences.

4. **Limited validity duration** - Specify the link's lifetime. This can be quickly selected from predefined periods or set to a custom period of time. If the lifetime duration is set to start from a future moment, the link will remain inactive until that time arrives. Leave the option unselected for a permanent geo link configuration.
5. **Preview** - Check what the configured geo link looks like from the geo link web interface from the end-user's perspective. The preview feature enables quick swapping between the user and geo link interfaces for a more accurate representation of the geo link configuration.

After pressing the "Create" button, a pop-up dialogue appears with the generated link. The link can be copied and provided to end-users or shared via the social network buttons:
