# \[Proof] Gauss's Generation of Wilson's Theorem

_Proof of the product of all the positive integers less than_ $$m$$ _and relatively prime to_ $$m$$ _is congruent to_ $$1 \space (mod \space m)$$_, unless_ $$m = 4, p^t, 2p^t$$_, where_ $$p$$ _is an odd prime and_ $$t$$ _is positive integer, in which case it is congruent to_ $$-1 \space (mod \space m)$$_, i.e._

$$
\prod_{(a, m) = 1} a \equiv \begin{cases} -1 &\text{if } m = 4, p^t, 2p^t \space \text{where } p \text{ is odd prime} \\ 1 &\text{otherwise} \end{cases}
$$

Wilson's Theorem is the special case $$(p-1)! \equiv -1 \space (mod \space p)$$ when $$p$$ is odd prime.

The idea behind the proof is similar to that of Wilson's Theorem, which is by pairing the positive integers $$a, b$$ less than $$m$$ and co-prime to $$m$$ in which $$ab \equiv 1 \space (mod \space m)$$, such that we can omit those pairs while calculating the product. The only integers we need to care about are those with inverse being itself, i.e. $$x^2 \equiv 1 \space (mod \space m)$$. By studying the number of solutions in different cases we can evaluate the product above.

When $$m = p^t$$, the congruence $$x^2 \equiv 1 \space (mod \space p^t)$$ implies $$x^2 - 1 = (x + 1)(x - 1) \equiv 0 \space (mod \space p^t)$$. Hence, $$p^t \space | \space (x + 1)(x-1)$$. Assume $$p \space | \space (x + 1)$$ and $$p \space | \space (x - 1)$$, as $$(x + 1) - (x - 1) = 2$$, $$p \space | \space 2$$, which is false as $$p$$ is odd prime. Hence, $$p^t$$ can only divides one of them, meaning $$p^t \space | \space (x+1)$$ or $$p^t \space | \space (x - 1)$$. It means $$x \equiv \pm 1 \space (mod \space p^t)$$ are the only solutions to $$x^2 \equiv 1 \space (mod \space p^t)$$.

When $$m = 2^t$$, the congruence $$x^2 \equiv 1 \space (mod \space 2^t)$$ has 1 solution $$x \equiv 1 \space (mod \space 2)$$ when $$t = 1$$ and 2 solution  $$x \equiv \pm 1 \space (mod \space 4)$$ when $$t = 2$$. When $$t > 2$$, similarily the congruence implies $$2^t \space | \space (x+1)(x-1)$$. As $$(x + 1) - (x - 1) = 2$$, we have $$2 \space | \space (x + 1)$$ and $$2^{t-1} \space | \space (x - 1)$$ or $$2 \space | \space (x - 1)$$ and $$2^{t-1} \space | \space (x + 1)$$. It means $$x = 2^{t-1}q + 1$$ or $$x = 2^{t-1}q - 1$$. When $$q = 2n$$, we have $$x \equiv \pm 1 \space (mod \space 2^t)$$, and when $$q = 2n + 1$$, we have $$x \equiv 2^{t-1} \pm 1 \space (mod \space 2^t)$$, as $$x \equiv 2^{t-1} - 1 \equiv 2^{t-1} - 2^t - 1 \equiv -(2^{t-1} + 1) \space (mod \space 2^t)$$, we have $$x \equiv \pm (2^{t-1} + 1) \space (mod \space 2^t)$$. Hence, there are in total 4 solutions.

When $$m = 2^{t_0}p_1^{t_1}p_2^{t_2}...p_r^{t_r}$$, solving $$x^2 \equiv 1 \space (mod \space m)$$ is equivalent to solving the system of congruences $$x^2 \equiv 1 \space (mod \space 2^{t_0}), x^2 \equiv 1 \space (mod \space p_1^{t_1}), ..., x^2 \equiv 1 \space (mod \space p_r^{t_r})$$. From the above, each congruence modulo $$p_i^{t_i}$$ has 2 solutions and it has $$2^k$$ solutions modulo $$2^{t_0}$$ with $$k = 0$$ when $$t_0 = 0, 1$$ and $$k = 1$$ when $$t_0 = 2$$ and $$k = 2$$ when $$t_0 > 2$$. Hence, by Chinese Remainder Theorem, the congruence modulo $$m$$ has $$2^{r + k}$$ solutions. Also, the solutions are in pairs of $$x$$ and $$-x$$ and $$(x)(-x) \equiv -x^2 \equiv -1 \space (mod \space m)$$.

From the above result, the product will be only congruent to $$-1$$ modulo $$m$$ when there are exactly 2 solutions for $$x^2 = 1 \space (mod \space m)$$, meaning $$r + k = 1$$, which implies $$m = 4, p^t, 2p^t$$. For the other cases, when $$r + k = 0$$, meaning $$m = 1, 2$$, $$\prod_{(a, m) = 1} a \equiv 1 \space (mod \space m)$$. When $$r + k \ge 2$$, $$\prod_{(a, m) = 1} a \equiv (-1)^{2^{r+k-1}} \equiv [(-1)^2]^{2^{r+k-2}} \equiv 1 \space (mod \space m)$$ as well.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Exercise 4.2.15 (P161), 4.2.16 (P161), 4.3.34 (P170), 6.1.44 (P224)
* [https://youtu.be/3JBaDZqtgug?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=1218](https://youtu.be/3JBaDZqtgug?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=1218)
