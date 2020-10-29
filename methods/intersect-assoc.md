---
description: >-
  The intersectAssoc() method all similar to intersect(), but this applies with
  additional index check
---

# ArrayUtils-&gt;intersectAssoc\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first" => 1, "second" => 2, "third" => 3]);

//General array comparison
$arrayUtils->intersectAssoc(["first" => 404, "second" => 2]);
// expected output: ["second" => 2]
```
{% endcode %}

## Syntax

```php
$arrayUtils->intersectAssoc(iterable ...$iterables) : ArrayUtils;
```

### Parameter

* `$iterables`

  > Arrays to compare.

### Return value

* A array containing all of the values that intersects with another array.

## Polymorphism

```php
$arrayUtils->intersectAssocAs(iterable ...$iterables) : array;
```

```php
ArrayUtils::intersectAssocFrom(iterable $from, iterable ...$iterables) : ArrayUtils;
```

```php
ArrayUtils::intersectAssocFromAs(iterable $from, iterable ...$iterables) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-intersect-key" %}



