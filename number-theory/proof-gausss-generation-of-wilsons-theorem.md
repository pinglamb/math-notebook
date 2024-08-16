# \[Proof] Gauss's Generation of Wilson's Theorem

_Proof of the product of all the positive integers less than_ $$m$$ _and relatively prime to_ $$m$$ _is congruent to_ $$1 \space (mod \space m)$$_, unless_ $$m = 4, p^t, 2p^t$$_, where_ $$p$$ _is an odd prime and_ $$t$$ _is positive integer, in which case it is congruent to_ $$-1 \space (mod \space m)$$_, i.e._

$$
\prod_{(a, m) = 1} a \equiv \begin{cases} -1 &\text{if } m = 4, p^t, 2p^t \space \text{where } p \text{ is odd prime} \\ 1 &\text{otherwise} \end{cases}
$$

Wilson's Theorem is the case when $$p$$ is odd prime and $$t = 1$$, hence $$(p-1)! \equiv -1 \space (mod \space p)$$.

The idea behind to proof is similar to that of Wilson's Theorem, which is by pairing the positive integers $$a, b$$ less than $$m$$ and co-prime to $$m$$ in which $$ab \equiv 1 \space (mod \space m)$$, such that we can omit those pairs in the final product. The only integers we need to care about are those with inverse being itself, i.e. $$x^2 \equiv 1 \space (mod \space m)$$. By studying the number of solutions in different cases we can evaluate the product above.

When $$m = 2$$, $$(1) \equiv 1 \space (mod \space 2)$$.

When $$m = 4$$, $$(1)(3) = 3 \equiv -1 \space (mod \space 4)$$.

When $$m = p^t$$, the congruence $$x^2 \equiv 1 \space (mod \space p^t)$$ implies $$x^2 - 1 = (x + 1)(x - 1) \equiv 0 \space (mod \space p^t)$$. Hence, $$p^t \space | \space (x + 1)(x-1)$$. Assume $$p \space | \space (x + 1)$$ and $$p \space | \space (x - 1)$$, as $$(x + 1) - (x - 1) = 2$$, $$p \space | \space 2$$, which is false as $$p$$ is odd prime. Hence, $$p^t$$ can only divides one of them, meaning $$p^t \space | \space (x+1)$$ or $$p^t \space | \space (x - 1)$$. It means $$x \equiv \pm 1 \space (mod \space p^t)$$ are the only solutions to $$x^2 \equiv 1 \space (mod \space p^t)$$, so $$\prod_{(a, m) = 1} a = (1)(-1) \equiv -1 \space (mod \space p^t)$$.

