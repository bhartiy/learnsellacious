---
title: 'Product and Shipping Scope'
media_order: 'Screenshot 2020-05-16 at 3.11.15 PM.png,Screenshot 2020-05-16 at 3.25.35 PM.png,Screenshot 2020-05-16 at 3.37.02 PM.png,unnamed.png,Screenshot 2020-05-16 at 3.42.58 PM.png,Screenshot 2020-05-16 at 3.46.11 PM.png,Screenshot 2020-05-16 at 7.03.27 PM.png,Screenshot 2020-05-16 at 7.05.54 PM.png,Screenshot 2020-05-16 at 7.13.12 PM.png,unnamed (1).png,unnamed (2).png,Screenshot 2020-05-16 at 7.24.17 PM.png,Screenshot 2020-05-16 at 7.28.22 PM.png,Screenshot 2020-05-16 at 7.36.27 PM.png,Screenshot 2020-05-16 at 7.03.27 PM (1).png,Screenshot 2020-05-16 at 7.54.41 PM.png,unnamed (3).png,Screenshot 2020-05-16 at 8.03.16 PM.png,Screenshot 2020-05-16 at 8.13.53 PM.png,Screenshot 2020-05-16 at 8.16.37 PM.png'
taxonomy:
    category:
        - docs
visible: true
---

**Written by:** Indresh Maurya
**Date:** 20-05-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

### Product Scope:


In product scope, the seller has the option to divide store delivery time into slots.  These slots then used to deliver products accordingly. Product scope consists of four kinds of Delivery Time Selection.
A. None
B. Day
C. Day & Time Slots
D. Date & Time (Without Slots) 

![](Screenshot%202020-05-16%20at%203.11.15%20PM.png)

**NONE:**  No delivery slot will be used during placing orders. Buyer can palce order as usual.

**DAY:**  This option sets the whole day delivery time as one slot. Sellers can choose **Limit per slot** and **Available till today** which means the time till when the buyer can place an order in case the same day is being selected for delivery.

![](Screenshot%202020-05-16%20at%203.25.35%20PM.png)

Now when a buyer adds a product in the cart there is an option to select a delivery date. 

![](Screenshot%202020-05-16%20at%203.37.02%20PM.png)

Selected slots will be showing and can be edited in cart and summary steps.

![](unnamed.png)
![](Screenshot%202020-05-16%20at%203.42.58%20PM.png)

Slots will reflect on the order details page, order email, and invoices.

![](Screenshot%202020-05-16%20at%203.46.11%20PM.png)

**DATE & TIME SLOTS:**  This option provides an option for the seller to divide the delivery time into slots. **Slot duration, Slot padding**(time between two delivery slots), and **Preparation time** can be set from the seller profile.

![](Screenshot%202020-05-16%20at%207.03.27%20PM.png)

Now when a buyer adds a product in the cart there is an option to **select delivery date and slot** which will be reflected in cart, summery, order details, and order email/invoice.

![](Screenshot%202020-05-16%20at%207.05.54%20PM.png)


**DATE & TIME (WITHOUT SLOT):**  This option provides an option to the buyer to choose **Day and Point of time** for the delivery. In this case, sellers can set **Available till today** and **Preparation time**.

![](Screenshot%202020-05-16%20at%207.13.12%20PM.png)

Now when a buyer adds a product in the cart there is an option to pick a day and time.

![](unnamed%20%281%29.png)

Which will be reflected in cart, summery, order details, and order email/invoice.

![](unnamed%20%282%29.png)
![](Screenshot%202020-05-16%20at%207.24.17%20PM.png)

Orders done by any of the above methods will show in the backend **Delivery Orders View** and can be processed further from there. 

![](Screenshot%202020-05-16%20at%207.28.22%20PM.png)




---

### Shipping Scope:
(Available in version 2.0-beta1)

In shipping scope, a seller has the option to **define shipping rules for the delivery slots**. 

![](Screenshot%202020-05-16%20at%207.36.27%20PM.png)

After choosing shipping scope sellers can set **Slot duration**, **Slot padding**(time between two delivery slots), and **Preparation time** from the seller profile.

![](Screenshot%202020-05-16%20at%207.03.27%20PM%20%281%29.png)

Creating shipping rules for slots is the most important step in this case. Delivery shipping rules can be created only when you choose the shipping scope.
Here **Add to slots**  means this rates will be added into slot rate of that day/hour. For example your **flat rate** is $10 and **same day rate** is $20, if you enable add to slot rate your shipping for same day slot will be $30.If not enabled, rate for same day will be $20 and in calendar todays date will be disabled.

![](Screenshot%202020-05-16%20at%207.54.41%20PM.png)

In delivery shipping, rates can be defined for **Next Hours, Next Days**, and for the **Same Day**. When it comes to rates for slots, either **Flat Rate** can be defined for all-day slots or **individually for weekdays slots**.

![](unnamed%20%283%29.png)
![](Screenshot%202020-05-16%20at%208.03.16%20PM.png)

**NOTE:**  Delivery type shipping rules can only be created for sellers(not site-wide) and only one rule per seller. This only can be used when **Shipped by Seller** and Shipping selection is **Sellerwise or Product wise**.

Once the delivery shipping is enabled, the buyer will get the option to select shipping for the slot in the shipping step.

![](Screenshot%202020-05-16%20at%208.13.53%20PM.png)

Selected slot and shipping rate will reflect in summary and can be edited from here.

![](Screenshot%202020-05-16%20at%208.16.37%20PM.png)

After placing order slots and shipping will reftect in orders details, invoices and order email.
