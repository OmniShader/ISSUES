# Change Log of Omni Shader Tools for Unity (VSCode Extension)

## 1.1.3

About Live Testing feature, see more details in this blog: <https://omnishader.amlovey.com/blog/?blog=live-testing>

Updates in this release:
- Improve notification message display logic
- Fix a bug that live testing result is not correct in some cases

## 1.1.2

Add the Live Testing feature which can grey out preprocessor directive code blocks that don't match conditions, by using comments starting with `//!` and followed by some keywords. 

Multiple keywords are joined by `;` and use `:` to join the keyword and its value. 

For example: `//! DEBUG;STEP:1` has two keywords, one is `DEBUG` and the other is `STEP` with value `1`. 

This feature is not available in the Basic version.

## 1.1.1

- Quick fix for a bug that document comments have inline tags was broken in some cases

## 1.1.0

- Add hover information support for normal macro definitions if they have document comments
- Add support for enums with bitfield clauses
- Improve hover information by ignoring some inline doxygen tags
- Clicking the "Omni Shader" status bar item will now check license status

## 1.0.9

- Add a status bar item to show backend language server status
- Add javadoc style document comments support. The supported tags are @params and @return
- Add docgen tags support for `@brief` and `@details`
- When inputting a document comment `//*` on functions/fields/variables, automatically generate javadoc style documentation
- Improve information display on hover information
- Fix a bug that hover information does not show up when hovering macro function definition

## 1.0.8

- Open full SignatureHelp feature to Basic version
- Add document comments support for properties in shaderlab syntax
- Add C# style document comments support for tags `summary`, `param` and `returns`
- When inputting a document comment `///` on functions/fields/variables, automatically generate C# style XML documentation 

## 1.0.7

- Optimize workspace setup time during language server startup
- Fix bug that members of buffer statement are mssing

## 1.0.6

- Fix bug that code completion return no results when code line start with `#` in some cases
- Fix bug that workspace path with spaces will cause shader searching failed
- Fix bug that while/for loop body without braces will not break into new line 

## 1.0.5

- Add incremental syntax parsing mode, defaulting to `true`. If you encounter some unexpected errors, try to disable it in settings `omnishader.incrementalParsing`
- Improve shader file searching and matching algorithm to speed up language server startup
- Fix bug that clearing content of shader will make backend language server stop working
- Fix bug that code parsing may be broken by field access in some cases

## 1.0.4

- Add intellisense support for Enumeration
- Fix a formatting bug for block comments

## 1.0.3

- Fix a bug that path parsing is not correctly in some cases
- Fix a parser bug about 'varying' keyword that may break intellisense
  
## 1.0.2

Add Linux support, and Happy New Year and best wishes to you and your family!

## 1.0.1

- Add `UnityPerMaterial`, `UnityPerFrame` and `UnityPerDraw` to completion
- Add a setting `omnishader.disableCompiledShader` for disabling language features of compiled or generated shader file from Unity Editor Inspector and enabled by default
- Fix an IO error when activating license

## 1.0.0

- Add parser support for namespace and enum of hlsl
- Add formatting support for namespace and enum of hlsl
- Add hover information support for tags
- Improve notification information for more clarity
- Fix a formatting bug that macro call will not break into new line in some cases
- Fix a bug that vscode will open non-existed file in Go To Definition feature
- Fix a bug that else clause formatting will be broken in some cases

## 0.0.31b

- Improve license activation workflow to make it more smooth

## 0.0.30b

- Add `#version` support for glsl
- Add some missing builtin functions and types for hlsl
- Fix bug that cannot get members of array item in completions
- Fix bug that cause mismatch errors are not correctly for conditional expression

## 0.0.29b

- Add completions and hover information support for `#pragma` directives 
- Fix a syntax parser bugs that cause functions to be missing in intellisense 
- Fix some formatting bugs

## 0.0.28b

- Hot fix for IO error when activating omnishader

## 0.0.27b

