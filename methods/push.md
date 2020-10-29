---
description: The push() method push elements onto the end of array
---

# ArrayUtils-&gt;push\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1,5));

//Push 0 and 10
$arrayUtils->push(0, 10);
// expected output: [1, 2, 3, 4, 5, 0, 10]
```
{% endcode %}

## Syntax

```php
$arrayUtils->push(mixed ...$values) : ArrayUtils;
```

### Parameter

* `$values`

  > A values to push into array

### Return value

* oneself back for method chaining.

## Polymorphism

```php
$arrayUtils->pushAs(mixed ...$values) : array;
```

```php
ArrayUtils::pushFrom(iterable $from, mixed ...$values) : ArrayUtils;
```

```php
ArrayUtils::pushFromAs(iterable $from, mixed ...$values) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-push.php" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/push" %}



