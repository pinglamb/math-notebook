# Apollonian Circles

Apollonian Circles are two families of circles such that every circles in the first family intersects orthogonally with every circles in the second family, and vice verse.

## By Complex Number

_\[Problem] Let_ $$z, a, b \in \Complex$$ _correspond to points_ $$P, A, B$$ _in the complex plane. Let_ $$C_\lambda$$ _be the locus of_ $$P$$ _defined by_ $$|PA|/|PB| = \lambda$$_, where_ $$\lambda$$ _is a fixed real positive constant. Show that_ $$C_\lambda$$ _is a circle if_ $$\lambda \not = 1$$ _and find its centre and radius._

\[Solution] As $$|z - a|^2 = (z - a)(\bar{z} - \bar{a})$$ and $$|z - b|^2 = (z - b)(\bar{z} - \bar{b})$$, we have

$$
(1 - \lambda^2)z\bar{z} - (a - \lambda^2b)\bar{z} - (\bar{a} - \lambda^2\bar{b})z + |a|^2 - \lambda^2|b|^2 = 0
$$

From that, we can see the centre $$w_\lambda$$ should be

$$
w_\lambda = {a - \lambda^2b \over 1 - \lambda^2}
$$

By rearranging the terms, we have

$$
\begin{aligned} (z - w_\lambda)(\bar{z} - \bar{w_\lambda}) &= {1 \over (1 - \lambda^2)^2}\left( (1 - \lambda^2)\lambda^2|b|^2 - (1 - \lambda^2)|a|^2 + |a - \lambda^2b|^2\right) \\ &= {1 \over (1 - \lambda^2)^2} \left( \lambda^2|b|^2 + \lambda^2|a|^2 +\lambda^2(\bar{a}b + a\bar{b})\right) \\ &= \left( {\lambda \over 1 - \lambda^2} |a - b| \right)^2 \end{aligned}
$$

Therefore,

$$
r_\lambda = {\lambda \over 1 - \lambda^2} |a - b|
$$

When $$\lambda = 1$$, $$|z - a| = |z - b|$$, hence it becomes the perpendicular bisector of $$a$$ and $$b$$.



_\[Problem] For the case_ $$a = -b = p$$_,_ $$p \in \R$$_, and for each fixed_ $$\mu \in \R$$_, show that_

$$
S_\mu = \Set{ z \in \Complex  | |z - i\mu| = \sqrt{p^2 + \mu^2}}
$$

_is a circle passing through_ $$A$$ _and_ $$B$$ _with its centre on the perpendicular bisector of_ $$AB$$_._

\[Solution] By definion, $$S_\mu$$ is a circle with centre $$w_\mu = i\mu$$ and radius $$r_\mu = \sqrt{p^2 + \mu^2}$$. As $$a = p$$, $$|a - i\mu| = |p - i\mu| =\sqrt{p^2 + \mu^2}$$, the circle passes through $$A$$. Similarily, it passes through $$B$$.

As $$|a - i\mu| = |b - i\mu|$$, the centre of the circle $$i\mu$$ is always equidistant from $$A$$ and $$B$$, therefore it is the perpendicular bisector of $$AB$$.



_\[Problem] Show that the circles_ $$C_\lambda$$ _and_ $$S_\mu$$ _intersect orthogonally for all_ $$\lambda$$ _and_ $$\mu$$_._

\[Solution] As $$a = -b = p$$, we have

$$
w_\lambda = {p - \lambda^2(-p) \over 1 - \lambda^2} = {1 + \lambda^2 \over 1 - \lambda^2}\,p
$$

and $$|a - b| = 2p$$, hence

$$
r_\lambda = {2\lambda p \over 1 - \lambda^2}
$$

Suppose $$C_\lambda$$ and $$S_\mu$$ intersects at $$z$$, we have $$|z - w_\lambda|^2 = r_\lambda^2 =  \left({2\lambda p \over 1 - \lambda^2} \right)^2$$ and $$|z - w_\mu|^2 = r_\mu^2 = p^2 + \mu^2$$. The square of the distance between the two centres is

$$
\begin{aligned} |w_\lambda - w_\mu|^2 &= \left| {1 + \lambda^2 \over 1 - \lambda^2}p - i\mu \right|^2 \\ &= \left({1 + \lambda^2 \over 1 - \lambda^2} \right)^2p^2 + \mu^2 \\ &= { 1 + 2\lambda^2 +\lambda^4 \over (1 - \lambda^2)^2}\,p^2+ \mu^2 \\ &= {1 - 2\lambda^2 + \lambda^4 \over (1 -\lambda^2)^2}\,p^2 + {4\lambda^2 \over (1 - \lambda^2)^2}\,p^2 + \mu^2 \\ &= \left({2\lambda p \over 1 - \lambda^2} \right)^2 + p^2 + \mu^2 \\ &= r_\lambda^2 + r_\mu^2 \end{aligned}
$$

Hence, for any $$\lambda$$ and $$\mu$$, by the converse of Pythagorean Theorem, the radii drawn to the points of intersection meet at right angle and the two circles $$C_\lambda$$ and $$S_\mu$$ intersects orthogonally.

## References

* [https://en.wikipedia.org/wiki/Apollonian\_circles](https://en.wikipedia.org/wiki/Apollonian\_circles)
* [https://www.cut-the-knot.org/Curriculum/Geometry/LocusCircle.shtml](https://www.cut-the-knot.org/Curriculum/Geometry/LocusCircle.shtml)
