---
description: 'The intersectKey() method all similar to intersect(), but this applies to keys'
---

# ArrayUtils-&gt;intersectKey\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first" => 1, "second" => 2, "third" => 3]);

//General array comparison
$arrayUtils->intersectKey(["first" => 404, "second" => 2]);
// expected output: ["first" => 1, "second" => 2]
```
{% endcode %}

## Syntax

```php
$arrayUtils->intersectkey(iterable ...$iterables) : ArrayUtils;
```

### Parameter

* `$iterables`

  > Arrays to compare.

### Return value

* A array containing all of the values that intersects with another array.

## Polymorphism

```php
$arrayUtils->intersectkeyAs(iterable ...$iterables) : array;
```

```php
ArrayUtils::intersectkeyFrom(iterable $from, iterable ...$iterables) : ArrayUtils;
```

```php
ArrayUtils::intersectkeyFromAs(iterable $from, iterable ...$iterables) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-intersect-assoc" %}



