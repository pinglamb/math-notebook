# Lecture 1 - Introduction

Prime number is the central concept of number theory, we begin our study by understanding more about primes.

## Prime Numbers

### Definition

A prime is an integer greater than $$1$$ that is divisible by no positive integers other than $$1$$ and itself. Therefore, they have exactly two divisors.

### The Infinitude of Primes

**\[Lemma] Every integer greater than** $$1$$ **has a prime divisor.**

\[Proof] Assume there are some integers greater than $$1$$ that have no prime divisors, by the Well-Ordering Principle, there is a smallest integer $$m$$ that satisfy that. We can see that $$m$$ cannot be prime otherwise it will be its own prime divisor, therefore $$m = ab$$ where $$1 < a, b < m$$. However, $$a$$ and $$b$$ are integers with prime divisors and their prime divisors are also prime divisors of $$m$$. It contradicts with the assumption and hence every integer greater than $$1$$ has a prime divisor.

**\[Theorem] There are infinitely many primes.**

[\[Proof\]](lecture-1-introduction.md#the-infinitude-of-primes) Assume there are finite number of primes, namely $$p_1, p_2, ..., p_n$$. Consider the number $$m = p_1p_2p_3...p_n + 1$$, by the above lemma, $$m$$ has a prime divisor. However, if any of the known prime  $$p_i$$ is a prime divisor of $$m$$, as $$p_i \space | \space p_1p_2p_3...p_n$$, $$p_i$$ has to divide $$1$$ which is impossible. Therefore, $$m$$ must have a divisor which is a new prime which contradicts with the assumption. Hence, there are infinitely many primes.

Be noted that $$m$$ itself is not necessary a prime, e.g. $$2 \cdot 3 \cdot 7 \cdot 43 + 1 = 1807 = 13 \cdot 139$$.

### Finding Primes

One of the way to find primes is called the [_sieve of Eratosthenes_](https://en.wikipedia.org/wiki/Sieve\_of\_Eratosthenes)_,_ which we list out integers from $$1$$ to $$n$$ and keep crossing out multiples of known primes one by one. We can stop when we reach $$\sqrt{n}$$ because of the following theorem:

**\[Theorem] If** $$m$$ **is a composite number,** $$m$$ **has a prime divisor not exceeding** $$\sqrt{n}$$**.**

\[Proof] As $$m$$ is composite, $$m = ab$$, We must have either $$a \le \sqrt{n}$$ or $$b \le \sqrt{n}$$, otherwise $$ab > (\sqrt{n})^2 > n$$. Hence, $$m$$ has a prime divisor $$\le \sqrt{n}$$.

### Mersenne Primes

Mersenne primes are primes of the form $$2^n - 1$$, where $$n$$ is prime. $$n$$ has to be a prime otherwise we can factorize the number as  $$2^{ab} - 1 = (2^a - 1)(2^{ab-a} + ...)$$. Not all prime number $$n$$ produces mersenne primes, e.g. $$2^{11} - 1 = 2047 = 23 \cdot 199$$.

### Fermat Primes

Fermat Primes are primes of the form $$2^{2^n} + 1$$. The exponent is $$2^n$$ because we can factorize $$2^{ab} + 1$$with $$a$$ odd. However, not all of them are primes, e.g. $$2^{2^5} + 1$$ is divisible by $$641$$.

### Prime Generator by Polynomials

There are no polynomials $$f(x)$$ that is always prime for every $$x$$ because if the constant term $$a_0 > 1$$, $$f(a_0)$$ is not a prime. If $$a_0 = 1$$, we can substitude $$x + k$$ such that the constant term is greater than $$1$$.

### Number of Primes

\[Definition] $$\pi(x)$$, where $$x$$ is a positive real number, is a function denotes the number of primes not exceeding $$x$$.

Gauss provides a close estimation of $$\pi(x)$$:

$$
\pi(x) \approx \frac{x}{log(x)}
$$

**\[The Prime Number Theorem] The ratio of** $$\pi(x)$$ **to** $$x/log(x)$$ **approaches** $$1$$ **as** $$x$$ **grows without bound.**

The proof involves the use of complex analysis.

## Fundamental Theorem of Arithmetic

Every positive integer greater than $$1$$ can be written uniquely as a product of primes up to orders.

The other way of expressing it by Euler is base on the following factorization of Riemann Zeta Function:

$$
\begin{aligned} \zeta(s) &= \frac{1}{1^s} + \frac{1}{2^s} + \frac{1}{3^s} + ... \\ &= \begin{aligned} &(1 + 1/2^s + 1/4^s + 1/8^s + ...) \\ &(1 + 1/3^s + 1/9^s + ...) \\ &(1 + 1/5^s + 1/25^s + ...) \, ... \end{aligned} \\ &= \frac{1}{1 - 2^{-s}}\frac{1}{1 - 3^{-s}}\frac{1}{1 - 5^{-s}} ... \end{aligned}
$$

As an example, as $$12 = 2^2 \cdot 3$$, we can see that $$1/12^s$$ is the product of the terms $$1/4^s$$, $$1/3^s$$ and many $$1$$s. Therefore, the above factorization is true when every integers can be written as product of primes.

It also implies that there are infinitely many primes because by substituding $$s = 1$$, $$\zeta(1)$$ is the harmonic series which is infinite. However, if there are finite number of terms, the factorized form will equal to a finite value. Hence, there are infinitely many primes.

## Diophantine Equations

Diophantine Equations are equations which the solutions have to come from the set of integers. Examples like $$x^2 + y^2 = z^2$$ (Pythagoras Equation), $$2x^2 = y^2$$ (Proof of $$\sqrt{2}$$ being irrational) and $$x^n +y^n = z^n$$ (Fermat Last Theorem).

Linear diophantine equation can be solved by the Euclidean Algorithm which will be discussed later.

## References

* [https://youtu.be/EzE6it9kAsI?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8](https://youtu.be/EzE6it9kAsI?list=PL8yHsr3EFj53L8sMbzIhhXSAOpuZ1Fov8)
* Kenneth H Rosen _Elementary Number Theory_, 2011 - Chapter 3
