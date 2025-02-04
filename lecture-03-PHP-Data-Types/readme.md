# Lecture 03: PHP Variables & Data Types

## Recap of Previous Concepts
Before diving into new concepts, let's quickly review what we covered previously:
- Variables and Constants in PHP
- Using `var_dump()` and `print_r()` for debugging
- Global Variables in PHP

---

## Variables Pass by Value vs. Pass by Reference
By default, PHP variables are **passed by value**, meaning that when you assign a variable to another, it creates a copy. Any change to one variable does not affect the other.

### Example: Pass by Value
```php
$num = 10;
$num2 = $num;
$num = 20;

echo $num2; // Output: 10
```
Since `$num2` was assigned a copy of `$num`, changes to `$num` do not affect `$num2`.

### Example: Pass by Reference
If we want `$num2` to reflect changes made to `$num`, we need to use **pass by reference**:
```php
$num = 10;
$num2 = &$num; // Reference assignment
$num = 20;

echo $num2; // Output: 20
```
Here, `$num2` is now a reference to `$num`, meaning any change to `$num` will also update `$num2`.

---

## Variable Variables
PHP allows us to use variable names dynamically. This is known as **Variable Variables**.

### Example:
```php
$name = "john";
$$name = "Doe";

echo $name; // Output: john
echo ${$name}; // Output: Doe
```
Here, `$$name` creates a new variable named `john`, and its value is set to `Doe`.

---

## PHP is a Loosely Typed Language
PHP does not require explicit data type declarations. It dynamically determines the data type based on the assigned value at runtime.

Example:
```php
$var = 10; // Integer
$var = "Hello"; // String
$var = 10.5; // Float
```
The same variable can hold different types of values at different times.

---

## PHP Data Types
PHP has three main categories of data types:

### 1. Scalar Types (Single Value Types)
#### **String**
A sequence of characters enclosed in quotes (`""` or `''`).
```php
$data = "PHP Learning";
echo $data; // Output: PHP Learning
```

#### **Integer**
A whole number (positive, negative, or zero) without decimal points.
```php
$data = 25;
echo $data; // Output: 25
```

#### **Float (Double)**
A number with decimal points.
```php
$data = 12.5;
echo $data; // Output: 12.5
```

#### **Boolean**
Represents `true` or `false` values.
```php
$data = true;
var_dump($data); // Output: bool(true)
```

---

### 2. Compound Types (Multiple Values)
#### **Array**
Stores multiple values in a single variable.
```php
$data = ["HTML", "CSS", "JavaScript", "PHP", "Python"];
echo $data[0]; // Output: HTML
```

#### **Object**
Instances of user-defined classes.
```php
class Car {
    public $brand = "Toyota";
}

$data = new Car();
echo $data->brand; // Output: Toyota
```

---

### 3. Special Type
#### **NULL**
Represents a variable with no value.
```php
$data = null;
var_dump($data); // Output: NULL
```

---

## Type Hinting (PHP 8+)
In modern PHP versions, we can enforce types using **type hinting** for function parameters and return values.

Example:
```php
function addNumbers(int $a, int $b): int {
    return $a + $b;
}
echo addNumbers(5, 10); // Output: 15
```

---

## Summary
- **Pass by Value vs. Reference:** Assigning variables normally creates copies, while `&` makes a reference.
- **Variable Variables:** Use `$$` to create dynamic variable names.
- **Loosely Typed Nature:** PHP determines variable types dynamically at runtime.
- **PHP Data Types:** Includes Scalar (String, Integer, Float, Boolean), Compound (Array, Object), and Special (NULL).
- **Type Hinting in PHP 8+:** Allows enforcing types at function and class levels.

This concludes Lecture 03. In the next lecture, we will explore **PHP Operators and Expressions.**



---

## Follow on Social Media
📌 **YouTube**: [Future Programming](https://www.youtube.com/@futureprogramming)  
📌 **Instagram**: [instagram.com/futureprogrammingofficial](https://instagram.com/futureprogrammingofficial)  
📌 **Facebook**: [web.facebook.com/futureprogrammingofficial](https://web.facebook.com/futureprogrammingofficial)  
📌 **TikTok**: [tiktok.com/@futureprogramming](https://tiktok.com/@futureprogramming)  
📌 **GitHub**: [github.com/futurewebprogramming](https://github.com/futurewebprogramming)  
📌 **Facebook Group**: [web.facebook.com/groups/futureprogrammingofficial](https://web.facebook.com/groups/futureprogrammingofficial)

