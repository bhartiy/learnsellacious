---
title: 'How to SQl for getting|updating product and stock list of seller'
taxonomy:
    category:
        - docs
visible: true
---

You can run below code in your database to get the sql for getting|updating product and stock list of seller.<br>

**TO get the SQL of Products and their stock of that seller, run the below SQL.**

<pre>
<code>
//View product/seller stocks<br>
SELECT 
	`psx`.`id` `psx_id`,
    `p`.`title` `product_title`, `u`.`name` `seller_name`,
	`psx`.`disable_stock`, `psx`.`stock`, `psx`.`over_stock`, `psx`.`stock_reserved`, `psx`.`stock_sold` 
FROM `#__sellacious_product_sellers` `psx` 
INNER JOIN `#__sellacious_products` `p` ON `P`.`id` = `psx`.`product_id`
INNER JOIN `#__users` `u` ON `u`.`id` = `psx`.`seller_uid`;
</code>
</pre>

**TO get the SQL of Variants and their stock of that seller, run the below SQL.**

<pre>
<code>
//View variant/seller stocks<br>
SELECT 
	`vsx`.`id` `vsx_id`,
    `p`.`title` `product_title`,
    `v`.`title` `variant_title`, `u`.`name` `seller_name`,
	`vsx`.`stock`, `vsx`.`over_stock`, `vsx`.`stock_reserved`, `vsx`.`stock_sold` 
FROM `#__sellacious_variant_sellers` `vsx` 
INNER JOIN `#__sellacious_variants` `v` ON `v`.`id` = `vsx`.`variant_id`
INNER JOIN `#__sellacious_products` `p` ON `p`.`id` = `v`.`product_id`
INNER JOIN `#__users` `u` ON `u`.`id` = `vsx`.`seller_uid`;
</code>
</pre>

**TO update the Products stock, run the below SQL.**

<pre>
<code>
//Update products stock <br>
UPDATE `#__sellacious_products_sellers`
SET `stock` = 100, `over_stock` = 50, `stock_reserved` = 10, `stock_sold` = 1000
WHERE `product_id` = 500 AND `seller_uid` = 100;
</code>
</pre>

**TO update the Variants stock, run the below SQL.**

<pre>
<code>
//Update variants stock<br>
UPDATE `#__sellacious_variant_sellers`
SET `stock` = 100, `over_stock` = 50, `stock_reserved` = 10, `stock_sold` = 1000
WHERE `variant_id` = 500 AND `seller_uid` = 100;
</code>
</pre>

> Replace the `#_` with table prefix of your site database. 