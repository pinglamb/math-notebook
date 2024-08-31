# \[Proof] Lucas's Converse of Fermat's Little Theorem

_Let_ $$m$$ _be a positive integer. If there exists an_ $$g$$ _such that_

$$
g^{m-1} \equiv 1 \space (mod \space m)
$$

_and_

$$
g^{(m - 1) / p_i} \not \equiv 1 \space (mod \space m)
$$

_for all prime divisors_ $$p_i$$ _of_ $$m - 1$$_, then_ $$m$$ _is a prime._



Let $$d = ord_m(g)$$, $$g^d \equiv 1 \space (mod \space m)$$. Also, $$d \space | \space m - 1$$, therefore $$m - 1 = dq$$. Assume $$q > 1$$, then $$q$$ must be divisible by at least one of the prime divisor $$p_i$$ of $$m - 1$$. However, it implies$$g^{(m - 1)/p_i} = g^{dq/p_i} \equiv (1)^{q/p_i} \equiv 1 \space (mod \space m)$$, which contradicts with the hypotheses. Hence, $$q = 1$$ and $$ord_m(g) = m - 1$$. As $$ord_m(g) \le \varphi(m)$$ and $$\varphi(m) \le m - 1$$, we have $$\varphi(m) = m - 1$$ and hence $$m$$ is prime.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Section Theorem 9.18 (P379)
