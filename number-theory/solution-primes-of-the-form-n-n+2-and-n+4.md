# \[Solution] Primes of the form n, n+2 and n+4

_\[Cambridge Math IA Example Sheet 1 Q1] The numbers 3, 5, 7 are all prime. Does it ever happen again that three numbers of the form_ $$n$$_,_ $$n + 2$$_,_ $$n + 4$$ _are all prime?_

By listing few examples, $$\{ 5, 7, 9 \}$$, $$\{ 17, 19, 21 \}$$, $$\{ 29, 31, 33 \}$$, we can see that each group of numbers will contain at least one number which is multiple of $$3$$, which shows that statement is probably not true.

Consider $$n = 3m$$ or $$n = 3m + 1$$ or $$n = 3m + 2$$.

When $$n = 3m$$, $$n$$ is prime only when $$n = 3$$, otherwise $$n$$ is a multiple of $$3$$ therefore not prime.

When $$n = 3m + 1$$, the next 2 numbers are $$3m + 3$$ and $$3m + 5$$, in which $$3m + 3$$ is a multiple of $$3$$ therefore not prime.

When $$n = 3m + 2$$, the next 2 numbers are $$3m + 4$$ and $$3m + 6$$, in which $$3m + 6$$ is a multiple of $$3$$ therefore not prime.

Hence, $$\{ 3, 5, 7 \}$$ are the only numbers of the form $$n$$, $$n + 2$$, $$n + 4$$ which are all prime.
