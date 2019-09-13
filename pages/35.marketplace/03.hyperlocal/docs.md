---
title: 'Sellacious Hyperlocal'
media_order: 'hyperlocal1.png,hyperlocal2.png,hyperlocal3.png,hyperlocal4.png,hyperlocal5.png,hyperlocal6.png,hyperlocal7.png,rento mozo.png,hyperlocal.png,hyperlocalsdasd2.png,Region based .png,By distance.png,google api.png,gc by radius.png,gc by region.png,p location.png,product config.png'
taxonomy:
    category:
        - docs
visible: true
---

Hyperlocal is a major feature of sellacious. With the help of hyperlocal you can create your own store for local or international buyers. 

This hyperlocal package consists of a module and plugin. Which both are already built in sellacious latest version. We are upgrading this feature of sellacious day by day and adding many more additions to this feature.

_Hyperlocal is compatible to the sellacious version 1.6.x and above. If your site isn't updated yet to the latest sellacious, please update it to use hyperlocal and many more exciting feature of sellacious._

### Use cases for Sellacius Hyperlocal
Before we move to installation and configuration part lets understand use cases for Sellacious Hyperlocal. Basically there are three use cases of hyperlocal
1. [Region based](https://www.sellacious.com/learn/marketplace/hyperlocal#region-based)
2. [Radius based](https://www.sellacious.com/learn/marketplace/hyperlocal#radius-based)
3. [Product based](https://www.sellacious.com/learn/marketplace/hyperlocal#product-based)

### 1. Region Based 
In region based, hyperlocal displays a search form to find products by Location in Sellacious. It is done by **Address matching by Region**. If Address Matching is selected as region, then Sellacious will search products by the selected region. For example, if it is City/District/State/Country then the results will be displayed from that particular City/District/State/Country.
In other words it show Stores which can deliver and products which can be delivered to user location.
**Note:** Sellers can can opt for multiple regions(City/District/State/Country) for delivery of their products.


![](rento%20mozo.png)
### Configuration for Region based
For region based filtering select by region in address matching tab in joomla administrator

![](Region%20based%20.png)

and in Global Configuration of Sellacious backend

![](gc%20by%20region.png)

### 2. Radius Based

In radius based, it will search products based on distance from users current location and specified distance around it. This may sometimes span across geo-political regional boundary, viz another state or city if they fall within given distance.
Seller will choose the radius within which he wants to avail delivery of his products and hyperlocal will create a circle based on geolocation data and if user falls within that circle he will see products from that seller.
For example there are two sellers owning store1 and store2,they will be able to deliver products within their radius.
Seller1 can avail products in circle A and seller2 can vavil products in circle B. Accordingly user can see products from the circle in which they reside and if users(like user3) fall in the intersection of both the circle they can see the products from both the sellers.

![](hyperlocalsdasd2.png)


**Enterprise** version of sellacious supports **warehouse** functionality too which means a seller can have multiple warehouses with delivery capability in area where the warehouse is located. So now Seller can avail delivery in area where warehouse is located as well as the store radius.

![](hyperlocal.png)


### Configuration for Radius based
For radius based filtering select by distance in address matching tab in joomla administrator

![](By%20distance.png)

and in Global Configuration of Sellacious backend

![](gc%20by%20radius.png)

### 3. Product Based

Each product has Its Location and Product Coordinates saved with it so Sellacious Hyperlocal can filter it with this information. In case product location is not defined, hyperlocal will inherit the location of store/warehouse and product will be shown to the user if the user falls under the region or radius of concerned seller.

### Configuration for Product based

![](p%20location.png)

![](product%20config.png)







