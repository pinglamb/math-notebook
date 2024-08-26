# \[Proof] Powers of Primitive Root forms a reduced residue system

_Let_ $$r$$ _be the primitive root of_ $$m$$_, with_ $$(r, m) = 1$$_, the integers_ $$r^1, r^2, ..., r^{\varphi(m)}$$ _form a reduced residue system modulo_ $$m$$_._

Assume $$r$$ is an integer relative prime to $$m$$, if $$(r^k, m) = d\not = 1$$, $$r^kx + my = r(r^{k-1}x) + my = d$$, it implies $$(r, m) = d \not = 1$$ which contradicts with the assumption. Hence, $$(r, m) = 1 \implies (r^k, m) = 1$$.

Assume $$r$$ is an integer relative prime to $$m$$, if $$i \equiv j \space (mod \space ord(r))$$, $$i = ord(r) \cdot q + j$$, it follows $$r^i \equiv r^{ord(r)q} \cdot r^j \equiv r^j \space (mod \space m)$$. If $$r^i \equiv r^j \space (mod \space m)$$ with $$i \ge j$$, as $$(r^j, m) = 1$$, dividing both side by $$r^j$$ we have $$r^{i-j} \equiv 1 \space (mod \space m)$$, it follows $$ord(r) \space | \space i - j$$ and $$i \equiv j \space (mod \space ord(r))$$. Hence, $$r^i \equiv r^j \space (mod \space m) \iff i \equiv j \space (mod \space ord(r))$$.

With the above, we can prove $$r^1, r^2, ..., r^{\varphi(m)}$$ form a reduced residue system modulo $$m$$ by showing every one of them is relatively prime to $$m$$ and they are incongruent to each other. As $$(r, m) = 1$$, $$(r^k, m) = 1$$ for $$k = 1, 2, ... \varphi(m)$$, hence they are integers all relative prime to $$m$$. Assume there exists $$i$$ and $$j$$, with $$1 \le i, j \le \varphi(m)$$, such that $$r^i \equiv r^j \space (mod \space m)$$, it implies $$i \equiv j \space (mod \space ord(r))$$. However, as $$ord(r) = \varphi(m)$$, $$i \equiv j \space (mod \space \varphi(m))$$ implies $$i = j$$. Hence, no two of these powers are congruent modulo $$m$$. This shows when $$r$$ is primitive root of $$m$$, $$r^1, r^2, ..., r^{\varphi(m)}$$ form a reduced residue system modulo $$m$$.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Section 9.1 (P351)
