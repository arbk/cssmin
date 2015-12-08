# Whats new in Version 3.0.1 #

## Compatibility changes to Version 3.0.0 ##
Version 3.0.1 will throw no more error messages via "trigger\_error" by default (See also: [Issue #40](http://code.google.com/p/cssmin/issues/detail?id=40)).

To reactivate the throwing of error messages you can set the verbose mode of CssMin to `true`.
```
CssMin::setVerbose(true);
```

Independently of the verbose mode triggered errors will get stored in CssMin.
```
if (CssMin::hasErrors())
	{
	$error = CssMin::getErrors();
	// do something with the errors
	}
```

## Support for @-moz-keyframes / @-webkit-keyframes ##
The parser and minifier filter [ConvertLevel3AtKeyframes](MinifierFilterConvertLevel3AtKeyframes.md) now support "@-moz-keyframes" and "@-webkit-keyframes".

## New minifier filter SortRulesetProperties ##
Added the 3r party minifier filter [SortRulesetProperties](MinifierFilterSortRulesetProperties.md).