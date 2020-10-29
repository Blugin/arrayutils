---
description: >-
  The reduceRight() method all similar to reduce(), but It works in reverse
  order.
---

# reduceRight\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 10));

//This is like a 10 factorial
$arrayUtils->reduceRight(function($accumulator, $value){ return $accumulator * $value; }, 1);
// expected output: 3628800



$arrayUtils->reduceRight(
    function($accumulator, $value){
        echo  "$accumulator * $value = " . ($accumulator * $value) . PHP_EOL;
        return $accumulator * $value; }, 1));
//echo 1 * 10 = 10
//echo 10 * 9 = 90
//echo 90 * 8 = 720
//echo 720 * 7 = 5040
//echo 5040 * 6 = 30240
//echo 30240 * 5 = 151200
//echo 151200 * 4 = 604800
//echo 604800 * 3 = 1814400
//echo 1814400 * 2 = 3628800
//echo 3628800 * 1 = 3628800
//expected output: 3628800
```
{% endcode %}

## Syntax

```php
$arrayUtils->reduceRight(callable $callback, mixed $initialValue = null) : mixed;
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
ArrayUtils::reduceRightFrom(iterable $from, callable $callback, mixed $initialValue = null) : mixed;
```

## References

{% page-ref page="./" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/ReduceRight" %}



