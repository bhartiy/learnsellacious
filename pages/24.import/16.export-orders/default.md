---
title: 'Export Orders'
media_order: 'Screenshot (4).png,Screen Shot 2021-08-11 at 3.35.15 PM.png,Screen Shot 2021-08-11 at 3.35.29 PM.png,Screen Shot 2021-08-11 at 3.35.39 PM.png,Screenshot 2021-08-11 at 4.02.19 PM.png,Screen Shot 2021-08-11 at 4.10.58 PM.png,Screen Shot 2021-08-11 at 4.47.09 PM.png,Screenshot 2021-08-12 at 5.17.00 PM.png,Screenshot 2021-08-12 at 5.27.25 PM.png'
---

**Written by** : Rashi Gupta
**Date** : 11-08-2021
**Compatibility** : Sellacious v2.0.0-rc5

With export order functionality orders can be exported in form of csv file.
**NOTE: Importer plugin needs to be installed in order to export functionality to work** 
Orders can be exported by three methods-

1. From orders view by export orders
2. From orders importer template
3. By export link with secret-key

##### From Orders page in backend

1. Go to the sellacious backend in shop menu,
2. Go to the orders page
3. Click on the Export orders button to export the orders

![Screenshot%20%284%29](Screenshot%20%284%29.png "Screenshot%20%284%29")

4. Orders will be downloaded in csv format

##### From orders importer template

1. Go to the sellacious backend->import utility->templates
3. Click on the new export button in order importer template

![Screenshot%202021-08-12%20at%205.17.00%20PM](Screenshot%202021-08-12%20at%205.17.00%20PM.png "Screenshot%202021-08-12%20at%205.17.00%20PM")

5. Select the export type: Order exporter

![Screen%20Shot%202021-08-11%20at%203.35.15%20PM](Screen%20Shot%202021-08-11%20at%203.35.15%20PM.png "Screen%20Shot%202021-08-11%20at%203.35.15%20PM")

5. Then select the export template: Order template

![Screen%20Shot%202021-08-11%20at%203.35.29%20PM](Screen%20Shot%202021-08-11%20at%203.35.29%20PM.png "Screen%20Shot%202021-08-11%20at%203.35.29%20PM")

6. Click on the queue export button
7. Export started and shows the success message, you can also download exported csv from here.

![Screenshot%202021-08-11%20at%204.02.19%20PM](Screenshot%202021-08-11%20at%204.02.19%20PM.png "Screenshot%202021-08-11%20at%204.02.19%20PM")

An email will also be send containing export log and export csv file, which can be downloaded.
the recipients can be added in basic info tab of order import-export template.

![Screenshot%202021-08-12%20at%205.27.25%20PM](Screenshot%202021-08-12%20at%205.27.25%20PM.png "Screenshot%202021-08-12%20at%205.27.25%20PM")

##### By export link with secret-key

As export link can be generated which can run export orders by just sending the request from browser.
1.To generate link go to Export options tab of import-export orders template, Enter your secret key and save your export order link will be generated

![Screen%20Shot%202021-08-11%20at%204.10.58%20PM](Screen%20Shot%202021-08-11%20at%204.10.58%20PM.png "Screen%20Shot%202021-08-11%20at%204.10.58%20PM")

 2. You can choose how do you want to receive the exported file by **Email link only** or **Immediate Download and Email Link**
 3. You can copy the export link by click on **copy to click**
 4. To run export order paste the export link in browser and export order will be executed. Your export scv will be generated and email will be send to recipients.

**ADDITIONALLY:**

If you want to export certain number of columns in our export csv, In template, we have CSV columns tab where we can map the columns then Only mapped columns goes in the exported csv.

![Screen%20Shot%202021-08-11%20at%204.47.09%20PM](Screen%20Shot%202021-08-11%20at%204.47.09%20PM.png "Screen%20Shot%202021-08-11%20at%204.47.09%20PM")