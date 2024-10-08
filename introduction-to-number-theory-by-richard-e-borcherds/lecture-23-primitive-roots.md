# Lecture 23 - Primitive Roots

## Definition of Primitive Roots

**\[Definition of** $$ord_m(a)$$**].** Let $$a$$ and $$m$$ be integers with $$a \not = 0$$, $$m > 0$$ and $$(a, m) = 1$$, the order of $$a$$ modulo $$m$$, is **the least positive integer** $$n$$ **such that** $$a^n \equiv 1 \space (mod \space m)$$. (by Gauss)

Let $$x$$ be an positive integer, then $$a^x \equiv 1 \space (mod \space m)$$ if and only if $$ord(a) \space | \space x$$. The proof is as follows. Assume $$ord(a) \space | \space x$$, meaning $$x = ord(a) \cdot k$$, it follows $$a^x = a^{ord(a)k} \equiv (1)^k \equiv 1 \space (mod \space m)$$. Assume $$a^x \equiv 1 \space (mod \space m)$$, by division algorithm we have $$x = ord(a) \cdot k + r$$, with $$0 \le r < ord(a)$$, it follows $$a^x = a^{ord(a)k + r} = a^{ord(a)k} \cdot a^r \equiv a^r \equiv 1\space (mod \space m)$$. As $$ord(a)$$ is the least positive integer such that $$a^n \equiv 1 \space (mod \space m)$$, we conclude that $$r = 0$$, and hence $$x = ord(a) \cdot k$$ and $$ord(a) \space | \space x$$.

By Euler's Theorem, we have $$a^{\varphi(m)} \equiv 1 \space (mod \space m)$$. Combine with the above theorem, we have $$ord(a) \space | \space \varphi(m)$$. $$a$$ **is called a primitive root of** $$m$$ **if** $$ord(a) = \varphi(m)$$**.**

## Powers of Primitive Roots

The primitive root $$g$$ of $$m$$ also has the property that **the integers** $$g^1, g^2, ... g^{\varphi(m)}$$ **form a reduced residue system module** $$m$$, meaning it will loop through all the positive integers co-prime to $$m$$ that are less than $$m$$ [\[Proof\]](../number-theory/proof-powers-of-primitive-root-form-a-reduced-residue-system.md).

Conversely, assume the powers of an integer $$g$$ are all relatively prime to $$m$$ and no two of them are congruent modulo $$m$$, $$g^k \equiv 1 \space (mod \space m)$$ for exactly one $$k$$ with $$1 \le k \le \varphi(m)$$, it follows $$ord(g) = k$$. Consider the integers $$g^1$$ and $$g^{k+1}$$, $$g^1 \equiv g^{k+1} \space (mod \space m)$$ because $$1 \equiv k+1 \space (mod \space ord(g))$$. If $$k < \varphi(m)$$, $$1 < k + 1 \le \varphi(m)$$, it follows $$g^{k+1}$$ is one of the integer relatively prime to $$m$$ which is congruent to $$g^1$$ modulo $$m$$, which contradicts with the assumption. Hence, $$ord(g) = \varphi(m)$$ and $$g$$ is primitive root of $$m$$.

## Existence of Primitive Roots

There are few properties about existence of primitive roots emerged while finding the primitive root of various integers.

The first integer having no primitive root is $$8$$. The obstruction is that $$x^2 \equiv 1 \space (mod \space 8)$$ has 4 distinct solutions. If $$m$$ has a primitive root $$g$$, the only solutions to $$x^2 \equiv 1 \space (mod \space m)$$ should be $$g^{\varphi(m)} \equiv 1$$ and $$g^{\varphi(m) / 2} \equiv -1$$. It turns out there are no primtive roots modulo $$2^n$$ for $$n > 2$$ [\[Proof\]](../number-theory/proof-no-primitive-roots-for-powers-of-2-except-2-and-4.md).

While finding the primitive root of $$9 = 3^2$$, which can be $$1, 2, 4, 5, 7, 8$$. As a primitive root of $$9$$ is also a primitive of $$3$$ [\[Proof\]](../number-theory/proof-primitive-root-of-prime-powers-is-also-primitive-root-of-the-prime.md), we only need to check $$2, 5, 8$$. In general, if we know $$g$$ is a primitive root of $$p$$, we only need to check $$g + tp$$ for $$p^2$$ (turns out that **if** $$p$$ **is odd prime and** $$g$$ **is a primitive root modulo** $$p$$**, either** $$g$$ **or** $$g+p$$ **is the primitive root modulo** $$p^2$$ **and if** $$g'$$ **is a primitive root modulo** $$p^2$$**,** $$g'$$ **is a primitive root modulo** $$p^n$$ **for all positive integers** $$n$$ [\[Proof\]](../number-theory/proof-existence-of-primitive-root-modulo-powers-of-odd-prime-or-twice-that.md)).

