# Changelog

## [0.2.0] - 2020-05-12

### Fixed

* Fixed bug that manifested in crashes while typing. The underlying problem is I was mutating nodes that "belonged" to result objects with no way to update the enclosing result. The fix was to make a copy of the node before mutating. I might want to make Node be a struct but I'm not ready to do that investigation yet.

## [0.1.0] - 2020-05-10

### Added

* `IncrementalParsingTextStorage.rawText` to get text without formatting replacements applied.

## [0.0.1] - 2020-05-07

The initial "MVP" release! Provides an implementation of NSTextStorage that does incremental parsing of its contents and uses the resulting parse tree to determine the text attributes. E.g., it can provide syntax highlighting that changes as you type.