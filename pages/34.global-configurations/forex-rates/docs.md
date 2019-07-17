---
title: 'Forex Rates'
visible: true
---

Forex Rates: The forex is used for the exchange of the currency.

**CRON Job Only**: choose whether the forex rates should be updated only when called via CRON. Disable this to process on every page load. The rates will be retrieved only once in a day.The CRON is the time-based job scheduler used to schedule the jobs to run periodically at fixed times, dates or intervals.
When you have enabled ‘CRON Job Only’ above. Then you must pass a CRON Key to validate CRON calls.Use this URL for CRON Job: http://yourwebsite.com/index.php?task=forex.update&cron_key=YOUR_CRON_KEY

**CRON key**:When you have enabled ‘CRON Job Only’ above. Then you must pass a CRON key to validate CRON calls.Empty CRON Key is not allowed. The CRON is the time-based job scheduler used to schedule the jobs to run periodically at fixed times, dates or intervals.
