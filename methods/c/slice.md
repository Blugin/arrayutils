---
description: The slice() method returns an array with selected from start to end
---

# slice\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 10));

$arrayUtils->slice(2);    // expected output: [3, 4, 5, 6, 7, 8, 9, 10]
$arrayUtils->slice(2, 4); // expected output: [3, 4]
$arrayUtils->slice(-4);   // expected output: [7, 8, 9, 10]
```
{% endcode %}

## Syntax

```php
$arrayUtils->slice(int $start = 0, int $end = null, bool $preserve_keys = false) : ArrayUtils;
```

### Parameter

* `$start` ![](../../.gitbook/assets/badge_optional.svg) 

  > Zero-based index at which to start extraction.
  >
  > Default is `0`.

* `$end` ![](../../.gitbook/assets/badge_optional.svg) 

  > Zero-based index at which to start extraction.
  >
  > Default is `count($array)`.

* `$preserveKeys` ![](../../.gitbook/assets/badge_optional.svg) 
  * When set to **`TRUE`** keys will be preserved.  Default is **`FALSE`** which will re-index the chunk numerically

### Return value

* A sliced array.

## Prefixing

```php
$arrayUtils->sliceAs(int $start = 0, int $end = null, bool $preserve_keys = false) : array;
```

```php
ArrayUtils::sliceFrom(iterable $from, int $start = 0, int $end = null, bool $preserve_keys = false) : ArrayUtils;
```

```php
ArrayUtils::sliceFromAs(iterable $from, int $start = 0, int $end = null, bool $preserve_keys = false) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-slice.php" %}

{% embed url="https://www.php.net/manual/en/function.array-chunk" %}



