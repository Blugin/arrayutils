---
description: The shift() method removes the first element and returns that element
---

# ArrayUtils-&gt;shift\(\)

{% code title="Example.php" %}
```php
<?php
use kim\present\utils\arrays\ArrayUtils;

ArrayUtils::from(range(1, 20))->chunk(4);
//[
//  [ 1,  2,  3,  4],
//  [ 5,  6,  7,  8],
//  [ 9, 10, 11, 12],
//  [13, 14, 15, 16],
//  [17, 18, 19, 20]
//]

ArrayUtils::from(range(1, 20))->chunk(4, true);
//[
//  [ 0 =>  1,  1 =>  2,  2 =>  3,  3 =>  4],
//  [ 4 =>  5,  5 =>  6,  6 =>  7,  7 =>  8],
//  [ 8 =>  9,  9 => 10, 10 => 11, 11 => 12],
//  [12 => 13, 13 => 14, 14 => 15, 15 => 16],
//  [16 => 17, 17 => 18, 18 => 19, 19 => 20]
//]
```
{% endcode %}

## Syntax

```php
$arrayUtils->shift() : mixed;
```

### Return value

* The first value of array.

## Polymorphism

```php
ArrayUtils::shift() : mixed;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-shift.php" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/shift" %}



