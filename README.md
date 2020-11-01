# Introduction

![](.gitbook/assets/title.svg)

## \#⃣What is ArrayUtils?

ArrayUtils is a library that provides a great way to manipulate arrays.

The ~~evil~~ PHP array functions give developers the pain of:

* Some functions **requires array first**, but some functions **require array last**...  
* Some functions **returns result**, but some functions **modify referenced variables**...
* Code was **line-break** because since it is a the function...
* Each function has **different parameters to the callback function**...
* No modern functions using arrays. Such as `every`, `some`

I created this library to solve these problems and make code flow like `js-array`

## \#⃣What happens when I use it? <a id="importing"></a>

Processing arrays through this library makes the code flow much clearer than pure PHP.

Pure PHP's array functions, when nested, reverse the code and get deeper and deeper indentations.

ArrayUtils solves these problems and makes the code easier to figure out.

Also, if you Using the `arrow-function` added in PHP 7.4, you can write more neatly.

{% tabs %}
{% tab title="Pure PHP" %}
```php
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
{% endtab %}

{% tab title="with ArrayUtils" %}
```php
use kim\present\utils\arrays\ArrayUtils;

$playerFiles = scandir(Server::getInstance()->getDataPath() . "players/");
$onlinePlayers = Server::getInstance()->getOnlinePlayers();

$onlineNames = ArrayUtils::mapAssocFromAs($onlinePlayers, function(Player $player) : array{ return [strtolower($player->getName()), $player->getName()]; });
$playerNames = ArrayUtils::filterFrom($playerFiles, function(string $fileName) : bool{ return substr($fileName, -strlen(".dat")) === ".dat"; }) 
    ->map(function(string $fileName) : string{ return substr($fileName, 0, -strlen(".dat")); })
    ->map(function(string $playerName) use($onlineNames) : string{ return $onlineNames[strtolower($playerName)] ?? $playerName; })
    ->mapAssocAs(function(string $playerName) : array{ return [strtolower($playerName), $playerName]; });
```
{% endtab %}

{% tab title="PHP >= 7.4 with ArrayUtils" %}
```php
use kim\present\utils\arrays\ArrayUtils;

$playerFiles = scandir(Server::getInstance()->getDataPath() . "players/");
$onlinePlayers = Server::getInstance()->getOnlinePlayers();

$onlineNames = ArrayUtils::mapAssocFromAs($onlinePlayers, fn(Player $player) => [strtolower($player->getName()), $player->getName()]);
$playerNames = ArrayUtils::filterFrom($playerFiles, fn(string $fileName) => substr($fileName, -strlen(".dat")) === ".dat") 
    ->map(fn(string $fileName) => substr($fileName, 0, -strlen(".dat")))
    ->map(fn(string $playerName) => $onlineNames[strtolower($playerName)] ?? $playerName)
    ->mapAssocAs(fn(string $playerName) => [strtolower($playerName), $playerName]);
```
{% endtab %}
{% endtabs %}

