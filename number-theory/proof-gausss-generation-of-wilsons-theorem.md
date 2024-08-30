# \[Proof] Gauss's Generation of Wilson's Theorem

_Proof of the product of all the positive integers less than_ $$m$$ _and relatively prime to_ $$m$$ _is congruent to_ $$1 \space (mod \space m)$$_, unless_ $$m = 4, p^n, 2p^n$$_, where_ $$p$$ _is an odd prime and_ $$n$$ _is positive integer, in which case it is congruent to_ $$-1 \space (mod \space m)$$_, i.e._

$$
\prod_{(a, m) = 1} a \equiv \begin{cases} -1 &\text{if } m = 4, p^n, 2p^n \space \text{where } p \text{ is odd prime} \\ 1 &\text{otherwise} \end{cases}
$$

Wilson's Theorem is the special case $$(p-1)! \equiv -1 \space (mod \space p)$$ when $$p$$ is odd prime.

## Wilson's Theorem and $$x^2 \equiv 1 \space (mod \space m)$$

The idea behind the proof is similar to that of Wilson's Theorem, which is by pairing the positive integers $$a, b$$ less than $$m$$ and co-prime to $$m$$ in which $$ab \equiv 1 \space (mod \space m)$$, such that we can omit those pairs while calculating the product. The only integers we need to care about are those with inverse being itself, i.e. $$x^2 \equiv 1 \space (mod \space m)$$. By studying the number of solutions in different cases we can evaluate the product above.

When $$m = p^n$$, the congruence $$x^2 \equiv 1 \space (mod \space p^n)$$ implies $$x^2 - 1 = (x + 1)(x - 1) \equiv 0 \space (mod \space p^n)$$. Hence, $$p^n \space | \space (x + 1)(x-1)$$. Assume $$p \space | \space (x + 1)$$ and $$p \space | \space (x - 1)$$, as $$(x + 1) - (x - 1) = 2$$, $$p \space | \space 2$$, which is false as $$p$$ is odd prime. Hence, $$p^n$$ can only divides one of them, meaning $$p^n \space | \space (x+1)$$ or $$p^n \space | \space (x - 1)$$. It implies $$x \equiv \pm 1 \space (mod \space p^n)$$ are the only solutions to $$x^2 \equiv 1 \space (mod \space p^n)$$.

When $$m = 2^m$$, the congruence $$x^2 \equiv 1 \space (mod \space 2^m)$$ has only one solution $$x \equiv 1 \space (mod \space 2)$$ for $$n = 1$$ and two solutions  $$x \equiv \pm 1 \space (mod \space 4)$$ when $$n = 2$$. When $$n > 2$$, similarily the congruence implies $$2^n \space | \space (x+1)(x-1)$$. As $$(x + 1) - (x - 1) = 2$$, we have $$2 \space | \space (x + 1)$$ and $$2^{n-1} \space | \space (x - 1)$$ or $$2 \space | \space (x - 1)$$ and $$2^{n-1} \space | \space (x + 1)$$. It means $$x = 2^{n-1}q + 1$$ or $$x = 2^{n-1}q - 1$$. When $$q$$ is even, we have $$x \equiv \pm 1 \space (mod \space 2^n)$$, and when $$q$$ is odd, we have $$x \equiv 2^{n-1} \pm 1 \space (mod \space 2^n)$$, as $$x \equiv 2^{n-1} - 1 \equiv 2^{n-1} - 2^n - 1 \equiv -(2^{n-1} + 1) \space (mod \space 2^n)$$, we have $$x \equiv \pm (2^{n-1} + 1) \space (mod \space 2^n)$$. Hence, there are in total 4 solutions.

