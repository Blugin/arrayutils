---
description: >-
  The intersect() method computes the intersection with other arrays and returns
  the values that intersects with another array.
---

# ArrayUtils-&gt;intersect\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first", "second", "third"]);

//General array comparison
$arrayUtils->intersect(["first", "third"]);
// expected output: ["first", "third"]
```
{% endcode %}

## Syntax

```php
$arrayUtils->intersect(iterable ...$iterables) : ArrayUtils;
```

### Parameter

* `$iterables`

  > Arrays to compare.

### Return value

* A array containing all of the values that intersects with another array.

## Polymorphism

```php
$arrayUtils->intersectAs(iterable ...$iterables) : array;
```

```php
ArrayUtils::intersectFrom(iterable $from, iterable ...$iterables) : ArrayUtils;
```

```php
ArrayUtils::intersectFromAs(iterable $from, iterable ...$iterables) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-intersect" %}



