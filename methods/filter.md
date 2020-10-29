---
description: >-
  The filter() method creates a new array with all elements that pass the
  function.
---

# ArrayUtils-&gt;filter\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 10));

//Filtering values ​​between 3 and 6
$arrayUtils->filter(function($num){ return $num < 3 || $num > 6; });
// expected output: [1, 2, 7, 8, 9, 10]
```
{% endcode %}

## Syntax

```php
$arrayUtils->filter(callable $callback) : ArrayUtils;
```

### Parameter

* `$callback`

  > A function to test each element of the array.  
  > Return a value that coerces to `TRUE` to keep the element, or to `FALSE` otherwise.  
  > Function taking three arguments:
  >
  > * `$value` The current element being processed in the array.
  > * `$key` The index of the current element being processed in the array.
  > * `$array`   The array `every` was called upon.

### Return value

* A filtered array.

## Polymorphism

```php
$arrayUtils->filterAs(callable $callback) : array;
```

```php
ArrayUtils::filterFrom(iterable $from, callable $callback) : ArrayUtils;
```

```php
ArrayUtils::filterFromAs(iterable $from, callable $callback) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-filter.php" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/filter" %}



