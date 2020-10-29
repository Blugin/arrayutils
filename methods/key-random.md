---
description: The keyRandom() method returns random key
---

# ArrayUtils-&gt;keyRandom\(\)

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

### Parameter

* `$size`
  * The size of each chunk
* `$preserveKeys` ![](../.gitbook/assets/badge_optional.svg) 
  * When set to **`TRUE`** keys will be preserved. Default is **`FALSE`** which will reindex the chunk numerically

### Return value

* Returns a multidimensional numerically indexed array, starting with zero, with each dimension containing `size` elements.

## Polymorphism

```php
ArrayUtils::keyRandomFrom(iterable $from) : int|string|null;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-rand" %}



