---
description: The countValues() method counts all the values of an array
---

# countValues\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["a", "a", "a", "b", "c", "c", "d"]);

//General usage
$arrayUtils->countValues();
// expected output: ["a" => 3, "b" => 1, "c" => 2, "d" => 1]
```
{% endcode %}

## Syntax

```php
$arrayUtils->countValues() : ArrayUtils;
```

### Return value

* A associative array of values from array as keys and their count as value.

## Polymorphism

```php
$arrayUtils->countValuesAs() : array;
```

```php
ArrayUtils::countValuesFrom(iterable $from) : ArrayUtils;
```

```php
ArrayUtils::countValuesFromAs(iterable $from) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-count-values" %}



