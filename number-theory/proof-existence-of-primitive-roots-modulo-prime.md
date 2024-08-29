# \[Proof] Existence of Primitive Roots modulo Prime

Let $$p$$ be a prime, the idea for proving the existence of primitive roots modulo $$p$$ is by showing if $$d$$ is a divisor of $$p - 1$$, then there are exactly $$\varphi(d)$$ integers of order $$d$$ modulo $$p$$.

We first show that there are either no or exactly $$\varphi(d)$$ integers of order $$d$$ modulo $$p$$. There is nothing to prove if there is no integers with order $$d$$ modulo $$p$$, so assume there is an integer $$a$$ with $$ord(a) = d$$. Consider the polynomial $$x^d - 1$$, it has exactly $$d$$ incongruent roots modulo $$p$$ [\[Proof\]](proof-lagranges-theorem.md), which are $$a, a^2, a^3, ..., a^d$$. It means these are the only possible integers with order $$d$$ modulo $$p$$. However, as $$ord(a^u) = d / (d, u)$$ [\[Proof\]](proof-order-of-powers-of-a-modulo-m.md), only those integers $$a^u$$ with $$(u, d) = 1$$ has order $$d$$ modulo $$p$$, and there are exactly $$\varphi(d)$$ integers like that among them. Hence, there are either no integers of order $$d$$ modulo $$p$$, or if we found one, we can derive the others and there are in total $$\varphi(d)$$ of them.

Furthermore, there are in total $$p - 1$$ integers less than $$p$$ and by Fermat's Theorem, their orders modulo $$p$$ must be a divisor of $$p - 1$$. Let $$F(d)$$ be the number of integers with order $$d$$ modulo $$p$$, $$\sum_{d | p - 1}F(d) = p - 1$$. As shown above, $$F(d) = 0$$ or $$F(d) = \varphi(d)$$, but we also have $$\sum_{d | p - 1} \varphi(d) = p - 1$$ [\[Proof\]](proof-sum-of-phi-of-all-divisors-n.md). It means $$F(d)$$ can't be $$0$$ for any $$d$$ as the sum of all $$\varphi(d)$$ can almost be $$p - 1$$, hence $$F(d) = \varphi(d)$$.

Therefore, we can conclude that there are exactly $$\varphi(p - 1)$$ integers with order $$p - 1$$, i.e. primitive roots, modulo $$p$$, and hence every prime has a primtive root.

* [https://youtu.be/E8UTP0DiCCg?t=1172](https://youtu.be/E8UTP0DiCCg?t=1172)
* Kenneth H Rosen _Elementary Number Theory_, 2011 - Section 9.2 (P354)
