---
description: >-
  The flatMap() method create a new array formed by applying function and then
  flattening the result by one level
---

# flatMap\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from([-3, 2, -4, 5, 9]);

//Element duplication
$arrayUtils->flatMap(function($num){ return [$num, $num]; });
// expected output: [-3, -3, 2, 2, -4, -4, 5, 5, 9, 9]

//Remove negative and split the odd numbers into an even number and a 1
$arrayUtils->flatMap(function($num){
  if($num< 0)       return [];
  if($num % 2 == 0) return [$num];
  else              return [$num - 1, 1]; });
// expected output: [2, 4, 1, 8, 1]
```
{% endcode %}

## Syntax

```php
$arrayUtils->flatMap(callable $callback) : ArrayUtils;
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

* A new array with each element being the result of the callback function and flattened to a depth of 1.

## Prefixing

```php
$arrayUtils->flatMapAs(callable $callback) : array;
```

```php
ArrayUtils::flatMapFrom(iterable $from, callable $callback) : ArrayUtils;
```

```php
ArrayUtils::flatMapFromAs(iterable $from, callable $callback) : array;
```

## References

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/flatMap" %}



