---
description: >-
  The of() static method creates a new, ArrayUtils instance from variadic
  function arguments
---

# ArrayUtils::of\(\)

{% code title="Example.php" %}
```php
<?php
use kim\present\utils\arrays\ArrayUtils;

ArrayUtils::of(3,6,9);
//ArrayUtils(array(3, 6, 9))
```
{% endcode %}

## Syntax

```php
ArrayUtils::of(mixed ...$elements) : ArrayUtils
```

### Parameter

* `...$elements` 
  * Elements used to create the array.

### Return value

* A new `ArrayUtils` instance.

## Polymorphism

{% hint style="warning" %}
This method not have polymorphic element
{% endhint %}

## References

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/of" caption="" %}

