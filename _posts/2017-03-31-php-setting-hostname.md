---
layout: post
title: Php Setting hostname
tags: [sql, shitpost]
comment: true
---

Setting nama server di php denga menggunakan $_SERVER.
Kalau mau liat lebih lanjut bisa cari di $_SERVER seperti script dibawah.
```php
<?php
  print_r($_SERVER);
?>
```
Contoh mengatur url untuk browser :

```php
<?php
	$setHostName = $_SERVER['REQUEST_SCHEME'].'://'.$_SERVER['SERVER_NAME'].
	$_SERVER['REQUEST_URI'];
	
	print($setHostName); //Result = http://localhost/trush/php7/set_server.php
?>
```

Kali aja bermanfaat.