When $$m = 2^{n_0}p_1^{n_1}p_2^{n_2}...p_r^{n_r}$$, solving $$x^2 \equiv 1 \space (mod \space m)$$ is equivalent to solving the system of congruences $$x^2 \equiv 1 \space (mod \space 2^{n_0}), x^2 \equiv 1 \space (mod \space p_1^{n_1}), ..., x^2 \equiv 1 \space (mod \space p_r^{n_r})$$. From the above, each congruence modulo $$p_i^{n_i}$$ has 2 solutions and it has $$2^k$$ solutions modulo $$2^{n_0}$$ with $$k = 0$$ when $$n_0 = 0, 1$$ and $$k = 1$$ when $$n_0 = 2$$ and $$k = 2$$ when $$n_0 > 2$$. Hence, by Chinese Remainder Theorem, the congruence modulo $$m$$ has $$2^{r + k}$$ solutions. Also, the solutions are in pairs of $$x$$ and $$-x$$ and $$(x)(-x) \equiv -x^2 \equiv -1 \space (mod \space m)$$.

From the above result, the product will be only congruent to $$-1$$ modulo $$m$$ when there are exactly 2 solutions for $$x^2 = 1 \space (mod \space m)$$, meaning $$r + k = 1$$, which implies $$m = 4, p^n, 2p^n$$. For the other cases, when $$r + k = 0$$, meaning $$m = 1, 2$$, $$\prod_{(a, m) = 1} a \equiv 1 \space (mod \space m)$$. When $$r + k \ge 2$$, $$\prod_{(a, m) = 1} a \equiv (-1)^{2^{r+k-1}} \equiv [(-1)^2]^{2^{r+k-2}} \equiv 1 \space (mod \space m)$$ as well.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Exercise 4.2.15 (P161), 4.2.16 (P161), 4.3.34 (P170), 6.1.44 (P224)
* [https://youtu.be/3JBaDZqtgug?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=1218](https://youtu.be/3JBaDZqtgug?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8\&t=1218)

## Wilson's Theorem and Primitive Roots

We can also prove the generalization using primitive roots. Let $$g$$ be an primitive root modulo $$m$$, which exists when $$m = 4, p^n$$ and $$2p^n$$, we can express all the $$\varphi(m)$$ integers relatively prime to $$m$$ and less than $$m$$ by powers of $$g$$, i.e. $$g^1, g^2, ... g^{\varphi(m)}$$. By multiplying them all together, we will get $$g^{\varphi(m)(\varphi(m) + 1)/2}$$. As $$g^{\varphi(m) / 2} \equiv -1 \space (mod \space m)$$, we have $$g^{\varphi(m)(\varphi(m) + 1)/2} \equiv (-1)^{\varphi(m) + 1} \equiv -1\space (mod \space m)$$ as $$\varphi(m) + 1$$ for $$m > 2$$ is always odd.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Exercise 9.3.14 (P368)

## Primitive Roots and $$x^2 \equiv 1 \space (mod \space m)$$

From the above, we can see that the integer $$m$$ has primitive roots if and only if the only solutions of the congruence $$x^2 \equiv 1 \space (mod \space m)$$ are $$x \equiv \pm 1 \space (mod \space m)$$. If the congruence has more than 2 solutions, then the integer $$m$$ does not have primitive roots.

Let $$g$$ be a primitive root modulo $$m$$, we can express all the $$\varphi(m)$$ integers relatively prime to $$m$$ and less than $$m$$ by powers of $$g$$, i.e. $$g^0, g^1, ..., g^{\varphi(m)-1}$$. Let $$x \equiv g^n\space (mod \space m)$$, where $$0 \le n \le \varphi(m) - 1$$, we have $$x^2 \equiv g^{2n} \space (mod \space m)$$, therefore $$ord_m(g) = \varphi(m) \space | \space 2n$$. Hence, $$n = k(\varphi(m) / 2)$$ for some integer $$k$$ and $$x = g^n = (g^{(\varphi(m) / 2)})^k \equiv (-1)^k \equiv \pm 1 \space (mod \space m)$$.

Conversely, if $$m$$ does not have primitive roots, $$m$$ is not of the form $$1, 2, 4, p^n$$ and $$2p^n$$. From the above, we can see that $$x^2 \equiv 1 \space (mod \space m)$$ has more than 2 solutions.

* Kenneth H Rosen _Elementary Number Theory_, 2011 - Exercise 9.3.13 (P368)
