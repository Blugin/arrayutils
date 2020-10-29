---
description: The mapToArray() static method cast all elements of the iterable to an array
---

# ArrayUtils::mapToArray\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

ArrayUtils::mapToArray([
    1,
    [2, 3],
    new class()extends \StdClass{public $arrayStart = 0;},
    new ArrayObject([1, 2, 3, 4, 5]),
    new ArrayIterator(["ArrayUtils", "mapToArray"])
]));
//Array(
//  Array(1),
//  Array(2, 3),
//  Array("arrayStart" => 0),
//  Array(1, 2, 3, 4, 5),
//  Array("ArrayUtils", "mapToArray")
//)
```
{% endcode %}

## Syntax

```php
ArrayUtils::mapToArray(iterable $iterables) : array
```

### Parameter

* `$iterable`

  > An iterable containing an iterable. It converted to an array.

### Return value

* A new array containing elements converted to an array.

## Polymorphism

{% hint style="warning" %}
This method not have polymorphic element
{% endhint %}

## References

{% embed url="https://www.php.net/manual/en/language.types.iterable" %}



