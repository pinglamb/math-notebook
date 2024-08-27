# Lecture 23 - Primitive Roots

## Definition of Primitive Roots

**\[Definition of** $$ord_m(a)$$**].** Let $$a$$ and $$m$$ be integers with $$a \not = 0$$, $$m > 0$$ and $$(a, m) = 1$$, the order of $$a$$ modulo $$m$$, is **the least positive integer** $$n$$ **such that** $$a^n \equiv 1 \space (mod \space m)$$. (by Gauss)

Let $$x$$ be an positive integer, then $$a^x \equiv 1 \space (mod \space m)$$ if and only if $$ord(a) \space | \space x$$. The proof is as follows. Assume $$ord(a) \space | \space x$$, meaning $$x = ord(a) \cdot k$$, it follows $$a^x = a^{ord(a)k} \equiv (1)^k \equiv 1 \space (mod \space m)$$. Assume $$a^x \equiv 1 \space (mod \space m)$$, by division algorithm we have $$x = ord(a) \cdot k + r$$, with $$0 \le r < ord(a)$$, it follows $$a^x = a^{ord(a)k + r} = a^{ord(a)k} \cdot a^r \equiv a^r \equiv 1\space (mod \space m)$$. As $$ord(a)$$ is the least positive integer such that $$a^n \equiv 1 \space (mod \space m)$$, we conclude that $$r = 0$$, and hence $$x = ord(a) \cdot k$$ and $$ord(a) \space | \space x$$.

By Euler's Theorem, we have $$a^{\varphi(m)} \equiv 1 \space (mod \space m)$$. Combine with the above theorem, we have $$ord(a) \space | \space \varphi(m)$$. $$a$$ **is called a primitive root of** $$m$$ **if** $$ord(a) = \varphi(m)$$**.**

## Powers of Primitive Roots

The primitive root $$g$$ of $$m$$ also has the property that **the integers** $$g^1, g^2, ... g^{\varphi(m)}$$ **form a reduced residue system module** $$m$$, meaning it will loop through all the positive integers co-prime to $$m$$ that are less than $$m$$ [\[Proof\]](../number-theory/proof-powers-of-primitive-root-forms-a-reduced-residue-system.md).

Conversely, assume the powers of an integer $$g$$ are all relatively prime to $$m$$ and no two of them are congruent modulo $$m$$, $$g^k \equiv 1 \space (mod \space m)$$ for exactly one $$k$$ with $$1 \le k \le \varphi(m)$$, it follows $$ord(g) = k$$. Consider the integers $$g^1$$ and $$g^{k+1}$$, $$g^1 \equiv g^{k+1} \space (mod \space m)$$ because $$1 \equiv k+1 \space (mod \space ord(g))$$. If $$k < \varphi(m)$$, $$1 < k + 1 \le \varphi(m)$$, it follows $$g^{k+1}$$ is one of the integer relatively prime to $$m$$ which is congruent to $$g^1$$ modulo $$m$$, which contradicts with the assumption. Hence, $$ord(g) = \varphi(m)$$ and $$g$$ is primitive root of $$m$$.

## Existence of Primitive Roots

There are few properties about existence of primitive roots emerged while finding the primitive root of various integers.

The first integer having no primitive root is $$8$$. The obstruction is that $$x^2 \equiv 1 \space (mod \space 8)$$ has 4 distinct solutions. If $$m$$ has a primitive root $$g$$, the only solutions to $$x^2 \equiv 1 \space (mod \space m)$$ should be $$g^{\varphi(m)} \equiv 1$$ and $$g^{\varphi(m) / 2} \equiv -1$$. It turns out $$m$$ **has a primitive root if and only if** $$x^2 \equiv 1 \space (mod \space m)$$ **has exactly 2 solutions**. <mark style="color:red;">\[Proof]</mark>

While finding the primitive root of $$9 = 3^2$$, which can be $$1, 2, 4, 5, 7, 8$$. As a primitive root of $$9$$ is also a primitive of $$3$$ [\[Proof\]](../number-theory/proof-primitive-root-of-prime-powers-is-also-primitive-root-of-the-prime.md), we only need to check $$2, 5, 8$$. In general, if we know $$g$$ is a primitive root of $$p$$, we only need to check $$g + tp$$ for $$p^2$$ (turns out that **if** $$p$$ **is odd prime and** $$g$$ **is a primitive root modulo** $$p$$**, either** $$g$$ **or** $$g+p$$ **is the primitive root modulo** $$p^2$$ **and if** $$g'$$ **is a primitive root modulo** $$p^2$$**,** $$g'$$ **is a primitive root modulo** $$p^n$$ **for all positive integers** $$n$$). <mark style="color:red;">\[Proof]</mark>

For the case of $$10 = 2 \cdot 5$$, there is a 1-to-1 mapping between the reduced residue classes modulo $$10$$ and that modulo $$5$$. If $$p$$ is odd prime and $$g$$ is a primitive root modulo $$p$$, either $$g$$ or $$g + p$$, whichever is odd, is a primitive root of $$2p$$. It is further extended to **integers in the form** $$2p^n$$ **with primitive root being** $$g$$ **or** $$g + p^n$$**, whichever is odd**. <mark style="color:red;">\[Proof]</mark>

For the case of $$11$$ and $$13$$, if $$p$$ is an odd prime, as the $$ord_p(a) \space | \space p - 1$$, by counting the number of integers that are relatively prime to $$p$$ with $$ord_p(a) = d$$, where $$d \space | \space p - 1$$. It turns out that **there are exactly** $$\varphi(d)$$ **integers of order** $$d$$ **modulo** $$p$$**, hence there are** $$\varphi(\varphi(p))$$ **primitive roots modulo** $$p$$**, which proves every odd prime has primitive root**. <mark style="color:red;">\[Proof]</mark>

For the case of $$12 = 4 \cdot 3$$ and $$15 = 3 \cdot 5$$, we can see that by Chinese Remainder Theorem, the congruence $$x^2 \equiv 1 \space (mod \space 12)$$ has $$2 \cdot 2 = 4$$ solutions. Hence, they don't have primitive roots.

To conclude, integers of the form $$8n$$, $$4p$$ and $$pq$$ don't have primitive roots. Hence, the remaining cases are $$2, 4, p^n, 2p^n$$.

## How to find Primitive Root

<mark style="color:red;">\[Check if an integer is primitive root]</mark>

<mark style="color:red;">\[From one primitive root to another]</mark>



