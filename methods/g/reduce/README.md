---
description: >-
  The reduce() method iteratively reduce the array to a single value using a
  callback function
---

# reduce\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 10));

//This is like a 10 factorial
$arrayUtils->reduce(function($accumulator, $value){ return $accumulator * $value; }, 1);
// expected output: 3628800



$arrayUtils->reduce(
    function($accumulator, $value){
        echo  "$accumulator * $value = " . ($accumulator * $value) . PHP_EOL;
        return $accumulator * $value; }, 1));
//echo 1 * 1 = 1
//echo 1 * 2 = 2
//echo 2 * 3 = 6
//echo 6 * 4 = 24
//echo 24 * 5 = 120
//echo 120 * 6 = 720
//echo 720 * 7 = 5040
//echo 5040 * 8 = 40320
//echo 40320 * 9 = 362880
//echo 362880 * 10 = 3628800
//expected output: 3628800
```
{% endcode %}

## Syntax

```php
$arrayUtils->reduce(callable $callback, mixed $initialValue = null) : mixed;
```

### Parameter

* `$callback`

  > A function that produces an element of the new Array, taking four arguments:
  >
  > * `$accumulator`The accumulator accumulates callback's return values. It is the accumulated value previously returned in the last invocation of the callback—or `$initialValue`, if it was supplied \(see below\).
  > * `$value` The current element being processed in the array.
  > * `$key` The index of the current element being processed in the array.
  > * `$array`   The array `every` was called upon.

* `$initialValue` ![](../../../.gitbook/assets/badge_optional.svg) 
  * A value to use as the first argument to the first call of the callback.

### Return value

* The result value.

## Prefixing

```php
ArrayUtils::reduceFrom(iterable $from, callable $callback, mixed $initialValue = null) : mixed;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-reduce.php" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/Reduce" %}



