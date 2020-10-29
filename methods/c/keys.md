---
description: The keys() method return all the keys of an array
---

# keys\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first" => 1, "second" => 2, "third" => 3]);

//Get all keys
$arrayUtils->keys();
// expected output: ["first", "second", "third"]
```
{% endcode %}

## Syntax

```php
$arrayUtils->keys() : ArrayUtils;
```

### Return value

*  A array of all the keys in `array`.

## Prefixing

```php
$arrayUtils->keysAs() : array;
```

```php
ArrayUtils::keysFrom(iterable $from) : ArrayUtils;
```

```php
ArrayUtils::keysFrom(iterable $from) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-keys" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/keys" %}



