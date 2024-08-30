# \[Proof] Existence of Primitive Root modulo Powers of Odd Prime or Twice that

### **\[**$$p \rarr p^2$$**]** If $$g$$ is primitive root modulo an odd prime $$p$$, either $$g$$ or $$g + p$$ is primitive root modulo $$p^2$$

Let $$p$$ be an odd prime and $$g$$ is a primitive root modulo $$p$$, $$ord_p(g) = p - 1$$.

Let $$d = ord_{p^2}(g)$$, $$g^d \equiv 1 \space (mod \space p^2)$$, therefore $$g^d \equiv 1 \space (mod \space p)$$, which implies $$ord_p(g) = p - 1 \space | \space d$$. On the other hand, by Euler's Theorem, $$ord_{p^2}(g) \space | \space \varphi(p^2) \implies d \space | \space p(p - 1)$$. By combining both conditions, $$d = p - 1$$ or $$d = p(p - 1)$$.

For the case $$d = p(p - 1)$$, we are done and $$g$$ is a primitive root modulo $$p^2$$ by definition.

For the case $$d = p - 1$$, we have $$g^{p - 1} \equiv 1 \space (mod \space p^2)$$. Consider the integer $$g + p$$, it is also a primitive root of $$p$$ as $$g \equiv g + p \space (mod \space p)$$, hence by the above arguments, $$ord_{p^2}(g + p)$$ will be either $$p - 1$$ or $$p(p - 1)$$. However,

$$
\begin{aligned} (g + p)^{p - 1} &= g^{p-1} + (p - 1)g^{p-2}p + {p - 1 \choose 2}g^{p - 3}p^2 + ... \\ &\equiv 1 - pg^{p-2} \enspace (mod \space p^2) \end{aligned}
$$

As $$(g, p) = 1$$, $$(g^{p-2}, p) = 1$$, $$pg^{p-2} \not \equiv 0 \space (mod \space p^2)$$ and therefore $$(g + p)^{p-1} \not \equiv 1 \space (mod \space p^2)$$. Hence, $$ord_{p^2}(g + p) = p(p - 1)$$ and $$g + p$$ is a primitive root modulo $$p^2$$.

It is rare that when $$g$$ is a primitive root modulo $$p$$ but $$g^{p-1} \equiv 1 \space (mod \space p^2)$$, meaning a primitive root modulo $$p$$ is very likely a primitive root modulo $$p^2$$ as well. But if that occurs, $$g + p$$ is a primitive root modulo $$p^2$$.

### **\[**$$p^2 \rarr p^n$$**]** If $$g$$ is a primitive root modulo $$p^2$$, $$g$$ is a primitive root modulo $$p^n$$ for $$n \ge 1$$.

Let $$g$$ be a primitive root modulo $$p^2$$, the key idea is to show that $$g^{p^{n-2}(p - 1)} \not \equiv 1 \space (mod \space p^n)$$ by Mathematical Induction.

When $$n = 2$$, as $$g$$ is a primitive root modulo $$p^2$$, $$g^{p - 1} \not \equiv 1 \space (mod \space p^2)$$.

When $$n = k$$, $$g^{p^{k-2}(p-1)} \not \equiv 1 \space (mod \space p^k)$$, it implies

$$
g^{p^{k-2}(p-1)} \equiv 1 + tp^{k-1} \enspace (mod \space p^k)
$$

for some $$t \not | \enspace p$$. Hence,

$$
\begin{aligned} g^{p^{k-1}(p-1)} &= (1 + tp^{k-1})^p \\ &= 1 + p(tp^{k-1}) + {p \choose 2}(tp^{k-1})^2 + ...\end{aligned}
$$

As $$k \ge 2 \implies 2k \ge k + 2 \implies 2k - 2 \ge k$$, and $$p \space | \space {p \choose 2}$$ for $$p > 2$$, the term $${p \choose 2}(tp^{k-1})^2$$ is divisible by $$p^{k+1}$$ (_and that's why it doesn't work for_ $$p = 2$$). Hence, as $$t \not | \enspace p$$,

