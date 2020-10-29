---
description: The unique() method removes duplicate values
---

# ArrayUtils-&gt;unique\(\)

{% code title="Example.php" %}
```php
<?php
use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["a", "a", "a", "b", "c", "c", "d"]);

$arrayUtils->unique();
// expected output: ["a", "b", "c", "d"]
```
{% endcode %}

## Syntax

```php
$arrayUtils->unique(int $sort_flags = SORT_STRING) : ArrayUtils;
```

### Parameter

* `$sortFlags` ![](../.gitbook/assets/badge_optional.svg) 

  > Used to modify the sorting behavior using these values:
  >
  >
  >
  > Sorting type flags:
  >
  > * **`SORT_REGULAR`** - compare items normally \(don't change types\)
  > * **`SORT_NUMERIC`** - compare items numerically
  > * **`SORT_STRING`** - compare items as strings
  > * **`SORT_LOCALE_STRING`** - compare items as strings, based on the current locale.

### Return value

* A filtered array.

## Polymorphism

```php
$arrayUtils->uniqueAs(int $sort_flags = SORT_STRING) : array;
```

```php
ArrayUtils::uniqueFrom(iterable $from, int $sort_flags = SORT_STRING) : ArrayUtils;
```

```php
ArrayUtils::uniqueFromAs(iterable $from, int $sort_flags = SORT_STRING) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-chunk" %}



