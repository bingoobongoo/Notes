In programming, memory is undoubtedly the most vital part of everything computer does. We can imagine computer memory as a long, one-dimensional line (or street) with houses alongside. Each house is like 1 byte od data and every house has its own unique address.

> [!NOTE] REMEMBER
> Pointer is just an integer that holds memory address. 

## Ampersands
An ampersand sign used as below stands for retriving memory address of a variable. It can be then assigned to another pointer variable.

```C++
int var = 8;
void* ptr = &var; // assigning address of var to our pointer
```

## Dereferencing a pointer
When we want to acces a data the pointer points to, we can ***dereference*** that pointer and changing the value it points to like this:

```C++
int var = 8;
int* ptr = &var;
*ptr = 2; // dereferencing ptr pointer and changing value
```


> [!NOTE] Pointer Type
> Note that when we want to dereference our pointer we need to make sure that our pointer has a proper type. If we wanted to assing integer to the value the pointer points to, we would need to make sure our pointer is of type *int*.


