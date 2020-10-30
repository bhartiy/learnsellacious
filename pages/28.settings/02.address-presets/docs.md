---
title: 'Address Presets'
media_order: 'Screenshot 2020-10-30 at 11.12.02 AM.png,Screenshot 2020-10-30 at 11.16.25 AM.png,Screenshot 2020-10-30 at 11.21.42 AM.png,Screenshot 2020-10-30 at 11.27.26 AM.png,Screenshot 2020-10-30 at 11.48.08 AM.png,Screenshot 2020-10-30 at 11.52.18 AM.png,Screenshot 2020-10-30 at 11.54.43 AM.png'
taxonomy:
    category:
        - docs
visible: true
---

**Written by:** Indresh Maurya
**Date:** 29-10-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

Not all countries follow same address formate, Address Preset feature inables us to predefine set of address format for different countries.
We have already provided set of address formate which can be seen under Address Preset menu in settings.
![](Screenshot%202020-10-30%20at%2011.12.02%20AM.png)
You can Edit or Add new address preset from here. The option provided in this feature are as follows
**Title:** Title for address preset
**Applied on Countries:** Select applied countries for this address preset in this field. **NOTE-** Only one address preset can be applied to one counrty so avoid selecting countries which are aleady present on other presets or remove ot from other preset and then you can add here.
![](Screenshot%202020-10-30%20at%2011.16.25%20AM.png)
**Address Form Fields:** From here we can enable what fields we want to show/hide/make required in our modal when asking for address on frontend.
![](Screenshot%202020-10-30%20at%2011.21.42%20AM.png)
Address lines can be multiple lines and can be mandatory individually
![](Screenshot%202020-10-30%20at%2011.48.08%20AM.png)
To know more about Addres form go to [Address Fields](https://www.sellacious.com/documentation-v2#/learn/global-configurations/frontend-display-options/address-fields)

**Shortcodes for Address Format:** Short code are provided for configuring how saved address will show on various places.**NOTE:** COUNTRY_ISO and STATE_ISO codes can be used for showing them in iso formate like US For United States etc.
**Address Format:** Put short codes in the order which you want to display saved addresses on various places.
![](Screenshot%202020-10-30%20at%2011.27.26%20AM.png)

Now when saving address in address modal if you change country other fields will show up according to created preset.
![](Screenshot%202020-10-30%20at%2011.52.18%20AM.png)
And address will render according to saved format by short codes
![](Screenshot%202020-10-30%20at%2011.54.43%20AM.png)