# ImportImports minifier filter #

## Description ##
This filter external stylesheets defined in @import at-rules will get parsed and inserted into the current stylesheet.
Imported stylesheets are allowed to have their own @import at-rules. It is required to set set the configuration
parameter `BasePath` to a valid path. All paths defined in @import at-rules will get interpreted based on this base path.

If there are media type defined in the @import at-rule there will be alot of processing to simulate the browsers behavior. This includes:

  1. document level rulesets get wrapped into a @media at-rule block with the media types defined in the @import at-rule.
  1. @font-face, @media, @page at-rule blocks and other at-rule statements will get moved to the top.
  1. @media at-rule blocks with no matching media types will get removed.
  1. @media at-rule blocks with partial matching media types the unmatching media types will get removed.
  1. @media at-rule blocks with the same media types as the @import at-rule the containing rulesets get moved to document level and the @media at-rule block removed.
  1. @import at-rules with no media type (or only the "all" media type) defined the media type of the @import at-rule will get set to the media types defined in the parent @import at-rule.
  1. @import at-rules with partial matching media types the unmatching media types will get removed
  1. @import at-rule with no matching media type will get removed.

## Configuration: ##
  * BasePath: Defines the base path. Every resource path of any @import at-rule will get interpreted based on the configured base path.

## Defaults: ##
  * `false`

## Example ##
  * _not available_