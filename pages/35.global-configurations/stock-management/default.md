---
title: 'Stock Management'
media_order: 'screenshot-localhost-2020.06.12-18_56_58.png,Screen Shot 2020-06-12 at 7.23.09 PM.png,Screen Shot 2020-06-12 at 7.29.58 PM.png,Screen Shot 2020-06-12 at 7.32.03 PM.png'
visible: true
---

**Written By**: Rashi Gupta
**Date**: 12-06-2020
**Compatibility**: Sellacious v2.0.0-Beta1+

**Stock Management**: You can choose at what level the stock value can be set. If set to ‘Use Global Setting’ it would not be possible to enter stock at category level and product level, and once the stock ends the product will be marked as out of stock.

You can Manage stock from 3 ways:
1. From 'use global setting'
2. From 'use category setting'
3. From 'use individual product setting'

**Default intitial stock**: Set a default initial stock value for all products, this can be overridden in the category if stock management is set to category level. You can change the initial stock by scroll bar placed on the text box.

**Default over stock limit**: Set a default over stock sales limit value for all products, this can be overridden in the category if stock management is set to category level.

**Check Stock in Front-end**: If check stock in front-end is enable, it will check stock on frontend and show message "Insufficient stock" if stock is not present in that quantity.

![](screenshot-localhost-2020.06.12-18_56_58.png)

**1. Use Global Setting**: If you set stock management setting is use global setting, stock+over-stock will be saved from global in product.
</br>**2. Use Category Setting**: When you set stock management setting is use category setting, stock management tab is showing in category. From category, you can set stock management from 3 ways: 1. Global, 2. Category, 3. Individual Product
![](Screen%20Shot%202020-06-12%20at%207.23.09%20PM.png)
Global: If you save global in category, stock will be saved from global setting.
Category: If you save category, stock will be saved from category itself.
Individual Product: If you save individual product, stock will be saved from product.
</br>**3. Use Individual Product Setting**: When you set stock management is use individual setting, stock will be saved from product.
![](Screen%20Shot%202020-06-12%20at%207.29.58%20PM.png)
If you enable the stock management button, stock will be shown in list like stock+over-stock.
If you disable the stock management button, stock will be shown in list like ∞
![](Screen%20Shot%202020-06-12%20at%207.32.03%20PM.png)

**Note**: You can mark the product is umlimited only product wise.

You can also manage stock from the inventory manager and by import:

**Managing stock in bulk:**
</br>**Inventory Manager :** Inventory is used for managing the stock in your website. This feature will be useful for  the premium users only. You can change the cost price, margin price, list price, fixed price and stock from inventory window.
1. Go to the sellacious panel of your website.
2. To manage your inventory, first navigate to shop on the left side of the panel. Then,click on inventory manager      option from the dropped down menu.
3. You can change pricing and stock of any product of your inventory under inventory manager.
4. Select any product from the inventory manager then edit the fields. You can edit the cost price, Margin price,      List price and Stock from inventory window.
5. Then click on the save button for save the changes and click on save button to save the details.

**Import :** Import is used to update stocks in csv file and then import that file  in Sellacious. This feature will be useful in updation of stocks when products are in bulk. You can change the cost price ,stock , fixed price in a csv file and import it in Sellacious.
1.  Go to the sellacious panel of your website.
2. To import, first navigate to import utility on the left side of panel. Then click on importer option from the        dropped down menu.
3. In the Sellacious native format, select download with all specifiacations column and open the downloaded file.
4. Write the Product Title whose stock you want to change, and make the changes in the columns.
5. Download the file in .csv format.
6. Edit this file to Add/Update stock.
7. In the Import utility on the left pane, selects importers.
8. In the Sellacious native format, select upload csv and upload the downloaded csv file.
9. Select options which you want to import in Import configuration.
10. Click refresh Cache from left sidebar.
11. And your changes will be updated.
