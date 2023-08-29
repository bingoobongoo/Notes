Library in C++ can be expressed as compressed code with additional functionalities ([[Data Structures|data structures]], data types, functions etc.) that we can add to our project and use as we want.  There are static and dynamic libraries.

## .lib files
It's a file extension that basically means everything in that file creates static library that can be used by our program.

## .dll files
This file extension means *Dynamic Linked Library*. It is a dynamic version of .lib file.

## .cpp files
This file extension basically tells C++ [[Compiler|compiler]] , that this file can be translated into machine code, which is then used by the [[Linker|linker]] in order to create C++ program. It is essential part of  .lib files.

## .h files
Another file extension used for [[Header Files|header files]]. These files are usually inside *include* directory and contain declarations of classes and functions inside our .lib file.

## How a static library work?
A static library is compiled with our source code before the program even runs. Everything is checked in terms of proper syntax and linking and only after the program is executed.

## How a dynamic library work?
A dynamic library is used by our program in runtime, so it's not added at the very beginning of compilation and linking. Our program just dynamically uses it whenever it needs some functionalities. It is somewhat less efficient than static library.

## How to use static library in a project?
To use static library in a project we need to ensure that:
- Our [[compiler]] knows where to find library's include folder so that we can use *#include* directive in our project's source code. 
- Our [[linker]] knows the location of the folder that contains our .lib files, so that in the linking process it can link declarations in .h files with definitions in .cpp files (which in this case are in .lib file).
- We need to specifically type in the names of library and header file we want to use in our program in compiler and linker settings.
After these steps, we can freely create our project using functionalities of external static libraries.

## How to use dynamic library in a project?
To use dynamic library in a project we need to ensure similar steps as with static library. We need to specify paths to any .lib files that is binded with .dll file if any exist. We need to specify names, but we also need to move our main .dll file to the folfer with our main executable file.