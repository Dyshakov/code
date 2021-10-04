#  Пример кода PHP #

## Подключение к базе данных

Подключение к БД
```php

<?php

$server = '127.0.0.1';
$user_name = 'root';
$password = 'root';
$db_name = 'testDB';

$connection = mysqli_connect($server, $user_name, $password, $db_name);

?>

```

Проверка подключения

```php

<?php

if ($connection)
{
  echo "Подключение к базе данных прошло успешно";
}
else
{
  echo "Не удалось подключиться к базе данных";
  echo mysql_connect_error(); //вывод ошибок
  exit(); //остановка скрипта
}

```

## Создание простой регистрации

Создание формы для отправки данных `html`

```html
<form method = "POST" action = "/sign_up.php">
		<input type="text" placeholder="Ваш логин" name="login">
		<br>
		<input type="text" placeholder="Ваш пароль" name="password">
		<br>
		<input type="submit" value="Отправить">
</form>
```

Обработка данных из формы `php`
```php
//Получение данных из формы с помощью метода POST
$login = $_POST[login];
$pass = $_POST[password];

//SQL запрос к базе данных, который создает новое поле в таблице "users". В столбец "login" и "password" он записывает данные из переменных "$login" и "$pass"
$result = mysqli_query($connection, "INSERT INTO `users`(`login`, `password`) VALUES ('$login', '$pass')");
