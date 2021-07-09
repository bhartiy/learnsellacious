---
title: 'DHL/DHL Express Shipping Plugin'
taxonomy:
    category:
        - docs
media_order: 'Screenshot 2021-06-26 at 4.17.59 PM.png,unnamed.png,Screenshot 2021-06-26 at 4.20.21 PM.png,Screenshot 2021-06-26 at 4.21.11 PM.png,Screenshot 2021-06-26 at 4.32.57 PM.png,Screenshot 2021-06-26 at 4.35.38 PM.png,Screenshot 2021-07-08 at 12.44.44 PM.png,Screenshot 2021-07-08 at 12.58.25 PM.png,Screenshot 2021-07-08 at 3.12.30 PM.png,Screenshot 2021-07-08 at 3.21.03 PM.png,Screenshot 2021-07-08 at 3.24.58 PM.png,Screenshot 2021-07-08 at 3.28.57 PM.png,Screenshot 2021-07-08 at 3.38.39 PM.png,Screenshot 2021-07-08 at 4.53.20 PM.png,Screenshot 2021-07-08 at 4.57.19 PM.png,Screenshot 2021-07-08 at 5.03.16 PM.png,Screenshot 2021-07-08 at 7.03.02 PM.png,Screenshot 2021-07-08 at 7.15.04 PM.png,Screenshot 2021-07-08 at 7.16.28 PM.png,Screenshot 2021-07-08 at 7.27.31 PM.png,Screenshot 2021-07-09 at 10.09.43 AM.png,Screenshot 2021-07-09 at 10.19.26 AM.png,Screenshot 2021-07-09 at 10.20.26 AM.png,Screenshot 2021-07-09 at 10.21.29 AM.png,Screenshot 2021-07-09 at 10.32.07 AM.png,Screenshot 2021-07-09 at 10.36.25 AM.png,Screenshot 2021-07-09 at 10.45.17 AM.png,Screenshot 2021-07-09 at 10.55.16 AM.png,Screenshot 2021-07-09 at 10.43.45 AM.png,Screenshot 2021-07-09 at 10.57.13 AM.png,Screenshot 2021-07-09 at 11.03.46 AM.png'
published: true
visible: true
---

Written by: Indresh Maurya
Date: 30-06-202

Steps for Dhl/Dhl Express plugin installation, testing and implementation are as follows-

**1. Installation:** Install provided plugin from joomla backend->manage->extensions->install. Once installed, enable it.
![Screenshot%202021-06-26%20at%204.17.59%20PM](Screenshot%202021-06-26%20at%204.17.59%20PM.png "Screenshot%202021-06-26%20at%204.17.59%20PM")
for DHl Express
![Screenshot%202021-07-08%20at%2012.44.44%20PM](Screenshot%202021-07-08%20at%2012.44.44%20PM.png "Screenshot%202021-07-08%20at%2012.44.44%20PM")

**2. Shipping rule creation:** when plugin is enabled you will get the option to select dhl api during shipping rule creation. Create shipping rule and save api credentials which are 
Site ID, Password, Account Number, Outbound Account Number
![unnamed](unnamed.png "unnamed")
for DHL Express we need Site ID/Username, Password, Account Number
![Screenshot%202021-07-08%20at%2012.58.25%20PM](Screenshot%202021-07-08%20at%2012.58.25%20PM.png "Screenshot%202021-07-08%20at%2012.58.25%20PM")

**3. Geolocation:** Make sure you have geolocation available for country, state, district and zip. These geolocations needed for seller origin only, you can either manually create or install in bulk.
NOTE: For DHL Express state code in State location is required.
![Screenshot%202021-07-09%20at%2011.03.46%20AM](Screenshot%202021-07-09%20at%2011.03.46%20AM.png "Screenshot%202021-07-09%20at%2011.03.46%20AM")
Usually this is provided by default by sellacious but in case you are creating manually make sure it is present. You can look for your states code on www.iso.org . 

**3. Shipment configuration:** configure your shipment configuration from settings->global configuration->shipment. To know more about this visit https://www.sellacious.com/documentation-v2#/learn/global-configurations/shippment

IMPORTANT: If ship by shop then save shipping origin here which will be used when dhl rates are being fetched in frontend checkout. Shop contact no. mandatory.
If shipped by a Concerned Seller then save shipping origin to seller’s profile which then will be used to fetch shipping rates on product of that seller. Seller’s contact no. mandatory.

Note: if you choose shipping selection cart wise then shop shipping origin will be used even if you had chosen shipped by Concerned Seller. In this scenario make sure  shop shipping origin is saved in the system.
![Screenshot%202021-06-26%20at%204.20.21%20PM](Screenshot%202021-06-26%20at%204.20.21%20PM.png "Screenshot%202021-06-26%20at%204.20.21%20PM")

