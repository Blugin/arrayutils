# How to use?

{% hint style="info" %}
The guide assumes intermediate level knowledge of **PHP-language** and [**poggit-virion**](https://github.com/poggit/support/blob/master/virion.md)\*\*\*\*
{% endhint %}

The easiest way to try out ArrayUtils is using the poggit. Poggit automatically merges virions, it is better to use this feature.

## \#⃣Importing ArrayUtils <a id="importing"></a>

As with all classes, must import ArrayUtils into your php file.

```php
use kim\present\utils\arrays\ArrayUtils;
```

## \#⃣Create ArrayUtils from value <a id="creating"></a>

There are 4 ways to create ArrayUtils.

### ⚡ 1. Use constructor

> In the most basic way, it's just created through the constructor.
>
> ```php
> $arr = new ArrayUtils([1,2,3,4,5]);
> echo $arr->join(", "); //1, 2, 3, 4, 5
> ```

### ⚡ 2. Use static from\(\) method

> Same method as [`Array.from()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/from) in java script
>
> ```php
> $arr = ArrayUtils::from([1,2,3,4,5]);
> echo $arr->join(", "); //1, 2, 3, 4, 5
> ```

### ⚡ 3. Use static of\(\) method

> Same method as [`Array.of()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/of) in java script
>
> ```php
> $arr = ArrayUtils::of(1,2,3,4,5);
> echo $arr->join(", "); //1, 2, 3, 4, 5
> ```

### ⚡ 4. Use magic suffix "From"

> > For a detailed description of the `from-suffix`, [click here](https://arrayutils.docs.present.kim/methods/main#from-suffix)
>
> All methods can be called statically with the suffix `From`
>
> ```php
> echo ArrayUtils::joinFrom([1,2,3,4,5], ", "); //1, 2, 3, 4, 5
> ```

## \#⃣Use the desired methods <a id="using"></a>

