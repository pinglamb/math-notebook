# \[Proof] Powers of Primitive Root forms a reduced residue system

_Let_ $$g$$ _be the primitive root of_ $$m$$_, with_ $$(g, m) = 1$$_, the integers_ $$g^1, g^2, ..., g^{\varphi(m)}$$ _form a reduced residue system modulo_ $$m$$_._

Assume $$g$$ is an integer relative prime to $$m$$, if $$(g^k, m) = d\not = 1$$, $$g^kx + my = g(g^{k-1}x) + my = d$$, it implies $$(g, m) = d \not = 1$$ which contradicts with the assumption. Hence, $$(g, m) = 1 \implies (g^k, m) = 1$$.

Assume $$a$$ is an integer relative prime to $$m$$, if $$i \equiv j \space (mod \space ord(g))$$, $$i = ord(a) \cdot q + j$$, it follows $$a^i \equiv a^{ord(a)q} \cdot a^j \equiv a^j \space (mod \space m)$$. Conversely, if $$a^i \equiv a^j \space (mod \space m)$$ with $$i \ge j$$, as $$(a^j, m) = 1$$, dividing both side by $$a^j$$ we have $$a^{i-j} \equiv 1 \space (mod \space m)$$, it follows $$ord(a) \space | \space i - j$$ and $$i \equiv j \space (mod \space ord(a))$$. Hence, $$a^i \equiv a^j \space (mod \space m) \iff i \equiv j \space (mod \space ord(a))$$.

With the above, we can prove $$g^1, g^2, ..., g^{\varphi(m)}$$ form a reduced residue system modulo $$m$$ by showing every one of them is relatively prime to $$m$$ and they are incongruent to each other. As $$(g, m) = 1$$, $$(g^k, m) = 1$$ for $$k = 1, 2, ... \varphi(m)$$, hence they are integers all relative prime to $$m$$. Assume there exists $$i$$ and $$j$$, with $$1 \le i, j \le \varphi(m)$$, such that $$g^i \equiv g^j \space (mod \space m)$$, it implies $$i \equiv j \space (mod \space ord(g))$$. However, as $$ord(g) = \varphi(m)$$, $$i \equiv j \space (mod \space \varphi(m))$$ implies $$i = j$$. Hence, no two of these powers are congruent modulo $$m$$. This shows when $$g$$ is primitive root of $$m$$, $$g^1, g^2, ..., g^{\varphi(m)}$$ form a reduced residue system modulo $$m$$.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Section 9.1 (P351)
