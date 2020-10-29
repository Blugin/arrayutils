---
description: The sum() method calculate the sum of values in an array
---

# ArrayUtils-&gt;sum\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 10));

$arrayUtils->sum();// expected output: 55
```
{% endcode %}

## Syntax

```php
$arrayUtils->sum() : int|float;
```

### Return value

*  The sum of values as an integer or float

## Polymorphism

```php
ArrayUtils::sumFrom(iterable $from) : int|float;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-sum.php" %}



