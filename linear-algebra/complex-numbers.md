# Complex Numbers

## Definition

A complex number is a number $$z \in \Complex$$ of the form $$z = a + bi$$ with $$a, b \in \R$$. We called $$a = \text{Re}(z)$$ the real part and $$b = \text{Im}(z)$$ the imaginary part.

## Basic Arithmetic

Let $$z_1 = a + bi$$ and $$z_2 = c + di$$, we have:

### Addition and Subtraction

Similar to vector addition,

$$
z_1 + z_2 = (a + c) + (b + d)i
$$

Geometrically, it can be thought as two vectors on the complex plane with the sum of them being the vector formed by joining them head to tail.

We can see that $$(\Complex, +)$$ forms a group with identity $$0$$ and additive inverse $$(-a) + (-b)i$$. Subtraction is defined as adding the additive inverse, hence

$$
z_1 - z_2 = (a - c) + (b - d)i
$$

### Multiplication and Division

Given $$i^2 = -1$$, we get the following by expanding the terms:

$$
z_1z_2 = (ac - bd) + (ad + bc)i
$$

$$(\Complex, \times)^\ast$$ is also a group with identity $$1$$. To find the inverse, we need to find $$c, d$$  in terms of $$a, b$$ such that $$ac - bd = 1$$ and $$ad + bc = 0$$. Hence,

$$
z^{-1} = {1 \over z} = {a \over a^2 + b^2} + {-b \over a^2 + b^2}i
$$

Division is defined as multiplying the inverse

$$
{z_1 \over z_2} = z_1z_2^{-1}
$$

## Complex Conjugate

### Definition

The complex conjugate $$\bar{z}$$ of $$z = a + bi$$ is

$$
\bar{z} = a - bi
$$

Geometrically, $$z$$ and $$\bar{z}$$ are mirror images of each other in the real axis.

Also, base on definition, we have

$$
\overline{(\overline{z})} = z
$$

### Properties

Conjugation is _distributive_ over addition, subtraction, multiplication and division, hence

$$
\begin{aligned} \overline{z_1 \pm z_2} &= \overline{z_1} \pm \overline{z_2} \\ \overline{z_1z_2} &= \overline{z_1} \cdot \overline{z_2} \\ \overline{{z_1 \over z_2}} &= {\overline{z_1} \over \overline{z_2}} \end{aligned}
$$

From the above, we can conclude the following as well

$$
\begin{aligned} \overline{z^{-1}} &= (\overline{z})^{-1} \\ \overline{z^n} &= (\overline{z})^n \end{aligned}
$$

Also, base on the definition, we have

$$
z\bar{z} = a^2 + b^2
$$

which is always real and non-negative.

With that, we can convert complex fraction to a complex number by

$$
{ z_1 \over z_2} = {z_1 \over z_2} \cdot {\overline{z_2} \over \overline{z_2}} = {ac + bd \over c^2 + d^2} + {bc - ad \over c^2 + d^2}i
$$

## Modulus

### Definition

The _modulus_ $$|z|$$ of $$z$$ is defined by

$$
|z| = \sqrt{a^2 + b^2}
$$

which is the length of line segment from $$0$$ to $$z$$.

### Properties

From the definition, we can see that

$$
\begin{aligned} |\bar{z}| &= |z| \\ z\overline{z} &= |z|^2 \\ |z_1z_2| &= |z_1||z_2|  \end{aligned}
$$

Geometrically, $$|z_1 - z_2|$$ **is the distance between the two points** $$z_1$$ **and** $$z_2$$. We have the following inequalities about modulus:

$$
\begin{aligned} |\text{Re}(z)| &\le |z| \\ |\text{Im}(z)| &\le |z| \\ |z_1 + z_2 + ... + z_n| &\le |z_1| + |z_2| + ... + |z_n| \\ |z_1 - z_3| &\le |z_1 - z_2| + |z_2 + z_3| \\ ||z_1| - |z_2|| &\le |z_1 \pm z_2| \end{aligned}
$$

## Argument

### Definition

The _argument_ $$\arg(z)$$ of $$z$$ is defined by

$$
\arg(z) = \tan^{-1}\left({b \over a}\right)
$$

which is the angle $$\theta$$ between the positive real axis and the line segment from $$0$$ to $$z$$ measured in the anti-clockwise direction.

$$\arg(z)$$ has a period of $$2\pi$$ and $$\tan^{-1}$$ is single valued on the interval $$(-{\pi \over 2}, {\pi \over 2})$$, the following formula gives the principle value of $$\theta \in (-\pi, \pi]$$:

$$
\theta = 2\tan^{-1} \left( {b \over a + |z|} \right)
$$

### Properties

With the polar form, we can later see that

$$
\begin{aligned} \arg(z_1z_2) &= \arg(z_1) + \arg(z_2) \\ \arg(z^{-1}) &= \arg(\bar{z}) = - \arg(z) \end{aligned}
$$

## References

* Alan F. Beardon, Algebra and Geometry, 2005 - Chapter 3
