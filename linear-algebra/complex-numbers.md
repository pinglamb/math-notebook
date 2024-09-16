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

### Properties

Conjugation is _distributive_ over addition, subtraction, multiplication and division, hence

$$
\begin{aligned} \overline{z_1 \pm z_2} &= \overline{z_1} \pm \overline{z_2} \\ \overline{z_1z_2} &= \overline{z_1} \cdot \overline{z_2} \\ \overline{{z_1 \over z_2}} &= {\overline{z_1} \over \overline{z_2}} \\ \overline{z^{-1}} &= (\overline{z})^{-1} \end{aligned}
$$

Also, base on the definition, we have

$$
z\bar{z} = a^2 + b^2
$$

which is real and non-negative.

With that, we can convert complex fraction to a complex number by

$$
{ z_1 \over z_2} = {z_1 \over z_2} \cdot {\overline{z_2} \over \overline{z_2}} = {ac + bd \over c^2 + d^2} + {bc - ad \over c^2 + d^2}i
$$

