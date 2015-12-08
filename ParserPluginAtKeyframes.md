# AtKeyframes parser plugin #

## Description ##
This plugin is responsible to parse @keyframes at-rule blocks, rulesets and declarations.

```
// @keyframes at-rule start
@keyframes "bounce"
	{
	// @keyframes at-rule ruleset start
	from
		{
		top: 100px; // @keyframes at-rule ruleset declaration
		animation-timing-function: ease-out; // @keyframes at-rule ruleset declaration
		}
	// @keyframes at-rule ruleset end and start of the next ruleset... 
	25%	
		{
		top: 50px;
		animation-timing-function: ease-in;
		}
	50%	
		{
		top: 100px;
		animation-timing-function: ease-out;
		}
	75%
		{
		top: 75px;
		animation-timing-function: ease-in;
		}
	to	
		{
		top: 100px;
		}
	}
// @keyframes at-rule end
```

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `true`