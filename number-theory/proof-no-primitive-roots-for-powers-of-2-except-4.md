# \[Proof] No Primitive Roots for Powers of 2 except 4

_Proof of no primitive roots modulo_ $$2^n$$_, with_ $$n \ge 3$$_._

We have to show that for all odd integers $$a$$, its order modulo $$2^n$$ is at most $$\varphi(2^n) / 2 = 2^{n-2}$$ and hence they are not primitive roots modulo $$2^n$$. It means we have to prove $$a^{2^{n-2}} \equiv 1 \space (mod \space 2^n)$$.

When $$n = 3$$, $$1^2 \equiv 3^2 \equiv 5^2 \equiv 7^2 \equiv 1 \space (mod \space 2^3)$$, hence $$a^2 \equiv 1 \space (mod \space 2^3)$$.

Assume it is true for $$n = k$$, $$a^{2^{k-2}} \equiv 1 \space (mod \space 2^k)$$, it implies $$a^{2^{k-2}} \equiv 1 + t(2^k) \space (mod \space 2^{k+1})$$, and

$$
\begin{aligned} a^{2^{k-1}} &= (1 + t2^k)^2 \\ &= 1 + t(2^{k+1}) + t^2(2^{2k}) \\ &\equiv 1 \enspace (mod \space 2^{k+1}) \end{aligned}
$$

By Induction, $$a^{2^{n-2}} \equiv 1 \space (mod \space 2^n)$$, meaning the order of all odd integers $$a$$ modulo $$2^n$$ is at most $$\varphi(2^n)$$/2 and hence there are no primitive roots.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Theorem 9.11 (P364)
