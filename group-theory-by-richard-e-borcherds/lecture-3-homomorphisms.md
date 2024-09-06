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

When considering sets, functions are allowed to do anything, as we can map any element in domain to any element in codomain. However, as groups have some additional structure on top of sets, we are more interested in functions that respect/preserve the group structure, and they are called _homomophisms_.

### Definition of Homomophism

Let $$(G, \ast)$$ and $$(H, \times)$$ be groups. A function $$f$$ is a homomophism iff

$$
(\forall a, b \in G) \space f(a \ast b) = f(a) \times f(b)
$$

### Preservation of Identity

Homomophism has identity preserved, meaning

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
