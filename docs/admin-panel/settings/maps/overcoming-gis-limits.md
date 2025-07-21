# Overcoming GIS limits

_In this text, GIS services (or Geographic Information Systems services) refer to combination of services like geocoding, routing, distance calculations, street view and similar._

When relying on free or public GIS services, such as Google API keys or OpenStreetMaps servers, you may encounter usage limits. This can lead to services like geocoding, routing, or street maps becoming unavailable or functioning very slowly. To avoid these issues, we recommend using Navixy's Premium GIS package or a similar paid GIS service.

There are several solutions to solve the issue of API limits:

* **Enable the Navixy GIS package (recommended)**\
  This is the most convenient and inexpensive method. More information on GIS packages can be found here: [Maps](./)
* **Enable paid services in your Google Maps account**\
  Activating paid subscriptions for Google Maps APIs or similar paid services increases your usage limits. For information on prices and conditions, please refer to Google. In this case we recommend creating two separate Google API keys and restrict them accordingly. The first key should only allow access to the Google Maps JavaScript API and Google Street View Image API, while the second key should only allow access to the Google Maps Geocoding API, Google Maps Geolocation API, and Google Maps Directions API. You can monitor usage statistics in your Google Developer Console.
* **Install your own Nominatim server**\
  More information on Nominatim can be found here: [Nominatim](https://docs.navixy.com/on-premise/nominatim)

If you have any questions regarding these solutions, please do not hesitate to contact our customer success team.
