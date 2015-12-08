# CompressExpressionValues minifier plugin #

## Description ##
This plugin compress the content of expresssion() declaration values.

For compression [JSMin](https://github.com/rgrove/jsmin-php/) is required and have to be already included or
loadable via [autoloading](http://goo.gl/JrW54).

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `false`

## Before: ##
```
width: expression( Math.round( Math.random() * 100 ) );
```

## After: ##
```
width:expression(Math.round(Math.random()*100));
```