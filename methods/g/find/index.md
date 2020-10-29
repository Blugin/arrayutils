---
description: 'The findIndex() method all similar to find(), but return index'
---

# findIndex\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot", "Bacon"]);

//Find value's index ​​starting with B
$arrayUtils->findIndex(function($name){ return $name[0] === "B"; });
// expected output: 1
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

### Return value

* The **key** of the **first element** in the array that pass function. Otherwise, `NULL` is returned.

## Prefixing

```php
ArrayUtils::findFrom(iterable $from, callable $callback) : mixed;
```

## References

[https://www.php.net/manual/en/function.array-chunk](https://www.php.net/manual/en/function.array-chunk)