For the case of $$10 = 2 \cdot 5$$, there is a 1-to-1 mapping between the reduced residue classes modulo $$10$$ and that modulo $$5$$. If $$p$$ is odd prime and $$g$$ is a primitive root modulo $$p$$, either $$g$$ or $$g + p$$, whichever is odd, is a primitive root of $$2p$$. It is further extended to **integers in the form** $$2p^n$$ **with primitive root being** $$g$$ **or** $$g + p^n$$**, whichever is odd** [\[Proof\]](../number-theory/proof-existence-of-primitive-root-modulo-powers-of-odd-prime-or-twice-that.md).

For the case of $$11$$ and $$13$$, let $$p$$ is an odd prime, by Fermat's Theorem, $$ord_p(a) \space | \space p - 1$$. Therefore, by counting the number of integers with order $$d$$ modulo $$p$$, for each divisor $$d$$ of $$p-1$$, we can have an idea about if there are integers relatively prime to $$p$$ with order $$p - 1$$. It turns out this method can be used to prove that **there are exactly** $$\varphi(d)$$ **integers of order** $$d$$ **modulo** $$p$$**, hence there are** $$\varphi(\varphi(p))$$ **primitive roots modulo** $$p$$**, which implies every odd prime has primitive root** [\[Proof\]](../number-theory/proof-existence-of-primitive-roots-modulo-prime.md).

For the case of $$12 = 4 \cdot 3$$ and $$15 = 3 \cdot 5$$, we can see that by Chinese Remainder Theorem, the congruence $$x^2 \equiv 1 \space (mod \space 12)$$ has $$2 \cdot 2 = 4$$ solutions, which has a similar obstruction as $$8$$. Hence, they don't have primitive roots. It can be shown that $$m$$ does not have a primitive root unless $$m$$ is a prime power or twice a prime power, with the prime being odd [\[Proof\]](../number-theory/proof-no-primitive-roots-for-m-having-2-distinct-odd-prime-factors.md).

To conclude, integers of the form $$8n$$, $$4p$$ and $$pq$$ don't have primitive roots and the remaining cases are $$1, 2, 4, p^n, 2p^n$$.

From the above, we can also see that the existence of primitive roots modulo $$m$$ has a close relationship with the number of solutions for the congruence $$x^2 \equiv 1 \space (mod \space m)$$. It turns out **the congruence** $$x^2 \equiv 1 \space (mod \space m)$$ **having exactly 2 solutions is a sufficient and necessary conditions for the existence** [\[Proof\]](../number-theory/proof-gausss-generation-of-wilsons-theorem.md).

## How to find Primitive Root

We can find a primitive root modulo $$p$$ by trial and error. First of all, we have to find the prime factors of $$\varphi(p - 1) = q_1^{t_1}q_2^{t_2}...q_r^{t_r}$$. After that, we pick a random number $$a$$ less than $$p$$ and check if it has order less than $$p - 1$$ by testing if any of the congruence $$a^{(p - 1)/q_k} \equiv 1 \space (mod \space p)$$ holds for $$k = 1, 2, ..., r$$. If none of them holds, $$a$$ is a primitive root modulo $$p$$. We only need to check the prime factors themselves without caring about their powers or products because if $$a^{(p - 1)/d_1d_2} \equiv 1 \space (mod \space p)$$, $$(a^{(p-1)/d_1d_2})^{d_2} = a^{(p-1)/d_1} \equiv 1 \space (mod \space p)$$ as well.

Once we know $$g$$ is a primitive root modulo $$p$$, we can easily derive the others by the fact that the powers of $$g$$ form a reduced residue system modulo $$p$$ [\[Proof\]](../number-theory/proof-powers-of-primitive-root-form-a-reduced-residue-system.md) and $$ord_p(g^u) = (p - 1) / (p - 1, u)$$ [\[Proof\]](../number-theory/proof-order-of-powers-of-a-modulo-m.md). We can list out the integers $$t_1, t_2, ..., t_{\varphi(p - 1)}$$ less than $$p - 1$$ which are relative prime to $$p - 1$$, and all the $$g^{t_k}$$ are the primitive roots modulo $$p$$, in total $$\varphi(\varphi(p))$$ of them.

## References

* [https://www.youtube.com/watch?v=E8UTP0DiCCg](https://www.youtube.com/watch?v=E8UTP0DiCCg)
* Kenneth H Rosen _Elementary Number Theory_, 2011 - Chapter 9 (P347)

