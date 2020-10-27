---
title: 'Abandoned Cart Notification'
---



Execute Method: We have two methods to execute product rating notification email.
1. Run with Cron only: When you have enabled 'CRON Job Only'. Then you must pass a CRON Key to validate CRON calls. Empty CRON key is not allowed. The CRON is the time-based job scheduler used to schedule the jobs to run periodically at fixed times, dates or intervals.
Use this URL for CRON Job: http://yourwebsite.com/index.php?product_rating_notification=YOUR_CRON_KEY

2. Run on every Page Load: If you select run on every page load, you dont need to enter cron key after site URL. It will run by own on every page load.