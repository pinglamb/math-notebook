# \[Proof] Sum of Phi of all divisors = n

_Proof of_ $$\sum_{d | n}\varphi(d) = n$$

Consider splitting the integers from $$1$$ to $$n$$ into classes such that $$m \in C_d$$ if $$(m, n) = d$$. We can see that every integer is in a unique class as $$(m, n)$$ must be equal to one and only one of the divisors of $$n$$, so $$\sum_{d|n}|C_d| = n$$.

For a specific class $$C_d$$, as $$(m, n) = d \iff (m/d, n/d) = 1$$, it means that the integers in $$C_d$$ are those integers that is co-prime to $$n/d$$ multiply by $$d$$ (e.g. when $$n = 18$$, $$C_3 = \set{3, 15} = \set{3 \times 1, 3 \times 5}$$, with $$\set{1, 5}$$ are the integers co-prime to $$6$$). Therefore, $$|C_d| = \varphi(n / d)$$. Hence, $$\sum_{d|n}|C_d| = \sum_{d|n}\varphi(n/d) = \sum_{d|n}\varphi(d) = n$$.

In other words, the summatory function of $$\varphi(n)$$ is the identity function.

* [https://youtu.be/8I0z\_Lobtso?t=2638](https://youtu.be/8I0z\_Lobtso?t=2638)
* Kenneth H Rosen _Elementary Number Theory_, 2011 - Theorem 7.7 (P244)

