---
description: The pad() method pad array to the specified length with a value
---

# pad\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1,5));

//Fill with 0 to have 10 elements
$arrayUtils->pad(10, 0);
// expected output: [1, 2, 3, 4, 5, 0, 0, 0, 0, 0]

//Fill with 0 to have 10 elements, append to front of array
$arrayUtils->pad(-10, 0);
// expected output: [0, 0, 0, 0, 0, 1, 2, 3, 4, 5]
```
{% endcode %}

## Syntax

```php
$arrayUtils->pad(int $size, mixed $value) : ArrayUtils;
```

### Parameter

* `$size`
  * New size of the array.
* `$value`  
  *  Value to pad if `array` is less than `size`.

### Return value

* A padded array.

## Prefixing

```php
$arrayUtils->padAs(int $size, mixed $value) : array;
```

```php
ArrayUtils::padFrom(iterable $from, int $size, mixed $value) : ArrayUtils;
```

```php
ArrayUtils::padFromAs(iterable $from, int $size, mixed $value) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-pad" %}