**4. Product Shipping Dimensions:** Make sure product shipping dimensions are saved in the product.
![Screenshot%202021-06-26%20at%204.21.11%20PM](Screenshot%202021-06-26%20at%204.21.11%20PM.png "Screenshot%202021-06-26%20at%204.21.11%20PM")

**5. Address preset configuration:** On checkout make sure the buyer has the option to select all necessary fields when saving an address. Dhl requires buyers Name, address lines, country, state, city and zip to be saved in buyers address. Make them mandatory in your address preset. You can make State and district text only if geolocation is not present. 
![Screenshot%202021-07-08%20at%203.38.39%20PM](Screenshot%202021-07-08%20at%203.38.39%20PM.png "Screenshot%202021-07-08%20at%203.38.39%20PM")
You can manage these fields from address presets. To know more about address presets visit https://www.sellacious.com/documentation-v2#/learn/settings/address-presets.

**6. Getting shipping rates in checkout:** In checkout dhl shipping rule and rates will be shown and can be selected by the user. Here rates are shown along with the method from which is provided by the dhl.
![Screenshot%202021-06-26%20at%204.32.57%20PM](Screenshot%202021-06-26%20at%204.32.57%20PM.png "Screenshot%202021-06-26%20at%204.32.57%20PM")
NOTE: On some locations DHL may not provide the shipping. In that case dhl shipping rule will not show up, this may also happen when there is incorrect zip entered. Console log is provided in such case to verify this.

**Console debugging :** Console debugging is  available in in test mode only which can be enabled from shipping rule. 
![Screenshot%202021-07-08%20at%205.03.16%20PM](Screenshot%202021-07-08%20at%205.03.16%20PM.png "Screenshot%202021-07-08%20at%205.03.16%20PM")
In Console debugging we can check what are the informations are being exchange during fetching rates in checkout.

**Console debugging In DHL:**  DHL is xml based API so two xml documents are provided in console log
![Screenshot%202021-07-08%20at%203.21.03%20PM](Screenshot%202021-07-08%20at%203.21.03%20PM.png "Screenshot%202021-07-08%20at%203.21.03%20PM")
1.First document contains information what is send by sellacious to dhl in request for fetching rates.
From and to info: from is the sellers shipment origin and to is buyers shipping address
![Screenshot%202021-07-08%20at%203.24.58%20PM](Screenshot%202021-07-08%20at%203.24.58%20PM.png "Screenshot%202021-07-08%20at%203.24.58%20PM")
under Bkgdetails no. of pieces and individual  piece dimension and weight is shown
![Screenshot%202021-07-08%20at%203.28.57%20PM](Screenshot%202021-07-08%20at%203.28.57%20PM.png "Screenshot%202021-07-08%20at%203.28.57%20PM")
 2.Second xml document contains what is received from the dhl as response.
Any error will be sown in notes 
![Screenshot%202021-07-08%20at%204.53.20%20PM](Screenshot%202021-07-08%20at%204.53.20%20PM.png "Screenshot%202021-07-08%20at%204.53.20%20PM")
Rates related info  will come in Qtdshp
![Screenshot%202021-07-08%20at%204.57.19%20PM](Screenshot%202021-07-08%20at%204.57.19%20PM.png "Screenshot%202021-07-08%20at%204.57.19%20PM") 

**Console debugging In DHL Express:** DHL is json based API so two objects are provided in console log
1.Coustomerdatails contains information what is send by sellacious to dhl in request for fetching rates and products contains information what we are getting in response
![Screenshot%202021-07-08%20at%207.03.02%20PM](Screenshot%202021-07-08%20at%207.03.02%20PM.png "Screenshot%202021-07-08%20at%207.03.02%20PM")
shipper and receiver details
![Screenshot%202021-07-08%20at%207.15.04%20PM](Screenshot%202021-07-08%20at%207.15.04%20PM.png "Screenshot%202021-07-08%20at%207.15.04%20PM")
package weight and dimensions
![Screenshot%202021-07-08%20at%207.16.28%20PM](Screenshot%202021-07-08%20at%207.16.28%20PM.png "Screenshot%202021-07-08%20at%207.16.28%20PM")
 2.Products object contains information of response send by dhl to sellacious
shipping type and total shipping (currency type BASEC)
![Screenshot%202021-07-08%20at%207.27.31%20PM](Screenshot%202021-07-08%20at%207.27.31%20PM.png "Screenshot%202021-07-08%20at%207.27.31%20PM")

