---
description: >-
  The concatSoft() method all similar to concat(), but not overwrite existing
  keys
---

# ArrayUtils-&gt;concatSoft\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["first" => 1, "second" => 2, "third" => 3]);

//Same key values are ignored
$arrayUtils->concat(["first" => 0, "4th" => 4]);
// expected output: ["first" => 1, "second" => 2, "third" => 3, "4th" => 4]

//Non-array values ​​can also be combined
$arrayUtils->concat(4, 5, 6);
// expected output: ["first" => 1, "second" => 2, "third" => 3, 4, 5, 6]
```
{% endcode %}

## Syntax

```php
$arrayUtils->concatSoft(mixed ...$values) : ArrayUtils;
```

### Parameter

* `$values`

  > A new array or value to merge with the existing array.  
  > If is not array \(Immutable into an array\), It will be wrapped in array.

  **Return value**

  * A merged array. The same key values ​​are ignored.

## Polymorphism

```php
$arrayUtils->concatSoftAs(mixed ...$values) : array;
```

```php
ArrayUtils::concatSoftFrom(mixed ...$values) : ArrayUtils;
```

```php
ArrayUtils::chunkFromAsconcatSoftFromAs(mixed ...$values) : array;
```

## References

{% page-ref page="concat.md" %}

