# \[Method] Reducing Polynomial Congruences modulo Prime Powers by Hensel's Lemma

_Given_ $$f(a) \equiv 0 \space (mod \space p^a)$$_, find the solutions of_ $$f(x) \equiv 0 \space (mod \space p^{a+1})$$_, where_ $$f(x)$$ _is a polynomial of degree_ $$n > 1$$ _and integer coefficients._

Suppose $$m = p_1^{a_1}p_2^{a_2}...p_k^{a_k}$$, we can solve the following congruences and finding the solution using Chinese Remainder Theorem:

$$
f(x) \equiv 0 \enspace (mod \space p_i^{a_i}) \text{ where } i = 1, 2, 3, ..., k
$$

To solve $$f(x) \equiv 0 \space (mod \space p^a)$$, we first observe that if $$f(r_{a+1}) \equiv 0 \space (mod \space p^{a+1})$$, $$f(r_{a+1}) = p^{a+1}q = p^a(pq)$$, which implies $$f(r_{a+1}) \equiv 0 \space (mod \space p^a)$$, meaning $$x \equiv r_{a+1} \space (mod \space p^a)$$ is also a solution of $$f(x) \equiv 0 \space (mod \space p^a)$$. Hence, if $$f(r_a) \equiv 0 \space (mod \space p^a)$$, $$r_{a+1} = r_a + tp^a$$.

By Taylor Expansion,

$$
\begin{aligned} f(r_{a+1}) &= f(r_a + tp^a) \\ &=f(r_a) +f'(r_a)(tp^a) + \frac{f''(r_a)}{2!}(tp^a)^2 + ... \end{aligned}
$$

First of all, when $$f(x) = x^n$$, $$f^{(k)}(x) = n(n-1)(n-2)...(n-k+1)x^{n-k}$$ for $$n \ge k$$ and $$f^{(k)}(x) = 0$$ for $$n < k$$, therefore $$\frac{f^{(k)}(r_a)}{k!}$$ is an integer as $$\frac{n(n-1)...(n-k+1)}{k!} = {n \choose k}$$. Also, $$(p^a)^k = p^a(p^{k - a})$$, when $$k > a \ge 1$$, $$ka - k - a \ge 0$$the term $$\frac{f^{(k)}(r_a)}{k!}(tp^a)^k$$ is dividible by $$p^{a+1}$$. Hence,

$$
f(r_{a+1}) \equiv f(r_a) + f'(r_a)(tp^a) \enspace (mod \space p^{a+1})
$$

Assume $$f(r_{a+1}) \equiv 0 \space (mod \space p^{a+1})$$, $$f(r_a) + f'(r_a)(tp^a) \equiv 0 \space (mod \space p^{a+1})$$, it follows that$$f'(r_a)(tp^a) \equiv -f(r_a) \space (mod \space p^{a+1})$$. As $$f(r_a) \equiv 0 \space (mod \space p^a)$$, $$f(r_a) = p^aq$$, we can divide both side by $$p^a$$. Hence,

$$
f'(r_a)t \equiv -f(r_a) / p^a \space (mod \space p)
$$

When $$f'(r_a) \not\equiv 0 \space (mod \space p)$$, $$(f'(r_a), p) = 1$$, hence $$f'(r_a)$$ has a unique inverse modulo $$p$$, i.e.

$$
t \equiv (-f(r_a)/p^a)\overline{f'(r_a)} \enspace (mod \space p)
$$

By substituding it back,

$$
r_{a+1} \equiv r_a - f(r_a)\overline{f'(r_a)} \enspace (mod \space p^{a+1})
$$

We lifted the solution of the congruence modulo $$p^a$$ to a unique solution of the same congruence modulo $$p^{a+1}$$. (Hensel's Lemma)

When $$f'(r_a) \equiv 0 \space (mod \space p)$$, it means $$f'(r_a)$$ is a multiple of $$p$$. Suppose $$d$$ is a positive integer such that $$p^d \space | \space f'(r_a)$$ but $$p^{d+1} \not | \enspace f'(r_a)$$. Assume $$f(r_a) \equiv 0 \space (mod \space p^a)$$ and let

$$
r_{a+1} = r_a + tp^{a-d}
$$

By Taylor Expansion,

$$
\begin{aligned} f(r_{a+1}) &= f(r_a + tp^{a-d}) \\ &= f(r_a) +f'(r_a)(tp^{a-d}) + \frac{f''(r_a)}{2!}(tp^{a-d})^2 + ... \end{aligned}
$$

We can see that when $$2a - 2d > a + 1 \implies a \ge 2d + 1$$, all the terms $$\frac{(f^{(k)}(r_a)}{k!}(tp^{a-d})^k$$ with $$k \ge 2$$ are divisible by $$p^{a+1}$$. Also, as $$f'(r_a) = p^dq$$, $$f(r_{a+1}) \equiv f(r_a) + tq(p^{a - d + d}) \equiv 0 \space (mod \space p^a)$$, $$x \equiv r_{a+1} \space (mod \space p^a)$$ is also a solution of the congruence modulo $$p^a$$. Assume $$f(r_{a+1}) \equiv 0 \space (mod \space p^{a+1})$$$$p^{a+1}$$, $$f(r_a) + (p^dq)(tp^{a-d}) \equiv 0 \space (mod \space p^{a+1})$$, it follows

$$
tq = -f(r_a) / p^a \enspace (mod \space p)
$$

As $$p^{d+1} \not | \enspace f'(r_a)$$,  $$(q, p) = 1$$ and $$q$$ has a unique inverse modulo $$p$$, i.e.

$$
t = (\frac{-f(r_a)}{p^a})\overline{(\frac{f'(r_a)}{p^d})} \enspace (mod \space p)
$$

Hence, when $$a \ge 2d + 1$$, we can lift a solution of the congruence module $$p^a$$ to a unique solution of the same congruence modulo $$p^{a+1}$$. Furthermore, from the Taylor Expansion,

$$
f'(r_{a+1}) = f'(r_a) +f''(r_a)(tp^{a-d}) + \frac{f'''(r_a)}{2!}(tp^{a-d})^2 + ...
$$

With $$a \ge 2d + 1 \implies a - d \ge d + 1$$, all the terms except $$f'(r_a)$$ are divisible by $$p^{d+1}$$, hence $$f'(r_{a+1}) \equiv f'(r_a) \equiv 0 \space (mod \space p^d)$$ and $$f'(r_{a+1}) \equiv f'(r_a) \not \equiv 0 \space (mod \space p^{d+1})$$, meaning $$p^d \space | \space f'(r_{a+1})$$ but $$p^{d+1} \not | \enspace f"(r_{a+1})$$. Therefore, with the same argument as described above, the solution can then be lifted to solutions of arbitrarily high powers of $$p$$, whenever $$a \ge 2d + 1$$.$$p$$
