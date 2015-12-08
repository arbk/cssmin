# SortRulesetProperties minifier filter #

## Description ##
This filter will sort ruleset properties by their name. This will slightly improve the compression ratio as for example of the [Apache Module mod\_deflate](http://httpd.apache.org/docs/2.0/mod/mod_deflate.html).

**Warning: Because of the nature of this filter, this filter may change the lexical meaning of the stylesheet and may break some browser hacks.**

To activate this filter you have to extend the minifier filter configuration:
```
$filters = array
	(
	/* ... your normal filter configuration ... */
	"SortRulesetProperties" => true
	);
```

This filter was created by: Rowan Beentje - [Assanka <http://assanka.net>](http://assanka.net).

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `false`

## Before: ##
```
div.my
	{
	width:		240px;
	padding:	0.25em;
	color:		black;
	border:		1px solid black;
	}
```

## After: ##
```
div.my{border:1px solid #000;color:#000;padding:.25em;width:240px}
```