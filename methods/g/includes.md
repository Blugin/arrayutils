---
description: >-
  The includes() method tests whether an array includes a certain value among
  its entries
---

# includes\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot"]);

//Check array includes "Banana"
$arrayUtils->includes("Banana");
// expected output: true

//Check array includes "Banana" from 2
$arrayUtils->includes("Banana");
// expected output: false

//Check array includes "Baccon"
$arrayUtils->includes("Baccon");
// expected output: false
```
{% endcode %}

## Syntax

```php
$arrayUtils->includes(mixed $needle, int $start = 0) : bool;
```

### Parameter

* `$needle`
  * The value to search for.
* `$start` ![](../../.gitbook/assets/badge_optional.svg) 
  *  The position in this array at which to begin searching for `valueToFind`.
  *  Defaults to `0`.

### Return value

* A `boolean` the whether the element exists in the array

## Prefixing

```php
ArrayUtils::includesFrom(iterable $from, mixed $needle, int $start = 0) : bool;
```

## References

{% embed url="https://www.php.net/manual/en/function.in-array" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/includes" %}



