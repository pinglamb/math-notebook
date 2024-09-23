# Apollonian Circles

Apollonian Circles are two families of circles such that every circles in the first family intersects orthogonally with every circles in the second family, and vice verse.

## By Complex Number

Let $$z, a, b \in \Complex$$ correspond to points $$P, A, B$$ in the complex plane. Let $$C_\lambda$$ be the locus of $$P$$ defined by $$|PA|/|PB| = \lambda$$, where $$\lambda$$ is a fixed real positive constant. Show that $$C_\lambda$$ is a circle if $$\lambda \not = 1$$ and find its centre and radius.

As $$|z - a|^2 = (z - a)(\bar{z} - \bar{a})$$ and $$|z - b|^2 = (z - b)(\bar{z} - \bar{b})$$, we have

$$
(1 - \lambda^2)z\bar{z} - (a - \lambda^2b)\bar{z} - (\bar{a} - \lambda^2\bar{b})z + |a|^2 - \lambda^2|b|^2 = 0
$$

From that, we can see the centre $$w$$ should be

$$
w = {a - \lambda^2b \over 1 - \lambda^2}
$$

By rearranging the terms, we have

$$
\begin{aligned} (z - w)(\bar{z} - \bar{w}) &= {1 \over (1 - \lambda^2)^2}\left( (1 - \lambda^2)\lambda^2|b|^2 - (1 - \lambda^2)|a|^2 + |a - \lambda^2b|^2\right) \\ &= {1 \over (1 - \lambda^2)^2} \left( \lambda^2|b|^2 + \lambda^2|a|^2 +\lambda^2(\bar{a}b + a\bar{b})\right) \\ &= \left( {\lambda \over 1 - \lambda^2} |a - b| \right)^2 \end{aligned}
$$

Therefore,

$$
r = {\lambda \over 1 - \lambda^2} |a - b|
$$

When $$\lambda = 1$$, $$|z - a| = |z - b|$$, hence it becomes the perpendicular bisector of $$a$$ and $$b$$.

## References

* [https://en.wikipedia.org/wiki/Apollonian\_circles](https://en.wikipedia.org/wiki/Apollonian\_circles)
