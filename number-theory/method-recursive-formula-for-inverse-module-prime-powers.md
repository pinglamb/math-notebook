# \[Method] Recursive Formula for Inverse module Prime Powers

_Let_ $$a$$ _be an integer and_ $$p$$ _is prime such that_ $$(a, p) = 1$$_. Use Hensel's Lemma to find a recursive formula for the solutions of the congruence_ $$ax \equiv 1 \space (mod \space p^k)$$_, for all positive integers_ $$k$$_._

Let $$f(x) = ax - 1$$, $$f'(x) = a$$, as $$(a, p) = 1$$, $$f'(x) \not \equiv 0 \space (mod \space p)$$ for all integers $$x$$, by Hensel's Lemma, the solution of the congruence module $$p^{k}$$ can always be lifted to the congruence module $$p^{k+1}$$.

Let $$r_k$$ be the solution of $$ax \equiv 1 \space (mod \space p^k)$$, $$r_1$$ is the solution of the congruence $$ax \equiv 1 \space (mod \space p)$$. As $$f'(r_k)=a \space (mod \space p)$$, $$\overline{f'(r_k)} = r_1 \space (mod \space p)$$. Hence,

$$
\begin{aligned} r_{k+1} &\equiv r_k - f(r_k)\overline{f'(r_k)} \\ &\equiv r_k - (ar_k - 1)(r_1) \\ &\equiv r_k(1 - ar_1) + r_1 \enspace (mod \space p^k) \end{aligned}
$$

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Problem 4.4.11 (P177)
