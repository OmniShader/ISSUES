# Change Log of Omni Shader Tools for Unity (VS Extension)

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
