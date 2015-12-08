# CompressUnitValues minifier plugin #

## Description ##
This plugin compress unit values.

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `false`

## Before: ##
```
border: 0px solid black;
padding: 0.5em;
margin: 0 0 0 0;
```

## After: ##
```
border:0 solid black;
padding:.5em;
margin:0;
```