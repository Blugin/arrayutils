---
description: The concat() method merge one or more arrays
---

# concat\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first" => 1, "second" => 2, "third" => 3]);

//Same key values ​​are overwritten
$arrayUtils->concat(["first" => 0, "4th" => 4]);
// expected output: ["first" => 0, "second" => 2, "third" => 3, "4th" => 4]

//Non-array values ​​can also be combined
$arrayUtils->concat(4, 5, 6);
// expected output: ["first" => 1, "second" => 2, "third" => 3, 4, 5, 6]
```
{% endcode %}

## Syntax

```php
$arrayUtils->concat(mixed ...$values) : ArrayUtils;
```

### Parameter

* `$values`

  > A new array or value to merge with the existing array.  
  > If is not array \(Immutable into an array\), It will be wrapped in array.

### Return value

* A merged array. The same key values ​​are overwritten.

## Prefixing

```php
$arrayUtils->concatAs(mixed ...$values) : array;
```

```php
ArrayUtils::concatFrom(mixed ...$values) : ArrayUtils;
```

```php
ArrayUtils::concatFromAs(mixed ...$values) : array;
```

## References

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/concat" %}

{% embed url="https://www.php.net/manual/en/function.array-merge" %}



