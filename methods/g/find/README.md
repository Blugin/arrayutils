---
description: The find() method find the value of the first element that pass function.
---

# find\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot", "Bacon"]);

//Find values ​​starting with B
$arrayUtils->find(function($name){ return $name[0] === "B"; });
// expected output: "Banana"
```
{% endcode %}

## Syntax

```php
$arrayUtils->find(callable $callback) : mixed;
```

### Parameter

* `$callback`

  > A function to execute on each value in the array, taking 3 arguments:
  >
  > * `$value` The current element being processed in the array.
  > * `$key` The index of the current element being processed in the array.
  > * `$array`   The array `every` was called upon.

### 

### Return value

*  The **value** of the **first element** in the array that pass function. Otherwise, `NULL` is returned.

## Prefixing

```php
ArrayUtils::findFrom(iterable $from, callable $callback) : mixed;
```

## References

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/find" %}



