---
title: 'SEO Settings'
media_order: 'Screenshot (20).png,Screen Shot 2020-10-27 at 6.38.01 PM.png,Screen Shot 2020-10-27 at 6.40.18 PM.png,Screenshot 2021-02-13 at 3.19.32 PM.png,Screenshot 2021-02-13 at 3.40.16 PM.png,Screenshot 2021-02-18 at 2.23.28 PM.png'
---

In SEO setting, we have two configuration where we can write JS script for order success and order failure.
1. **Order Success Script**: You can enter here Order Success JS Script for your website, that will execute on order success.

2. **Order Failure Script**: You can enter here enter Order Failure JS Script for your website, that will execute on order failure.

![](Screenshot%20%2820%29.png)

Here, I write script in order success sript. 
![](Screen%20Shot%202020-10-27%20at%206.40.18%20PM.png)
After completing order successfully, alert box will show as per order success script.
![](Screen%20Shot%202020-10-27%20at%206.38.01%20PM.png)

#### Nofollow settings:
These settings allow us to add rel=nofollow to various pages in sellacous. Which helps us to manage our SEO.
![](Screenshot%202021-02-13%20at%203.19.32%20PM.png)
**Add rel=nofollow to product links:** This adds rel=nofollow to all the product list pages in sellacous.
**Add robots meta tag to products page:** This helps us to add robots meta tags on product list page. The robots can be added in following combinations-
index-nofollw, noindex-follow, noindex-nofollow
**Add disallow for products links in robots.txt:** This helps us to disallow all the products list page links.
**Add nofollow to category links on levels:** Add robots meta tag to category pages on levels
**Add robots meta tag to category page:** This helps us to add robots meta tags on category page.
**Add robots meta tag to category pages on levels:** Add robots meta tag to category pages on levels.
**Disallow categories links in robots.txt:** This helps us to disallow all the category page links.

**Note:** These settings can be overriden if seleced in category level.
![](Screenshot%202021-02-13%20at%203.40.16%20PM.png)

#### Google Structured Data
Config is added for existing products markup and local business markup for store.
![](Screenshot%202021-02-18%20at%202.23.28%20PM.png)
Config added to show/hide Products markup in Global and Product category.
Config added to show/hide Product markup in Global.
Config added to show/hide Store markup in Global and Seller Profile.

If enabled, Store markup should show following Local Business Structured data in "View source" if available,
**Store Markup:**
Store logo url
Store name
Store address, country, locality, state, zip
Store geo coordinates
Store url
Mobile/Telephone no.
Store Timings
Store reviews
**Product markup:**
Name => Product title
Product images
Product description
SKU
Brand => Manufacturer
Product rating
Offer => Seller currency, price, instock/out of stock, Seller name, Url

**Note:** These settings can be overriden if seleced in category and seller profile.
