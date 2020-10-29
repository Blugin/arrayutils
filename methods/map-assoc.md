---
description: >-
  The mapAssoc() method all similar to map(), but this applies with additional
  index check
---

# ArrayUtils-&gt;mapAssoc\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1,5));

//Squared all elements
$arrayUtils->mapAssoc(function($num){ return ["$num * $num", $num * $num]; });
// expected output: [
//  "1 * 1"   => 1,
//  "2 * 2"   => 4,
//  "3 * 3"   => 9,
//  "4 * 4"   => 16,
//  "5 * 5"   => 25
//]
```
{% endcode %}

## Syntax

```php
$arrayUtils->mapAssoc(callable $callback) : ArrayUtils;
```

### Parameter

* `$callback`

  > A function that produces an element of the new Array, taking three arguments:
  >
  > * `$value` The current element being processed in the array.
  > * `$key` The index of the current element being processed in the array.
  > * `$array`   The array `every` was called upon.

### 

### Return value

* A new array with each element being the result of the callback function.

## Polymorphism

```php
$arrayUtils->mapAssocAs(callable $callback) : array;
```

```php
ArrayUtils::mapAssocFrom(iterable $from, callable $callback) : ArrayUtils;
```

```php
ArrayUtils::mapAssocFromAs(iterable $from, callable $callback) : array;
```

## References

{% page-ref page="map.md" %}



