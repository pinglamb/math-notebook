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

In geometry, the projection of $$\bold{b}$$ onto $$\bold{a}$$ is the part of $$\bold{b}$$ that is parallel to $$\bold{a}$$, denoted by $$\bold{b}^{\perp}$$. When $$0 \le \theta \le \pi/2$$, $$|\bold{b}^{\perp}| = |\bold{b}| \cos \theta$$ and $$\bold{b}^{\perp}$$ is in same direction as $$\bold{a}$$, Therefore,

$$
\bold{b}^{\perp} = (|\bold{b}|\cos\theta)\,\bold{\hat{a}}
$$

When $$\pi / 2 < \theta \le \pi$$, $$|\bold{b}^{\perp}| = |\bold{b}| \cos (\pi - \theta)$$ and $$\bold{b}^{\perp}$$ is in opposite direction as $$\bold{a}$$. Therefore,

$$
\bold{b}^{\perp} = \left(-|\bold{b}|\cos(\pi -\theta)\right)\,\bold{\hat{a}} = (|\bold{b}|\cos\theta)\,\bold{\hat{a}}
$$

Hence,&#x20;

$$
\bold{b}^{\perp} = |\bold{b}|{\bold{b} \cdot \bold{a} \over |\bold{b}||\bold{a}|}\bold{\hat{a}} = {\bold{b} \cdot \bold{a} \over |\bold{a}|^2}\bold{a} = (\bold{b} \cdot \bold{\hat{a}})\,\bold{\hat{a}}
$$

### Properties

Base on the definiton, we can see that scalar multiplication is _commutative_, i.e.

$$
\bold{a} \cdot \bold{b} = \bold{b} \cdot \bold{a}
$$

A scalar product of a vector with itself is always $$\ge 0$$

$$
\bold{a} \cdot \bold{a} = |\bold{a}|^2 \ge 0
$$

with equality holds if and only if $$\bold{a} = \bold{0}$$.

If $$\bold{a} \cdot \bold{b} = 0$$ and $$\bold{a} \not = \bold{0}$$ and $$\bold{b} \not = \bold{0}$$, then $$\bold{a} \perp \bold{b}$$ and $$\theta = \pi/2$$.

### Linearity in the Arguments

From the definition, we can see that for $$\lambda \in \R$$,

$$
\bold{a} \cdot (\lambda\bold{b}) = (\lambda \bold{a}) \cdot \bold{b} = \lambda(\bold{a} \cdot \bold{b})
$$

According to the following graph,

<figure><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/aa/Dot_product_distributive_law.svg/320px-Dot_product_distributive_law.svg.png" alt=""><figcaption></figcaption></figure>

We can see that $$\bold{b}^{\perp} + \bold{c}^{\perp} = (\bold{b} + \bold{c})^{\perp}$$. Hence,

$$
\begin{aligned} {\bold{a} \cdot \bold{b} \over |\bold{a}|^2}\bold{a} + {\bold{a} \cdot \bold{c} \over |\bold{a}|^2}\bold{a} &= {\bold{a} \cdot (\bold{b} + \bold{c}) \over |\bold{a}|^2}\bold{a} \\ (\bold{a} \cdot \bold{b} + \bold{a} \cdot \bold{c})(\bold{a} \cdot \bold{a}) &= [\bold{a} \cdot (\bold{b} + \bold{c})](\bold{a} \cdot \bold{a}) \\ \bold{a} \cdot \bold{b} + \bold{a} \cdot \bold{c} &= \bold{a} \cdot (\bold{b} + \bold{c})\end{aligned}
$$

Combining the above, we have what we called _linearity in the second argument_,

$$
\bold{a} \cdot (\lambda \bold{b} + \mu \bold{c}) = \lambda \bold{a} \cdot \bold{b} + \mu \bold{a} \cdot \bold{c}
$$

In fact, as scalar multiplication of vectors in real vector spaces is commutative, we also have linearity in the first argument (which might not be true in other vector spcaes).

## Vector Product

## Bases and Components

## Vector Equations

## Lines, Planes and Spheres

## References

* [Stephen J. Cowley _Algebra and Geometry Lectures Notes_, 2006 - Chapter 2](https://www.damtp.cam.ac.uk/user/sjc1/teaching/AandG/notes.pdf)
* [https://math.stackexchange.com/questions/1109142/proving-that-the-dot-product-is-distributive](https://math.stackexchange.com/questions/1109142/proving-that-the-dot-product-is-distributive)
