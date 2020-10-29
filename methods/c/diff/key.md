---
description: 'The diffAssoc() method all similar to diff(), but this applies to keys'
---

# diffKey\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first" => 1, "second" => 2, "third" => 3]);

//General array comparison
$arrayUtils->diffKey(["first" => 404, "second" => 404]);
// expected output: ["third" => 3]
```
{% endcode %}

## Syntax

```php
$arrayUtils->diffKey(iterable ...$iterables) : ArrayUtils;
```

### Parameter

* `$iterables`

  > Arrays to compare.

### Return value

* A array containing all the entries that are not present in any of the other arrays. \(Keys are preserved\)

### 

## Prefixing

```php
$arrayUtils->diffKeyAs(iterable ...$iterables) : array;
```

```php
ArrayUtils::diffKeyFrom(iterable $from, iterable ...$iterables) : ArrayUtils;
```

```php
ArrayUtils::diffKeyFromAs(iterable $from, iterable ...$iterables) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-diff-key" %}

{% page-ref page="./" %}



