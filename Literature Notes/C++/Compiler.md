Compiler in C++ basically translates programming language in text files to machine code (.obj files), which is further used by [[linker]] to do operations. It checks syntax and make sure there are no errors in our code. But before program starts compiling, there is also time for a [[preprocessor]].

## Debug
A debug build is a very slow version of your program, with all
optimizations turned off, all function inlining disabled, and full debug-
ging information included. This build is used when testing brand new
code and also to debug all but the most trivial problems that arise during
development.

## Release
A release build is a faster version of your program, but with de-
bugging information and assertions still turned on. This allows you to see your game run-ning at a speed representative of the final product, but it still gives you some opportunity to debug problems.

## Production
A production configuration is intended for building the fi-
nal game that you will ship to your customers. It is sometimes called a
“Final” build or “Disk” build. Unlike a release build, all debugging in-
formation is stripped out of a production build, all assertions are usually
turned off, and optimizations are cranked all the way up. A production
build is very tricky to debug, but it is the fastest and leanest of all build
types.