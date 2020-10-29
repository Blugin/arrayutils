---
description: The pop() method removes the last element and returns that element
---

# ArrayUtils-&gt;pop\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot"]);

//Gets last value
$arrayUtils->pop();
// expected output: "Carrot"

$arrayUtils;
// expected output: ["Apple", "Banana"]
```
{% endcode %}

## Syntax

```php
$arrayUtils->pop() : mixed;
```

### Return value

* The last value of array.

## Polymorphism

```php
ArrayUtils::pop() : mixed;
```

## References

{% embed url="https://www.php.net/manual/en/function.array-pop.php" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global\_Objects/Array/pop" %}



