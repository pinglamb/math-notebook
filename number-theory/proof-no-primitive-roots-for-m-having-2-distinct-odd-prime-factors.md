# \[Proof] No Primitive Roots for m having 2 distinct odd prime factors

_Proof of no primitive roots modulo_ $$m$$ _except_ $$m$$ _is of the form_ $$p^n$$ _or_ $$2p^n$$_._

Let $$m = p_1^{n_1}p_2^{n_2}...p_r^{n_r}$$, $$\varphi(m) = \varphi(p_1^{n_1})\varphi(p_2^{n_2})...\varphi(p_r^{n_r})$$. We have to first show that when $$U = [\varphi(p_1^{n_1}), \varphi(p_2^{n_2}), ..., \varphi(p_r^{n_r})]$$, the least common mulitple of $$\varphi(p_i^{n_i})$$, $$a^U \equiv 1 \space (mod \space m)$$. By definition, $$\varphi(p_i^{n_i}) \space | \space U$$, therefore by Euler's Theorem,

$$
a^U \equiv 1 \enspace(mod \space p_i^{n_i})
$$

for all $$i = 1, 2, ..., r$$. As all the $$p_i^{n_i}$$ are all pairwise relatively prime, we have

$$
a^U \equiv 1 \enspace (mod \space m)
$$

As $$U \le \varphi(m)$$, in order for $$a$$ to be a primitive root modulo $$m$$, we need to have $$U = \varphi(m)$$, it means all the $$\varphi(p_i^{n_i})$$ has to be pairwise relatively prime. The condition doesn't hold when $$m$$ has more than 2 odd prime factors as $$\varphi(p_i^{n_i})$$ will be even when $$p$$ is odd. Also, as $$\varphi(4) = 2$$, integer $$m$$ $$m$$of form $$4p_1^{n_1}p_2^{n_2}...p_r^{n_r}$$ will also have $$U < \varphi(m)$$.

To conclude, whenever $$\varphi(p_i^{n_i})$$ has common factors among them, all the integer $$a$$ relatively prime to $$m$$ can only have their order modulo $$m$$ at most equal to the least common multiple $$U$$ of $$\varphi(p_i^{n_i})$$ and hence no primitive roots. The only remaining case is $$p^n$$ and $$2p^n$$.$$u$$

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Theorem 9.13 (P365)
