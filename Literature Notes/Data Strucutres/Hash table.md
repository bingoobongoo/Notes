A **Hash table (HT)** is a [[Data Structures|data structure]] that provides a mapping from keys to values using a technique called **hashing**.  

![[Pasted image 20230723134140.png]]

We refer to these as **key-value pairs**. Keys must be unique.

Hash tables are often used to track item frequencies. For instance, counting the number of times a word appears in a given text.

## Hash function

A **hash function** $H(x)$ is a function that maps a key $x$ to a whole number in a fixed range. For example, $H(x) = (x^2 - 6x + 9)\mod10$ maps all integer keys to the range $<0,9>$:

$H(4)=(16-24+9)\mod10=1$
$H(-7)=(49+42+9)\mod10=0$

We can also define hash functions for arbitrary objects such as string, lists, tuples, multi data objects, etc...
For  a string $s$ let $H(s)$ be a hash function defined below where $ASCII(x)$ returns the ASCII value of the character $x$:

```
H(s):
sum := 0
for char in s:
	sum = sum + ASCII(char)
return sum%50
```

### Properties of Hash funtions

If $H(x)=H(y)$ then $x$ and $y$ **might be equal**, but if $H(x)\neq H(y)$ then $x$ and $y$ are **certainly not equal**. This property can be used to dramatically speed up comparisons of big objects. That's because instead of comparing large files manually, we can use their hash values first to determine is it worthwhile to compare them. When hash values aren't equal, then they can't be the same.


> [!NOTE] Checksums
> Hahs functions for files are more sophisticated than these used for hashtables. Instead for files we use what are called **cryptographic hash functions** also called **checksums**.

A hash function $H(x)$ must be **deterministic**. 
This means that if $H(x)=y$ then $H(x)$ must always produce $y$ and never another value. This may seem obvious, but it is critical to the functionality of a hash function.

We try very hard to make **uniform** hash functions to minimize the number of hash collisions. A **hash collision** is when two objects $x$, $y$ hash to the same value.

### Hashable type

The keys used in hash table must be immutable data types, so that if a key of type $T$ is immutable and we have a hash function $H(k)$ defined for all keys $k$ of type $T$ then we say a key of type T is **hashable**.

## Hash table lookup

When we want to retrive information from hash table fast, we can use hash function to speed up this process. We simply use hash function $H(x)$ where $x$ is a key of a value in hashtable. By hashing key, we receive another integer which will be index. 
Then if we want to find what is the index of key $k$, we just compute $H(k)$.

### Hash table collisions

If there is a **hash collision** we cannot assign a key to specific index beacause it is already taken. In that situation we use one of many hash collisions techniques to handle this. The two most popular ones are **[[#Separate chaining|separate chaining]]** and **[[#Open addressing|open addressing]]**.

#### Separate chaining

It deals with hash collisions by maintaining a data structure (usually a [[Linked Lists|linked list]]) to hold all the different values which hashed to a particular value. 

![[Pasted image 20230723151251.png]]


> [!NOTE] Note
> The data structure used to cache the items which hashed to a particular value is not limited to a linked list. Some implementations use on or a mixture of: [[Arrays|arrays]], [[Binary Tree|binary trees]], etc...


#### Open addressing

It deals with hash collisions by finding another place within the hash table for the object ot go by offsetting it from the position to which it hashed to.

If the position our key hashed to is occupied we try another position in the hash table by offsetting the current position subject to a **probing sequence $P(x)$**. We keep doing this until an unoccupied slot is found. 

There are an infinite amount of probing sequences you can come up with, here are a few:
* Linear probing
$$P(x) = ax+b$$
- Quadratic probing
$$P(x)=ax^2+bx+c$$
- Double hashing
$$P(k,x)=x*H_2(k)$$
- Pseudo RNG
$$P(k,x)=x*RNG(H(k),x)$$
When using open addressing the **key-value pairs are stored in the table (array) itself** as opposed to a data structure like in separate chaining.
This means we need to care a great deal about the size of our hash table and how many elements are currently in th table.

### [[Big-O Notation|Complexity]]

| Operation | Average | Worst |
| --- | --- | --- |
| Insertion | $O(1)$ | $O(n)$ |
| Removal | $O(1)$ | $O(n)$ |
| Search | $O(1)$ | $O(n)$ |


> [!NOTE] Constant time behaviour
> The constant time behaviour attributed to hash tables is only true if you have a good **uniform hash funtion**.


