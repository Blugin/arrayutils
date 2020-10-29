---
description: The every() method tests whether all elements pass the function
---

# ArrayUtils-&gt;every\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 30));

//Test if all elements are less than 40
$arrayUtils->every(function($num){ return $num < 40; });
// expected output: true

//Test if all elements are less than 30
$arrayUtils->every(function($num){ return $num < 40; });
// expected output: false
```
{% endcode %}

## Syntax

```php
$arrayUtils->every(callable $callback) : bool;
```

### Parameter

* `$callback`

  > A function to test for each element, taking three arguments:
  >
  > * `$value` The current element being processed in the array.
  > * `$key` The index of the current element being processed in the array.
  > * `$array`   The array `every` was called upon.

### Return value

* A `boolean` the whether all elements pass the function

## Polymorphism

```php
ArrayUtils::everyFrom(iterable $from, callable $callback) : bool;
```

## References

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/every" %}



