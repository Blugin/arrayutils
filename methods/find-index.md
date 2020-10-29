---
description: 'The findIndex() method all similar to find(), but return index'
---

# ArrayUtils-&gt;findIndex\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot", "Bacon"]);

//Find value's index ​​starting with B
$arrayUtils->findIndex(function($name){ return $name[0] === "B"; });
// expected output: 1
```
{% endcode %}

## Syntax

```php
$arrayUtils->find(callable $callback) : mixed;
```

### Parameter

* `$size`
  * The size of each chunk
* `$preserveKeys` ![](../.gitbook/assets/badge_optional.svg) 
  * When set to **`TRUE`** keys will be preserved. Default is **`FALSE`** which will reindex the chunk numerically

### Return value

* The **key** of the **first element** in the array that pass function. Otherwise, `NULL` is returned.

## Polymorphism

```php
ArrayUtils::findFrom(iterable $from, callable $callback) : mixed;
```

## References

[https://www.php.net/manual/en/function.array-chunk](https://www.php.net/manual/en/function.array-chunk)

