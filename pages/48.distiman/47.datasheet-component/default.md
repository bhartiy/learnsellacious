---
title: 'Datasheet Component'
media_order: 'Screenshot 2020-08-07 at 3.22.21 PM.png,Screenshot 2020-08-07 at 3.25.09 PM.png,Screenshot 2020-08-07 at 3.33.15 PM.png,Screenshot 2020-08-07 at 3.42.14 PM.png'
taxonomy:
    category:
        - docs
---

**Written by:** Indresh Maurya
**Date:** 03-08-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

This chapter deals with the Datasheet Component layout and configuration related to it. Datasheet enables us to show list page in sheet format.
![](Screenshot%202020-08-25%20at%205.04.20%20PM.png)
To enable this component follow these steps-

## Installation

**1.** Install and enable Datasheet component **com_sellaciousdatasheet.zip** from joomla backend. Go to **Manage->Extention->Install.** 
![](Screenshot%202020-08-07%20at%203.22.21%20PM.png)
then go to **Manage->Extention->Manage** and make sure it is enabled
![](Screenshot%202020-08-07%20at%203.25.09%20PM.png)

**2.** Now go to **Setings->Global Configuration->Frontend Display Options->Product Options** and select datasheet layout 
![](Screenshot%202020-08-07%20at%203.33.15%20PM.png)
**3.** For that first make a datasheet configuration menu if not done already. To Know more how to make Backoffice menu go to https://www.sellacious.com/documentation-v2#/learn/settings/menu-manager 
![](Screenshot%202020-08-07%20at%203.42.14%20PM.png)
**4.** This view provides you option to what to show and in what order on datasheet list page/details page.

## Cofiguration
Separate view is provided for datasheet configuration which will give options to manage the elements in datasheet list view as well as detail page. These configuration can be done on three level
**1. [Global Level](https://www.sellacious.com/documentation-v2#/learn/distiman/datasheet-component/datasheet-global-configurations)**
**2. Category Level**
**3. Product Level**

### Complementary Configurations

**Hide Variants:** By default sellacious selects best price listing of a product and displays it in list view. It can be a seller's product or a variant of main product and when clicked, it redirects to respective product details page rather than main product details page. To always show main product in list page and redirect main product details page, enable Hide Variants from list page section of Frontend display options.

![](Screenshot%202020-08-14%20at%2011.15.17%20AM.png)

**Hide Variant Specifications:** In specification section of product details page all product related specifications  viz global, product and variant specifications are shown. To hide variant specifications from product details page disable it from Backend Display Options.

![](Screenshot%202020-08-14%20at%2011.45.59%20AM.png)

**Config to hide placeholder image:** Placeholder image can be hidden from details page if no image is provided. Configuration is provided in frontend display options.
![](Screenshot%202020-08-25%20at%206.28.28%20PM.png)

**Config to show manufactures in cart:** Frontend display options config allows you to show manufacturer instead of seller in cart.

![](Screenshot%202020-08-29%20at%207.42.52%20PM.png)