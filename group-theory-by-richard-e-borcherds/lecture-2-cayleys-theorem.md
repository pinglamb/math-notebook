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

## References

* [https://youtu.be/AZUDhtnz-Do](https://youtu.be/AZUDhtnz-Do?list=PL8yHsr3EFj51pjBvvCPipgAT3SYpIiIsJ)
* Alan F. Beardon, Algebra and Geometry, 2005 - Section 1.3 (P6)
