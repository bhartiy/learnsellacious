---
title: 'Backend / Frontend Language Switcher'
media_order: 'translation3.png,front1.png,front2.png,front3.png'
taxonomy:
    category:
        - docs
visible: true
---

**Sellacious backend Language Switcher:**
In sellacious backend there's inbluilt language switcher, from which you can change the language of the backend.

![](translation3.png)

---

**Frontend Language Switcher:**

To enable the language switcher on the frontend, you need to complete below steps:
1. Install languages
2. Enable and configure the plugins
3. Navigate language Menus
4. Configure the module in frontend

**Install languages:**

To enable the language switcher in the frontend, you need more than one language. You can know about the language installation from here. We're installing French languages here. [How to install languages in sellacious?](https://www.sellacious.com/documentation-v2#/learn/languages/installing-languages)

**Enable and configure the plugins:**

To use language switcher in the frontend, you need to enable the plugins listed below:
1. System - Language Code: This plugin provides the ability to change the language code in the generated HTML document to improve SEO.
The fields will appear when the plugin is enabled and saved.

2. System - Language Filter: This plugin filters the displayed content depending on the language. This plugin is to enable the Language Switcher module. By default, this plugin will try to detect the language settings of the visitor browser and display the site in this language (if available). You can also configure this plugin according to your needs.

**Navigate language Menus:**

You need to create menus for languages available (English and French). We'll need separate menus pointing towards to English and French. To create menus for diff languages follow below steps:
1. Go to Joomla administrator > Menus > Manage > Add new menu.
2. First, create a menu for the French language:<br>
Title: enter **French Menu**.<br>
Menu Type: enter **frenchmenu**.<br>
Description: enter a description, ie **Menu for French content**.<br>
Click Save & Close.<br>
3. Now create another menu for the English language:<br>
Title: enter **English Menu**.<br>
Menu Type: enter **englishmenu**.<br>
Description: enter a description, ie **Menu for English content**.<br>
Click Save & Close.

---

**Language Menu Item**

Now, we need to create the menus items in both menus. In this documentation, we'll create menu items for the Sellacious products.<br>
First, we'll create a menu item for the French menu:
1. Go to Joomla administrator > Menus > French Menu > Add New Menu Item.
2. Select the menu item type, Sellacious > Products.
3. Enter Title Des produits (Products in French). You can give it anything you want. This title will be visible for the users.
4. Make sure Menu should be selected French Menu and language should be French as we're creating the menu item for French Menu and save the menu.<br>

To Create Menu items in the English language, repeat the above steps to step (2).
3. Enter the title Products.
4. Make sure Menu should be selected English Menu and language should be English as we're creating the menu item for English Menu and save the menu.
You can repeat the above process to create more menus in the French and English language.

---

**Default Home Page**

To publish these menus on the frontend, let's assign default home pages in both languages.
You can do that by clicking on the star in the Home column next to the menu item. The star will change into the flag of the British for English language and of the French flag for French Langauge. We have assigned the Products menu item in English menu and Des produits menu item in French menu as default home page.

---

**Associate different language Menus**

Now, you have menus in different languages (English and French) which needs to be associated with each other so the site can know which menu is the translation of which menu. To associate the English menu with their translation in French:
1. Go to Joomla administrator > Menus > English Menu > Products.
2. Click on the tab Associations and select the appropriate French menu item: Des produits and save the menu.
You need to repeat the above process for other menus of their association are available.

---

**Assign Menu Modules**

Now, both menus and their menu items are created. To visualize these menus on the frontend, we need to assign the menu modules to these menus.
1. Go to Joomla administrator > Menus > Manage.
2. Click on the Add a module for this menu. It will open a new menu module. 
3. To configure the module:<br>
Title: French Menu.<br>
Language: Select French (FR).<br>
Position: Select position-7 (or any position you want to assign).<br>
Click Save & Close.
Repeat the above process to create a module for the English menu. To configure the module for English menu:<br>
Title: English Menu.<br>
Language: Select English (en-GB).<br>
Position: Select position-7 (or any position you want to assign).<br>
Click Save & Close.

---

**Unpublish the Default Menu**

Apart from our two new menus, the website also contains the Main Menu, which is part of the Site default setup. If you have installed Sellacious without sample data, this menu contains only a Home item. Even if our bilingual site will use the new English Menu and the new French Menu, your site still needs this default Main Menu and its Home menu item to function. Your site also requires the Main Menu module to remain assigned to Language: All.
As we don't need to publish Main Menu on the frontend, we need to unpublish the Main Menu module.

1. Go to Extensions > Modules. 
2. Search the Main Menu module and unpublish it.


