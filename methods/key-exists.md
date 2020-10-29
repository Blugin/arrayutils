---
description: The keyExists() method tests whether the requested index exists.
---

# ArrayUtils-&gt;keyExists\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot", "FAV" => "Becon"]);

//Check array has each indexs
$arrayUtils->keyExists(1);      // expected output: true
$arrayUtils->keyExists(2);      // expected output: true
$arrayUtils->keyExists(3);      // expected output: false
$arrayUtils->keyExists("HATE"); // expected output: false
$arrayUtils->keyExists("FAV");  // expected output: true
```
{% endcode %}

## Syntax

```php
$arrayUtils->keyExists(int|string $key) : bool;
```

### Parameter

* `$key`

  > The index being checked.

### Return value

* `Boolean` the whether the requested index exists

## Polymorphism

```php
ArrayUtils::keyExistsFrom(iterable $from, int|string $key) : bool;
```

## References

{% embed url="https://www.php.net/manual/en/function.isset" %}

{% embed url="https://www.php.net/manual/en/function.array-key-exists" %}



