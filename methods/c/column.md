---
description: The column() method returns the values from a single column in the input array
---

# column\(\)

{% code title="Example.php" %}
```php
<?php
use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from([
    ["any" => "first",  1, 2, 3],
    ["any" => "second", 4, 5, 6],
    ["any" => "third",  7, 8, 9]
]);

// Use "any" value in internal array as value of array
$arrayUtils->column("any");
// expected output: ["first", "second", "third"]


// Use 2nd value in internal array as value,
// Use "any" in internal array as key of array
$arrayUtils->column(1, "any");
// expected output: ["first" => 2, "second" => 5, "third" => 8]


// Use value in internal array as value,
// Use "any" in internal array as key of array
$arrayUtils->column(null, "any");
// expected output: [
//   "first"  => ["any" => "first",  1, 2, 3],
//   "second" => ["any" => "second", 4, 5, 6],
//   "third"  => ["any" => "third",  7, 8, 9]
//]
```
{% endcode %}

## Syntax

```php
$arrayUtils->column(mixed $valueKey, mixed $indexKey = null) : ArrayUtils;
```

### Parameter

* `$valueKey`

  > The key value of the element to be used as the value.
  >
  > If is null, Use element to value.

* `$indexKey` ![](../../.gitbook/assets/badge_optional.svg) 

  > The key value of the element to be used as the key.  
  > Default is `NULL`. If is null, Re-index from 0.

### Return value

* A array of values representing a single column from the input array.

## Prefixing

```php
$arrayUtils->columnAs(mixed $valueKey, mixed $indexKey = null) : array;
```

```php
ArrayUtils::columnFrom(iterable $from, mixed $valueKey, mixed $indexKey = null) : ArrayUtils;
```

```php
ArrayUtils::(iterable $from, mixed $valueKey, mixed $indexKey = null) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-column" %}



