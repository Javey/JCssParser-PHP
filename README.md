JCssParser-PHP
==============

A lightweight css parser written in php. Refer to [reworkcss](https://github.com/reworkcss/css)

#Useage

##parse

```php
<?php
require_once('JCssParser.class.php');
$parser = new JCssParser();
$cssNode = $parser->parse('.a{width: 2px}');
```

##stringify

```php
require_once('JCssStringifier.class.php');
$stringifier = new JCssStringifier();
$cssDoc = $stringifier->stringify($cssNode);
```
