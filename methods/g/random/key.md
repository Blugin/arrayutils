---
description: The keyRandom() method returns random key
---

# keyRandom\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple" => 0, "Banana" => 1, "Carrot" => 2]);

//Gets random key
$arrayUtils->keyRandom();
// output is random, so always different
```
{% endcode %}

## Syntax

```php
$arrayUtils->keyRandom() : int|string|null;
```

### Return value

* A random key from array. If array is empty, returns `NULL`.

## Prefixing

```php
ArrayUtils::keyRandomFrom(iterable $from) : int|string|null;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-rand" %}



