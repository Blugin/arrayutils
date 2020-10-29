---
description: The reverse() method reverses an array
---

# reverse\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["orange", "banana", "apple", "raspberry", "kiwi"]);


$arrayUtils->reverse();
// expected output: ["kiwi", "raspberry", "apple", "banana", "orange"]
```
{% endcode %}

## Syntax

```php
$arrayUtils->reverse(bool $preserveKeys = false) : ArrayUtils;
```

### Parameter

* `$preserveKeys` ![](../../.gitbook/assets/badge_optional.svg) 
  * When set to **`TRUE`** keys will be preserved.  Default is **`FALSE`** which will re-index the chunk numerically

### Return value

* A reversed array.

## Prefixing

```php
$arrayUtils->reverseAs(bool $preserveKeys = false) : array;
```

```php
ArrayUtils::reverseFrom(iterable $from, bool $preserveKeys = false) : ArrayUtils;
```

```php
ArrayUtils::reverseFromAs(iterable $from, bool $preserveKeys = false) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-reverse.php" %}



