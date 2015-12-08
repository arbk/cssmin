# ConvertNamedColors minifier plugin #

## Description ##
This plugin convert named color values to hexadecimal notation. Supported named color values are:

  * [HTML 4.01 web colors](http://www.w3.org/TR/REC-html40/types.html#h-6.5)
  * [X11 color names supported by CSS Level 3](http://en.wikipedia.org/wiki/X11_color_names)
  * [The color "orange" as defined in CSS Level 2.1](http://www.w3.org/TR/2003/WD-CSS21-20030915/syndata.html#color-units)

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `false`

## Before: ##
```
border: 1px solid red;
```

## After: ##
```
border:1px solid f00;
```