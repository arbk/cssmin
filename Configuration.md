# Configuration #

## Syntax ##
```
string CssMin::minify(string $source [, array $filters = array()][, array $plugins = array()]);
```

### string $source ###
The source css as string.

### array $filters ###
The filter configuration as array (optional). The configuration array must use the name of the filter as key and as
value `true`, `false` or an array with configuration parameters getting passed to the filter.

#### Example filter configuration ####
```
$filters = array
	(
	"ImportImports"			=> array("BasePath" = "path/to/base"),
	"RemoveComments"		=> true, 
	"RemoveEmptyRulesets"		=> true,
	"RemoveEmptyAtBlocks"		=> true,
	"ConvertLevel3AtKeyframes"	=> array("RemoveSource" => false),
	"ConvertLevel3Properties"	=> true,
	"Variables"			=> true,
	"RemoveLastDelarationSemiColon"	=> true
	);
```

#### Default filter configuration ####
```
$filters = array
	(
	"ImportImports"			=> false,
	"RemoveComments"		=> true, 
	"RemoveEmptyRulesets"		=> true,
	"RemoveEmptyAtBlocks"		=> true,
	"ConvertLevel3AtKeyframes"	=> false,
	"ConvertLevel3Properties"	=> false,
	"Variables"			=> true,
	"RemoveLastDelarationSemiColon"	=> true
	);
```

See also: [Minifier filters](MinifierFilters.md)

### array $plugins ###
The plugin configuration as array (optional). The configuration array must use the name of the plugin as key and as
value `true`, `false` or an array with configuration parameters getting passed to the plugin.

#### Example plugin configuration ####
```
$plugins = array
	(
	"Variables"			=> true,
	"ConvertFontWeight"		=> true,
	"ConvertHslColors"		=> true,
	"ConvertRgbColors"		=> true,
	"ConvertNamedColors"		=> true,
	"CompressColorValues"		=> true,
	"CompressUnitValues"		=> true,
	"CompressExpressionValues"	=> true
	);
```

#### Default plugin configuration ####
```
$plugins = array
	(
	"Variables"			=> true,
	"ConvertFontWeight"		=> false,
	"ConvertHslColors"		=> false,
	"ConvertRgbColors"		=> false,
	"ConvertNamedColors"		=> false,
	"CompressColorValues"		=> false,
	"CompressUnitValues"		=> false,
	"CompressExpressionValues"	=> false
	);
```

See also: [Minifier plugins](MinifierPlugins.md)

## Examples ##
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