- Add support for include path start with "Assets"
- Add some missing builtin functions for dx12
- Fix bug that path intellisense not provide library files in same folder in some cases
- Fix bug that function parameter with default value will be parsed incorrectly

## 0.0.26b

- Add formatting setting option for macro `omnishader.formatting.macroMatchIndent`
- Add path intellisense support for `#include`
- Add support for `#warning`
- Improve tags formatting that tags items will wrap to next line if tags count larger than 3

## 0.0.25b

- Add support for function declaration parameter with default value
- Add support for generic types
- Add some missing primitive types for hlsl
- Add support for multiple variables list with default value assigned
- Add support for parameter list with preprocessor of function declaration
- Fix unresolved symbol diagnostics for some cases

## 0.0.24b

- Show information message when license is activating
- Fix bug that error diagnostics for matrix swizzling incorrect in some cases

## 0.0.23b

- Fix a bug that Omni Shader Activate command is not response sometimes
e
## 0.0.22b

- Hot fix a crash bug in backend language server

## 0.0.21b

- Add support for `CustomEditorForRenderPipeline`
- Add support for .editorconfig
- Add formatting support for tabsize and insert spaces base on vscode editor config
- Add some missing HLSL builtin functions
- Improve error diagnostics on conditional blocks and assignments

## 0.0.20b

- Hot fix for a regression bug for formatting

## 0.0.19b

- Add syntax parser support for initializer list
- improve glsl support for builtin variables


## 0.0.18b

- Hot fix: fix bug that cannot execute Omni Shader Activate command

## 0.0.17b

- Fixed Function expression are case insensitive now
- Fix bug that macro call in struct will show errors in some cases
- Fix few formatting bugs
- Fix few syntax parser errors

## 0.0.16b

- Add generic type support for type mismatch error diagnostics
- Add INCLUDECG and INCLUDEHLSL support
- Add support for Grab Pass
- Add support for formatting to be able to place braces on new lines or not by setting `omnishader.formatting.braceOnNewLine` to true or false
- Fix bunch of document formatting bugs

## 0.0.15b

- Add type mismatch error diagnostics support for assignments, binary expressions and conditional blocks
- Improve error diagnostics for unresolved symbols
- Improve hover information for some types
- Fix bug that basic completion in free mode is not working in some scenarios
- Fix bug that no error dialog will show if activate license failed

## 0.0.13b

- Improve language server startup time

## 0.0.12b

- Add support for cbuffer or tbuffer statements
- Fix bug that variables in conditional block are not included in definitions
- Fix bug that variables declaration with default value are not included in definitions
- Serveral bug fixes that finding definitions of symbols are not correctly

## 0.0.11b

- Disable diagnostics by default, enable it by setting `omnishader.enableDiagnostics` to true


## 0.0.10b

- Add support for opening shader files outside a project, but intellisense is not fully supported due to lack of unity editor version information
- Add support for `#include_with_pragmas` directive of Unity
- Add diagnostics support for include errors, undefined symbols errors, syntax errors and missing symbols errors
- Improve workspace searching algorithms

## 0.0.8b

- Improve include file searching algorithms
- Fix bug that lower case 'pass' will break code formatting
- Fix bug that remove all contents of a shader will break intellisense

## 0.0.7b

- License checking supports offline now
- Fix bug that code completion in string and comments provide incorrect results
- Fix bug that backend language server stops working when provided incorrect path to backend language server
- Fix bug that code formatting will be broken in some scenario when fixed function in Pass 


## 0.0.6b

- Add fallback syntax support for shaderlab
- Improve include file search algorithms for better performance and stability
- Fix bug that comments at the beginning of shader will break parsing
- Fix bug that inline functions are parsing incorrectly
- Fix bug that uniform variables are sometimes parsing incorrectly

## 0.0.5b

- Update metadata

## 0.0.4b

- Add command "Omni Shader: Open Web Site"
- Fix binary expression formatting bug
- Fix number literal formatting bug

## 0.0.3b

- Improve hover information on functions 
- Downgrade VSCode version requirement to 1.95.0+

## 0.0.1b

- First beta release
