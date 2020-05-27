---
title: 'Seller''s payment method'
media_order: 'Screenshot 2020-05-08 at 3.08.21 PM.png,Screenshot 2020-05-08 at 3.03.27 PM.png,Screenshot 2020-05-08 at 3.01.47 PM.png,Screenshot 2020-05-08 at 2.59.03 PM.png,Screenshot 2020-05-08 at 2.55.16 PM.png,Screenshot 2020-05-08 at 2.53.23 PM.png,Screenshot 2020-05-08 at 2.48.32 PM.png,Screenshot 2020-05-08 at 4.35.53 PM.png'
taxonomy:
    category:
        - docs
visible: true
---

**Written by:** Indresh Maurya
**Date:** 08-05-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

Sellers can have their own payment methods in sellacious. To enable sellers to create their own payment method follow these steps-

1. First you have to grant permission to sellers to create/edit payment methods. Go to Settings->permissions and select Seller category and component Sellacious.

![](Screenshot%202020-05-08%20at%202.53.23%20PM.png)

In payment method section give relevant permission to seller like this


![](Screenshot%202020-05-08%20at%202.55.16%20PM.png)

2. Now select the payment method plugins which you want to avail to the seller. For this go to Settings->global configuration->Sellers->Limit Seller Payment Methods

![](Screenshot%202020-05-08%20at%204.35.53%20PM.png)

3. Now on seller logins payment method menu will be accessible to seller

![](Screenshot%202020-05-08%20at%203.01.47%20PM.png)

Seller can create own payment method here, by choosing available plugins 

![](Screenshot%202020-05-08%20at%203.03.27%20PM.png)

4. Now when a buyer places an order of that sellers product, sellers payment method will show up in payment options,

![](Screenshot%202020-05-08%20at%203.08.21%20PM.png)

Buyer can choose that method and place an order.




Here is some additional information about working of seller payment methods.

1. Each Seller can have its own payment method.
2. A seller's payment method can only be used when the cart contains only that particular seller's item(s).
3. A seller's payment method can only be used with the shopping cart.
4. When a seller's payment method is used and not the global one, the commission for the shop/site owner will not be applied.
5. A withdrawal transaction will be created for the seller whose payment method is used except for the E-wallet handler payment method.
6. When a seller's payment method is used and the shop owner owes any amount from the seller for that particular order, then that amount will be credited to the shop owner and debited from the seller as the seller receives the entire order amount such as for shipping charge when shipping is done by the shop owner.
7. Sellers payment method limit can be added from the Global Configuration.
8. If a seller payment method is used and a coupon is also used which belongs to the shop owner, then the shop owner will pay the coupon amount to the seller as the seller has not issued the coupon therefore the seller should get the exact amount for the order.