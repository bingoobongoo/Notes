***Const*** keyword in C++ is basically a promise that we, programmers, will not modify const variable in the future. It also improves security of our code, because trying to modify const variables will trigger warnings and errors. That doesn't mean that we cannot modify const variable. We can just as we can break our promise.

## Const [[pointers]]
Const pointer is specific type of a pointer, where the value the pointers point to cannot be changed directly, but the pointer intself can be freely changed to another place in memory.

```C++
const int* a = new int;
int variable = 2;
*a = variable; // error: cannot change const int pointer value
a = &variable; // valid operation
std::cout << *a; // *a = 2
```

However, when we swap *const* with *int* like this:

```C++
int* const a = new int;
int variable = 2;
*a = variable; // valid operation
a = &variable; // error: cannot change address of a pointer
```

we simply cannot change adress of a pointer, but can change value it points to. 

There is also last way we can write const pointer:

```C++
const int* const a = new int;
int variable = 2;
*a = variable; // error: cannot change const int pointer value
a = &variable; // error: cannot change address of a pointer
```

in which we simply cannot change neither the address nor the value pointer points to.

## Const in a class
The third way we can use ***const*** is in a class. When we use it after method declaration, we simply say that this method (const method) cannot modify any members of the class it belongs to.

```C++
class Entity {
private:
	int _x;
	int _y;
	const int* const variable;
public:
	// this method doesn't modify any class members, valid
	int get_x() const { return _x; } 
	// error: this method modifies _x class member
	int set_x(int value) const { _x = value; }
	// silly but valid method, it returns int pointer that has fixed address and a fixed value, and this method cannot modify any Entity class members, which it doesn't in this case
	const int* const foo() const { return variable; }
};
```

## Mutable keyword in C++
In case we want to modify a class variable by the const method, we nned to add ***mutable*** keyword before that specific variable, so that const methods can modify it even though, they are const methods and they cannot modify any class members (but again, mutable class member is an exception).