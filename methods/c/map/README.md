---
description: The map() method applies the callback to the elements
---

# map\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1,10));

//Squared all elements
$arrayUtils->map(function($num){ return $num * $num; });
// expected output: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
{% endcode %}

## Syntax

```php
$arrayUtils->map(callable $callback) : ArrayUtils;
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

## Prefixing

```php
$arrayUtils->mapAs(callable $callback) : array;
```

```php
ArrayUtils::mapFrom(iterable $from, callable $callback) : ArrayUtils;
```

```php
ArrayUtils::mapFromAs(iterable $from, callable $callback) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-map" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/map" %}



