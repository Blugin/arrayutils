---
description: >-
  The splice() method remove a portion of the array and replace it with
  something else
---

# splice\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(range(1, 10));

$arrayUtils->splice(2);
// expected output: [3, 4, 5, 6, 7, 8, 9, 10]
$arrayUtils;
// expected output: [1, 2]


//Reset
$arrayUtils = ArrayUtils::from(range(1, 10));

$arrayUtils->splice(2, 4, "Hi", "Bye", "Oh");
// expected output: [3, 4, 5, 6]
$arrayUtils->splice(-4);
// expected output: [1, 2, "Hi", "Bye", "Oh", 7, 8, 9]
```
{% endcode %}

## Syntax

```php
$arrayUtils->splice(int $offset, ?int $length = null, mixed ...$replacement) : ArrayUtils;
```

### Parameter

* `$offset`

  > The index at which to start changing the array.

* `$length`![](../../.gitbook/assets/badge_optional.svg) 

  > Length of array to be removed
  >
  > Default is `NULL`. If is null, It replaced to `count($array)-$offest`.

* `$replacement`![](../../.gitbook/assets/badge_optional.svg) 

  > Values to replace.  
  > If if empty, Removes elements in the selected range.

### Return value

* The array consisting of the extracted elements.

## Prefixing

```php
$arrayUtils->spliceAs(int $offset, ?int $length = null, mixed ...$replacement) : array;
```

```php
ArrayUtils::spliceFrom(iterable $from, int $offset, ?int $length = null, mixed ...$replacement) : ArrayUtils;
```

```php
ArrayUtils::spliceFromAs(iterable $from, int $offset, ?int $length = null, mixed ...$replacement) : array;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-splice.php" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/splice" %}



