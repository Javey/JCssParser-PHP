JCssParser-PHP
==============

A lightweight css parser written in php. Reference from [reworkcss](https://github.com/reworkcss/css)

#Useage

##parse

```php
<?php
require_once('JCssParser.class.php');
$parser = new JCssParser();
$cssNode = $parser->parse('.a{width: 2px}');
```
```php
print_r($cssNode);

Array
(
    [type] => stylesheet
    [stylesheet] => Array
        (
            [rules] => Array
                (
                    [0] => Array
                        (
                            [type] => rule
                            [selectors] => Array
                                (
                                    [0] => .a
                                )

                            [declarations] => Array
                                (
                                    [0] => Array
                                        (
                                            [type] => declaration
                                            [property] => width
                                            [value] => 2px
                                        )

                                )

                        )

                )

        )

)
```

##stringify

```php
<?php
require_once('JCssStringifier.class.php');
$stringifier = new JCssStringifier();
$cssDoc = $stringifier->stringify($cssNode);
```
