---
title: 'Datasheet Category Configurations'
media_order: 'Screenshot 2020-10-28 at 2.39.00 PM.png,image1.png,Screenshot 2020-10-28 at 3.33.35 PM.png,image2.png,image3.png,image4.png,image5.png,image6.png,image7.png,image8.png,image9.png,image10.png,image11.png,Screenshot 2020-10-28 at 3.51.00 PM.png'
taxonomy:
    category:
        - docs
visible: true
---

**Written by:** Indresh Maurya
**Date:** 28-10-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

Datasheet Category Configurations are as follows-
1. [List Page Options](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-category-configurations#list-page-options)
2. [Category Header Layout](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-category-configurations#category-header-layout)
3. [List page style](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-category-configurations#list-page-style)
4. [Detail page option](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-category-configurations#detail-page-option)
5. [Detail page option](https://www.sellacious.com/learn/distiman/datasheet-component/datasheet-category-configurations#detail-page-style)

### List Page Options

**Use Settings from:** Here we can decide whether to use global datasheet config for this category or use different category settings for this particular category.
![](Screenshot%202020-10-28%20at%202.39.00%20PM.png)
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
![](image1.png)

**Note** List page containing two or more than two categories will show only **Filterable global specifications** and Category list page will show global and category specific(core+variants) specifications. If all options are disabled then all will show. 

**Datasheet Default Sorting:** We can choose Default Sorting for list page datasheet from available options. These options also include Specifications.
![](image2.png)
**Datasheet Sorting Direction:** We can choose sorting direction (ascending/discending).

**Part Number elements:** You can choose Part Number elements wheather it is Product SKU, Seller SKU, Seller Name or all.
![](image3.png)
**Disable Hotlink in List:** Link to product details page can be disabled and can be shown as read only.
**Default List Limit:** We can set no. of products on list page under one pagination.
![](image4.png)

### Category Header Layout
Additional options are provided to configure the category page head layout.
**Category Head Layout:** Choose category head layout to be distiman or default.
**Show Category Image:** Show hide category image.
**Category Image Styling:** Choose wheather category image should behave as background.
**No. of Images:** Choose wheather to show image galery in case you have multiple category images.
![](image5.png)
![](image6.png)

### List page style
css of list page can be changed from here and can be reset to default at any time.
![](image7.png)

### Detail page option
You can manage detail page element from here

**Use Settings from:** Here we can decide whether to use global datasheet config for this category or use different category settings for this particular category.
![](image11.png)
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
![](image8.png)
**Show Long Description:** Show/hide Long Description.
**Show Price List:** Show/hide Price List (works only with dynamic pricing).
**Title for Stock:** Choose what should be title of stock.
**Unit for Stock (Text):** Choose what should be unit of stock.
![](image9.png)
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
![](image10.png)