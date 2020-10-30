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

Not all countries follow the same address format, the Address Preset feature enables us to predefine a set of address formats for different countries.
We have already provided a set of address formats which can be seen under the Address Preset menu in settings.
![](Screenshot%202020-10-30%20at%2011.12.02%20AM.png)
You can Edit or Add a new address preset from here. The option provided in this feature are as follows
**Title:** Title for address preset
**Applied on Countries:** Select applied countries for this address present in this field. **NOTE-** Only one address preset can be applied to one country so avoid selecting countries which are already present on other presets or remove it from other presets and then you can add here.
![](Screenshot%202020-10-30%20at%2011.16.25%20AM.png)
**Address Form Fields:** From here we can enable what fields we want to show/hide/make required in our modal when asking for an address on the frontend.
![](Screenshot%202020-10-30%20at%2011.21.42%20AM.png)
**Language Keys** can be used to translate Label of address fields. Clicking on it will take you to translation page where you can select language and translate.
Address lines can be multiple lines and can be mandatory individually
![](Screenshot%202020-10-30%20at%2011.48.08%20AM.png)
To know more about Address form go to [Address Fields](https://www.sellacious.com/documentation-v2#/learn/global-configurations/frontend-display-options/address-fields)

**Shortcodes for Address Format:** Short codes are provided for configuring how saved addresses will show up in various places.**NOTE:** COUNTRY_ISO and STATE_ISO codes can be used for showing them in iso format like US For United States etc.
**Address Format:** Put short codes in the order which you want to display saved addresses on various places.
![](Screenshot%202020-10-30%20at%2011.27.26%20AM.png)

Now when saving address in address modal if you change country other fields will show up according to created preset.
![](Screenshot%202020-10-30%20at%2011.52.18%20AM.png)
And address will render according to saved format by short codes
![](Screenshot%202020-10-30%20at%2011.54.43%20AM.png)