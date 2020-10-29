---
description: The values() method return all the values of an array
---

# values\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first" => 1, "second" => 2, "third" => 3]);

//Get all values
$arrayUtils->values();
// expected output: [1, 2, 3]
```
{% endcode %}

## Syntax

```php
$arrayUtils->values() : ArrayUtils;
```

### Return value

*  A array of all the values in `array`.

## Prefixing

```php
$arrayUtils->valuesAs() : array;
```

```php
ArrayUtils::valuesFrom(iterable $from) : ArrayUtils;
```

```php
ArrayUtils::valuesFromAs(iterable $from) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-values.php" %}

