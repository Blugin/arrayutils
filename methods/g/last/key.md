---
description: The keyLast() method returns last key
---

# keyLast\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple" => 0, "Banana" => 1, "Carrot" => 2]);

//Gets last key
$arrayUtils->keyLast();
// expected output: "Carrot"
```
{% endcode %}

## Syntax

```php
$arrayUtils->keyLast() : int|string|null;
```

### Return value

* A last key of array. If array is empty, returns `NULL`.

## Prefixing

```php
ArrayUtils::keyLastFrom(iterable $from) : int|string|null;
```

## References

[https://www.php.net/manual/en/function.array-key-last](https://www.php.net/manual/en/function.array-key-last.php)

