# Parser configuration #

## Syntax ##
```
string CssMin::parse(string $source [, array $plugins = array()]);
```

### string $source ###
The source css as string.

### array $plugins ###
The plugin configuration as array (optional). The configuration array must use the name of the plugin as key and as
value `true`, `false` or an array with configuration parameters getting passed to the plugin.

#### Example plugin configuration ####

**This is also the default configuration**

```
$plugins = array
	(
	"Comment"		=> true,
	"String"		=> true,
	"Url"			=> true,
	"Expression"	=> true,
	"Ruleset"		=> true,
	"AtCharset"		=> true,
	"AtFontFace"	=> true,
	"AtImport"		=> true,
	"AtKeyframes"	=> true,
	"AtMedia"		=> true,
	"AtPage"		=> true,
	"AtVariables"	=> true
	);
```

See also: [Parse plugins](ParserPlugins.md)

## Example ##

```
// Create configuration array (optional) 
$plugins = array(/*...*/);
// Parse via CssMin adapter function
$result = CssMin::parse(file_get_contents("path/to/source.css"), $plugins);
// Parse via CssParser class
$parser = new CssParser(file_get_contents("path/to/source.css"), $plugins);
$result = $parser->getTokens();
```