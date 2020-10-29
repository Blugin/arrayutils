---
description: The replace() method replaces elements from passed arrays into the first array
---

# ArrayUtils-&gt;replace\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["orange", "banana", "apple", "raspberry", "kiwi"]);


$arrayUtils->replace([0 => "pineapple", 4 => "cherry"]);
// expected output: ["pineapple", "banana", "apple", "raspberry", "cherry"]
```
{% endcode %}

## Syntax

```php
$arrayUtils->replace(iterable ...$iterables) : ArrayUtils;
```

### Parameter

* `$iterables`

  > Arrays to replace.

### 

### Return value

* A replaced array.

## Polymorphism

```php
$arrayUtils->replaceAs(iterable ...$iterables) : array;
```

```php
ArrayUtils::replaceFrom(iterable $from, iterable ...$iterables) : ArrayUtils;
```

```php
ArrayUtils::replaceFromAs(iterable $from, iterable ...$iterables) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-replace.php" %}



