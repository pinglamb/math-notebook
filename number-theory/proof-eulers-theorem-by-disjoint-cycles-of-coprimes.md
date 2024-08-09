# \[Proof] Euler's Theorem by Disjoint Cycles of Coprimes

_Proof of Euler's Theorem:_ $$a^{\varphi(m)} \equiv 1 \space (mod \space m)$$ _when_ $$(a, m) = 1$$_._

Let $$a, m$$ be integers with $$(a, m) = 1$$ and $${r_1, r_2, \mathellipsis, r_k}$$ be the residue classes co-prime to $$m$$, $$k = \varphi(m)$$. Consider the sequence of integers starting from $$1$$ and multiplying by $$a$$ until it repeats.

$$
1 \longrightarrow a = r_{1,1} \longrightarrow a^2 = r_{1,2} \longrightarrow \mathellipsis \longrightarrow 1
$$

The sequence only contains residue classes co-prime to $$m$$ as $$(a, m) = 1 \implies (a^n, m) = 1$$. As there are only $$k$$ residue classes co-prime to $$m$$, by Pigeonhole Principle, there must be 2 distinct powers $$x, y$$ of $$a$$ such that $$a^x \equiv a^y \space (mod \space m)$$, $$a^{x-y} \equiv 1 \space (mod \space m)$$. Therefore the above sequence must goes back to $$1$$ after some powers of $$a$$ and forms a cycle. If the sequence contains all $$k$$ residue classes, $$a^{\varphi(m)} \equiv 1$$.

Conside the case that the sequence doesn't include all the residuce classes, pick one $$r_{2, 1}$$ from the remaining to form similar sequence by starting from $$r_{2, 1}$$.

$$
r_{2,1} \longrightarrow r_{2,1}a = r_{2,2} \longrightarrow r_{2,1}a^2 = r_{2,3} \longrightarrow \mathellipsis \longrightarrow r_{2,1}
$$

We repeat this process until all $$r_i$$ belongs to one of sequence. We can see that all the sequences are disjoint because if any $$r_x = r_y$$ in 2 difference sequences, it implies that $$r_x a = r_y a, r_x a^2 = r_y a^2, \mathellipsis$$, which means the two sequence are the same. Also, we can derive from one sequence to another by multiplying every element of the sequence by $$r_x^{-1}r_y$$, which means all of them are of the same size.

Base of the above, we can conclude that the residue classes of $$m$$ co-prime to $$m$$ are forming disjoint sequences of the same size and one of them shows that $$a^x \equiv 1$$ for some $$x$$. It means $$ord(a) \space | \space \varphi(m)$$. Hence, $$a^{\varphi(m)} \equiv 1 \space (mod \space m)$$.

* [https://youtu.be/V4cB7t-zHxE?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=831](https://youtu.be/V4cB7t-zHxE?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=831)