$$
g^{p^{k-1}(p-1)} \equiv 1 + tp^k \not \equiv 1 \enspace (mod \space p^{k+1})
$$

By Induction, $$g^{p^{n-2}(p - 1)} \not \equiv 1 \space (mod \space p^n)$$ for $$k \ge 2$$.

Assume $$g$$ is a primitive root modulo $$p^k$$, $$ord_{p^k}(g) = p^{k-1}(p-1)$$. Let $$d = ord_{p^{k+1}}(g)$$, $$g^d \equiv 1 \space (mod \space p^{k+1})$$, therefore $$g^d \equiv 1 \space (mod \space p^k)$$ which implies $$p^{k-1}(p-1) \space | \space d$$. On the other hand, by Euler's Theorem, $$d \space | \space p^k(p - 1)$$. Hence, $$d = p^{k-1}(p - 1)$$ or $$d = p^k(p - 1)$$.

But from the above, $$g^{p^{k-1}(p - 1)} \not \equiv 1 \space (mod \space p^{k+1})$$. It follows $$d \not = p^{k-1}(p-1)$$. Hence, $$ord_{p^{k+1}}(g) = p^k(p - 1)$$ and $$g$$ is also a primitive root modulo $$p^{k+1}$$.

By Induction, when $$g$$ is a primitive modulo $$p^2$$, $$g$$ is also a primtive root modulo $$p^n$$ for $$n \ge 2$$. For the case $$k = 1$$, a primitive root modulo $$p^2$$ is always a primitive root modulo $$p$$ [\[Proof\]](proof-primitive-root-of-prime-powers-is-also-primitive-root-of-the-prime.md).

### \[$$p^t \rarr 2p^t$$] If $$g$$ is a primitive root modulo $$p^n$$, either $$g$$ or $$g + p^n$$, whichever is odd, is a primitive root modulo $$2p^n$$

Let $$g$$ be a primitive root modulo $$p^n$$ and $$g$$ is odd, $$ord_{p^n}(g) = \varphi(p^n) = p^{n-1}(p - 1)$$. Also, $$\varphi(2p^n) = \varphi(2) \cdot \varphi(p^n) = \varphi(p^n)$$.

Let $$d = ord_{2p^n}(g)$$, $$g^d \equiv 1 \space (mod \space 2p^n)$$, it follows $$g^d \equiv 1 \space (mod \space p^n)$$ and $$\varphi(p^n) \space | \space d$$. On the other hand, as $$g$$ is odd, we have $$g^{\varphi(2p^n)} \equiv 1 \space (mod \space 2)$$, together with $$g^{\varphi(p^n)} \equiv 1 \space (mod \space p^n)$$, we have $$g^{\varphi(2p^n)} \equiv 1 \space (mod \space 2p^n)$$, and therefore $$d \space | \space \varphi(2p^n)$$. Combining the two conditions with $$\varphi(p^n) = \varphi(2p^n)$$, we have $$d = \varphi(2p^n)$$ and hence $$g$$ is a primitive root modulo $$2p^n$$.

When $$g$$ is even, $$g + p^n$$ is odd, which is also a primitive root modulo $$p^n$$ as $$g \equiv g + p^n \space (mod \space p^n)$$. With the same arguments above, $$ord_{2p^n}(g + p^n) = \varphi(2p^n)$$ and $$g + p^n$$ is a primitive root modulo $$2p^n$$.

To conclude, once $$g$$ is a primitive root modulo $$p^n$$, either $$g$$ or $$g + p^n$$, whichever is odd, is a primitive root modulo $$2p^n$$.$$g^{\varphi(2p^n) \equiv 1 \space (mod \space 2p^n)$$

* [https://youtu.be/AfRpXi8r0So](https://youtu.be/AfRpXi8r0So)
* Kenneth H Rosen _Elementary Number Theory_, 2011 - Section 9.3 (P360)
