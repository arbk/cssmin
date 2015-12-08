# ConvertLevel3Properties minifier filter #

## Description ##
This filter convert [CSS Level 3 properties](MinifierFilterConvertLevel3Properties#Supported_properties.md) (and some browser specific properties) to browser specific counterparts.

## Configuration: ##
  * `true` / `false`

## Defaults: ##
  * `true`

## Before: ##
```
div
	{
	border-radius: 1em;
	}
```

## After: ##
```
div{-moz-border-radius:1em;-webkit-border-radius:1em;border-radius:1em;}
```

## Supported properties ##
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