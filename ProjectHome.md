# What is CssMin? #

CssMin is a css parser and minfier. It minifies css by removing unneeded whitespace character, comments, empty blocks and empty declarations. In addition declaration values can get rewritten to shorter notation if available. The minification if [configurable](MinifierConfiguration.md).

CssMin has some benefits. It supports the rewrite of [CSS Level 3 properties to their browser specific counterparts](MinifierFilterConvertLevel3Properties.md) and
is able to simulate [CSS Variables](MinifierFilterVariables.md).

**CssMin Version 3 is released. Check out [What's new in Version 3.0](WhatsNewVersion30.md) / [3.0.1](WhatsNewVersion301.md) and [download](http://code.google.com/p/cssmin/downloads/list) the new version.**

# Requirements: #
  * PHP 5.x

# Syntax: #
```
string CssMin::minify(string $source [, array $filters = array()][, array $plugins = array()]);
```

## string $source ##
The source css as string.

### array $filters ###
The filter configuration as array (optional). See [Filter Configuration](MinifierConfiguration#array_$filters.md)

### array $plugins ###
The plugin configuration as array (optional). See: [Plugin Configuration](MinifierConfiguration#array_$plugins.md)

## Example ##
```
// Simple minification WITHOUT filter or plugin configuration
$result = CssMin::minify(file_get_contents("path/to/source.css"));

// Minification WITH filter or plugin configuration 
$filters = array(/*...*/);
$plugins = array(/*...*/);
// Minify via CssMin adapter function
$result = CssMin::minify(file_get_contents("path/to/source.css"), $filters, $plugins);
// Minify via CssMinifier class
$minifier = new CssMinifier(file_get_contents("path/to/source.css"), $filters, $plugins);
$result = $minifier->getMinified();
```