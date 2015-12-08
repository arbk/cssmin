# Variables minifier plugin #

## Description ##
This plugin search for variables and replace them with the variable value. This plugin requires the
[Variables filter](MinifierFilterVariables.md).

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `true`

## Before: ##
```
@variables
	{
	defaultFontColor: #444444;
	defaultBorderColor: black;
	}
div.Test
	{
	color: var(defaultFontColor);
	border: 1px solid var(defaultBorderColor);
	}
```

## After: ##
```
div.Test{color:#444444;border:1px solid black;}
```