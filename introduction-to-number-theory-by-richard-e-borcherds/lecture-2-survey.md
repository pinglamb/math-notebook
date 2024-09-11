# Lecture 2 - Survey

## Congruences

### Definition

$$a \equiv b \, (mod \, m)$$ means $$a - b$$ is divisible by $$m$$, i.e. $$a - b = mq$$ for some integer $$q$$.

### Fermat's Theorem

$$a^p \equiv a \, (mod \, p)$$ or $$a^{p-1} \equiv 1 \, (mod \, p)$$ if $$a$$ is not divisible by $$p$$.

### Euler's Theorem

$$a^{\varphi(m)} \equiv 1 \, (mod \, m)$$ if $$(a, m) = 1$$, where $$\varphi(m)$$ is the number of integers less than $$m$$ that are relatively prime to $$m$$.

## Quadratic Equations

### Quadratic Residues

If $$x^2 \equiv a \, (mod \, p)$$ has a solution, $$a$$ is called a quadratic residue of $$p$$.

### Legendre Symbol

Let $$p$$ be an odd prime and $$a$$ be an integer not divisible by $$p$$,

$$
\left( {a \over p} \right) = \begin{cases} 1 &\text{if } a  \text{ is quadratic residue of } p \\ -1 & \text{otherwise} \end{cases}
$$

### Quadratic Reciprocity

Let $$p$$ and $$q$$ be distinct odd primes,

$$
\left( {p \over q} \right) \left( {q \over p} \right) = (-1)^{{p - 1 \over 2}{q - 1 \over 2}}
$$

## References

* [https://youtu.be/mduJOLdKrak?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8](https://youtu.be/mduJOLdKrak?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8)
