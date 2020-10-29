---
description: >-
  The indexOf() method get first index at which a given element can be found in
  the array
---

# indexOf\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot"]);

//Check array includes "Banana"
$arrayUtils->indexOf("Banana");
// expected output: 1

//Check array includes "Carrot" from 2
$arrayUtils->indexOf("Banana");
// expected output: null

//Check array includes "Baccon"
$arrayUtils->indexOf("Baccon");
// expected output: null
```
{% endcode %}

## Syntax

```php
$arrayUtils->indexOf(mixed $needle, int $start = 0) : int|string|null;
```

### Parameter

* `$needle`
  * The value to search for.
* `$start` ![](../../.gitbook/assets/badge_optional.svg) 

  *  The position in this array at which to begin searching for `valueToFind`.
  *  Defaults to `0`.

### Return value

* The  first index of the element in the array. If not founded, returns `NULL`.

## Prefixing

```php
ArrayUtils::indexOfFrom(iterable $from, mixed $needle, int $start = 0) : int|string|null;
```

## References

[https://www.php.net/manual/en/function.array-chunk](https://www.php.net/manual/en/function.array-chunk)

