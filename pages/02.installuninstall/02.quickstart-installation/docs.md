---
title: 'Quickstart Install'
media_order: 'quickstart1.jpg,joomla1.jpg,Sample-data.jpg,remove.jpg,webmaster.jpg,quickstart.png,install1.png,install2.png,install3.png,install4.png,install5.png,quickstart1.png,install11.png,install12.png,install13.png,Screen Shot 2020-05-09 at 5.29.38 PM.png,Screen Shot 2020-05-09 at 5.50.42 PM.png,Screen Shot 2020-05-09 at 9.35.50 AM.png,Screen Shot 2020-05-09 at 5.50.25 PM.png,Screen Shot 2020-05-09 at 5.54.51 PM.png,Screen Shot 2020-05-09 at 6.png,Screen Shot 2020-05-09 at 6.35.39 PM.png'
published: true
taxonomy:
    category:
        - docs
visible: true
---

**Written by:** Rashi Gupta
**Date:** 12-05-2020
**Compatibility:** Sellacious v2.0.0-Beta1+

When you download Sellacious, you will find zip SQuickv2-Quickstart_v2.x.x.zip. Quickstart is an exact replica of what you see on our demo. This is for both multivendor and single vendor marketplace and configuring correctly will convert a simple single vendor marketplace to a multivendor marketplace and vice-versa. 

Quickstart is very easy to install same as the Joomla installation. The quickstart package is free and consists of sample data quickstart packages comes free with all our Free or Paid templates. The default free template "SQuick" also contain this magical file. It normally takes just 10 minutes to create a multivendor website using our quickstart.

1. Download the quickstart package from https://www.sellacious.com/download.
![](quickstart1.png)
2. Unzip quickstart package "SQuickv2-Quickstart_v2.x.x.zip". When installing on Localhost place the unziped folder inside `htdocs` folder. When installing on server use website root folder, mostly its named as `public html` or `www`.
3. In XAMPP, all databases bydefault are under user `root` with no password.
4. For online server, 
*  Go to cPanel > Databases > MySQL databases
![](Screen%20Shot%202020-05-09%20at%205.54.51%20PM.png)
*  Create new database and add new user.
![](Screen%20Shot%202020-05-09%20at%205.50.25%20PM.png)![](Screen%20Shot%202020-05-09%20at%206.35.39%20PM.png)
*  After that add new user to the new craeted database
![](Screen%20Shot%202020-05-09%20at%206.png)
5. For local server,open your browser navigate to the folder containing the Quickstart package files(i.e. localhost/folder). For online server, navigate to your main domain or appropriate subdomain (i.e http://mydomain.com/), depending on where you have uploaded the Quickstart installation package.
6. You will be redirected to the installation page of Quickstart.
7. Fill the required fields mentioned on the Installer screen. First is store setting, enter store email and password.
![](install1.png)
8. Second is database, enter the database name with root user (for local server). If you install it on live, enter that database name, username and password that you created in step4(cPanel).
![](install2.png)
9. In third license step, choose your subscription plan and activate that plan (use licence key if already baught plan)and click on next.
![](install3.png)
Related points
* To activate the license for the first time https://www.sellacious.com/learn/premiumlicenses/new-subscription
* To upgrade the license, https://www.sellacious.com/learn/premiumlicenses/upgrade-to-premium
10. Fourth is overview step, In which store setting and database configurations are showing.
![](install4.png)
11. Final last one is installing step. After successfull installation, please remove the installation folder by clicking the option. ![](install5.png) ![](install11.png)
12. You can login to the Joomla administrator panel by www.domain.com/administrator.
![](install12.png)
13. You can login to the Sellacious administrator panel by www.domain.com/sellacious
![](install13.png)








