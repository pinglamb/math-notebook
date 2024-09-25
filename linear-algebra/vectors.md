# Vectors

The discussion here focuses on vectors in 2D and 3D spaces, i.e. $$\R^2$$ and $$\R^3$$. It begins from defining vectors and various operations among them geometrically. It then can be extended to algebraic definitions and generalized to the concept of [vector spaces](vector-spaces.md).

## Definition

In $$\R^2$$ and $$\R^3$$, a vector is a quantity that is specified by a \[positive] _magnitude_ and a _direction_ in space. A vector $$\bold{v}$$ is represented geometrically as a line segment $$\vec{AB}$$ with magnitude $$|\bold{v}|$$ and with direction from $$A$$ to $$B$$. With a chosen origin $$O$$, every point $$P$$ in 2D/3D space has a position vector $$\bold{x} = \vec{OP}$$.

When $$|\bold{v}| = 0$$, we have the zero/null vector, denoted by $$\bold{0}$$.

When $$|\bold{v}| \not= 0$$, a unit vector is a vector in the same direction as $$\bold{v}$$ with magnitude equals to $$1$$, denoted by $$\bold{\hat{v}}$$. Hence,

$$
\bold{\hat{v}} = {\bold{v} \over |\bold{v}|}
$$

## Vector Addition

Vectors add according to the Parallelogram Law of Addition,

$$
\bold{a} + \bold{b} = \bold{c} \iff \vec{OA} + \vec{OB} = \vec{OC}
$$

where $$OACB$$ is a parallelogram.

### Properties

As $$\vec{OA} = \vec{BC}$$ and $$\vec{OB} = \vec{AC}$$ (opposite sides of the parallelogram),

$$
\vec{OC} = \vec{OA} + \vec{AC} = \vec{OB} + \vec{BC}
$$

Hence, vector addition is _commutative_, i.e.

$$
\bold{a} + \bold{b} = \bold{b} + \bold{a}
$$

Geometrically we can deduce that vector addition is _associative_, i.e.

$$
\bold{a} + (\bold{b} + \bold{c}) = (\bold{a} + \bold{b}) + c
$$

The _null/zero vector_ $$\bold{0}$$ is the _additive identity_, i.e.

$$
\bold{a} + \bold{0} = \bold{0} + \bold{a} = \bold{a}
$$

The _inverse_ of $$\bold{a}$$, namely $$-\bold{a}$$, is a vector parallel to $$\bold{a}$$ with same magitude, i.e. $$|-\bold{a}| = |\bold{a}|$$, but opposite direction, and we have

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

### Properties

Geometrically, we can see that multiplication by scalars is _distributive_ over vector addition

$$
\begin{aligned} (\lambda + \mu)\bold{a} &= \lambda\bold{a} + \mu\bold{a} \\ \lambda (\bold{a} + \bold{b}) &= \lambda\bold{a} + \lambda\bold{b} \end{aligned}
$$

and _associative_

$$
\lambda(\mu\bold{a}) = (\lambda\mu)\bold{a}
$$

and has _multiplicative identity_ $$1$$

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

## Scalar Product

Let $$A, B, C$$ be the vertices and $$\alpha = \angle BAC$$ of a triangle in 2D, according to Cosine Law we have

$$
|CB|^2 = |AB|^2 + |AC|^2 - 2|AB||AC|\cos\alpha
$$

By putting them in vector terms, let $$\bold{a} = \vec{AB}$$ and $$\bold{b} = \vec{AC}$$, we have $$\vec{CB} = \bold{a} - \bold{b}$$. Hence,

$$
|\bold{a} - \bold{b}|^2 = |\bold{a}|^2 + |\bold{b}|^2 - 2|\bold{a}||\bold{b}|\cos\alpha
$$

The scalar/dot product of two vectors $$\bold{a}$$ and $$\bold{b}$$ is defined to be the scalar number

$$
\bold{a} \cdot \bold{b} = |\bold{a}| |\bold{b}|\cos\theta
$$

where $$0 \le \theta \le \pi$$ is the non-reflex angle between $$\bold{a}$$ and $$\bold{b}$$ once they are placed "tail to tail" or "head to head".

Later on we can see that with such definition, we have (which is consistent with binomial expansion)

$$
(\bold{a} - \bold{b})^2 = (\bold{a} - \bold{b}) \cdot (\bold{a} - \bold{b}) = \bold{a} \cdot \bold{a} + \bold{b} \cdot \bold{b} - 2(\bold{a} \cdot \bold{b})
$$

\[TODO Geometric meaning]

### Properties

Base on the definiton, we can see that it is _commutative_, i.e.

$$
\bold{a} \cdot \bold{b} = \bold{b} \cdot \bold{a}
$$

A scalar product of a vector with itself is always $$\ge 0$$

$$
\bold{a} \cdot \bold{a} = |\bold{a}|^2 \ge 0
$$

with equality holds if and only if $$\bold{a} = \bold{0}$$.

\[TODO Linearity Property]
