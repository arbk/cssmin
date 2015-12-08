# RemoveEmptyRulesets minifier filter #

## Description ##
This filter will remove empty rulesets. This filter should always run after filters removing tokens of rulesets like the
[RemoveComments](MinifierFilterRemoveComments.md) filter.

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `true`

## Before: ##
```
div
	{
	/* No declarations */
	}
```

## After: ##
```
null
```