---
description: >-
  The flat() method creates a new array with all sub-array elements concatenated
  into it recursively up to the specified depth.
---

# ArrayUtils-&gt;flat\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from([
    [1, 2, 3],
    [[4, 5, 6], [7, 8, 9]],
    10
]);

//To flat single level array
$arrayUtils->flat();
// expected output: [1, 2, 3, [4, 5, 6], [7, 8, 9], 10]

//To flat two level array
$arrayUtils->flat(2);
// expected output: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
{% endcode %}

## Syntax

```php
$arrayUtils->flat(int $dept = 1) : ArrayUtils;
```

### Parameter

* `$dept` ![](../.gitbook/assets/badge_optional.svg) 
  * The depth level that should be flattened. Default is `1`.

### Return value

* A new array with the sub-array elements concatenated into it.

## Polymorphism

```php
$arrayUtils->flatAs(int $dept = 1) : array;
```

```php
ArrayUtils::flatFrom(iterable $from, int $dept = 1) : ArrayUtils;
```

```php
ArrayUtils::flatFromAs(iterable $from, int $dept = 1) : array;
```

## References

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/flat" %}



