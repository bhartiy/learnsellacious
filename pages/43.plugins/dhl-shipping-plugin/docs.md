---
title: 'DHL Shipping Plugin'
taxonomy:
    category:
        - docs
media_order: 'Screenshot 2021-06-26 at 4.17.59 PM.png,unnamed.png,Screenshot 2021-06-26 at 4.20.21 PM.png,Screenshot 2021-06-26 at 4.21.11 PM.png,Screenshot 2021-06-26 at 4.25.32 PM.png,Screenshot 2021-06-26 at 4.32.57 PM.png,Screenshot 2021-06-26 at 4.35.38 PM.png'
published: true
visible: true
---

Sellacious Dhl Configuration

**Installation:** Install provided plugin from joomla backend->manage->extensions->install. Once installed, enable it.
![Screenshot%202021-06-26%20at%204.17.59%20PM](Screenshot%202021-06-26%20at%204.17.59%20PM.png "Screenshot%202021-06-26%20at%204.17.59%20PM")
Shipping rule: when plugin is enabled you will get the option to select dhl api during shipping rule creation. Create shipping rule and save api credentials which are 
Site ID, Password, Account Number, Outbound Account Number
![unnamed](unnamed.png "unnamed")
**Geolocation:** Make sure you have geolocation available from country to zip level  for both seller and buyer when they are saving their respective addresses,  If not you can create it manually from sellacious backend->settings->geolocations. You can also purchase and install geolocation in bulk from here.https://www.sellacious.com/apps-and-integrations/geolocations

Shipment configuration: configure your shipment configuration from settings->global configuration->shipment. To know more about this visit https://www.sellacious.com/documentation-v2#/learn/global-configurations/shippment

IMPORTANT: If ship by shop then save shipping origin here which will be used when dhl rates are being fetched in frontend checkout. Shop contact no. mandatory.
If shipped by a concerned seller then save shipping origin to seller’s profile which then will be used to fetch shipping rates on product of that seller. Seller’s contact no. mandatory.

Note: if you choose shipping selection cart wise then shop shipping origin will be used even if you had chosen shipped by shop. In this scenario make sure  shop shipping origin is saved in the system.
![Screenshot%202021-06-26%20at%204.20.21%20PM](Screenshot%202021-06-26%20at%204.20.21%20PM.png "Screenshot%202021-06-26%20at%204.20.21%20PM")
**Product Shipping Dimensions:** Make sure dimensions are set for the product. Also, dimensions units should be proper eg. Length, Width, Height in CM and Weight in KG.
![Screenshot%202021-06-26%20at%204.21.11%20PM](Screenshot%202021-06-26%20at%204.21.11%20PM.png "Screenshot%202021-06-26%20at%204.21.11%20PM")
Now on checkout make sure the buyer has the option to select all necessary fields when saving an address. Dhl requires buyers name, address line 1, company name, country, state, district/city, zip to be saved in buyers address. Make them mandatory in your address preset.
![Screenshot%202021-06-26%20at%204.25.32%20PM](Screenshot%202021-06-26%20at%204.25.32%20PM.png "Screenshot%202021-06-26%20at%204.25.32%20PM")
You can manage these fields from address presets. To know more about address presets visit https://www.sellacious.com/documentation-v2#/learn/settings/address-presets.

In checkout dhl shipping rule and rates will be shown
![Screenshot%202021-06-26%20at%204.32.57%20PM](Screenshot%202021-06-26%20at%204.32.57%20PM.png "Screenshot%202021-06-26%20at%204.32.57%20PM")
When payment is approved shipping labels will be generated  which can be printed from backend orders view 
![Screenshot%202021-06-26%20at%204.35.38%20PM](Screenshot%202021-06-26%20at%204.35.38%20PM.png "Screenshot%202021-06-26%20at%204.35.38%20PM")

