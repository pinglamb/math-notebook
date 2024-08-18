# \[Proof] Infinitely Many Primes

_**Prove there are infinitely many primes.**_

Assume there are finite number of primes, namely $$p_1, p_2, p_3, ..., p_n$$. Consider the number $$m = p_1p_2p_3...p_n + 1$$, if $$m$$ is divisible by any of the known primes, meaning $$p_i \space | \space m$$, as $$p_i \space | \space p_1p_2p_3...p_n$$, $$p_i \space | \space 1$$, which is impossible. Hence, $$m$$ has a new prime factor not listed above and it means there are infinitely many primes.



_**Prove there are infinitely many primes of form**_ $$4n+3$$_**.**_

Assume there are finite number of primes of the form $$4n+3$$, namely $$p_1, p_2, p_3, ..., p_k$$. Consider the number $$m = 4p_1p_2p_3...p_k - 1$$, we can see that $$m$$ itself is of the form $$4n+3$$. If $$m$$ is prime, as $$m$$ is not any of the number listed above, $$m$$ is a new prime of the form $$4n+3$$. Suppose $$m$$ is not a prime, as the product $$(4a + 1)(4b + 1) = 4(4ab + a + b) + 1$$ is again of the form $$4n + 1$$, $$m$$ must have a prime factor $$d$$ of the form $$4n + 3$$. If $$d$$ is one of the primes $$p_i$$ listed above, as $$p_i \space | \space m - 4p_1p_2p_3...p_n$$, $$p_i \space | \space -1$$, which is impossible. Hence, $$d$$ is a new prime not listed above of the form $$4n + 3$$ and it means there are infinitely many primes of such form.



_**Prove there are infinitely many primes of form**_ $$4n+1$$_**.**_

We cannot use $$m = 4p_1p_2p_3...p_n + 1$$ as it is possible that all prime factors of $$m$$ are of the form $$4n + 3$$. In order to prove that, we have to first prove $$n^2 + 1$$ must contain at least one prime factor of the form $$4n + 1$$.
