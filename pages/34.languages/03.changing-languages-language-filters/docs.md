---
title: 'Backend / Frontend Language Switcher'
media_order: 'translation3.png,front1.png,front5.png,front6.png,front7.png,front8.png,front9.png,front10.png,front11.png,front12.png,front13.png,front14.png,front15.png,front16.png,front17.png,front18.png,front19.png,front20.png,front21.png'
taxonomy:
    category:
        - docs
visible: true
---

**Sellacious backend Language Switcher:**
In sellacious backend there's inbuilt language switcher, from which you can change the language of the backend.

![](translation3.png)

---

**Frontend Language Switcher:**

To enable the language switcher on the frontend, you need to complete below steps:
1. Install languages
2. Enable and configure the plugins
3. Navigate language Menus
4. Configure the module in frontend

---

**1. Install languages:**

To enable the language switcher in the frontend, you need more than one language. You can know about the language installation from here. We're installing French languages here. [How to install languages in sellacious?](https://www.sellacious.com/documentation-v2#/learn/languages/installing-languages)

---

**2. Enable and configure the plugins:**

To use language switcher in the frontend, you need to enable the plugins listed below:

![](front1.png)

1. **System - Language Code:** This plugin provides the ability to change the language code in the generated HTML document to improve SEO.
The fields will appear when the plugin is enabled and saved.

2. **System - Language Filter:** This plugin filters the displayed content depending on the language. This plugin is to enable the Language Switcher module. By default, this plugin will try to detect the language settings of the visitor browser and display the site in this language (if available). You can also configure this plugin according to your needs.

![](front5.png)

---

**3. Navigate language Menus:**

You need to create menus for languages available (English and French). We'll need separate menus pointing towards to English and French. To create menus for diff languages follow below steps:
1. Go to Joomla administrator > Menus > Manage > Add new menu.

![](front7.png)

2. First, create a menu for the French language:
* Title: enter **French Menu**.
* Menu Type: enter **frenchmenu**.
* Description: enter a description, i.e **Menu for French content**.
* Click Save & Close.

![](front6.png)

3. Now create another menu for the English language:
* Title: enter **English Menu**.
* Menu Type: enter **englishmenu**.
* Description: enter a description, i.e **Menu for English content**.
* Click Save & Close.

![](front8.png)

---

>**Language Menu Item**

Now, we need to create the menus items in both menus. In this documentation, we'll create menu items for the Sellacious products.<br>
First, we'll create a menu item for the French menu:
1. Go to Joomla administrator > Menus > French Menu > Add New Menu Item.

![](front9.png)

2. Select the menu item type, Sellacious > Products.
3. Enter Title Des products (Products in French). You can give it anything you want. This title will be visible for the users.
4. Make sure Menu should be selected French Menu and language should be French as we're creating the menu item for French Menu and save the menu.<br>

![](front10.png)

To Create Menu items in the English language:
1. Go to Joomla administrator > Menus > English Menu > Add New Menu Item.

![](front11.png)

2. Select the menu item type, Sellacious > Products.
3. Enter the title Products.
4. Make sure Menu should be selected English Menu and language should be English as we're creating the menu item for English Menu and save the menu.

![](front12.png)

You can repeat the above process to create more menus in the French and English language.

---

>**Default Home Page**

To publish these menus on the frontend, let's assign default home pages in both languages.<br>
You can do that by clicking on the star in the Home column next to the menu item. The star will change into the flag of the British for English language and of the French flag for French Langauge.

![](front13.png)

We have assigned the Products menu item in English menu and Des products menu item in French menu as default home page.

![](front14.png)

---

>**Associate different language Menus**

Now, you have menus in different languages (English and French) which needs to be associated with each other so the site can know which menu is the translation of which menu. To associate the English menu with their translation in French:<br>
1. Go to Joomla administrator > Menus > English Menu > Products.
2. Click on the tab Associations and select the appropriate French menu item:Des produits and save the menu.<br>

![](front15.png)

You can view the available association in Menu item List view.

![](front16.png)

You need to repeat the above process for other menus of their association if available.

---

>**Assign Menu Modules**

Now, both menus and their menu items are created. To visualize these menus on the frontend, we need to assign the menu modules to these menus.
1. Go to Joomla administrator > Menus > Manage.
2. Click on the Add a module for this menu. It will open a new menu module.

![](front17.png)

3. To configure the module for French Menu:
* Title: French Menu.
* Language: Select French (FR).
* Position: Select position-7 (or any position you want to assign).
* Click Save & Close.

![](front18.png)

4. Repeat the above process to create a module for the English menu.
To configure the module for English menu:
* Title: English Menu.
* Language: Select English (en-GB).
* Position: Select position-7 (or any position you want to assign).
* Click Save & Close.

![](front19.png)

---

>**Unpublish the Default Menu**

Apart from our two new menus, the website also contains the Main Menu, which is part of the Site default setup. If you have installed Sellacious without sample data, this menu contains only a Home item. Even if our bilingual site will use the new English Menu and the new French Menu, your site still needs this default Main Menu and its Home menu item to function. Your site also requires the Main Menu module to remain assigned to Language: All.
As we don't need to publish Main Menu on the frontend, we need to unpublish the Main Menu module.

1. Go to Extensions > Modules. 
2. Search the Main Menu module and unpublish it.

![](front20.png)

---

**4. Configure the module in frontend**

We have now two sets of Menus: one French and another English. Of course, only one menu will be visible on the frontend, either French or English Menu, which will depend on the browser settings of the visitor. As we want the user to be able to switch from a language to another, we need to add the built-in _Language Switcher Module_.

1. Go to Joomla administrator > Extensions > Modules. Click on the button New and select Language Switcher module type.
2. Enter a Title: for example, Choose your language.
3. Position: Select position-7 ( Or any position you want).
4. Language: Select All, as this module will be displayed regardless of the selected language.<br>

![](front21.png)

After saving this module, you can see the language switcher module on the right column of the site.

![](front22.png)