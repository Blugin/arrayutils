---
description: The pad() method split an array into chunks
---

# ArrayUtils-&gt;pad\(\)

{% code title="Example.php" %}
```php
<?php
use kim\present\utils\arrays\ArrayUtils;

ArrayUtils::from(range(1, 20))->chunk(4);
//[
//  [ 1,  2,  3,  4],
//  [ 5,  6,  7,  8],
//  [ 9, 10, 11, 12],
//  [13, 14, 15, 16],
//  [17, 18, 19, 20]
//]

ArrayUtils::from(range(1, 20))->chunk(4, true);
//[
//  [ 0 =>  1,  1 =>  2,  2 =>  3,  3 =>  4],
//  [ 4 =>  5,  5 =>  6,  6 =>  7,  7 =>  8],
//  [ 8 =>  9,  9 => 10, 10 => 11, 11 => 12],
//  [12 => 13, 13 => 14, 14 => 15, 15 => 16],
//  [16 => 17, 17 => 18, 18 => 19, 19 => 20]
//]
```
{% endcode %}

## Syntax

```php
$arrayUtils->pad(int $size, mixed $value) : ArrayUtils;
```

### Parameter

* `$size`
  * The size of each chunk
* `$preserveKeys`  
  * When set to **`TRUE`** keys will be preserved. Default is **`FALSE`** which will reindex the chunk numerically

### Return value

* Returns a multidimensional numerically indexed array, starting with zero, with each dimension containing `size` elements.

## Polymorphism

```php
$arrayUtils->padAs(int $size, mixed $value) : array;
```

```php
ArrayUtils::padFrom(iterable $from, int $size, mixed $value) : ArrayUtils;
```

```php
ArrayUtils::padFromAs(iterable $from, int $size, mixed $value) : array;
```

## References

[https://www.php.net/manual/en/function.array-chunk](https://www.php.net/manual/en/function.array-chunk)

