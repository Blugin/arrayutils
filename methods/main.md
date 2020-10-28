# Main

## \#⃣Method type

The method types are largely divided into two by return values

### ⚡Generic method

> The generic-method is returns an single result.
>
> Method chaining stops when this type of method is called.
>
> > ex\) `join()`, `first()`, `sum()`, `reduce()`...



### ⚡Chaining method

> > For a detailed description of the method chaining method, [click here](https://en.wikipedia.org/wiki/Method_chaining)

> This chaining-method returns an `ArrayUtils` instance.  
> Because of this, allowing the calls to be chained together in a single statement without requiring variables to store the intermediate results.







## \#⃣Method polymorphism

### ⚡ Magic suffix `"From"` <a id="from-suffix"></a>

Suffixing "From" to the any methods can called statically.

It can be used by giving an `iterable` as the first argument.

{% tabs %}
{% tab title="Example" %}
```php
$arr = ArrayUtils::reverseFrom([1,2,3,4,5]);

var_export((array) $arr);
//array (0 => 5, 1 => 4, 2 => 3, 3 => 2, 4 => 1
```
{% endtab %}

{% tab title="is same to" %}
```php
$arr = ArrayUtils::from([1,2,3,4,5])->reverse();

var_export((array) $arr);
//array (0 => 5, 1 => 4, 2 => 3, 3 => 2, 4 => 1
```
{% endtab %}
{% endtabs %}



### ⚡ Magic prefix`"As"` <a id="as-prefix"></a>

Prefixing "As" to the chaining method for returns a pure array.

{% tabs %}
{% tab title="Example" %}
```php
$arr = ArrayUtils::from([1,2,3,4,5]);

var_export($arr->reverseAs());
//array (0 => 5, 1 => 4, 2 => 3, 3 => 2, 4 => 1)
```
{% endtab %}

{% tab title="is same to" %}
```php
$arr = ArrayUtils::from([1,2,3,4,5]);

var_export((array) $arr->reverse());
//array (0 => 5, 1 => 4, 2 => 3, 3 => 2, 4 => 1)
```
{% endtab %}
{% endtabs %}



{% hint style="success" %}
You can use two functions at once.

```php
var_export(ArrayUtils::reverseFromAs([1,2,3,4,5]));
//array (0 => 5, 1 => 4, 2 => 3, 3 => 2, 4 => 1)
```
{% endhint %}



