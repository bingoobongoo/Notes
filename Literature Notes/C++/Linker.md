Linking is a post-compiling stage in C++, when the declarations in our translation-units are matched (linked) with their definitions. For example, declarations in [[header files]] are linked with their definitions in [[Libraries#.cpp files|.cpp]] files. 

## Linker Settings
The linker also exposes a number of options. You can control what type of
output file to produce—an executable or a [[Libraries#.dll files|DLL]]. You can also specify which
external [[libraries]] should be linked into your executable, and which directory
paths to search in order to find them. A common practice is to link with [[Compiler#Debug|debug]] libraries when building a debug executable and with optimize libraries when building in [[Compiler#Release|release]] mode.