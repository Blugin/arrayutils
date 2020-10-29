---
description: >-
  The fill() method changes all values to a static value, from a start index to
  an end index
---

# fill\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 10));

//Full fill with 0
$arrayUtils->fill(0);
// expected output: [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]

//Fill with 0 from position 2 until position 4
$arrayUtils->fill(0, 2, 4);
// expected output: [1, 2, 0, 0, 5, 6, 7, 8, 9, 10]

//Fill with 0 from position 4 until end
$arrayUtils->fill(0, 4);
// expected output: [1, 2, 3, 4, 0, 0, 0, 0, 0, 0]
```
{% endcode %}

## Syntax

```php
$arrayUtils->fill(mixed $value, int $start = 0, int $end = null) : ArrayUtils;
```

### Parameter

* `$value` 

  > Value to fill the array with.

* `$start`![](../../../.gitbook/assets/badge_optional.svg) 

  > Start index, default `0`.

* `$end` ![](../../../.gitbook/assets/badge_optional.svg) 

  > End index, default `count($array)`.

### Return value

* A filled array.

## Prefixing

```php
$arrayUtils->fillAs(mixed $value, int $start = 0, int $end = null) : array;
```

```php
ArrayUtils::fillFrom(iterable $from, mixed $value, int $start = 0, int $end = null) : ArrayUtils;
```

```php
ArrayUtils::fillFromAs(iterable $from, mixed $value, int $start = 0, int $end = null) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-fill-keys" %}



