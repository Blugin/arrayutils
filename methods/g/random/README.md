---
description: The random() method returns random value
---

# random\(\)

{% code title="Example.php" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$arrayUtils = ArrayUtils::from(["Apple", "Banana", "Carrot"]);

//Gets random value
$arrayUtils->random();
// output is random, so always different
```
{% endcode %}

## Syntax

```php
$arrayUtils->random() : mixed;
```

### Return value

* A random value from array. If array is empty, returns `NULL`.

## Prefixing

```php
ArrayUtils::randomFrom(iterable $from) : mixed;
```

