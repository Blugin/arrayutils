---
description: 'The mapKey() method all similar to map(), but this applies to keys'
---

# ArrayUtils-&gt;mapKey\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1,5));

//Squared all elements
$arrayUtils->mapKey(function($num){ return "$num * $num"; });
// expected output: [
//  "1 * 1"   => 1,
//  "2 * 2"   => 2,
//  "3 * 3"   => 3,
//  "4 * 4"   => 4,
//  "5 * 5"   => 5
//]
```
{% endcode %}

## Syntax

```php
$arrayUtils->mapKey(callable $callback) : ArrayUtils;
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
$arrayUtils->mapKeyAs(callable $callback) : array;
```

```php
ArrayUtils::mapKeyFrom(iterable $from, callable $callback) : ArrayUtils;
```

```php
ArrayUtils::mapKeyFromAs(iterable $from, callable $callback) : array;
```

## References

{% page-ref page="map.md" %}



