---
title: 'DHL/DHL Express Shipping Plugin'
taxonomy:
    category:
        - docs
media_order: 'Screenshot 2021-06-26 at 4.17.59 PM.png,unnamed.png,Screenshot 2021-06-26 at 4.20.21 PM.png,Screenshot 2021-06-26 at 4.21.11 PM.png,Screenshot 2021-06-26 at 4.32.57 PM.png,Screenshot 2021-06-26 at 4.35.38 PM.png,Screenshot 2021-07-08 at 12.44.44 PM.png,Screenshot 2021-07-08 at 12.58.25 PM.png,Screenshot 2021-07-08 at 3.12.30 PM.png,Screenshot 2021-07-08 at 3.21.03 PM.png,Screenshot 2021-07-08 at 3.24.58 PM.png,Screenshot 2021-07-08 at 3.28.57 PM.png,Screenshot 2021-07-08 at 3.38.39 PM.png,Screenshot 2021-07-08 at 4.53.20 PM.png'
published: true
visible: true
---

**Configuration**

**Installation:** Install provided plugin from joomla backend->manage->extensions->install. Once installed, enable it.
![Screenshot%202021-06-26%20at%204.17.59%20PM](Screenshot%202021-06-26%20at%204.17.59%20PM.png "Screenshot%202021-06-26%20at%204.17.59%20PM")
for DHl Express
![Screenshot%202021-07-08%20at%2012.44.44%20PM](Screenshot%202021-07-08%20at%2012.44.44%20PM.png "Screenshot%202021-07-08%20at%2012.44.44%20PM")
**Shipping rule:** when plugin is enabled you will get the option to select dhl api during shipping rule creation. Create shipping rule and save api credentials which are 
Site ID, Password, Account Number, Outbound Account Number
![unnamed](unnamed.png "unnamed")
for DHL Express we need Site ID/Username, Password, Account Number
![Screenshot%202021-07-08%20at%2012.58.25%20PM](Screenshot%202021-07-08%20at%2012.58.25%20PM.png "Screenshot%202021-07-08%20at%2012.58.25%20PM")

**Geolocation:** Make sure you have geolocation available for country, state, district and zip. These geolocations needed for seller origin only, you can either manually create or install in bulk.
NOTE: For DHL Express state code in State location is required. Usually this is provided by default by sellacious but in case you are creating manually make sure it is present. You can look for your states code on www.iso.org . 

**Shipment configuration:** configure your shipment configuration from settings->global configuration->shipment. To know more about this visit https://www.sellacious.com/documentation-v2#/learn/global-configurations/shippment

IMPORTANT: If ship by shop then save shipping origin here which will be used when dhl rates are being fetched in frontend checkout. Shop contact no. mandatory.
If shipped by a Concerned Seller then save shipping origin to seller’s profile which then will be used to fetch shipping rates on product of that seller. Seller’s contact no. mandatory.

Note: if you choose shipping selection cart wise then shop shipping origin will be used even if you had chosen shipped by Concerned Seller. In this scenario make sure  shop shipping origin is saved in the system.
![Screenshot%202021-06-26%20at%204.20.21%20PM](Screenshot%202021-06-26%20at%204.20.21%20PM.png "Screenshot%202021-06-26%20at%204.20.21%20PM")
**Product Shipping Dimensions:** Make sure product shipping dimensions are saved in the product.

![Screenshot%202021-06-26%20at%204.21.11%20PM](Screenshot%202021-06-26%20at%204.21.11%20PM.png "Screenshot%202021-06-26%20at%204.21.11%20PM")
Now on checkout make sure the buyer has the option to select all necessary fields when saving an address. Dhl requires buyers Name, address lines, country, state, city, zip to be saved in buyers address. Make them mandatory in your address preset. You can make State and district text only if geolocation is not present. 
![Screenshot%202021-07-08%20at%203.38.39%20PM](Screenshot%202021-07-08%20at%203.38.39%20PM.png "Screenshot%202021-07-08%20at%203.38.39%20PM")
You can manage these fields from address presets. To know more about address presets visit https://www.sellacious.com/documentation-v2#/learn/settings/address-presets.

In checkout dhl shipping rule and rates will be shown and can be selected by the user. Here rates are shown along with the method from which is provided by the dhl.
![Screenshot%202021-06-26%20at%204.32.57%20PM](Screenshot%202021-06-26%20at%204.32.57%20PM.png "Screenshot%202021-06-26%20at%204.32.57%20PM")
NOTE: On some locations DHL may not provide the shipping. In that case dhl shipping rule will not show up, this may also happen when there is incorrect zip entered. Console log is provided in such case to verify this.(in test mode only). Console logging is explained later in detail.

When payment is approved shipping labels will be generated  which can be printed from backend orders view. In cart wise and seller wise shipping will show in list view and in item wise shipping it is shown in drawer against individual items.
![Screenshot%202021-06-26%20at%204.35.38%20PM](Screenshot%202021-06-26%20at%204.35.38%20PM.png "Screenshot%202021-06-26%20at%204.35.38%20PM")
![Screenshot%202021-07-08%20at%203.12.30%20PM](Screenshot%202021-07-08%20at%203.12.30%20PM.png "Screenshot%202021-07-08%20at%203.12.30%20PM")


**More on Labels:** 
1. Label consist of minimum 2 waybill documents, one for the package and one for the driver.
2. If there are 2 items in order, it would generate 1 waybill doc for the driver and 2 waybill documents 1 for each package.
3. If an order has multiple quantities of a product, 1 waybill document with summed up package weight and 1 waybill doc for the driver.
4. There is no return label yet for returned orders.


**Console logging of shipment info:** In test mode we can check what are the informations are being exchange during fetching rates in checkout.
In DHL: 
DHL is xml based API so two xml documents are provided in console log
![Screenshot%202021-07-08%20at%203.21.03%20PM](Screenshot%202021-07-08%20at%203.21.03%20PM.png "Screenshot%202021-07-08%20at%203.21.03%20PM")
First doc contains information what is send by sellacious to dhl in request for fetching rates.
From and to info: from is the sellers shipment origin and to is buyers shipping address
![Screenshot%202021-07-08%20at%203.24.58%20PM](Screenshot%202021-07-08%20at%203.24.58%20PM.png "Screenshot%202021-07-08%20at%203.24.58%20PM")
under Bkgdetails no. of pieces and individual  piece dimension and weight is shown
![Screenshot%202021-07-08%20at%203.28.57%20PM](Screenshot%202021-07-08%20at%203.28.57%20PM.png "Screenshot%202021-07-08%20at%203.28.57%20PM")
 
 Second xml doc contains what is received from the dhl as response.
Any error will be sown in notes 

![Screenshot%202021-07-08%20at%204.53.20%20PM](Screenshot%202021-07-08%20at%204.53.20%20PM.png "Screenshot%202021-07-08%20at%204.53.20%20PM")


**Limitations:**
(DHL API Limitation)
1.Weight in label is shown in KG and in single decimal point only so if item weight is 0.015 kg it will show 0.0 kg
2.Address (address line1, 2 etc) to be less than 38 character, if more it will be truncated. 
3.Seller shipping origin (state) to have state code in geolocations.


