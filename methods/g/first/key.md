---
description: The keyFirst() method returns first key
---

# keyFirst\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple" => 0, "Banana" => 1, "Carrot" => 2]);

//Gets first key
$arrayUtils->keyFirst();
// expected output: "Apple"
```
{% endcode %}

## Syntax

```php
$arrayUtils->keyFirst() : int|string|null;
```

### Return value

* A first key of array. If array is empty, returns `NULL`.

## Prefixing

```php
ArrayUtils::keyFirstFrom(iterable $from) : int|string|null;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-key-first" %}



