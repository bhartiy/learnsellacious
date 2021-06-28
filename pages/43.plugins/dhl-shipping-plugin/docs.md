---
title: 'Dhl shipping Plugin'
taxonomy:
    category:
        - docs
---

Your page content goes here.Sellacious Dhl Configuration


Installation: Install provided plugin from joomla backend->manage->extensions->install. Once installed, enable it.



Shipping rule: when plugin is enabled you will get the option to select dhl api during shipping rule creation. Create shipping rule and save api credentials which are 
Site ID, Password, Account Number, Outbound Account Number




Geolocation: Make sure you have geolocation available from country to zip level  for both seller and buyer when they are saving their respective addresses,  If not you can create it manually from sellacious backend->settings->geolocations. You can also purchase and install geolocation in bulk from here.https://www.sellacious.com/apps-and-integrations/geolocations



Shipment configuration: configure your shipment configuration from settings->global configuration->shipment. To know more about this visit https://www.sellacious.com/documentation-v2#/learn/global-configurations/shippment

IMPORTANT: If ship by shop then save shipping origin here which will be used when dhl rates are being fetched in frontend checkout. Shop contact no. mandatory.
If shipped by a concerned seller then save shipping origin to seller’s profile which then will be used to fetch shipping rates on product of that seller. Seller’s contact no. mandatory.

Note: if you choose shipping selection cart wise then shop shipping origin will be used even if you had chosen shipped by shop. In this scenario make sure  shop shipping origin is saved in the system.




Product Shipping Dimensions: Make sure dimensions are set for the product. Also, dimensions units should be proper eg. Length, Width, Height in CM and Weight in KG.



Now on checkout make sure the buyer has the option to select all necessary fields when saving an address. Dhl requires name, country, state, district, city, zip to be saved in buyers address.


You can manage these fields from address presets. To know more about address presets visit https://www.sellacious.com/documentation-v2#/learn/settings/address-presets.

In checkout dhl shipping rule and rates will be shown





When payment is approved shipping labels will be generated  which can be printed from backend orders view 




