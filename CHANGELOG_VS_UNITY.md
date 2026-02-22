# Change Log of Omni Shader Tools for Unity (VS Extension)

## 1.1.0

Add the Live Testing feature which can grey out preprocessor directive code blocks that don't match conditions, by using comments starting with `//!` and followed by some keywords. 

Multiple keywords are joined by `;` and use `:` to join the keyword and its value. 

For example: `//! DEBUG;STEP:1` has two keywords, one is `DEBUG` and the other is `STEP` with value `1`. 

This feature is not available in the Basic version.

## 1.0.9

- Add a status bar text to show backend language server status
- Add hover information support for normal macro definitions if they have document comments
- Add support for enums with bitfield clauses
- Improve hover information by ignoring some inline doxygen tags
- Fix bug that Code Completions are not working on `#pragma`

## 1.0.8

- Add javadoc style document comments support. The supported tags are @params and @return
- Add docgen tags support for @brief
- When inputting a document comment `//*` on functions/fields/variables, automatically generate javadoc style documentation
- Improve information display on hover information
- Fix a possible crash that caused by copy&paste in VS2026
- Fix a possible crash that caused by very large shader files
- Fix a bug that '\t' was not correctly parsed in document comments template

## 1.0.7

- Open full SignatureHelp feature to Basic version
- Add document comments support for properties in shaderlab syntax
- Add C# style document comments support for tags `summary`, `param` and `returns`
- When inputting a document comment `///` on functions/fields/variables, automatically generate C# style XML documentation 

## 1.0.6

- Optimize workspace setup time during language server startup
- Fix bug that members of buffer statement are mssing


## 1.0.5

- Fix bug that code completion return no results when code line start with `#` in some cases
- Fix bug that workspace path with spaces will cause shader searching failed
- Fix bug that while/for loop body without braces will not break into new line 

## 1.0.4

- Add incremental syntax parsing mode, defaulting to `true`. If you encounter some unexpected errors, try to disable it via `Tools -> Options -> Text Editor -> UnityShader -> Configuration -> Enable Incremental Parsing`
- Improve shader file searching and matching algorithm to speed up language server startup
- Fix bug that clearing content of shader will make backend language server stop working
- Fix bug that code parsing may be broken by field access in some cases
- Fix bug that Cut (ctrl+x) will may cause VS exception occurs

## 1.0.3

- Add intellisense support for Enumeration
- Fix outlining is not working when error dialognostics are disabled.
- Fix a formatting bug for block comments
  
## 1.0.2

- Fix a bug that path parsing is not correctly in some cases
- Fix a parser bug about 'varying' keyword that may break intellisense

## 1.0.1

- Add `UnityPerMaterial`, `UnityPerFrame` and `UnityPerDraw` to completion
- Add a setting for disabling language features of compiled or generated shader file from Unity Editor Inspector and enabled by default
- Fix an IO error when activating license

## 1.0.0

- Add parser support for namespace and enum of hlsl
- Add formatting support for namespace and enum of hlsl
- Add hover information support for tags
- Fix a formatting bug that macro call will not break into new line in some cases
- Fix a bug that else clause formatting will be broken in some cases

## 0.0.17b

- Add `#version` support for glsl
- Add some missing builtin functions and types for hlsl
- Fix bug that cannot get members of array item in completions
- Fix bug that cause mismatch errors are not correctly for conditional expression

## 0.0.16b

- Add completions and hover information support for `#pragma` directives 
- Fix a syntax parser bugs that cause functions to be missing in intellisense 
- Fix some formatting bugs

## 0.0.15b

- Add Ctrl + Left Click to jump to definition
- Add support for include path start with "Assets"
- Add some missing builtin functions for dx12
- Fix bug that path intellisense not provide library files in same folder in some cases
- Fix bug that function parameter with default value will be parsed incorrectly

## 0.013b

- Add formatting setting option for macro `omnishader.formatting.macroMatchIndent`
- Add path intellisense support for `#include`
- Add support for `#warning`
- Improve tags formatting that tags items will wrap to next line if tags count larger than 3

## 0.0.12b

- Add support for function declaration parameter with default value
- Add support for generic types
- Add some missing primitive types for hlsl
- Add support for multiple variables list with default value assigned
- Add support for parameter list with preprocessor of function declaration
- Fix unresolved symbol diagnostics for some cases

## 0.0.11b

- Add support for `CustomEditorForRenderPipeline`
- Add formatting support for tabsize and insert spaces base on editor config
- Add some missing HLSL builtin functions
- Improve error diagnostics on conditional blocks and assignments

## 0.0.10b

- Add syntax parser support for initializer list
- improve glsl support for builtin variables

## 0.0.9b

- Fixed Function expression are case insensitive now
- Fix bug that macro call in struct will show errors in some cases
- Fix few formatting bugs
- Fix few syntax parser errors

## 0.0.8b

- Add generic type support for type mismatch error diagnostics
- Add INCLUDECG and INCLUDEHLSL support
- Add support for Grab Pass
- Add support for formatting to be able to place braces on new lines
- Fix bunch of document formatting bugs

## 0.0.7b

- Add type mismatch error diagnostics support for assignments, binary expressions and conditional blocks
- Improve error diagnostics for unresolved symbols
- Improve hover information for some types
- Fix bug that basic completion in free mode is not working in some scenarios
- Fix bug that no error dialog will show if activate license failed

## 0.0.6b

- Improve language server startup time

## 0.0.5b

- Add support for `#include_with_pragmas` directive of Unity
- Add diagnostic error support for include errors, undefined symbols errors, syntax errors and missing symbols errors. 
Its diabled by default. Enable it via `Tools -> Options -> Text Editor -> UnityShader -> Configuration -> Enable Diagnostics`
- Add support for cbuffer or tbuffer statements
- Fix bug that variables in conditional block are not included in definitions
- Fix bug that variables declaration with default value are not included in definitions
- Serveral bug fixes that finding definitions of symbols are not correctly

## 0.0.4b

- Fix bug that failed to active license

## 0.0.3b

- Fix a notification bug

## 0.0.2b

- Improve include file searching algorithms
- Fix bug that doucments are not updated when there are changes

## 0.0.1b

- First beta release
