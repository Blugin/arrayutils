---
description: >-
  The combine() method returns new array by using one array for keys and another
  for values
---

# ArrayUtils-&gt;combine\(\)

{% code title="Example.php" %}
```php
<?php
use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first", "second", "third"]);

//General usage
$arrayUtils->combine([1, 2, 3]);
//["first" => 1, "second" => 2, "third" => 3]

//Combine itself
$arrayUtils->combine();
//["first" => "first", "second" => "second", "third" => "third"]
```
{% endcode %}

## Syntax

```php
$arrayUtils->combine(iterable|null $valueArray = null) : ArrayUtils;
```

### Parameter

* `$valueArray` ![](../.gitbook/assets/badge_optional.svg) 

  > An array of elements to use as values.  
  > Default is `NULL`. If is null, Use itself.

### Return value

*  A combined array.

{% hint style="danger" %}
If the number of elements for each array isn't equal, It will be throw error
{% endhint %}

## Polymorphism

```php
$arrayUtils->combineAs(iterable|null $valueArray = null) : array;
```

```php
ArrayUtils::combineFrom(iterable $from, iterable|null $valueArray = null) : ArrayUtils;
```

```php
ArrayUtils::combineFromAs(iterable $from, iterable|null $valueArray = null) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-combine" %}



