# ConvertLevel3AtKeyframes minifier filter #

## Description ##
This filter will convert @keyframes at-rule block to browser specific counterparts.

## Configuration: ##
  * RemoveSource: if set to `true` the CSS Level 3 @keyframes block will get removed.

## Defaults: ##
  * `false`

## Before: ##
```
@keyframes "bounce"
	{
	from
		{
		top: 100px;
		animation-timing-function: ease-out;
		}
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
```

## After: ##
```
@keyframes "bounce"
	{
	from
		{
		top: 100px;
		animation-timing-function: ease-out;
		}
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
@-moz-keyframes "bounce"
	{
	from
		{
		top: 100px;
		animation-timing-function: ease-out;
		}
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
@-webkit-keyframes "bounce"
	{
	from
		{
		top: 100px;
		animation-timing-function: ease-out;
		}
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
```

## After (with `RemoveSource` is `true`): ##
```
@-moz-keyframes "bounce"
	{
	from
		{
		top: 100px;
		animation-timing-function: ease-out;
		}
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
@-webkit-keyframes "bounce"
	{
	from
		{
		top: 100px;
		animation-timing-function: ease-out;
		}
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
```