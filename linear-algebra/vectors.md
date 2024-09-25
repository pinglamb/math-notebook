# Vectors

The discussion here focuses on vectors in 2D and 3D spaces, i.e. $$\R^2$$ and $$\R^3$$. It begins from defining vectors and various operations among them geometrically. It then can be extended to algebraic definitions and generalized to the concept of [vector spaces](vector-spaces.md).

## Definition

In $$\R^2$$ and $$\R^3$$, a vector is a quantity that is specified by a \[positive] _magnitude_ and a _direction_ in space. A vector $$\bold{v}$$ is represented geometrically as a line segment $$\vec{AB}$$ with magnitude $$|\bold{v}|$$ and with direction from $$A$$ to $$B$$. With a chosen origin $$O$$, every point $$P$$ in 2D/3D space has a position vector $$\bold{x} = \vec{OP}$$.

## Vector Addition

Vectors add according to the Parallelogram Law of Addition,

$$
\bold{a} + \bold{b} = \bold{c} \iff \vec{OA} + \vec{OB} = \vec{OC}
$$

where $$OACB$$ is a parallelogram.

As $$\vec{OA} = \vec{BC}$$ and $$\vec{OB} = \vec{AC}$$ (opposite sides of the parallelogram),

$$
\vec{OC} = \vec{OA} + \vec{AC} = \vec{OB} + \vec{BC}
$$

Hence, vector addition is _commutative_, i.e.

$$
\bold{a} + \bold{b} = \bold{b} + \bold{a}
$$

Geometrically we can deduce that vector addition is associative, i.e.

$$
\bold{a} + (\bold{b} + \bold{c}) = (\bold{a} + \bold{b}) + c
$$

The null/zero vector $$\bold{0}$$ is a vector with zero magnitude, i.e. $$|\bold{0}| = 0$$, we have

$$
\bold{a} + \bold{0} = \bold{0} + \bold{a} = \bold{a}
$$

The inverse of $$\bold{a}$$, namely $$-\bold{a}$$, is a vector parallel to $$\bold{a}$$ with same magitude, i.e. $$|-\bold{a}| = |\bold{a}|$$, but opposite direction, and we have

$$
\bold{a} + (-\bold{a}) = (-\bold{a}) + \bold{a} = \bold{0}
$$

We can therefore define subtraction by

$$
\bold{b} - \bold{a} = \bold{b} + (-\bold{a})
$$

According to the above, the set of $$\R^2$$/$$\R^3$$ vectors form a abelian group under addition.

## Multiplication by Scalars

Let $$\bold{a}$$ be an vector and $$\lambda \in \R$$, $$\lambda\bold{a}$$ is defined as a vector parallel to $$\bold{a}$$, with magnitude $$|\lambda| |\bold{a}|$$ and same direction as $$\bold{a}$$ when $$\lambda > 0$$ and opposite direction to $$\bold{a}$$ when $$\lambda < 0$$.

Geometrically, we can see that multiplication by scalars is distributive over vector addition

$$
\begin{aligned} (\lambda + \mu)\bold{a} &= \lambda\bold{a} + \mu\bold{a} \\ \lambda (\bold{a} + \bold{b}) &= \lambda\bold{a} + \lambda\bold{b} \end{aligned}
$$

and associative

$$
\lambda(\mu\bold{a}) = (\lambda\mu)\bold{a}
$$

and has identity $$1$$

$$
1\bold{a} = \bold{a}
$$

When $$\lambda = 0$$, since $$0|\bold{a}| = 0$$,  we have

$$
0\bold{a} = \bold{0}
$$

When $$\lambda = -1$$, since $$|(-1)\bold{a}| = |-1| |\bold{a}| = |a|$$ and is of oppositie direction as $$\bold{a}$$, by definition,

$$
(-1)\bold{a} = -\bold{a}
$$
