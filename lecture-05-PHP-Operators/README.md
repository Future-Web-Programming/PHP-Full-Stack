# PHP Assignment Operators

In PHP, operators are special symbols used to perform operations on variables and values. Operators help you perform a variety of tasks, such as mathematical calculations, string manipulations, logical comparisons, and more. Understanding operators is essential for writing effective and efficient PHP code. PHP operators are categorized into several types such as Arithmetic operators,
Assignment operators,
Comparison operators,
Increment/Decrement operators,
Logical operators,
String operators,
Array operators,
Conditional assignment operators 
Let's lern us step by step, 

## Assignment operator 
Assignment operators are used to assign values to variables.

let's learn basics of assignment operator today advance we will learn in upcoming chapter.

PHP uses the `=` to represent the assignment operator.

The following shows how to assign a value to a variable using the assignment operator:

`$variable_name = expression;`

On the `left side` of the assignment operator `(=)` is a `variable` to which you want to assign a value. And on the `right side` of the assignment operator (`=`) is a value or an expression.

When evaluating the assignment operator `(=)`, PHP evaluates the expression on the right side first and assigns the result to the variable on the left side. For example:

```php

$x = 10;
$y = 20;
$total = $x + $y;

echo $total;
```





## Arithmetic Operators
Arithmetic operators are used to perform basic arithmetic operations like addition, subtraction, multiplication, division, and modulus.


### Addition `+`

```php 
// Define two numbers
$x = 20;
$y = 15;
$x + $y
```
```php
// Addition
echo "Addition: " . ($x + $y);
```

Sum the operands

### Subtraction `–`

```php 
// Define two numbers
$x = 20;
$y = 15;
$x - $y
```
```php
// Subtraction
echo "Subtraction of two numbers: " . ($x - $y);
```

$x – $y

Differences in the Operands

### `*` Multiplication

```php 
// Define two numbers
$x = 20;
$y = 15;
$x * $y
```
```php
// Multiplication
echo "Multiplication of two numbers: " . ($x * $y);
```

### `/` Division

```php 
// Define two numbers
$x = 20;
$y = 15;
$x / $y
```
```php
// Division
echo "Division of two numbers: " . ($x / $y);
```


### `**` Exponentiation

```php 
// Define two numbers
$x = 20;
$y = 15;
$x ** $y
```
```php
// Exponentiation
echo "Multiplication of two numbers: " . ($x ** $y);
```

`%` Modulus
```php 
// Define two numbers
$x = 20;
$y = 15;
$x * $y
```
```php
// Modulus
echo "Modulus of two numbers: " . ($x % $y);
```

