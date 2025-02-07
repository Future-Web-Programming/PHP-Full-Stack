# Lecture-04: Type Casting and Type Juggling

## PHP Type Juggling

### Summary:
In this tutorial, you’ll learn about PHP type juggling and Type Casting in Detail and how it works.

[![Lecture -04 Type Casting and Type Juggling](https://i9.ytimg.com/vi/4RDaNtSD5s0/mqdefault.jpg?v=67a5a812&sqp=COjQlr0G&rs=AOn4CLAteX8Sx851-cuvnUVXwsQr2yynVw)](https://youtu.be/4RDaNtSD5s0)

### Introduction to PHP Type Juggling
PHP is a loosely typed programming language, meaning that when you define a variable, you don’t need to declare its type explicitly. PHP determines the type by the context in which the variable is used.

For example, if you assign a string to a variable, its type will be a string:

```php
$my_var = 'PHP'; // a string
```

And if you assign an integer to the same variable, its type will change to an integer:

```php
$my_var = 'PHP'; // a string
$my_var = 100; // an integer
```

### How Type Juggling Works
PHP automatically converts variables to the common, comparable type when performing operations or comparisons. Consider the following example:

```php
$qty = 20;
if ($qty == '20') {
    echo 'Equal';
}
```

#### Output:
```
Equal
```

Since PHP converts the string `'20'` to an integer (20) before comparison, the result evaluates as `true`, and "Equal" is displayed.

### Type Juggling in Arithmetic Operations
PHP also applies type juggling in arithmetic operations, converting values automatically when needed:

```php
$total = 100;
$qty = "20";
$total = $total + $qty;

echo $total; // 120
```

Even though `$qty` is a string, PHP converts it to an integer before performing the addition.

Consider a slightly different example:

```php
$total = 100;
$qty = "20 pieces";
$total = $total + $qty;

echo $total; // 120
```

Here, PHP extracts the numeric value `20` from the string "20 pieces" and converts it to an integer before summation.

### Summary of Type Juggling
- PHP determines variable types based on assigned values dynamically.
- When comparing different types, PHP implicitly converts them to a common comparable type.
- PHP applies automatic type conversions in arithmetic operations.

## PHP Type Casting

### Introduction to PHP Type Casting
Type casting enables explicit conversion of a value from one type to another using specific operators.

#### Type Casting Operators:

| Cast Operator | Conversion To |
|--------------|--------------|
| (array)      | Array        |
| (bool) or (boolean) | Boolean |
| (int) or (integer) | Integer |
| (object)     | Object       |
| (real), (double), or (float) | Float |
| (string)     | String       |

### Casting to an Integer
To cast a value to an integer, use the `(int)` operator:

```php
echo (int)12.5 . '<br>'; // 12
echo (int)12.1 . '<br>'; // 12
echo (int)12.9 . '<br>'; // 12
echo (int)-12.9 . '<br>'; // -12
```

If a string is non-numeric, it is converted to `0`:

```php
$message = 'Hi';
$num = (int) $message;
echo $num; // 0
```

For numeric strings, PHP extracts leading numbers before conversion:

```php
$amount = (int)'100 USD';
echo $amount; // 100
```

Casting `null` to an integer results in `0`:

```php
$qty = null;
echo (int)$qty; // 0
```

### Casting to a Float
To convert a value to a float, use `(float)`:

```php
$amount = (float)100;
echo $amount; // 100
```

### Casting to a String
To convert a value to a string, use `(string)`, but PHP often does this automatically:

```php
$amount = 100;
echo (string)$amount . " USD"; // 100 USD
```

For `true` and `false`, `(string)` casting results in:

```php
$is_user_logged_in = true;
echo (string)$is_user_logged_in; // 1
```

Casting `null` to a string results in an empty string (`""`).

Casting an array to a string generates a warning:

```php
$numbers = [1,2,3];
$str = (string) $numbers;

echo $str; // Warning: Array to string conversion
```

### Summary of Type Casting
- Type casting allows explicit conversion of a variable to a specific type.
- PHP provides type casting operators for arrays, booleans, integers, objects, floats, and strings.
- Non-numeric strings are converted to `0` when cast to an integer.
- `null` converts to `0` for integers and an empty string for strings.
- Type juggling happens automatically, but type casting provides manual control.

This concludes our lecture on **PHP Type Casting and Type Juggling**. 🚀


