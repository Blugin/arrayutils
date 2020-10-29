---
description: >-
  The sort() method sort an array by keys using a function or default sort
  function
---

# ArrayUtils-&gt;sortKey\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from([
    "orange" => 1, 
    "banana" => 2, 
    "apple" => 3,
    "raspberry" => 4, 
    "kiwi" => 5]);


$arrayUtils->sortKey();
// expected output: [
//  "apple" => 3,
//  "banana" => 2, 
//  "kiwi" => 5,
//  "orange" => 1, 
//  "raspberry" => 4
//]

$arrayUtils->sortKey(function($a, $b){ return strcmp($a, $b) * -1; })
// expected output: [
//  "raspberry" => 4,
//  "orange" => 1, 
//  "kiwi" => 5,
//  "banana" => 2, 
//  "apple" => 3
//]
```
{% endcode %}

## Syntax

```php
$arrayUtils->sortKey(?callable $callback = null) : ArrayUtils;
```

### Parameter

* `$callback` ![](../.gitbook/assets/badge_optional.svg) 

  > A function to compare element for sort, taking two arguments:
  >
  > * `$a` The comparison target A
  > * `$b` The comparison target B
  >
  > Default is `NULL`, If is null, Sort by default sort function.

### Return value

* A sorted array.

## Polymorphism

```php
$arrayUtils->sortKeyAs(?callable $callback = null) : array;
```

```php
ArrayUtils::sortKeyFrom(iterable $from, ?callable $callback = null) : ArrayUtils;
```

```php
ArrayUtils::sortKeyFromAs(iterable $from, ?callable $callback = null) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.ksort.php" %}

{% embed url="https://www.php.net/manual/en/function.uksort.php" %}

