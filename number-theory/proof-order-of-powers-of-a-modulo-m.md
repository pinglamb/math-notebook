# \[Proof] Order of Powers of a modulo m

_Proof of_ $$ord_m(a^u) = ord_m(a) / (ord_m(a), u)$$

Let $$s = ord_m(a^u)$$ and $$t = ord_m(a)$$. Let $$v = (t, u)$$, then $$t = t_1v$$ and $$u = u_1v$$ with $$(t_1, u_1) = 1$$. We have to show that $$s = t_1 = t / (t, v)$$.

Consider $$(a^u)^{t_1} = a^{(u_1v)(t/v)} = (a^t)^{u_1} \equiv 1 \space (mod \space m)$$, hence $$ord_m(a^u) = s \space | \space t_1$$.

Consider $$a^{us} =(a^u)^s \equiv 1 \space (mod \space m)$$, hence $$ord_m(a) = t \space | \space us$$. It follows $$t_1v \space | \space u_1vs$$ and hence $$t_1 \space | \space u_1s$$. As $$(t_1, u_1) = 1$$, $$t_1 \space | \space s$$.

Combining the two, we have $$ord_m(a^u) = s = t_1 = t / (t, u) = ord_m(a) / (ord_m(a), u)$$.

The implication is that the order of $$a^u$$ modulo $$m$$ is always less than or equal to that of $$a$$. The reason is that we can borrow the common factors $$(ord(a), u)$$ from $$u$$ so to maintain $$a^{ord(a)} \equiv 1$$. Also, if $$(ord_m(a), u) = 1$$, $$ord_m(a^u) = ord_m(a)$$, hence there are $$\varphi(ord_m(a))$$ integers having the same order as $$a$$ modulo $$m$$.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Theorem 9.4 (P351)
