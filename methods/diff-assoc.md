---
description: >-
  The diffAssoc() method all similar to @see __diff(), but this applies with
  additional index check
---

# ArrayUtils-&gt;diffAssoc\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first" => 1, "second" => 2, "third" => 3]);

//General array comparison
$arrayUtils->diffAssoc(["first" => 404, "second" => 2]);
//["first" => 1, "third" => 3]
```
{% endcode %}

## Syntax

```php
$arrayUtils->diffAssoc(iterable ...$iterables) : ArrayUtils;
```

### Parameter

* `$iterables`

  > Arrays to compare.

### Return value

* A array containing all the entries that are not present in any of the other arrays. \(Keys are preserved\)

## Polymorphism

```php
$arrayUtils->diffAssocAs(iterable ...$iterables) : array;
```

```php
ArrayUtils::diffAssocFrom(iterable $from, iterable ...$iterables) : ArrayUtils;
```

```php
ArrayUtils::diffAssocFromAs(iterable $from, iterable ...$iterables) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-diff-assoc" %}

{% page-ref page="diff.md" %}



