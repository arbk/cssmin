# Whitesmiths Formatter #

This formatter creates a formated output in the [Whitesmiths](http://en.wikipedia.org/wiki/Indent_style#Whitesmiths_style).
indent style.

## Syntax ##
```
string new CssOtbsFormatter(array $tokens [, string $indent = null][, array $padding = null]);
```

### array $tokens ###
Array of aCssTokens.

### string $indent ###
Indenation string. Defaults to 4 spaces.

### string $padding ###
Padding for declaration values.

## Example ##
```
$source = file_get_contents("path/to/source.css");
// Use a instance of CssParser to get tokens
$parser = new CssParser($source);
$tokens = $parser->getTokens();
// or use the adapter function of CssMin 
$tokens = CssMin::parse($source);
// Create a instance of the formatter; set the indent string to TAB and the declaration value padding to 32
$formatter = new CssWhitesmithsFormatter($tokens, "\t", 32);
// Print the formatted source
echo "<pre>" . (string) $formatter . "</pre>;
```