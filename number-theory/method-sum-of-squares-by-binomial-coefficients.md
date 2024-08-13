# \[Method] Sum of Squares by Binomial Coefficients

_Derive the formula for the series_ $$1^2 + 2^2 + 3^2 + \mathellipsis + n^2$$ _by Binomial Coefficients._

Consider the term $$n^2$$, we can rewrite it with:

$$
n^2 = 2 \Big[ \frac{n(n-1)}{2} \Big] + n = 2{n \choose 2} + {n \choose 1}
$$

So, by summing that over all natural numbers, we get:

$$
\begin{equation} \begin{split} \nonumber \sum k^2 &= 2 \sum {k \choose 2} + \sum {k \choose 1} \\[15pt] &= 2 {n+1 \choose 3} + {n+1 \choose 2} \\[15pt] &= 2 \Big[ \frac{(n+1)(n)(n-1)}{6} \Big] + \frac{(n+1)(n)}{2} \\[15pt] &= \frac{n(n+1)}{2} \Big[ \frac{2(n-1)}{3} + 1 \Big] \\[15pt] &= \frac{n(n+1)(2n+1)}{6} \end{split} \end{equation}
$$

