Preprocessing is a pre-compilation process, that checks for any C++ directives in source code (for example: *#include*, *#define*, *#ifdef*, etc.) and executes them. It is a very handy solution for configuration of our project from the level of code. 

## *#include*
This directive basically searches for file with name we provide and pastes its content to the file we are working on. We as a programmers can only see one line, but in reality this line is being substituted with actual code from another file in pre-compilation stage.

## *#define*
This directive takes two arguments. First one will be substituted with the second one in every place it is written in our code. So preprocessor searches for first argument in our code and chenges it to the second one defined by us before compilation.

## Preprocessor uses
Preprocessor can be used to save us a lot of time. We can mark some parts of our code to be run only when specific conditions are met. We can include thousands of lines of code with a simple directive. We can define our own variable names. We also can run specific parts of our codes in different builds (see [[compiler]]). The possibilities are plentiful.