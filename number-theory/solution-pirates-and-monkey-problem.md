# \[Solution] Pirates and Monkey Problem

**Problem**

Three pirates with a monkey have an unknown number of bananas and they would like to split them. At night, one of the pirate wakes up and split the bananas into 3 groups with 1 left, he gives that to the monkey and keeps his own share. The second and third pirates did the same and each time they do it, there is 1 extra that they give to the monkey. In the morning, they split the remaining bananas into 3 groups and gives the 4th banana to the moneky. What is the minimum number of bananas that can satify the above?



**Solution**

Let $$x$$ be the number of bananas,

After the first split, there are $$\frac{2}{3}(x - 1) = \frac{2}{3}x - \frac{2}{3}$$ bananas left.

After the second split, there are $$\frac{2}{3}(\frac{2}{3}x - \frac{2}{3} - 1) = \frac{4}{9}x - \frac{10}{9}$$ bananas left.

After the third split, there are $$\frac{2}{3}(\frac{4}{9}x - \frac{10}{9} - 1) = \frac{8}{27}x - \frac{38}{27}$$ bananas left.

For the final split to be able to happen,

$$
\frac{8}{27}x - \frac{38}{27} \equiv 1 \enspace (mod \space 3)
$$

$$
8x - 38 \equiv 27 \enspace (mod \space 81)
$$

$$
8x \equiv 65 \enspace (mod \space 81)
$$

As the inverse of 8 modulo 81 is $$71$$71, $$x \equiv 65 * 71 \equiv 79 \space (mod \space 81)$$, so the minimum number of bananas is 79.
