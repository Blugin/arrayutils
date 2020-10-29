---
description: The last() method returns last value
---

# ArrayUtils-&gt;last\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot"]);

//Gets last value
$arrayUtils->last();
// expected output: "Carrot"
```
{% endcode %}

## Syntax

```php
$arrayUtils->last() : mixed;
```

### Return value

* A last value of array. If array is empty, returns `NULL`.

## Polymorphism

```php
ArrayUtils::lastFrom(iterable $from) : mixed;
```

