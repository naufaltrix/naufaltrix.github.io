---
layout: post
title: Php Setting hostname
tags: [sql, shitpost]
comment: true
---

Setting php hosting di php, lumayan buat atur path

```php
<?php
	$setHostName = $_SERVER['REQUEST_SCHEME'].'://'.$_SERVER['SERVER_NAME'].'/'.$_SERVER['REQUEST_URI'];
	print($setHostName); //Result = http://localhost//trush/php7/set_server.php
?>
```

Kali aja bermanfaat.

