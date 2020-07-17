---
title: Requirements
external_links:
    no_follow: true
visible: true
---

Before we begin, please ensure that you have met the Minimum Requirements in order for Sellacious to run smoothly:

<hr>
## Minimum Requirements

In order for Sellacious to operate correctly, please ensure that the following system requirements are met:<br>
    
Joomla **3.9.x**. <small>Please note: **Joomla 4.x** in NOT supported yet</small>
PHP **v5.5+** or **v7.1+**
MySQL **v5.5.3+** or MariaDB **10.1.22+** <small>(with InnoDB suppert enabled)</small>

PHP Extension: **ZIP Library** - It is requires by Sellacious for much faster extraction process.
PHP Extension: **CURL Library** - It is requires by Sellacious to perform outgoing connections.
PHP Extension: **MB String Library** - It is used by Sellacious in manipulating of database strings.
PHP Extension: **MYSQLi** - It is used by Sellacious for database connection.
PHP Extension: **Sqlite 3.25.2+** - It is used by Sellacious for products catalog caching and search indexes for faster speed and performance.

PHP: **Safe Mode = Off**
PHP: **shell_exec = Enabled**
PHP: **passthru = On**
PHP: **magic_quotes_gpc = Off**
PHP: **max_execution_time = 30**

**Note:** Below are the minimum requirements. If you want to upload larger files, increase below settings accordingly. 

PHP: **upload_max_filesize = 50MB**
PHP: **post_max_size = 50MB**
PHP: **memory_limit = 64MB**
    
    
<hr>
<br>
## Recommended Settings

To get the best out of Sellacious, below are the list of recommended settings (in addition to the minimum requirements) for your site.<br>

Joomla **3.9.x** (latest in 3.9 series, see https://downloads.joomla.org/latest) installed
PHP **v7.3** and above
MariaDB **10.1.22+** (instead of MySQL)    

**Note:** Below are the minimum requirements. If you want to upload larger files, increase below settings accordingly. 

PHP: **upload_max_filesize = 128MB**
PHP: **post_max_size = 128MB**
PHP: **memory_limit = 128MB**