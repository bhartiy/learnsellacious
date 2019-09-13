---
title: 'How to add SMTP Mail Settings in sellacious ?'
media_order: 'smtp sttings.png'
taxonomy:
    category:
        - docs
visible: true
---

Simple Mail Transfer Protocol (SMTP) is the set of Internet standards for transmitting email across Internet networks. If you have an email provider, the best way to utilize that email within your Joomla site is to configure the SMTP settings in the Global Configurations area.

To configure your SMTP settings-
Go to Joomla Administrator >> System >> Global Configuration
Locate **mail settings **

Here you can fill the fields according to your email provider.

## **For gmail**

Mailer → SMTP
From Email → Your email address email@myemail.com
From Name → Your site name or your name Administrator of This Site
Sendmail Path → This should already be present if not it needs to be /usr/sbin/sendmail (this will not appear in Joomla 3.3)
SMTP Authentication → Select Yes
SMTP Security → SSL
SMTP Port → 465
SMTP Username → Your email address email@myemail.com
SMTP Password → Your email password
SMTP Host → smtp.gmail.com

![](smtp%20sttings.png)

You can test by sending a test mail.

After filling all the fields save configuration.

