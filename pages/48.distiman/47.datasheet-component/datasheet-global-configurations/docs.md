---
title: 'Datasheet Global Configurations'
media_order: 'Screenshot 2020-10-28 at 11.12.05 AM.png,Screenshot 2020-10-28 at 11.20.51 AM.png,Screenshot 2020-10-28 at 12.14.25 PM.png,Screenshot 2020-10-28 at 12.16.15 PM.png'
taxonomy:
    category:
        - docs
visible: true
---

**Written by:** Indresh Maurya
**Date:** 28-10-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

Global Datasheet Global Configurations are as follows-

### Distiman filter Module
**Datasheet Filters Layout:** Enable this option to get compact layout of filter module on list page.
**Note:** Compact layout works well with Manufacturer fiter, attribute filter and Submit by Apply button options. Attributes will show in module if only they are filterable. We can show/hide individual attribute filters(global/product/variant or all) in module. To know more about sellacious filter go to [Filter Configurations](https://www.sellacious.com/documentation-v2#/learn/frontend-product-filter/filter-configurations)
![](Screenshot%202020-10-28%20at%2011.20.51%20AM.png)
![](Screenshot%202020-10-28%20at%2011.12.05%20AM.png)
**Header Description:** This form can be used to show a description text over filter module.

### List Page Options
These are the list page options to show in datasheet-

**Datasheet Columns:** You can opt what column to show.
	Image- Image of product
    Product- Title of the product
    Part NO.- SKU of product
    Pdf- Product Attachment
    1 Piece Price- Best price of product
    Lowest Quantity Price- Price of lowest quantity in dynamic pricing
	Parice Range- Minimum and maximum price separated by dash
    Qty in Stock- Avaialble stock quantity of product
	Min Qty- Minimum order quantity
    Max Qty- Maximum order quantity
    Short Description- Short product description
    Global Specifications- Shows global specification columns
    Product Specifications- Shows product specification columns
    Variant Specifications- Shows variant specification columns
    Actions- Shows add to cart, buy now, rfq and quote request buttons based on configuration.
![](Screenshot%202020-10-28%20at%2012.14.25%20PM.png) 
**Note** List page containing two or more than two categories will show only **Filterable global specifications** and Category list page will show global and category specific(core+variants) specifications. If all options are disabled then all will show. 

**Datasheet Default Sorting:** We can choose Default Sorting for list page datasheet from available options.
![](Screenshot%202020-10-28%20at%2012.16.15%20PM.png)

**Datasheet Sorting Direction:** We can choose sorting direction (ascending/discending).

You can choose Part Number elements wheather it is Product SKU, Seller SKU, Seller Name or all.
Link to product details page can be disabled and can be shown as read only.



Additional options are provided to configure the category page head layout.



**List page style:** css of list page can be changed from here and can be reset to default at any time.



**Detail page option:** You can manage detail page element from here


**Product Layout:** Choose which layout should be used in Product Detail Page.
**Show Seller Logo:** Show/hide seller Logo.
**Show Manufacturer Logo:** Show/hide Manufacturer Logo.
**Show Part Number:** Show/hide Part Number.
**Show Product Title:** Show/hide Product Title.
**Show Short Description:** Show/hide Short Description.
**Show Specifications:** Show/hide Specifications.
**Show Features:** Show/hide Features.
**Show Images:** Choose between galery and primary image for product.
**Show Attachments:** Show/hide Attachments.
**Link Single Attachment with Title:** In case there is single attachment it will show as link.
**Title of the Attachments:** Give Title to the Attachments.
**Show Long Description:** Show/hide Long Description.
**Show Price List:** Show/hide Price List (works only with dynamic pricing).
**Show Tablular List:** Show/hide Variants section on details page.
**Variants List Columns:** Choose what Columns to show in variant section.
**Datasheet Default Sorting:** Enables you to set default sorting column for variant section datasheet.
**Datasheet Sorting Direction:** Chose sorting direction (ascending/discending).
**Table Header:** Show/hide List Header.
**Table Header:** Show/hide List Footer.



**Detail page style:** css of Detail page can be changed from here and can be reset to default at any time.

