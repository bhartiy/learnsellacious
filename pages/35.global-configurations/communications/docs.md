---
title: 'Communications/Text Msg/OTP'
media_order: 'Screenshot 2020-06-08 at 1.32.28 PM.png,Screenshot 2020-06-08 at 5.29.23 PM.png,Screenshot 2020-06-08 at 5.48.47 PM.png,Screenshot 2020-06-08 at 5.54.52 PM.png'
taxonomy:
    category:
        - docs
visible: true
---

**Written by:** Indresh Maurya
**Date:** 08-06-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

Communications consists of text mesaage and OPT finctionality which can be used to send OTP while login and registration and sending text notifications for order status change, seller chat and other evernts in the shop.
To enable this functionality in your shop follow these steps-

**1. Download and install sms plugin:-** We have these two plugins which can be used with sellacious for communications https://www.sellacious.com/apps-and-integrations/sms-integration . Download one which you want to use as a communication API.

If you are only buying plugin (not plugin+configuration) you can go further in this documentation and configure yourself. If you are buying it with configuration+support stop here and ask our team to do it for you.

Make sure you alredy sign up on respective website and purchased sms+otp balance. If not go to the website and do so. 
Twillio: https://www.twilio.com
Msg91: https://msg91.com

2. Install and enable the plugin from Joomla backend **Manage->Extention->Install**.

![](Screenshot%202020-06-08%20at%201.32.28%20PM.png)

3. After install and enable thsese two plugin the sms API will show in Settings->Global Configuration->Communications. Add Auth tokan and save.

![](Screenshot%202020-06-08%20at%205.29.23%20PM.png)
![](Screenshot%202020-06-08%20at%205.48.47%20PM.png)

4. Now configure OTP configuration from Global Confuguration->Login & Registration.

![](Screenshot%202020-06-08%20at%205.54.52%20PM.png)

