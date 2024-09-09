# Lecture 3 - Homomorphisms

## Functions

Before studying the relations between groups, we first revise the definition of functions and some of its properties.

### Defintion of Function

Given $$X, Y$$ be two sets, a function $$f: X \to Y$$ maps $$x \in X$$ to _exactly one_ $$y \in Y$$. $$X$$ is called the _domain_ and $$Y$$ is called the _codomain_.

We can compose two functions by applying one after another, e.g. let $$f: X \to Y$$ and $$g: Y \to Z$$ be two functions, then $$g \circ f: X \to Z$$ is a function with $$(g \circ f)(x) = g(f(x))$$.

### Injection, Surjection and Bijection

A function $$f$$ is _injective_ if it maps everything in $$Y$$ at most once, i.e.

$$
(\forall x, y \in X) \space f(x) = f(y) \implies x = y
$$

A function $$f$$ is surjective if it maps everything in $$Y$$ at least once, i.e.

$$
(\forall y \in Y, \exists x \in X) \space f(x) = y
$$

A function $$f$$ is bijective if it is both injective and surjective, i.e. it hits everything exactly once. A function has inverse $$f^{-1}$$ iff $$f$$ is bijective.

## Homomorphisms

When considering sets, functions are allowed to do anything, as we can map any element in domain to any element in codomain. However, as groups have some additional structure on top of sets, we are more interested in functions that respect/preserve the group structure, and they are called _homomorphisms_.

### Definition of Homomorphism

Let $$(G, \ast)$$ and $$(H, \times)$$ be groups. A function $$f$$ is a homomorphism iff

$$
(\forall a, b \in G) \space f(a \ast b) = f(a) \times f(b)
$$

### Preservation of Identity

Homomorphism has identity preserved, meaning

$$
f(e_G) = e_H
$$

where $$e_G$$ and $$e_H$$ are the identity of $$G$$ and $$H$$ repsectively. It is because $$f(e_G) = f(e_G \ast e_G) = f(e_G) \times f(e_G)$$ and it is only possible when $$f(e_G) = e_H$$ (the only solution to $$x \ast x = x$$ is $$e$$).

### Preservation of Inverse

Also, the inverse is also preserved, meaning

$$
f(a^{-1}) = f(a)^{-1}
$$

It is because $$e_H = f(e_G) = f(a \ast a^{-1}) = f(a) \times f(a^{-1})$$. Similarily, we have $$e_H = f(a^{-1}) \times f(a)$$. Hence, $$f(a^{-1}) = f(a)^{-1}$$.

### Image of Homomorphism

Let $$f: G \to H$$ be a homomorphism, then the _image_ of $$f$$ is

$$
\text{im} \, f = f(G) = \{ f(g): g \in G\}
$$

, which is a subgroup of $$H$$. It is of the same definition as the _image/codomain_ of a function.

### Kernel of Homomorphism

Let $$f: G \to H$$ be a homomorphism, then the _kernel_ of $$f$$ is

$$
\text{ker} \, f = f^{-1}(\{ e_H \}) = \{ g \in G : f(g) = e_H\}
$$

, which is a subgroup of $$G$$. It contains the elements in $$G$$ which maps to identity of $$H$$.

Also, for any $$a \in G$$, for all $$k \in \text{ker} \, f$$, we have

$$
f(aka^{-1}) = f(a)f(k)f(a^{-1}) = e_H
$$

Hence, $$aka^{-1} \in \text{ker} \, f$$ and $$\text{ker} \, f$$ is a _normal subgroup_ of $$G$$. We will discuss properties of normal subgroups later.

## Isomorphisms

Isomorphisms are bijective homomorphisms. Two groups $$G$$ and $$H$$ are isomorphic if there exists an isomorphism between them, denoted as $$G \cong H$$. Also, the inverse of isomorphism $$f^{-1}: H \to G$$ is also an isomorphism.

Isomorphic groups are considered to be "the same", except the elements and operations are being relabeled.

## Endomorphisms and Automorphisms

Endomorphisms are homomorphisms that has the same domain as codomain, meaning it is a mapping to itself. Automorphisms are isomorphisms that are also endomorphic.

Automorphism can be throught of a symmetry of the group as it is a bijection to itself preserving the structure. Hence, a set of automorphisms is also a group as it is symmetries of something.

## Examples

TODO
