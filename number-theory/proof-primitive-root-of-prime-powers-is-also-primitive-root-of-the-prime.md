# \[Proof] Primitive Root of Prime Powers is also Primitive Root of the Prime

_If_ $$g$$ _is a primitive root of_ $$p^{k+1}$$ _for_ $$k \ge 1$$_,_ $$g$$ _is also a primitive root of_ $$p^k$$ _and hence_ $$p$$_._

Assume $$g$$ is a primitive root of $$p^{k+1}$$, $$g \not = 1$$ and $$ord_{p^{k+1}}(g) = \varphi(p^{k+1}) = p^k(p-1)$$. Let $$d = ord_{p^k}(g)$$, $$g^d \equiv 1 \space (mod \space p^k)$$, it follows $$g^d \equiv 1 + tp^k \space (mod \space p^{k+1})$$. By raising both side to the power of $$p$$, we have $$g^{pd} \equiv (1 + tp^k)^p = 1 + p(tp^k) + {p \choose 2}(tp^k)^2 + ... \equiv 1 \space (mod \space p^{k+1})$$, therefore$$ord_{p^{k+1}}(g) \space | \space pd$$, which implies $$p^k(p - 1) \space | \space pd$$ and $$p^{k-1}(p - 1) \space | \space d$$. On the other hand, by Fermat's Theorem, we have $$d \space | \space p^{k-1}(p - 1)$$ as $$ord_{p^k}(g) \space | \space \varphi(p^k)$$. Hence, $$d = p^{k-1}(p-1)$$ and $$g$$ is a primitive root modulo $$p^k$$. It follows $$g$$ is also a primitive root of $$p$$.

The other way to see this is that a primitive root of higher power of $$p$$ is going through all the reduced residue classes modulo $$p^k$$, therefore it should also go through all the reduced residue classes modulo $$p$$.
