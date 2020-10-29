---
description: The some() method tests whether least one element pass the function
---

# ArrayUtils-&gt;some\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 30));

//Test if any elements is same to 20
$arrayUtils->some(function($num){ return $num === 20; });
// expected output: true

//Test if any elements is same to 40
$arrayUtils->some(function($num){ return $num === 40; });
// expected output: false
```
{% endcode %}

## Syntax

```php
$arrayUtils->some(callable $callback) : bool;
```

### Parameter

* `$callback`

  > A function to test for each element, taking three arguments:
  >
  > * `$value` The current element being processed in the array.
  > * `$key` The index of the current element being processed in the array.
  > * `$array`   The array `every` was called upon.

### Return value

* A `boolean` the whether any elements pass the function

## Polymorphism

```php
ArrayUtils::someFrom(iterable $from, callable $callback) : bool;
```

## References

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/some" %}



