# \[Proof] Multiplicativity of Euler Phi Function by Chinese Remainder Theorem

_Proof of_ $$\varphi(mn) = \varphi(m)\varphi(n)$$ _by Chinese Remainder Theorem._

Let $$m, n$$ be postive integers with $$(m, n) = 1$$, given

$$
\begin{align}x &\equiv a\enspace(mod \space m) \nonumber \\ x &\equiv b\enspace(mod\space n) \nonumber \end{align}
$$

By Chinese Remainder Theorem, there exists an unique congruence class $$[c]$$ (modulo $$mn$$), such that

$$
x \equiv c \enspace (mod \space mn)
$$

When $$a$$ is co-prime to $$m$$, as $$c \equiv a \space (mod \space m)$$, $$c$$ is also co-prime to $$m$$. Similarily, when $$b$$ is co-prime to $$n$$, $$c$$ is co-prime to $$n$$. As a result, $$c$$ is co-prime to $$mn$$.

Conversely, when $$c$$ is co-prime to $$mn$$, $$c$$ is co-prime to $$m$$ and $$n$$. As $$c \equiv a \space (mod \space m)$$ and $$c \equiv b \space (mod \space n)$$, $$a$$ is co-prime to $$m$$ and $$b$$ is co-prime to $$n$$.

It implies that $$(c, mn) = 1$$ $$\iff$$ $$(a, m) = 1$$ and $$(b, n) = 1$$, meaning for every pair of congruence classes $$[a]$$ and $$[b]$$ co-prime to $$m$$ and $$n$$ respectively maps to an unique congruence class $$[c]$$ that is co-prime to $$mn$$ and every $$[c]$$ co-prime to $$mn$$ has such mapping. Therefore, number of congruence classes co-prime to $$mn$$ is equal to number of congruence classes co-prime to $$m$$ multiplies by number of congruence classes co-prime to $$n$$, i.e.

$$
\varphi(mn) = \varphi(m)\varphi(n)
$$

* [https://www.youtube.com/watch?v=8I0z\_Lobtso\&t=1243s](https://www.youtube.com/watch?v=8I0z\_Lobtso\&t=1243s)