**7. Label Generation:** When payment is approved shipping labels will be generated  which can be printed from backend orders view. In cart wise and seller wise shipping will show in list view and in item wise shipping it is shown in drawer against individual items.
![Screenshot%202021-06-26%20at%204.35.38%20PM](Screenshot%202021-06-26%20at%204.35.38%20PM.png "Screenshot%202021-06-26%20at%204.35.38%20PM")
![Screenshot%202021-07-08%20at%203.12.30%20PM](Screenshot%202021-07-08%20at%203.12.30%20PM.png "Screenshot%202021-07-08%20at%203.12.30%20PM")
sometimes it may encountered that shipping rates and rule selection were ok but still lablel are not been generated. This may occure due to missing information what is needed to generate label. Order wise detailed log is provided in "/tmp" directory  for debugging of any such cases.

**Label Debugging in DHL:** Order wise xml docs for label debugging can be found in "/tmp/dhl-xml-api" directory wherever sellacous is installed. 
![Screenshot%202021-07-09%20at%2010.09.43%20AM](Screenshot%202021-07-09%20at%2010.09.43%20AM.png "Screenshot%202021-07-09%20at%2010.09.43%20AM")
Two docs (request and response) is provided for each order. These docs are generated when payment is approved for an order.
1.Request doc contains information of what is being send to dhl when label generation request is made by sellacious
like information of Consignee(buyer)
![Screenshot%202021-07-09%20at%2010.19.26%20AM](Screenshot%202021-07-09%20at%2010.19.26%20AM.png "Screenshot%202021-07-09%20at%2010.19.26%20AM")
Shipment Details
![Screenshot%202021-07-09%20at%2010.20.26%20AM](Screenshot%202021-07-09%20at%2010.20.26%20AM.png "Screenshot%202021-07-09%20at%2010.20.26%20AM")
Shipper details
![Screenshot%202021-07-09%20at%2010.21.29%20AM](Screenshot%202021-07-09%20at%2010.21.29%20AM.png "Screenshot%202021-07-09%20at%2010.21.29%20AM")

2.Response doc contains information of label barcode, buyer, shipper address, billing details, item dimentions/weight and error in if any.
errors are logged under condition fileld 
![Screenshot%202021-07-09%20at%2010.32.07%20AM](Screenshot%202021-07-09%20at%2010.32.07%20AM.png "Screenshot%202021-07-09%20at%2010.32.07%20AM")


**Label Debugging in DHL Express:**  Order wise json docs for label debugging can be found in "/tmp/dhl-express-api" directory wherever sellacous is installed. 
![Screenshot%202021-07-09%20at%2010.36.25%20AM](Screenshot%202021-07-09%20at%2010.36.25%20AM.png "Screenshot%202021-07-09%20at%2010.36.25%20AM")
Two json files (request and response) is provided for each order. These files are generated when payment is approved for an order.
1.Request files contains information of what is being send to dhl when label generation request is made by sellacious
like information of shipper and receiver (buyer)
![Screenshot%202021-07-09%20at%2010.43.45%20AM](Screenshot%202021-07-09%20at%2010.43.45%20AM.png "Screenshot%202021-07-09%20at%2010.43.45%20AM")
package dimensions and  weight
![Screenshot%202021-07-09%20at%2010.45.17%20AM](Screenshot%202021-07-09%20at%2010.45.17%20AM.png "Screenshot%202021-07-09%20at%2010.45.17%20AM")
2.Response json contains these details and pdf uri
![Screenshot%202021-07-09%20at%2010.57.13%20AM](Screenshot%202021-07-09%20at%2010.57.13%20AM.png "Screenshot%202021-07-09%20at%2010.57.13%20AM")
in case there is an error it will show that error then
![Screenshot%202021-07-09%20at%2010.55.16%20AM](Screenshot%202021-07-09%20at%2010.55.16%20AM.png "Screenshot%202021-07-09%20at%2010.55.16%20AM")

**More on Labels:** 
1. Label consist of minimum 2 waybill documents, one for the package and one for the driver.
2. If there are 2 items in order, it would generate 1 waybill doc for the driver and 2 waybill documents 1 for each package.
3. If an order has multiple quantities of a product, 1 waybill document with summed up package weight and 1 waybill doc for the driver.
4. There is no return label yet for returned orders.

**Limitations:**
(DHL API Limitation)
1.Weight in label is shown in KG and in single decimal point only so if item weight is 0.015 kg it will show 0.0 kg
2.Address (address line1, 2 etc) to be less than 38 character, if more it will be truncated. 
3.Seller shipping origin (state) to have state code in geolocations.

**Useful Links**
1. https://xmlportal.dhl.com
2. https://developer.dhl.com/api-reference
3. https://developer.dhl.com/documentation
