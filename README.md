# Introduction



![](.gitbook/assets/title.svg)

## \#⃣What is ArrayUtils? <a id="importing"></a>

## What is ArrayUtils?

ArrayUtils is a library that provides a great way to manipulate arrays.

ArrayUtils is a library that provides a great way to manipulate arrays  
It wraps the array in an object and provides a variety of methods.   
As it is itself an `ArrayObject`, it can be used like an array.

It wraps the array in an object and provides a variety of methods.   
As it is itself an `ArrayObject`, it can be used like an array.

PHP's array functions are painful for developers. \(like `array_map`, `array_filter`\)  
In addition, since it is a the `function` breaks every time.   
I created this library to solve these problems and make code flow like `js-array`

PHP's array functions are painful for developers. \(like `array_map`, `array_filter`\)

## What happens when I use it?



* Array first or callback function first...  
* Return value or reference a variable...  



## \#⃣What happens when I use it? <a id="importing"></a>

Processing arrays through this library makes the code flow much clearer than pure PHP.

Pure PHP's array functions, when nested, reverse the code and get deeper and deeper indentations like below.

{% code title="Pure PHP" %}
```php
<?php

$playerFiles = scandir(Server::getInstance()->getDataPath() . "players/";
$onlinePlayers = Server::getInstance()->getOnlinePlayers();

$onlineNames = array_column(
    array_map(
        function(Player $player) : array{ return [strtolower($player->getName()), $player->getName()]; },
        $onlinePlayers
    ), 1, 0
);
$playerNames = array_column(
    array_map(
        function(string $playerName) : array{ return [strtolower($playerName), $playerName]; },
        array_map(
            function(string $playerName) use($onlineNames) : string{ return $onlineNames[strtolower($playerName)] ?? $playerName; },
            array_map(
                function(string $fileName) : string{ return substr($fileName, 0, -strlen(\".dat\")); },
                array_filter($playerFiles, function(string $fileName) : bool{ return substr($fileName, -strlen(\".dat\")) === \".dat\"; })
            )
        )
    ), 1, 0
);
```
{% endcode %}



ArrayUtils solves these problems and makes the code easier to figure out.

The code is sorted in the order in which the array is processed, the order of method names and arguments is also consistent like below.

{% code title="with ArrayUtils" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$playerFiles = scandir(Server::getInstance()->getDataPath() . "players/");
$onlinePlayers = Server::getInstance()->getOnlinePlayers();

$onlineNames = ArrayUtils::mapAssocFromAs($onlinePlayers, function(Player $player) : array{ return [strtolower($player->getName()), $player->getName()]; });
$playerNames = ArrayUtils::filterFrom($playerFiles, function(string $fileName) : bool{ return substr($fileName, -strlen(".dat")) === ".dat"; }) 
    ->map(function(string $fileName) : string{ return substr($fileName, 0, -strlen(".dat")); })
    ->map(function(string $playerName) use($onlineNames) : string{ return $onlineNames[strtolower($playerName)] ?? $playerName; })
    ->mapAssocAs(function(string $playerName) : array{ return [strtolower($playerName), $playerName]; });
```
{% endcode %}



Also, if you Using the `array-function` added in PHP 7.4, you can write more neatly.

{% code title="PHP >= 7.4 with ArrayUtils" %}
```php
<?php use kim\present\utils\arrays\ArrayUtils;

$playerFiles = scandir(Server::getInstance()->getDataPath() . "players/");
$onlinePlayers = Server::getInstance()->getOnlinePlayers();

$onlineNames = ArrayUtils::mapAssocFromAs($onlinePlayers, fn(Player $player) => [strtolower($player->getName()), $player->getName()]);
$playerNames = ArrayUtils::filterFrom($playerFiles, fn(string $fileName) => substr($fileName, -strlen(".dat")) === ".dat") 
    ->map(fn(string $fileName) => substr($fileName, 0, -strlen(".dat")))
    ->map(fn(string $playerName) => $onlineNames[strtolower($playerName)] ?? $playerName)
    ->mapAssocAs(fn(string $playerName) => [strtolower($playerName), $playerName]);
```
{% endcode %}

