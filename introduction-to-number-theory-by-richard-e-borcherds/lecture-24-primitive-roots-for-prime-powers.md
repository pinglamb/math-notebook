# Lecture 24 - Primitive Roots for Prime Powers

## Summary of Primitive Roots

The following statements are equivant:

* $$m$$ has primitive root
* $$m$$ has $$\varphi(\varphi(m))$$ primitive roots
* $$m = 1, 2, 4, p^n$$ and $$2p^n$$, where $$p$$ is an odd prime
* Only solutions to $$x^2 \equiv 1 \space (mod \space m)$$ are $$x \equiv \pm 1 \space (mod \space m)$$ [\[Proof\]](../number-theory/proof-gausss-generation-of-wilsons-theorem.md)
* Wilson's Theorem holds (except $$1, 2$$): $$\prod_{(a, m) = 1} a \equiv -1 \space (mod \space m)$$ [\[Proof\]](../number-theory/proof-gausss-generation-of-wilsons-theorem.md)

## Almost Primitive Root modulo Powers of 2

When $$n \ge 3$$, there are no primitive roots modulo $$2^n$$ [\[Proof\]](../number-theory/proof-no-primitive-roots-for-powers-of-2-except-2-and-4.md). For any integer $$a$$ relative prime to $$2^n$$, we have $$a^{\varphi(2^n)/2} = a^{2^{n-2}} \equiv 1 \space (mod \space 2^n)$$.

$$5$$ **is almost a primitive root modulo** $$2^n$$ because $$ord_{2^n}(5) = \varphi(2^n) / 2 = 2^{n-2}$$ for $$n \ge 3$$. As stated above, $$5^{2^{n-2}} \equiv 1 \space (mod \space 2^n)$$, we have to show that $$5^{2^{n - 3}} \equiv 1 + 2^{n-1} \not \equiv 1 \space (mod \space 2^n)$$ by Induction.

When $$n = 3$$, $$5 \equiv 1 + 4 \space (mod \space 8)$$. Assume $$n = k$$ is true, $$5^{2^{k-3}} \equiv 1 + 2^{k-1} \space (mod \space 2^k)$$, it implies $$5^{2^{k-3}} = 1 + 2^{k-1} + t2^k$$. By squaring both sides, we have

$$
\begin{aligned} 5^{2^{k-2}} &= (1 + 2^{k-1})^2 + t(1 + 2^{k-1})(2^{k+1}) + (t2^k)^2 \\ &\equiv (1 + 2^{k-1})^2 \enspace (mod \space 2^{k+1}) \\ &\equiv 1 + 2^k \enspace (mod \space 2^{k+1})  \end{aligned}
$$

Hence, by induction, $$5^{2^{n - 3}} \equiv 1 + 2^{n-1} \not \equiv 1 \space (mod \space 2^n)$$, and $$ord_{2^n}(5) = 2^{n-2}$$.

Similar to a primitive root, we can represent all integers less than $$2^n$$ that are relatively prime to $$2^n$$ by $$\pm 5^k$$, with half of them which are of the form $$4n + 1$$ being $$5^k$$ and the remaining half which are of the form $$4n - 1$$ being $$-5^k$$.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Theorem 9.12 (P364)

## Discrete Logarithms

Let $$g$$ be a primitive root of $$m$$, as the integers $$g^1, g^2, ..., g^{\varphi(m)}$$ form a reduced residue system modulo $$m$$ [\[Proof\]](../number-theory/proof-powers-of-primitive-root-form-a-reduced-residue-system.md), there is an unique integer $$x$$ with $$1 \le x \le \varphi(m)$$ such that $$g^x \equiv a \space (mod \space m)$$ for all integers $$a$$ relative prime to $$m$$. Hence, we can define discrete logarithm by having $$x = ind_g(a)$$, with $$x$$ called the **index (or discrete logarithm) of** $$a$$ **to be base** $$g$$ **modulo** $$m$$.

Indices share many properties of logarithms, but with equalities replaced by congruences modulo $$\varphi(m)$$, for example, we have $$ind_g(ab) \equiv ind_g(a) + ind_g(b) \space (mod \space \varphi(m))$$.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Section 9.4 (P368)

## Primality Test base on Primitive Root

It is known that the converse of Fermat's Theorem is not true, meaning even if $$a^{m-1} \equiv 1 \space (mod \space m)$$, $$m$$ may still be composite. Composite numbers with such property are called _pseudoprimes_.

However, if there is an integer with order $$m - 1$$ modulo $$m$$, meaning the existence of primitive root $$g$$ modulo $$m$$, with $$ord_m(g) = m - 1$$, then $$m$$ is a prime. We can do such test if we know all the prime factors of $$m - 1$$, by checking if $$g^{(m - 1)/p_i} \not \equiv 1 \space (mod \space m)$$ for all prime divisors of $$m - 1$$. It is called the **Lucas's Converse of Fermat's Little Theorem**. [\[Proof\]](../number-theory/proof-lucass-converse-of-fermats-little-theorem.md)

This method seems to be not so efficient as it requires the factorization of $$m - 1$$, which can be a time-consuming task.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Section 9.5 (P378)

## References

* [https://youtu.be/AfRpXi8r0So](https://youtu.be/AfRpXi8r0So)
