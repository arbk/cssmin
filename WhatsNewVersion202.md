# Whats new in Version 2.0.2 #

## Compatibility changes to Version 2.0.1 ##

  * Configuration option "convert-color-values" renamed to "convert-rgb-color-values"

## Conversion of named color values ##

New configuration option "convert-named-color-values". Named color will get converted to hexadecimal notation. Supported color names are:
  * [HTML 4.01 web colors](http://www.w3.org/TR/REC-html40/types.html#h-6.5)
  * [X11 color names supported by CSS Level 3](http://en.wikipedia.org/wiki/X11_color_names)
  * [The color "orange" as defined in CSS Level 2.1](http://www.w3.org/TR/2003/WD-CSS21-20030915/syndata.html#color-units)

## Conversion of font-weight values ##

New configuration option "convert-font-weight-values".

The font weight values "normal" and "bold" get converted to "400" and "700"

## Conversion of HSL color values ##

New configuration option "convert-hsl-color-values". HSL color values will get converted to hexadecimal notation. So `hsl(232,36%,48%)` will get converted to `#4e5aa7`.


## convert-css3-properties ##

Supports now:

  * animation
  * animation-delay
  * animation-direction
  * animation-duration
  * animation-fill-mode
  * animation-iteration-count
  * animation-name
  * animation-play-state
  * animation-timing-function
  * appearance
  * backface-visibility
  * background-clip
  * background-composite
  * background-inline-policy
  * background-origin
  * background-position-x
  * background-position-y
  * background-size
  * behavior
  * binding
  * border-after
  * border-after-color
  * border-after-style
  * border-after-width
  * border-before
  * border-before-color
  * border-before-style
  * border-before-width
  * border-border-bottom-colors
  * border-bottom-left-radius
  * border-bottom-right-radius
  * border-end
  * border-end-color
  * border-end-style
  * border-end-width
  * border-fit
  * border-horizontal-spacing
  * border-image
  * border-left-colors
  * border-radius
  * border-border-right-colors
  * border-start
  * border-start-color
  * border-start-style
  * border-start-width
  * border-top-colors
  * border-top-left-radius
  * border-top-right-radius
  * border-vertical-spacing
  * box-align
  * box-direction
  * box-flex
  * box-flex-group
  * box-flex-lines
  * box-ordinal-group
  * box-orient
  * box-pack
  * box-reflect
  * box-shadow
  * box-sizing
  * color-correction
  * column-break-after
  * column-break-before
  * column-break-inside
  * column-count
  * column-gap
  * column-rule
  * column-rule-color
  * column-rule-style
  * column-rule-width
  * column-span
  * column-width
  * columns
  * filter
  * float-edge
  * font-feature-settings
  * font-language-override
  * font-size-delta
  * font-smoothing
  * force-broken-image-icon
  * highlight
  * hyphenate-character
  * hyphenate-locale
  * hyphens
  * ime-mode
  * interpolation-mode
  * layout-flow
  * layout-grid
  * layout-grid-char
  * layout-grid-line
  * layout-grid-mode
  * layout-grid-type
  * line-break
  * line-clamp
  * line-grid-mode
  * logical-height
  * logical-width
  * margin-after
  * margin-after-collapse
  * margin-before
  * margin-before-collapse
  * margin-bottom-collapse
  * margin-collapse
  * margin-end
  * margin-start
  * margin-top-collapse
  * marquee
  * marquee-direction
  * marquee-increment
  * marquee-repetition
  * marquee-speed
  * marquee-style
  * mask
  * mask-attachment
  * mask-box-image
  * mask-clip
  * mask-composite
  * mask-image
  * mask-origin
  * mask-position
  * mask-position-x
  * mask-position-y
  * mask-repeat
  * mask-repeat-x
  * mask-repeat-y
  * mask-size
  * match-nearest-mail-blockquote-color
  * max-logical-height
  * max-logical-width
  * min-logical-height
  * min-logical-width
  * object-fit
  * object-position
  * opacity
  * outline-radius
  * outline-bottom-left-radius
  * outline-bottom-right-radius
  * outline-top-left-radius
  * outline-top-right-radius
  * padding-after
  * padding-before
  * padding-end
  * padding-start
  * perspective
  * perspective-origin
  * perspective-origin-x
  * perspective-origin-y
  * rtl-ordering
  * scrollbar-3dlight-color
  * scrollbar-arrow-color
  * scrollbar-base-color
  * scrollbar-darkshadow-color
  * scrollbar-face-color
  * scrollbar-highlight-color
  * scrollbar-shadow-color
  * scrollbar-track-color
  * stack-sizing
  * svg-shadow
  * tab-size
  * table-baseline
  * text-align-last
  * text-autospace
  * text-combine
  * text-decorations-in-effect
  * text-emphasis
  * text-emphasis-color
  * text-emphasis-position
  * text-emphasis-style
  * text-fill-color
  * text-justify
  * text-kashida-space
  * text-overflow
  * text-security
  * text-size-adjust
  * text-stroke
  * text-stroke-color
  * text-stroke-width
  * text-underline-position
  * transform
  * transform-origin
  * transform-origin-x
  * transform-origin-y
  * transform-origin-z
  * transform-style
  * transition
  * transition-delay
  * transition-duration
  * transition-property
  * transition-timing-function
  * user-drag
  * user-focus
  * user-input
  * user-modify
  * user-select
  * white-space
  * window-shadow
  * word-break
  * word-wrap
  * writing-mode
  * zoom

> # Syntax: #
## Minification ##
```
string CssMin::minify(string $css, array [$config])
```
## Parse only ##
```
array CssMin::parse(string $css)
```

## $config ##

See: [Configuration](Configuration.md)

# Examples: #
```
// Simple example using the default configuration
$css = file_get_contents("path/to/source.css");
$css = CssMin::minify($css);
file_put_contents("path/to/target.css", $css);
```

```
// Example with full configuration
$css = file_get_contents("path/to/source.css");
$css = CssMin::minify($css, array
	(
	"remove-empty-blocks"		=> true,
	"remove-empty-rulesets"		=> true,
	"remove-last-semicolons"	=> true,
	"convert-css3-properties"	=> true,
	"convert-font-weight-values"	=> true, // new in v2.0.2
	"convert-named-color-values"	=> true, // new in v2.0.2
	"convert-hsl-color-values"	=> true, // new in v2.0.2
	"convert-rgb-color-values"	=> true, // new in v2.0.2; was "convert-color-values" in v2.0.1
	"compress-color-values"		=> true,
	"compress-unit-values"		=> true,
	"emulate-css3-variables"	=> true
	));
file_put_contents("path/to/target.css", $css);
```