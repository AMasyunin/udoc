# Maps

## Cartography in Navixy

To make GPS data easy to understand, the Navixy GPS-tracking platform utilizes digital Maps and Geographic Information Services (GIS).

* **Maps** enable users to identify their current location, view the location of events recorded in reports (such as fuel filling or draining), and see where specific events occurred (for example, pressing the SOS button).
* **GIS** provides additional information such as the exact address of a current location, estimated time and length for building routes, taking into account streets and traffic, and street view in any selected area. It is an essential feature for efficient fleet management and helps businesses make informed decisions.

On this page, we will explore the options and customization available with the Cartography feature in Navixy.

### Set of maps available to your users

To enhance the user experience of your service, you have the option to set default list of maps, map center point, and scale that will be used when logging into the platform for the first time. This allows for a more customized and streamlined experience for your users. To access Maps settings go to Admin Panel → Account management → [Service preferences](https://panel.navixy.com/#settings).

#### Selection of maps

You can define the list of available maps for your users by checking the boxes in [Service preferences](https://panel.navixy.com/#settings) in the Admin panel of your platform. To add more maps that are commonly used in your region, please contact our customer success team.

![Maps Available](<../attachments/screen shot 2023-05-07 at 2.18.49 pm-20230811-203941.png>)

#### Default map center and scale

By setting the default map view, map center location and map zoom parameter, you can improve experience for your users when they login to the system for the first time. These settings will be applied both to web interface and mobile apps.

Please note that the map stays where the user had last left it and the default only applies on first login or after clearing cookies.

![default map settings](<../attachments/screen shot 2023-05-07 at 2.18.55 pm-20230811-204001.png>)

### Using various Maps and GIS with Navixy

With Navixy, you have the freedom to choose from a variety of licensed maps and GIS (Geographic Information System) services, including Geocoding, Street View, Directions, Distance Matrix, and more. Your preferences may vary depending on your region and local demand. Here are just a few of the popular available options:

* Google Maps
* OpenStreetMaps
* Bing Maps
* Mapbox
* Yandex Maps

#### Adding Google Maps to your service

Google Maps services remain one of the most popular choices for premium maps and GIS worldwide. If you're interested in using Google Maps services with Navixy, there are two options available to you:

1. Activate Navixy “Premium GIS” package (recommended)
2. Provide your Google Maps license key

**How to activate Navixy Premium GIS**

To activate and upgrade to the Navixy Premium GIS Package, simply contact our customer success team. This package includes not only fully licensed Google Maps services, but also advanced GIS services from Navixy including a set of additional licensed maps, algorithms for routing and distance calculation, LBS/Cell-ID databases. Our team will guide you through the process and ensure a smooth upgrade experience, so you can start taking advantage of all the benefits that come with the Premium GIS Package.

**How to use your own map license form Google**

If you prefer using the license you purchased from Google, we can help you integrate Google Maps and its API with Navixy. Simply provide our team with the necessary information, and we'll take care of the rest. To create a key, go to the "[Get a key](https://developers.google.com/maps/documentation/geocoding/get-api-key)" webpage on Google's website. Once you've created the key, send it to Navixy's technical support along with your domain name information. For security purposes, we recommend creating two Google API keys and restricting them as follows:

* Google API key #1: Restrict it to the following APIs: Google Maps JavaScript API and Google Street View Image API.
* Google API key #2: Restrict it to the following APIs: Google Maps Geocoding API, Google Maps Geolocation API, and Google Maps Directions API.

Please note that if you change your domain name, you will need to create new keys and provide our team with the updated information. This will ensure that your maps and API continue to function properly with Navixy.

#### Adding other Maps and GIS

Activating additional Maps and GIS services with Navixy is a straightforward process. Here are the steps to follow:

1. Contact our customer success team to learn about the available options for additional maps and GIS services
2. Select the service(s) you want to activate and let our team know which ones you've chosen
3. Our team will provide you with the necessary instructions and help you activate the service(s)
4. Once activated, you can start using the new maps and GIS services right away

For more information about deploying your own tile server please refer to the separate document [Map tile servers](https://docs.navixy.com/on-premise/custom-maps).

Please note that Maps and GIS services that you deploy locally or in the cloud may require separate licenses or paid subscriptions. Our team will help you navigate this process and ensure that you have everything you need to take full advantage of Navixy's offerings.
