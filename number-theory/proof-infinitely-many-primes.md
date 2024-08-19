# \[Proof] Infinitely Many Primes

_**Prove there are infinitely many primes.**_

Assume there are finite number of primes, namely $$p_1, p_2, p_3, ..., p_n$$. Consider the number $$m = p_1p_2p_3...p_n + 1$$, if $$m$$ is divisible by any of the known primes, meaning $$p_i \space | \space m$$, as $$p_i \space | \space p_1p_2p_3...p_n$$, $$p_i \space | \space 1$$, which is impossible. Hence, $$m$$ has a new prime factor not listed above which implies there are infinitely many primes.



_**Prove there are infinitely many primes of the form**_ $$4n+3$$_**.**_

Assume there are finite number of primes of the form $$4n+3$$, namely $$p_1, p_2, p_3, ..., p_k$$. Consider the number $$m = 4p_1p_2p_3...p_k - 1$$, we can see that $$m$$ itself is of the form $$4n+3$$. If $$m$$ is prime, as $$m$$ is not any of the number listed above, $$m$$ is a new prime of the form $$4n+3$$. Suppose $$m$$ is not prime, as the product of $$(4a + 1)(4b + 1) = 4(4ab + a + b) + 1$$ is always of the form $$4n + 1$$, $$m$$ must have a prime factor $$d$$ of the form $$4n + 3$$. If $$d$$ is one of the primes $$p_i$$ listed above, as $$d \space | \space m - 4p_1p_2p_3...p_n$$, $$d \space | \space -1$$ which is impossible. Hence, $$d$$ is a new prime of the form $$4n + 3$$ not listed above which implies there are infinitely many primes of the form $$4n + 3$$.



_**Prove there are infinitely many primes of the form**_ $$4n+1$$_**.**_

We cannot use $$m = 4p_1p_2p_3...p_n + 1$$ as it is possible that all prime factors of $$m$$ are of the form $$4n + 3$$. In order to prove that, we have to first prove prime factors of $$n^2 + 1$$ must be either $$2$$ or of the form $$4n + 1$$.

Suppose $$p$$ is a prime factor of $$n^2 + 1$$, we can see that $$p$$ can be $$2$$. Assume $$p$$ is odd, as $$n^2 \equiv -1 \space (mod \space p)$$, $$n^4 \equiv 1 \space (mod \space p)$$. As there is no $$k < 4$$ such that $$n^k \equiv 1 \space (mod \space p)$$, $$ord_p(n) = 4$$. On the other hand, by Fermat's Little Theorem, $$n^{p-1} \equiv 1 \space (mod \space p)$$. It implies that $$ord_p(n) \space | \space p - 1$$, hence $$4 \space | \space p - 1$$. In conclusion, if $$p$$ is a prime factor of $$n^2 + 1$$, $$p = 2$$ or of the form $$4m + 1$$.

Assume there are finite number of primes of the form $$4n + 1$$, namely $$p_1, p_2, p_3, ..., p_k$$. Consider the number $$m = (2p_1p_2p_3...p_k)^2 + 1$$, we can see that $$m$$ itself is of the form $$4n + 1$$. If $$m$$ is a prime, as $$m$$ is not any of the number listed above, $$m$$ is a new prime of the form $$4n + 1$$. Suppose $$m$$ has a prime factor $$d$$, from the above, as $$d \ne 2$$, $$d$$ must be of the form $$4n + 1$$. If $$d$$ is one of the primes $$p_i$$ listed above, as $$p_i \space | \space m - (2p_1p_2p_3...p_k)^2$$, $$d \space | \space 1$$ which is impossible. Hence, $$d$$ is a new prime of the form $$4n + 1$$ not listed above which implies there are infinitely many primes of the form $$4n + 1$$.

* [https://youtu.be/E1tikA1GEVU?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=2117](https://youtu.be/E1tikA1GEVU?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=2117)
