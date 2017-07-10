---
layout: post
title: Dasar API
tags: [php, shitpost, ngulik]
comment: true
---

Untuk pembahasan selanjutnya gw mau bikin API yang sederhana dari kodingan, Intinya sih
bukan dari template, tetapi konsep dasar dari get API aja sebenernya, langsung aja di cek.

```php
<?php
  	$servername = "localhost";
	$username = "username";
	$password = "password";
	$dbname = "DatabaseName";

  	$conn = mysqli_connect($servername, $username, $password, $dbname);
  	function sampleTable() {
  		$a = (! $_GET['start']) ? 0 : $_GET['start'];
  		$b = (! $_GET['limit']) ? 10 : $_GET['limit'];

  		$getQuery = "SELECT * FROM nama_table LIMIT $_GET['start'], $_GET['limit']";
  		$result = mysqli_query($conn, $sql);

  		json_encode($result);
  	}
?>
```
Kalau udah dijalanaini ini function hasilnya adalah data JSon, dan ini bisa digunain untuk API.
Ini cara mudahnya aja, kalau mau RESTFULL (POST, GET, PUT, DELETE) bisa diliat caranya di google.  
Contoh data json bisa dilihat dibawah:

```json
[
  {
    "username": "naufal",
    "email": "naufal@sample.com"
  }
]
```

Kali aja bermanfaat.
