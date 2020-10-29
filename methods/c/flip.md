---
description: The flip() method exchanges all keys with their values in an array
---

# flip\(\)

{% code title="Example.php" %}
```php
<?php
use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["a", "b", "c", "d"]);

//General usage
$arrayUtils->flip();
// expected output: ["a" => 0, "b" => 1, "c" => 2, "d" => 3]
```
{% endcode %}

## Syntax

```php
$arrayUtils->flip() : ArrayUtils;
```

### Return value

* A flipped array on success and **`NULL`** on failure.

## Prefixing

```php
$arrayUtils->flipAs() : array;
```

```php
ArrayUtils::flipFrom(iterable $from) : ArrayUtils;
```

```php
ArrayUtils::flipFromAs(iterable $from) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-flip" %}



