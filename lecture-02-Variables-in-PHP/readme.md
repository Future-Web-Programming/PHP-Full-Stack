# Lecture 02: PHP Variables, Constants, var_dump(), print_r(), and Global Variables

## PHP Variables
Variables in PHP are used to store data and are prefixed with a `$` sign. PHP is loosely typed, meaning variables do not need explicit data type declarations.

### Example:
```php
$name = "John Doe";
$age = 25;
$price = 99.99;
```

## PHP Constants
Constants are like variables but cannot be changed once defined. They are defined using the `define()` function or `const` keyword.

### Example:
```php
define("SITE_NAME", "My Website");
echo SITE_NAME;
```

Using `const`:
```php
const VERSION = "1.0.0";
echo VERSION;
```

## PHP var_dump() Function

### Introduction to var_dump()
The `var_dump()` function is a built-in PHP function that outputs detailed information about a variable, including its type and value. It is commonly used for debugging.

#### Example:
```php
$balance = 100;
var_dump($balance);
```
**Output:**
```
int(100)
```

### Dumping Multiple Variables
```php
$amount = 200;
$message = "Insufficient balance";
var_dump($amount, $message);
```
**Output:**
```
int(200)
string(20) "Insufficient balance"
```

### Improving Readability with `<pre>` Tag
To make the output more readable, wrap the output in `<pre>` tags:
```php
$balance = 100;
echo '<pre>';
var_dump($balance);
echo '</pre>';
```

### Creating a Helper Function
Instead of manually adding `<pre>` tags every time, you can create a reusable function:
```php
function d($data) {
    echo '<pre>';
    var_dump($data);
    echo '</pre>';
}

$balance = 100;
d($balance);
```

### Dump and Die (`dd()` Function)
Sometimes, you may want to dump a variable and terminate the script immediately. You can achieve this using `die()` along with `var_dump()`:
```php
function dd($data) {
    echo '<pre>';
    var_dump($data);
    echo '</pre>';
    die();
}

$message = 'Dump and die example';
d($message);
```
This ensures the script stops execution after dumping the information.

---

## PHP print_r() Function
The `print_r()` function is similar to `var_dump()` but provides a simpler, human-readable output. It is useful for printing arrays and objects.

### Example:
```php
$array = ["Apple", "Banana", "Cherry"];
print_r($array);
```
**Output:**
```
Array ( [0] => Apple [1] => Banana [2] => Cherry )
```

For better formatting, wrap it in `<pre>`:
```php
echo '<pre>';
print_r($array);
echo '</pre>';
```

---

## PHP Global Variables
PHP has several predefined global variables that can be accessed from anywhere in a script. These include:

- **`$_GET`** – Captures data sent via URL parameters.
- **`$_POST`** – Captures data sent via a form submission.
- **`$_SESSION`** – Stores session variables.
- **`$_COOKIE`** – Stores cookies.
- **`$_SERVER`** – Contains server and execution environment details.
- **`$_FILES`** – Handles file uploads.

### Example:
```php
echo $_SERVER['SERVER_NAME'];
echo $_GET['name'];
```

---

## Summary
- **Variables** store data dynamically, while **constants** remain unchanged.
- The **`var_dump()` function** provides detailed variable information, useful for debugging.
- The **`print_r()` function** presents array and object data in a readable format.
- **Global variables** like `$_GET`, `$_POST`, and `$_SERVER` help manage user input and server details.

This concludes Lecture 02. In the next lecture, we will explore **PHP Data Types and Type Casting.**


---

## Follow on Social Media
📌 **YouTube**: [Future Programming](https://www.youtube.com/@futureprogramming)  
📌 **Instagram**: [instagram.com/futureprogrammingofficial](https://instagram.com/futureprogrammingofficial)  
📌 **Facebook**: [web.facebook.com/futureprogrammingofficial](https://web.facebook.com/futureprogrammingofficial)  
📌 **TikTok**: [tiktok.com/@futureprogramming](https://tiktok.com/@futureprogramming)  
📌 **GitHub**: [github.com/futurewebprogramming](https://github.com/futurewebprogramming)  
📌 **Facebook Group**: [web.facebook.com/groups/futureprogrammingofficial](https://web.facebook.com/groups/futureprogrammingofficial)

