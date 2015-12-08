# Whats new in Version 2.0 #

Version 2 is a complete rewrite of CssMin. The minification is now seperated into [Tokenization](http://en.wikipedia.org/wiki/Tokenization) and Minification.

The Tokenizer is written in plain PHP, requires no extensions, use no regular expressions and is optimized on savety and speed. On a decent machine 100KB complex css is tokenized in about 250 - 500ms.

The Minification is [configurable](Configuration.md) and make limited use of regular expressions.