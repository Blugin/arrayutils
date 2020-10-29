---
description: >-
  The diff() method compares with other arrays and returns the values that are
  not in any of the other arrays
---

# ArrayUtils-&gt;diff\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first", "second", "third"]);

//General array comparison
$arrayUtils->diff(["first", "4th"]);
//["second", "third"]
```
{% endcode %}

## Syntax

```php
$arrayUtils->diff(iterable ...$iterables) : ArrayUtils;
```

### Parameter

* `$iterables`

  > Arrays to compare.

### Return value

* A array containing all the entries that are not present in any of the other arrays. \(Keys are preserved\)

## Polymorphism

```php
$arrayUtils->diffAs(iterable ...$iterables) : array;
```

```php
ArrayUtils::diffFrom(iterable $from, iterable ...$iterables) : ArrayUtils;
```

```php
ArrayUtils::diffFromAs(iterable $from, iterable ...$iterables) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-diff" %}



