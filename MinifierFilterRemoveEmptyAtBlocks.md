# RemoveEmptyAtBlocks minifier filter #

## Description ##
This filter will remove empty @font-face, @media and @page at-rule blocks. This filter should always run after any
filters removing tokens like the [RemoveComments](MinifierFilterRemoveComments.md) or
[RemoveEmptyRulesets](MinifierFilterRemoveEmptyRulesets.md) filter.

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `true`

## Before: ##
```
@media print
	{
	/* No rulesets */
	}
```

## After: ##
```
null
```