# Lab9Web
# Modular
```
Nama   : Fathan Atallah Rasya Nugraha
NIM    : 312410425
Kelas  : TI.24.A3
```
## Code
### Index.php
```php
<?php 
require "config/app.php";
require "config/database.php";
?>
<link rel="stylesheet" href="assets/css/style.css">
<?php
$page = isset($_GET['page']) ? $_GET['page'] : 'home';

switch($page){
    case 'home':
        include "views/home.php";
        break;

    case 'user/list':
        require "modules/user.php";
        user_list();
        break;

    case 'about':
        include "views/about.php";
        break;

    default:
        echo "404 Page Not Found";
}
?>
```
### header.php
```php
<!DOCTYPE html>
<html>
<head>
    <title>Modular Project</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<div class="container">
<header>
    <h1>Sistem Modular PHP</h1>
    <nav>
        <a href="index.php?page=home">Home</a>
        <a href="index.php?page=user/list">User</a>
        <a href="index.php?page=about">About</a>
    </nav>
</header>
```

### footer.php
```php
<footer>
    <p>&copy; 2025 - Praktikum Modular</p>
</footer>
</div>
</body>
</html>
```
## Tampilan Home
![img](img/home.png)
