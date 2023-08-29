In order to make our code nice and clean, we often use header files, which are essential in bigger projects. Header files are just files with declarations of functions, attributes and whole bunch of other stuff that we intend to use.

We only write declaration, because C++ [[linker]] need to know that something exists before it starts to link it with actual definition which is in [[Libraries#.cpp files|.cpp]] files. It might look something like that:

```C++
int multiply(int a, int b);
int add(int a, int b);
int divide(int a, int b);
```

Code above is just declarations of functions which we would write in header file. In .cpp file we would write definitions for our functions:

```C++
int multiply(int a, int b) {
	return a*b;
}
int add(int a, int b) {
	return a+b;
}
int divide(int a, int b) {
	if (b == 0) { throw -1;}
	return a/b;
}
```

## Using directives
Storing all those declarations in one place has additional benefit. We can use [[preprocessor]] directive *[[Preprocessor#* include*|##include]]* to neatly copy those declarations to our source code.