# Whats new in Version 3.0 #

## Compatibility changes to Version 2.0.2 ##
  * The syntax of the minifier configuration was changed. See: [Minifier configuration](MinifierConfiguration.md)

## OOP ##
CssMin version 3 is a object orientated implementation of version 2. This fixes the major problem (at least for me)
of version 2: the maintainability. Also version 3 should be less error-prone and has a much better expandability.

### But there is always a price to pay ###
While the parser have the same speed as in version 2 the memory usage will be higher and the minification is ca. 20%
slower (with all configuration options turned on).

### Filters and plugins ###
Parser plugins encapsules the parse logic for different elements of the stylesheet. Parser plugins are using the parser
methods to change the parser state, buffer, etc. and return values for flow control of the parser process.

Minifier filter are used for pre-processing the array of tokens returned by the parser while minifier plugins getting
called on every token of the array of token returned by the parser. Minifier filters are able to insert, edit and remove
tokens; minifier plugins not. Both are using return values for flow control of the minification process.

### Source, build and minified version ###
The build version is a single file containing every php file of the source as combined version. The minified version is
a minified containing every php file of the source as combined and minified version. The source version is the normal
source with autoload mechanism.

## Variables now can get used as part of a declaration value ##
```
@variables
	{
	/* Variable declaration */
	myVar: black;
	}
div.Test2
	{
	/* Variable used as part of a declaration value */
	border: 1px solid var(myVar);
	}
```

## Parser for expression() declaration values ##
expresssion() declaration values will get parsed property even if the expression includes curly braces and semicolons.
Additional if [JSMin](https://github.com/rgrove/jsmin-php/) is defined the expression will get compressed using
[JSMin](https://github.com/rgrove/jsmin-php/).

## Formatters ##
For debugging purposes two formatter are included. The formatter will output a array of tokens with correct indentation
(and a optional declaration value padding). The formatters are:

  * [OTBS (The One True Brace Style)](OtbsFormatter.md)
  * [Whitesmiths](WhitesmithsFormatter.md)