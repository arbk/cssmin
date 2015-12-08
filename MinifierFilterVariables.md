# Variables minifier filter #

## Description ##
This filter will process the variable declarations in the parsed stylesheet and send the result to the
[Variables Plugin](MinifierPluginVariables.md).

The implementation of the emulation of CSS Level 3 variables is based on
[CSS Variables Revision 1.0](http://disruptive-innovations.com/zoo/cssvariables/) by Daniel Glazman
(Disruptive Innovations) and David Hyatt (Apple, Inc.)

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `true`

## Before: ##
```
@variables /* equals @variables all */
	{
	defaultTextColor:		#44444;
	defaultBorder:			1px solid #444444;
	}
@variables screen, projection /* multiple media scopes are possible */
	{
	anchorColor:			black;
	anchorTextDecoration:		none;
	}
@variables print
	{
	defaultTextColor:		black; /* overwrites defaultTextColor from media-scope "all" */
	defaultBorder:			1px solid black; /* overwrites defaultBorder from media-scope "all" */
	anchorColor:			black;
	anchorTextDecoration:		underline;
	}
@media screen
	{
	a
		{
		color:			var(anchorColor);
		text-decoration:	var(anchorTextDecoration);
		}
	table
		{
		border:			var(defaultBorder);
		color:			var(defaultTextColor);
		}
	}
@media print
	{
	a
		{
		color:			var(anchorColor);
		text-decoration:	var(anchorTextDecoration);
		}
	table
		{
		border:			var(defaultBorder);
		color:			var(defaultTextColor);
		}
	}
```

## After: ##
```
@media screen
	{
	a
		{
		color:			black;
		text-decoration:	none;
		}
	table
		{
		border:			1px solid #44444;
		color:			#44444;
		}
	}
@media print
	{
	a
		{
		color:			blue;
		text-decoration:	underline;
		}
	table
		{
		border:			1px solid black;
		color:			black;
		}
	}
```