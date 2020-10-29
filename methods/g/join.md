---
description: The join() method join array elements with a string
---

# join\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot"]);

//Joining array with multiple elements
$arrayUtils->join();         // "Apple,Banana,Carrot"
$arrayUtils->join(" and ");  // "Apple and Banana and Carrot"
$arrayUtils->join(" || ");   // "Apple || Banana || Carrot"

//Joining with prefix
$arrayUtils->join(" and ", "I like ");
// expected output: "I like  Apple and Banana and Carrot"

//Joining with prefix and suffix
$arrayUtils->join(" and ", "I like ", " little bit");
// expected output: "I like Apple and Banana and Carrot little bit"
```
{% endcode %}

## Syntax

```php
$arrayUtils->join(string $glue = ",", string $prefix = "", string $suffix = "") : string;
```

### Parameter

* `$glue` ![](../../.gitbook/assets/badge_optional.svg) 

  > The string to separate each pair of adjacent elements.  
  > Default: `","`

* `$prefix` ![](../../.gitbook/assets/badge_optional.svg) 

  > The prefix string.  
  > Default: `""`\(empty\)

* `$suffix`![](../../.gitbook/assets/badge_optional.svg) 

  > The suffix string.  
  > Default: `""`\(empty\)

### Return value

* A string with all array elements joined

## Prefixing

```php
ArrayUtils::joinFrom(iterable $from, string $glue = ",", string $prefix = "", string $suffix = "") : string;
```

## References

{% embed url="https://www.php.net/manual/en/function.implode" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/join" %}



