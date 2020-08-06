---
title: Permissions
media_order: 'Screenshot 2020-06-04 at 4.57.04 PM.png'
taxonomy:
    category:
        - docs
visible: true
---

**Written by:** Indresh Maurya
**Date:** 03-08-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

This section specifies the user category you want to give the permission. In Sellacious v2.0.0-Beta1+ sellacious user categories are considered as user groups. Also permissions can be selected component wise, means you have to select category and component and then set permission accordingly.

To set permissions go to **Settings->Permissions**, In User Category choose the category to which you want to set particular permissions and component for which you wnat to set pemissions.

Here either we can set permissions manually or can copy from any existing category.

![](Screenshot%202020-06-04%20at%204.57.04%20PM.png)

These are the component wise permissions-
[Global Permissions](https://www.sellacious.com/documentation-v2#/learn/settings/permissions/global-permissions)
[Sellacious Importer](https://www.sellacious.com/learn/settings/permissions/sellacious-importer)
[Languages](https://www.sellacious.com/learn/settings/permissions/languages)
[Menu Manager](https://www.sellacious.com/learn/settings/permissions/menu-manager)
[Sellacious](https://www.sellacious.com/learn/settings/permissions/sellacious)
[Sellacious Delivery](https://www.sellacious.com/learn/settings/permissions/sellacious-delivery)
[Advance Reporting](https://www.sellacious.com/learn/settings/permissions/advance-reporting)

**Please Note:**
* A user with Super Admin / Shop Owner access will always be Allowed irrespective of the denied settings anywhere.
* Inherit means this category will use the rules of its parent categories.
* Denied means users in this category and all sub-categories will not be allowed to perform the specific action irrespective of the sub-categories' Allowed setting.
* Allowed means the users in this category will be allowed to perform the specific action. But if any of the parent categories have Denied set, then Allowed will have no effect and Denied will be applied.