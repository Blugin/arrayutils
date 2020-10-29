---
description: >-
  The sort() method sort an array by values using a function or default sort
  function
---

# sort\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["orange", "banana", "apple", "raspberry", "kiwi"]);


$arrayUtils->sort();
// expected output: ["apple", "banana", "kiwi", "orange", "raspberry"]

$arrayUtils->sort(function($a, $b){ return strcmp($a, $b) * -1; })
// expected output: ["raspberry", "orange", "kiwi", "banana", "apple"]
```
{% endcode %}

## Syntax

```php
$arrayUtils->sort(?callable $callback = null) : ArrayUtils;
```

### Parameter

* `$callback` ![](../../../.gitbook/assets/badge_optional.svg) 

  > A function to compare element for sort, taking two arguments:
  >
  > * `$a` The comparison target A
  > * `$b` The comparison target B
  >
  > Default is `NULL`, If is null, Sort by default sort function.

### Return value

* A sorted array.

## Prefixing

```php
$arrayUtils->sortAs(?callable $callback = null) : array;
```

```php
ArrayUtils::sortFrom(iterable $from, ?callable $callback = null) : ArrayUtils;
```

```php
ArrayUtils::sortFromAs(iterable $from, ?callable $callback = null) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.sort.php" %}

{% embed url="https://www.php.net/manual/en/function.usort.php" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/sort" %}



