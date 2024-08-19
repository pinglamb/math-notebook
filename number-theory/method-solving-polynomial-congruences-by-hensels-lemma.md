# \[Method] Solving Polynomial Congruences by Hensel's Lemma

_Find the solutions of_ $$f(x) \equiv 0 \space (mod \space m)$$_, where_ $$f(x)$$ _is a polynomial of degree_ $$n > 1$$ _and integer coefficients._

Suppose $$m = p_1^{a_1}p_2^{a_2}...p_k^{a_k}$$, we can solve the following congruences and finding the solution using Chinese Remainder Theorem:

$$
f(x) \equiv 0 \enspace (mod \space p_i^{a_i}) \text{ where } i = 1, 2, 3, ..., k
$$

To solve $$f(x) \equiv 0 \space (mod \space p^a)$$, we first observe that if $$x \equiv r \space (mod \space p^a)$$ is a solution of $$f(x) \equiv 0 \space (mod \space p^a)$$, which means $$f(r) = p^aq = p^{a - 1}(pq)$$, it is also a solution of $$f(x) \equiv 0 \space (mod \space p^{a - 1})$$. Hence, $$r_a = r_{a - 1} + tp^{a-1}$$.

By Taylor Expansion,

$$
\begin{aligned} f(r_a) &= f(r_{a-1} + tp^{a-1}) \\ &=f(r_{a-1}) +f'(r_{a-1})(tp^{a-1}) + \frac{f''(r_{a-1})}{2!}(tp^{a-1})^2 + ... \end{aligned}
$$

First of all, when $$f(x) = x^n$$, $$f^{(k)}(x) = n(n-1)(n-2)...(n-k+1)x^{n-k}$$ for $$n \ge k$$ and $$f^{(k)}(x) = 0$$ for $$n < k$$, therefore $$\frac{f^{(k)}(r_{a-1})}{k!}$$ will be an integer as $$\frac{n(n-1)...(n-k+1)}{k!} = {n \choose k}$$. Also, $$(p^{a-1})^k = p^a(p^{ka - k - a})$$, when $$a \ge 2$$ and $$k \ge 2$$, $$ka - k - a \ge 0$$, therefore the term $$\frac{f^{(k)}(r_{a-1})}{k!}(tp^{a-1})^k$$ with $$k \ge 2$$ will be dividible by $$p^a$$. Hence,

$$
f(r_a) \equiv f(r_{a-1}) + f'(r_{a-1})(tp^{a-1}) \enspace (mod \space p^a)
$$

As $$r_a$$ is a solution of $$f(x) \equiv 0 \space (mod \space p^a)$$, $$f(r_{a-1}) + f'(r_{a-1})(tp^{a-1}) \equiv 0 \space (mod \space p^a)$$, it follows $$f'(r_{a-1})(tp^{a-1}) \equiv -f(r_{a-1}) \space (mod \space p^a)$$. As $$f(r_{a-1}) \equiv 0 \space (mod \space p^{a-1})$$, $$f(r_{a-1}) = p^{a-1}q$$, we can divide both side by $$p^{a-1}$$. Hence,

$$
f'(r_{a-1})t \equiv -f(r_{a-1}) / p^{a-1} \space (mod \space p)
$$

Suppose that $$f'(r_{a-1}) \not\equiv 0 \space (mod \space p)$$, $$(f'(r_{a-1}), p) = 1$$, hence, f'(r\_{a-1}) has an inverse modulo $$p$$ and we have a unique solution

$$
t \equiv (-f(r_{a-1})/p^{a-1})\overline{f'(r_{a-1})} \enspace (mod \space p)
$$

When $$f'(r_{a-1}) \equiv 0 \space (mod \space p)$$, From the Taylor Expansion, we can see that $$f(r_a) = f(r_{a-1}) \space (mod \space p^a)$$. Therefore, if $$f(r_{a-1}) \equiv 0 \space (mod \space p^a)$$, the congruence has solutions of the form $$r_{a-1} + tp^{k-1}$$, where $$t = 1, 2, 3, ..., p-1$$. Otherwise, the congruence has no solution.
