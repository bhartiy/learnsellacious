---
title: 'Microsite: a manufacturer''s perspective'
media_order: 'Screenshot 2021-08-05 at 3.14.46 PM.png,Screenshot 2021-08-05 at 5.49.46 PM.png,Screenshot 2021-08-05 at 5.55.41 PM.png'
---

Once the masterAPI plugin is enabled, menu is created and manufacturer backend login permission is given by shop owner a manufacturer can take following steps to manage the microsite-

**Login to sellacious backend:** manufacturer can login in sellacious backend (https://instocka.com/sellacious) and get the limited access to manage certain things based on permission. Managing microsite is one of them.

**Manage Microsite View:** After login go to manage microsite view

![Screenshot%202021-08-05%20at%203.14.46%20PM](Screenshot%202021-08-05%20at%203.14.46%20PM.png "Screenshot%202021-08-05%20at%203.14.46%20PM")

here there are 2 main functionalities available for manufacturer

1. Launching microsite
2. Generating embed code for a product

**1. Launching microsite :** Here you get option to choose your subdomain and launch your site. if the subdomain is available green button to launch microsite will show
![](https://www.sellacious.com/learn/user/pages/48.distiman/09.microsite/Screenshot%202021-08-05%20at%2011.25.18%20AM.png)

when you click on launch it will start launching your subdomain
![](https://www.sellacious.com/learn/user/pages/48.distiman/09.microsite/Screenshot%202021-08-05%20at%2011.27.49%20AM.png)
completion of launch may take 10 to 15 minutes. You can check status in mean time
![](https://www.sellacious.com/learn/user/pages/48.distiman/09.microsite/Screenshot%202021-08-05%20at%2011.28.45%20AM.png)
When its completed it will look something like this
![](https://www.sellacious.com/learn/user/pages/48.distiman/09.microsite/Screenshot%202021-08-05%20at%2011.36.29%20AM.png)

Clicking on view microsite takes you to manufacturers microsite frontend.

![](https://www.sellacious.com/learn/user/pages/48.distiman/09.microsite/Screenshot%202021-08-05%20at%2012.16.26%20PM.png)

Product list page shows all the products listed by you on the main site. In microsite products can be searched in search box and  details page similar to main site. Items can be added to cart and checkout.
**Note:** Checkout will redirect you to main website.

**2. Embed code:** Embed code of a product can be generated in this section which then can be used to show market source of the product on your own website. Suppose you have own website and product pages are there already, You can inject this embed code in the page and market-source of the product will show on details page. The Product and its sellers inventory details will show up in this section. This also enable you to add to cart and checkout from here.

![](https://www.sellacious.com/learn/user/pages/48.distiman/09.microsite/Screenshot%202021-08-05%20at%2012.53.37%20PM.png)


**How generate Embed code:**

Generate embed code of a product enter sku of the product in this field

![](https://www.sellacious.com/learn/user/pages/48.distiman/09.microsite/Screenshot%202021-08-05%20at%2012.44.31%20PM.png)

you can see this sku is now integrated with embed code

![](https://www.sellacious.com/learn/user/pages/48.distiman/09.microsite/Screenshot%202021-08-05%20at%2012.45.53%20PM.png)

this code can be copied by clicking anywhere on it.

**Automating the process of embed code:** As you can see the only variable in the embed code is product sku so by changing this value it can be used in many product pages.


**How to use embed code:**

Embed code can be used in a product details page. if you observe closely there are two part in embed code
1. head links 
2. div to render market-source

![Screenshot%202021-08-05%20at%205.49.46%20PM](Screenshot%202021-08-05%20at%205.49.46%20PM.png "Screenshot%202021-08-05%20at%205.49.46%20PM")

You need to put links head and div in body where you want to show market-source your product page
for example here its kept below description section

![Screenshot%202021-08-05%20at%205.55.41%20PM](Screenshot%202021-08-05%20at%205.55.41%20PM.png "Screenshot%202021-08-05%20at%205.55.41%20PM")
