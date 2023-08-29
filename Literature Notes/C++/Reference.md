Reference in C++ is somewhat like [[Pointers|pointer]]. It's not really a variable, becuase it is just a reference to another actual variable. So it is existing in our code like it was a variable, but it really is not. It's an alias of another variable.

```C++
int a = 5;
int& ref = a; // declaration of a reference
```

We can easily change value of a simply by changing value of a reference. That way we don't need to access ***a*** variable directly, but instead we accessing reference.

```C++
ref = 2; // the same as: a = 2;
```

## Passing reference to a function
When we normally pass arguments to fucntions, they are being copied underhood, which we don't want most of the time. We can instead pass a reference to our variable as a function argument or we can pass a memory address of our variable which will be then used.

```C++
void increment(int* value) { // passing pointer to function
	(*value)++;
}

void increment(int& value) { // passing reference
	value++;
}
```