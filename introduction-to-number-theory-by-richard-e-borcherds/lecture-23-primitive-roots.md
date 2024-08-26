# Lecture 23 - Primitive Roots

## Definition of Primitive Roots

**\[Definition of** $$ord_m(a)$$**].** Let $$a$$ and $$m$$ be integers with $$a \not = 0$$, $$m > 0$$ and $$(a, m) = 1$$, the order of $$a$$ modulo $$m$$, is the least positive integer $$n$$ such that $$a^n \equiv 1 \space (mod \space m)$$. (by Gauss)

Let $$x$$ be an positive integer, then $$a^x \equiv 1 \space (mod \space m)$$ if and only if $$ord(a) \space | \space x$$. The proof is as follows. Assume $$ord(a) \space | \space x$$, meaning $$x = ord(a) \cdot k$$, it follows $$a^x = a^{ord(a)k} \equiv (1)^k \equiv 1 \space (mod \space m)$$. Assume $$a^x \equiv 1 \space (mod \space m)$$, by division algorithm we have $$x = ord(a) \cdot k + r$$, with $$0 \le r < ord(a)$$, it follows $$a^x = a^{ord(a)k + r} = a^{ord(a)k} \cdot a^r \equiv a^r \equiv 1\space (mod \space m)$$. As $$ord(a)$$ is the least positive integer such that $$a^n \equiv 1 \space (mod \space m)$$, we conclude that $$r = 0$$, and hence $$x = ord(a) \cdot k$$ and $$ord(a) \space | \space x$$.

By Euler's Theorem, we have $$a^{\varphi(m)} \equiv 1 \space (mod \space m)$$. Combine with the above theorem, we have $$ord(a) \space | \space \varphi(m)$$. $$a$$ is called a primitive root of $$m$$ if $$ord(a) = \varphi(m)$$.

## Powers of Primitive Roots

The primitive root $$a$$ of $$m$$ also has the property that the integers $$a^1, a^2, ... a^{\varphi(m)}$$ form a reduced residue system module $$m$$, meaning it will loop through all the positive integers co-prime to $$m$$ that are less than $$m$$ [\[Proof\]](../number-theory/proof-powers-of-primitive-root-forms-a-reduced-residue-system.md).

Conversely, assume the powers of an integer $$a$$ are all relatively prime to $$m$$ and no two of them are congruent modulo $$m$$, $$a^k \equiv 1 \space (mod \space m)$$ for exactly one $$k$$ with $$1 \le k \le \varphi(m)$$, it follows $$ord(a) = k$$. Consider the integers $$a^1$$ and $$a^{k+1}$$, $$a^1 \equiv a^{k+1} \space (mod \space m)$$ because $$1 \equiv k+1 \space (mod \space ord(a))$$. If $$k < \varphi(m)$$, $$1 < k + 1 \le \varphi(m)$$, it follows $$a^{k+1}$$ is one of the above integers which will be congruent to $$a^1$$ modulo $$m$$, which contradicts with the assumption. Hence, $$ord(a) = \varphi(m)$$ and $$a$$ is primitive root of $$m$$.
