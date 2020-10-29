---
description: The first() method returns first value
---

# first\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot"]);

//Gets first value
$arrayUtils->first();
// expected output: "Apple"
```
{% endcode %}

## Syntax

```php
$arrayUtils->first() : mixed;
```

### Return value

* A first value of array. If array is empty, returns `NULL`.

## Prefixing

```php
ArrayUtils::firstFrom(iterable $from) : mixed;
```

