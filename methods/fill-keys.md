---
description: >-
  The fillKeys() method fills an array with the static value, using the values
  of the array as keys.
---

# ArrayUtils-&gt;fillKeys\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first", "second", "third"]);

//Fill keys with 0
$arrayUtils->fillKeys(0);
// expected output: ["first" => 0, "second" => 0, "third" => 0]
```
{% endcode %}

## Syntax

```php
$arrayUtils->fillKeys(mixed $value) : ArrayUtils;
```

### Parameter

* `$value` 

  > Value to fill the array with.

### Return value

* A filled array.

## Polymorphism

```php
$arrayUtils->fillKeysAs(mixed $value) : array;
```

```php
ArrayUtils::fillKeysFrom(iterable $from, mixed $value) : ArrayUtils;
```

```php
ArrayUtils::fillKeysFromAs(iterable $from, mixed $value) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-fill-keys" %}



