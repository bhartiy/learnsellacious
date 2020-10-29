---
title: 'Datasheet Global Configurations'
media_order: 'Screenshot 2020-10-28 at 11.12.05 AM.png,Screenshot 2020-10-28 at 11.20.51 AM.png,Screenshot 2020-10-28 at 12.14.25 PM.png,Screenshot 2020-10-28 at 12.16.15 PM.png,Screenshot 2020-10-28 at 12.23.33 PM.png,Screenshot 2020-10-28 at 12.35.14 PM.png,Screenshot 2020-10-28 at 12.39.01 PM.png,Screenshot 2020-10-28 at 12.26.42 PM.png,Screenshot 2020-10-28 at 12.40.41 PM.png,Screenshot 2020-10-28 at 12.45.12 PM.png,Screenshot 2020-10-28 at 12.50.16 PM.png,Screenshot 2020-10-28 at 1.12.10 PM.png,Screenshot 2020-10-28 at 3.33.35 PM.png,Screenshot 2020-10-28 at 3.51.00 PM.png,Screenshot 2020-10-28 at 3.57.41 PM.png'
taxonomy:
    category:
        - docs
visible: true
---

**Written by:** Indresh Maurya
**Date:** 28-10-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

Datasheet Global Configurations are as follows-
1.[Distiman Filter Module](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-global-configurations#distiman-filter-module)
2.[List Page Options](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-global-configurations#list-page-options)
3.[Category Header Layout](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-global-configurations#category-header-layout)
4.[List page style](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-global-configurations#list-page-style)
5.[Detail Page Option](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-global-configurations#detail-page-option)
6.[Detail Page Style](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-global-configurations#detail-page-style)

### Distiman filter Module

**Datasheet Filters Layout:** Enable this option to get compact layout of filter module on list page.
**Note:** Compact layout works well with Manufacturer fiter, attribute filter and Submit by Apply button options. Attributes will show in module if only they are filterable. We can show/hide individual attribute filters(global/product/variant or all) in module. To know more about sellacious filter go to [Filter Configurations](https://www.sellacious.com/documentation-v2#/learn/frontend-product-filter/filter-configurations)
![](Screenshot%202020-10-28%20at%2011.20.51%20AM.png)
![](Screenshot%202020-10-28%20at%2011.12.05%20AM.png)
**Header Description:** This form can be used to show a description text over filter module.

### List Page Options
These are the list page options to show in datasheet. These option can be ovverriden at category level-

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
![](Screenshot%202020-10-28%20at%203.33.35%20PM.png)
![](Screenshot%202020-10-28%20at%2012.14.25%20PM.png) 
**Note** List page containing two or more than two categories will show only **Filterable global specifications** and Category list page will show global and category specific(core+variants) specifications. If all options are disabled then all will show. 

**Datasheet Default Sorting:** We can choose Default Sorting for list page datasheet from available options. These options also include Specifications.
![](Screenshot%202020-10-28%20at%2012.16.15%20PM.png)

**Datasheet Sorting Direction:** We can choose sorting direction (ascending/discending).

**Part Number elements:** You can choose Part Number elements wheather it is Product SKU, Seller SKU, Seller Name or all.
![](Screenshot%202020-10-28%20at%2012.23.33%20PM.png)
**Disable Hotlink in List:** Link to product details page can be disabled and can be shown as read only.
**Default List Limit:** We can set no. of products on list page under one pagination.
![](Screenshot%202020-10-28%20at%2012.26.42%20PM.png)

### Category Header Layout
Additional options are provided to configure the category page head layout.
**Category Head Layout:** Choose categoty head layout to be distiman or default.
**Show Category Image:** Show hide category image.
**Category Image Styling:** Choose wheather category image should behave as background.
**No. of Images:** Choose wheather to show image galery in case you have multiple category images.
![](Screenshot%202020-10-28%20at%201.12.10%20PM.png)
![](Screenshot%202020-10-28%20at%2012.35.14%20PM.png)

### List page style
css of list page can be changed from here and can be reset to default at any time.
![](Screenshot%202020-10-28%20at%2012.39.01%20PM.png)


### Detail page option
You can manage detail page element from here

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
![](Screenshot%202020-10-28%20at%2012.45.12%20PM.png)
**Show Long Description:** Show/hide Long Description.
**Show Price List:** Show/hide Price List (works only with dynamic pricing).
**Title for Stock:** Choose what should be title of stock.
**Unit for Stock (Text):** Choose what should be unit of stock.
![](Screenshot%202020-10-28%20at%2012.50.16%20PM.png)
**Show Tablular List:** Show/hide Variants section on details page.
**Variants List Columns:** Choose what Columns to show in variant section.
![](Screenshot%202020-10-28%20at%203.57.41%20PM.png)
**Datasheet Default Sorting:** Enables you to set default sorting column for variant section datasheet.
**Datasheet Sorting Direction:** Chose sorting direction (ascending/discending).
**Table Header:** Show/hide List Header.
**Table Header:** Show/hide List Footer.
![](Screenshot%202020-10-28%20at%203.51.00%20PM.png)

### Detail page style
css of Detail page can be changed from here and can be reset to default at any time.
![](Screenshot%202020-10-28%20at%2012.40.41%20PM.png)