---
description: >-
  The unshift() method all similar to push(), but this push elements onto the
  start of array
---

# unshift\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1,5));

//Unshift 0 and 10
$arrayUtils->unshift(0, 10);
// expected output: [0, 10, 1, 2, 3, 4, 5]
```
{% endcode %}

## Syntax

```php
$arrayUtils->unshift(mixed ...$values) : ArrayUtils;
```

### Parameter

* `$values`

  > A values to unshift into array

### 

### Return value

* oneself back for method chaining.

## Prefixing

```php
$arrayUtils->unshiftAs(mixed ...$values) : array;
```

```php
ArrayUtils::unshiftFrom(iterable $from, mixed ...$values) : ArrayUtils;
```

```php
ArrayUtils::unshiftFromAs(iterable $from, mixed ...$values) : array;
```

## References

{% page-ref page="push.md" %}

{% embed url="https://www.php.net/manual/en/function.array-unshift.php" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/unshift" %}





