# Lecture 1 - Introduction

## Introduction

Group theory is an example of algebra. In algebra, instead of limiting our study to the manipulation of symbols (e.g. $$1 + 1, 2^n, ...$$), we allow the set of objects and operations to be anything, not just numbers. However, such a definition is too broad and therefore we categorize algebraic structures into different types, with _**groups**_ being one of them (and also _**rings**_, _**modules**_, ...).

In order to classify these structures, we need to have certain _**axioms**_, which say that the operations must follow certain rules, and the focus of group theory is the study of _**symmertries**_.

## Concrete Definition of Group

**A group is the set of symmetries of something, and symmetry of something is just a way of mapping something to itself perserving all the structures.**

To be more concrete, consider the symmetries of an equilateral triangles.

<figure><img src="../.gitbook/assets/equilateral-triangle.png" alt="" width="267"><figcaption><p>(From Dexter Chua's Notes)</p></figcaption></figure>

If we limit ourselves to preserve everything, we would only be allowed to do nothing. When studying the symmetries of the equilateral triangle, we only care about how the resultant objects look, but don't care about where the individual vertices went. Hence, we have six symmetries: three rotations (by $$0 \degree, 120 \degree, 240 \degree$$) and three reflections along the above axes. These six form the underlying set of the group of symmetries. With that, we can then define the operation being the combination of two symmetries to give a new symmetry, naturally meaning to do one after another, e.g. combining two $$120 \degree$$ rotation to get a $$240 \degree$$ rotation.

However, as we are studying algebra not geometry, we will abstract away the triangle and definite the group to have a set of six objects, say $$\{ e, r, r^2, s, rs, r^2s \}$$ ($$e$$ is doing nothing, $$r$$ is the rotation and $$s$$ is the reflection). Base on that, we can define rules about how we combine them by observing its properties.

First of all, the new symmetry we got after combining any two symmetries must be the same as one of the symmetry in the set. We say the group is "closed" with respect to the operation.

Secondly, we must have a "do nothing" symmetry, which when combined with another symmetry, the other symmetry is unchanged. It is called the identity element, normally named as $$1, 0$$ or $$e$$.

Thirdly, given a symmetry, we should have the reverse symmetry, which when combined the two together, we will end up "doing nothing", i.e. getting the identity element. It is called the inverse and normally named as $$a^{-1}$$.

Finally, let $$\ast$$ denote the group operation, given three symmetries, we can combine them, one after another, i.e. $$x \ast y \ast z$$. There are two ways to combine them, which are $$(x \ast y) \ast z$$ or $$x \ast (y \ast z)$$. However, intuitively they should yield the same result as we are always applying $$x$$ after $$y$$ after $$z$$, we have the associative rule $$(x \ast y) \ast z = x \ast (y \ast z)$$.

With the above, we can define the axioms of a group.

## Abstract Definition of Group - Group Axioms

**\[Definition of binary operation]** A (binary) operation is a ways of combining two elements to get a new element. Formally, it is a map $$\ast: S \times S \to S$$.

**\[Definition of Group]** A group is a set $$G$$ with a binary operation $$\ast$$ satifying the following axioms:&#x20;

1. **\[Closure]** For all $$a, b \in G$$, we have

$$
a \ast b \in G
$$

2. **\[Associativity]** For all $$a, b, c \in G$$, we have

$$
(a \ast b) \ast c = a \ast (b \ast c)
$$

3. **\[Identity]** There is a unique $$e \in G$$ such that for all $$a \in G$$, we have:

$$
a \ast e = e \ast a = a
$$

4. **\[Inverse]** For all $$a \in G$$, there is some $$a^{-1} \in G$$ such that:

$$
a^{-1} \ast a = a \ast a^{-1} = e
$$

Technically, the closure axiom is always true by the definition of binary operation $$\ast$$ so sometimes we will just omit it. However, in practice it is something we might have to check to make sure it is true.

The identity axiom can be replaced with a weaker statement that there exists $$e \in G$$ such that $$a \ast e = e \ast a = a$$ for all $$a \in G$$ and from that we will see $$e$$ is necessarily unique \[Proof]. Hence, in the proof of a group, we only need to show the existence of such $$e$$ without the need to show such $$e$$ is unique.

For the inverse axiom to be unambigious, we have to state the uniqueness of $$e$$ in the identity axiom. On the other hand, the notation $$a^{-1}$$ can only be unambigious if the inverse of $$a$$ is unique \[Proof].

To conlcude, we dervied the abstract notion of a group from its concrete notion by taking the combination of symmetries as the binary operation. Conversely, by [Cayley's Theorem](lecture-2-cayleys-theorem.md), we can show that these are the only axioms we need for a concrete group. Also, with this abstract definition, we can already study lots of properties about groups.

## Properties of Groups

With the above axioms, we can prove some of the properties about groups.

### Uniqueness of Identity

Suppose $$e$$ and $$e'$$ are the identities, for all $$a \in G$$, we have $$ae = ea = a$$ and $$ae' = e'a = e'$$. Hence, we have $$e' = e'e = ee' = e$$.

### Uniqueness of Inverse

Suppose $$b$$ and $$b'$$ are the inverses of $$a \in G$$, we have $$ba = ab = e$$ and $$b'a = ab' = e$$. Hence, $$b' = b'e = b'(ab) = (b'a)b = eb = b$$. Also, let $$a^{-1}$$ be the inverse of $$a$$, as $$(a^{-1})a =a(a^{-1}) = e$$, we can see that:

$$
(a^{-1})^{-1} = a
$$

### Inverse of ab

For $$a, b \in G$$, we have $$(b^{-1}a^{-1})ab = b^{-1}(a^{-1}a)b = b^{-1}eb = b^{-1}b = e$$ and $$ab(b^{-1}a^{-1}) = a(bb^{-1})a^{-1} = aea^{-1} = aa^{-1} = e$$, hence:

$$
(ab)^{-1} = b^{-1}a^{-1}
$$

### Cancellation Law

For $$a, b, c \in C$$, if $$ac = bc$$, then $$a = b$$ as $$(ac)c^{-1} = (bc)c^{-1}$$. Similarily, if $$ca = cb$$, then $$a = b$$.

From that, we can derive that the equation $$ax = b$$ has a unique solution, namely $$a^{-1}b$$. Similarily, for $$xa = b$$, the unique solution is $$ba^{-1}$$. Suppose $$x_1$$ and $$x_2$$ are the solutions, we have $$ax_1 = b = ax_2$$, by cancellation law, we have $$x_1 = x_2$$ and hence the solution is unique.

Also, for equation $$x^2 = x$$, as $$x^2 = xx = x = xe$$, by cancellation law, $$x = e$$ is the only solution.

## Commutative/Abelian Group

The commutative property, which is for all $$a, b \in G$$, $$a \ast b = b \ast a$$, is not included as an axiom of group. Groups with such property are called _**commutative**_ or _**abelian**_ groups.

For example, let $$G$$ be the set of the functions $$f(x) = ax + b$$ and $$f \ast g$$ be the binary operation $$f(g(x))$$. Let $$f(x) = ax + b$$, $$g(x) = cx + d$$ and $$h(x) = ex + f$$.

Firstly, $$G$$ is closed with respect to $$\ast$$, as

$$
(f \ast g)(x) =f(g(x)) = a(cx + d) + b = (ac)x + (ad + b) \in G
$$

Secondly, $$G$$ is associative with repsect to $$\ast$$, as

$$
\begin{aligned} (f \ast (g \ast h))(x) &= a(cex + cf + d) + b \\ &= acex + acf + ad + b \\ &= ac(ex + f) + ad + b \\ &= ((f \ast g) \ast h)(x) \end{aligned}
$$

Thirdly, $$e(x) = x$$ satisfies $$(e \ast f)(x) = (f \ast e)(x) = f(x)$$ for all $$f \in G$$.

Finally, for all $$f \in G$$,

$$
f^{-1}(x) = (1/a)x - b/a
$$

&#x20;is the inverse as $$(f^{-1} \ast f)(x) = (1/a)(ax + b) - b/a = x = e(x)$$ and $$(f \ast f^{-1})(x) = a((1/a)x - b/a) + b = x = e(x)$$.

Hence, $$(G, \ast)$$ is a group. However, as $$(g \ast f)(x) = c(ax + b) + d = (ac)x + cb + d \not = (f \ast g)(x)$$, $$(G, \ast)$$ is not abelian.

## Goals of Group Theory

1. Classify all groups (up to isomorphism)
2. Classify all the ways a group is symmetries of something (Representation Theory)

## References

* [https://youtu.be/RnqwFpyqJFw?list=PL8yHsr3EFj51pjBvvCPipgAT3SYpIiIsJ](https://youtu.be/RnqwFpyqJFw?list=PL8yHsr3EFj51pjBvvCPipgAT3SYpIiIsJ)
* Alan F. Beardon, Algebra and Geometry, 2005 - Section 1.2 (P2)
* [Dexter Chua, Part IA - Groups, 2014 - Chapter 0](https://dec41.user.srcf.net/notes/IA\_M/groups.pdf)
