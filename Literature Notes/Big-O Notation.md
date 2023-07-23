It is a mathematical notation that gives answer to how much time and space does [[Algorithms|algorithm]] need to do it's job in the **worst** case, helping to quantify performance as the input size gets **arbitrarily large**.

### Common classes of Big-O function

| Notation | Name | 
| --- | --- |
| *O* ($1$) | constant |
| *O* ($\log n$) | logarithmic |
| *O* ($n^c$) | fractional power[^1]|
| *O* ($n$) | linear |
|*O* ($n\log n$) | linearithmic |
|*O* ($n^c$) | polynomial[^2] |
|*O* ($c^n)$ | exponential[^3] |
|*O* ($n!$) | factorial |

![[Pasted image 20230621232430.png]]
### Big-O Properties
*O* ($n+c$) = *O* ($n$)
*O* ($cn$) = *O* ($n$)

Let $f(n)$ be a fucntion that describes a running time for a particular algorithm for an input size $n$ :
$$f(n) = 7\log n + 15n^2 + 2n^3 +8$$
Then:
$$O(f(n)) = O(n^3)$$

[^1]: $c \in (0,1)$
[^2]: $c \in (1, \infty)$
[^3]: $c \in (1, \infty)$

