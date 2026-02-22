# Change Log of Omni Shader Tools for HLSL (VS Extension)

## 1.0.6

- Add .hlsli file support
- Add the Live Testing feature which can grey out preprocessor directive code blocks that don't match conditions, by using comments starting with `//!` and followed by some keywords. This feature is not available in the Basic version. See more details in <https://omnishader.amlovey.com/blog/?blog=live-testing>.
- Improve notification message display logic

## 1.0.5

- Add a status bar text to show backend language server status
- Add hover information support for normal macro definitions if they have document comments
- Add support for enums with bitfield clauses
- Improve hover information by ignoring some inline doxygen tags

## 1.0.4

- Add javadoc style document comments support. The supported tags are @params and @return
- Add docgen tags support for `@brief` and `@details`
- When inputting a document comment `//*` on functions/fields/variables, automatically generate javadoc style documentation
- Improve information display on hover information
- Fix a possible crash that caused by copy&paste in VS2026
- Fix a possible crash that caused by very large shader files
- Fix a bug that '\t' was not correctly parsed in document comments template
- Fix a bug that hover information does not show up when hovering macro function definition

## 1.0.3

- Fix a crash bug that caused by possible out of bound exception.

## 1.0.2

- Open full SignatureHelp feature to Basic version
- Add document comments support for properties in shaderlab syntax
- Add C# style document comments support for tags `summary`, `param` and `returns`
- When inputting a document comment `///` on functions/fields/variables, automatically generate C# style XML documentation 

## 1.0.1

- Improve license activation workflow
- Fix bug that members of buffer statement are missing

## 1.0.0

- First release
