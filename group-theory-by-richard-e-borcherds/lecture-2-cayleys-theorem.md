# Lecture 2 - Cayley's Theorem

This lecture is around the study of the converse that groups axioms are the only axioms we need to define a concrete group, which is a set of symmetries of something.

## Permutations

A _permutation_ of a set $$X$$ is an invertible map $$f: X \to X$$, in other words, a bijection from $$X$$ to itself. The product of permutations is the same as composition of functions, $$gf(x) = g(f(x))$$.

The set of all permutations on $$X$$ is denoted as $$\text{Sym} \, X$$. $$\text{Sym} \, X$$ **forms a group with respect to composition of functions**. We prove that by group axioms:

* \[Associativity] Composition of functions is always associative
* \[Closure] Suppose $$f$$ and $$g$$ are two permutations, as $$g^{-1}f^{-1}$$ is the inverse of $$fg$$, $$fg \in X$$
* \[Identity] The identity map $$I_X: X \to X$$ is a permutation and $$fI_X = I_Xf = f$$
* \[Inverse] As $$f$$ is a bijection, $$f^{-1}$$ exists with $$(f^{-1})^{-1} = f$$, therefore $$f^{-1} \in X$$

A symmetric group $$S_n$$ is the group of permutations of a set $$X$$ with finite size $$|X| = n$$ (usually $$X = \{ 1, 2, 3, ..., n \}$$), i.e. $$\text{Sym} \, X = S_n$$. $$n$$ is the degree of $$S_n$$ (which is different from _order_).

## Group Actions

The intuitive way of interpreting group $$G$$ acts on a set $$X$$ is that $$G$$ is a group of some permutations of $$X$$. However, we can attain greater flexibility by defining group action as an homomorphism $$\theta$$ of $$G$$ onto some group $$\Gamma$$ of permutations of $$X$$. This means $$\theta$$ turns every element $$g \in G$$ into a permutation of $$X$$, in a way that respects the group structure, i.e. $$g(x)$$ actually means $$(\theta(g))(x)$$. If $$G$$ happens to be a group of permutations of $$X$$, we can take $$\theta$$ to be the identity map from $$G$$ to itself.

## References

* [https://youtu.be/AZUDhtnz-Do](https://youtu.be/AZUDhtnz-Do?list=PL8yHsr3EFj51pjBvvCPipgAT3SYpIiIsJ)
* Alan F. Beardon _Algebra and Geometry_, 2005 - Section 1.3 (P6), Section 14.5 (P303)
* [Dexter Chua _Part IA - Groups_, 2014 - Chapter 2.1](https://dec41.user.srcf.net/notes/IA\_M/groups.pdf)
