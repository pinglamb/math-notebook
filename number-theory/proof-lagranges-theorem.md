# \[Proof] Lagrange's Theorem

_Let_ $$f(x) = a_nx^n + a_{n-1}x^{n-1} + ... + a_1x + a_0$$ _be a polynomial of degree_ $$n \ge 1$$_, with integer coefficients and with leading coefficient_ $$a_n$$ _not divisible by_ $$p$$_, where_ $$p$$ _is a prime. Then_ $$f(x)$$ _has at most_ $$n$$ _incongruent roots modulo_ $$p$$_._

When $$n = 1$$, $$f(x) = a_1x + a_0$$. As $$(a_1, p) = 1$$, The inverse of $$a_1$$ modulo $$p$$ exists and hence the polynomial has exactly one root modulo $$p$$, namely $$x \equiv -a_0 \overline{a_1} \space (mod \space p)$$.

Assume it is true for $$n = k$$, meaning $$f(x) = a_kx^k + a_{k-1}x^{k-1} + ... + a_1x + a_0$$ has at most $$k$$ incongruent roots modulo $$p$$. When $$n = k + 1$$, assume it has $$k + 2$$ incongruent roots, namely $$r_0, r_1, ... ,r_k, r_{k+1}$$. As $$r_0$$ is a root, we can write $$f(x) = (x - r_0)g(x)$$, where $$g(x)$$ is a polynomial of degree $$k$$. By substituding the remaining $$k + 1$$ roots to $$f(x)$$, as $$r_i - r_0 \not \equiv 0 \space (mod \space p)$$, we can see that $$g(r_i) \equiv 0 \space (mod \space p)$$, hence $$g(x)$$ has $$k + 1$$ incongruent roots modulo $$p$$ which contradicts with the assumption. Therefore, we can conclude that polynomial $$f(x)$$ with degree $$n$$ has at most $$n$$ incongruent roots modulo $$p$$.

It is analogy to the Fundamental Theorem of Algebra stating polynomial $$f(x)$$ with degree $$n$$ has $$n$$ roots, counted with multiplicity. It only works for the case modulo a prime because of the existence of zero divisors modulo a composite number, for example, $$2 \cdot 3 \equiv 0 \space (mod \space 6)$$ but $$2 \not \equiv 0 \space (mod \space 6)$$ and $$3 \not \equiv 0 \space (mod \space 6)$$. Hence, for the step $$f(x) = (x - r_0)g(x) \equiv 0 \space (mod \space m)$$ doesn't imply $$(x - r_0) \equiv 0 \space (mod \space m)$$ or $$g(x) \equiv 0 \space (mod \space m)$$.



Let $$p$$ be a prime and let $$d$$ be a divisor of $$p - 1$$. Then the polynomial $$x^d -1$$ has exactly $$d$$ incongruent roots modulo $$p$$.

Let $$p - 1 = de$$, $$x^{p-1} - 1 = (x^d - 1)(x^{d(e - 1)} + x^{d(e - 2) }+ ... + x^d + 1) = (x^d - 1)g(x)$$. By Fermat's Theorem, $$x^{p-1} - 1$$ has exactly $$p - 1$$ incongruent roots, which are $$1, 2, ..., p - 1$$. By Lagrange's Theorem, $$g(x)$$ has at most $$d(e - 1)$$ incongruent roots. As roots of $$x^{p-1} - 1$$ are roots of either $$x^d - 1$$ or $$g(x)$$, there are at least $$p - 1 - d(e - 1) = d$$ incongruent roots for $$x^d - 1$$. On the other hand, $$x^d - 1$$ has at most $$d$$ incongruent roots by Lagrange's Theorem, hence $$x^d - 1$$ has exactly $$d$$ incongruent roots modulo $$p$$.

* [https://youtu.be/E-6llnLZ7J8?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=328](https://youtu.be/E-6llnLZ7J8?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=328)
* Kenneth H Rosen _Elementary Number Theory_, 2011 - Theorem 9.6, 9.7 (P355)
