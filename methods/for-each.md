---
description: The forEach() method executes a provided function once for each array element.
---

# ArrayUtils-&gt;forEach\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 10));

//Filtering values ​​between 3 and 6
$arrayUtils->forEach(function($num){ echo $num . "~"; });
// expected output: 1~2~3~4~5~6~7~8~9~10~
```
{% endcode %}

## Syntax

```php
$arrayUtils->forEach(callable $callback) : ArrayUtils;
```

### Parameter

* `$callback`

  > A function to execute on each element, taking three arguments:
  >
  > * `$value` The current element being processed in the array.
  > * `$key` The index of the current element being processed in the array.
  > * `$array`   The array `every` was called upon.

### Return value

* oneself back for method chaining.

## Polymorphism

```php
$arrayUtils->forEachAs(callable $callback) : array;
```

```php
ArrayUtils::forEachFrom(iterable $from, callable $callback) : ArrayUtils;
```

```php
ArrayUtils::forEachFromAs(iterable $from, callable $callback) : array;
```

## References

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/forEach" %}



