---
title: 'Datasheet Component'
media_order: 'Screenshot 2020-08-07 at 3.07.26 PM.png,Screenshot 2020-08-07 at 3.22.21 PM.png,Screenshot 2020-08-07 at 3.25.09 PM.png,Screenshot 2020-08-07 at 3.33.15 PM.png,Screenshot 2020-08-07 at 3.42.14 PM.png,Screenshot 2020-08-07 at 3.53.13 PM.png,Screenshot 2020-08-07 at 4.11.49 PM.png,Screenshot 2020-08-07 at 4.48.12 PM.png,image1.png,image3.png,Screenshot 2020-08-07 at 5.23.11 PM.png,Screenshot 2020-08-07 at 5.28.27 PM.png,Screenshot 2020-08-13 at 6.53.49 PM.png'
taxonomy:
    category:
        - docs
---

**Written by:** Indresh Maurya
**Date:** 03-08-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

This chapter deals with the Datasheet Component layout and configuration ralated to it. Datasheet enables us to show list page in sheet format.

![](Screenshot%202020-08-07%20at%203.07.26%20PM.png)

To enable this component follow these steps-

## Installation

**1.** Install and enable Datasheet component **com_sellaciousdatasheet.zip** from joomla backend. Go to **Manage->Extention->Install.** 

![](Screenshot%202020-08-07%20at%203.22.21%20PM.png)

then go to **Manage->Extention->Manage** and make sure it is enabled

![](Screenshot%202020-08-07%20at%203.25.09%20PM.png)

**2.** Now go to **Setings->Global Configuration->Frontend Display Options->Product Options** and select datasheet layout 

![](Screenshot%202020-08-07%20at%203.33.15%20PM.png)

## Cofiguration
Separate view is provided for datasheet configuration which will give options to manage the elements in datasheet list view as well as detail page. These configuration can be done on three level
**1. Global Level**
**2. Category Level**
**3. Product Level**

### Global Level

**1.** For that first make a datasheet configuration menu if not done already. To Know more how to make Backofiice menu go to https://www.sellacious.com/documentation-v2#/learn/settings/menu-manager 

![](Screenshot%202020-08-07%20at%203.42.14%20PM.png)

**2.** This view provides you option to waht to show and in what order on datasheet list page/details page.

**List Page Options:** You can opt what column to show and ordering of the columns. **Note** that specifications and cart buttons can't be removed and Ptoducts list page will show only global specifications and category list page will show global and category specific specifications. If all options are disabled then all will show. You can choose Part Number elements wheather it is Product SKU, Seller SKU, Seller Name or all.

![](Screenshot%202020-08-13%20at%206.53.49%20PM.png)
![](Screenshot%202020-08-07%20at%204.11.49%20PM.png)
**List page style:** css of list page can be changed from here and can be reset to default at any time.

![](Screenshot%202020-08-07%20at%203.53.13%20PM.png)

**Detail page option:** You can manage detail page element from here
![](image1.png)

**Product Layout:** Choose which layout should be used in Product Detail Page.
**Show Manufacturer Logo:** Show/hide Manufacturer Logo.
**Show Part Number:** Show/hide Part Number.
**Show Product Title:** Show/hide Product Title.
**Show Short Description:** Show/hide Short Description.
**Show Specifications:** Show/hide Specifications.
**Show Features:** Show/hide Features.
**Show Images:** Choose between galery and primary image for product.
**Show Attachments:** Show/hide Attachments.
**Title of the Attachments:** Show/hide Title of the Attachments.
**Show Long Description:** Show/hide Long Description.
**Show Price List:** Show/hide Price List.
**Show Variants List:** Show/hide Variants section on details page.
**Variants List Columns:** Choose what Columns to show in variant section.
**Variants List Header:** Show/hide List Header.
**Variants List Footer:** Show/hide List Footer.

![](image3.png)

**Detail page style:** css of Detail page can be changed from here and can be reset to default at any time.

![](Screenshot%202020-08-07%20at%204.48.12%20PM.png)


### Catgory Level

Same option are available in category edit and those options if enabled will apply on produsts of that category only. Also the option is given if you want to choose global layout for the category too.

![](Screenshot%202020-08-07%20at%205.23.11%20PM.png)

### Product Level

Same option are available in product edit and those options if enabled will apply on that particular produst. Also the option is given if you want to choose global layout or category layout.
Additional config for given for adding long description
![](Screenshot%202020-08-07%20at%205.28.27%20PM.png)