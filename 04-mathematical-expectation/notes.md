# Ch. 4: Mathematical Expectation

## Mean of a Random Variable

- Expected Value of $X$:
  - Let $X$ be a random variable with a probability distribution $f(x)$. The *mean* or *expected value*:

```math
\mu = E(X) = \sum_{x} x f(x) \hspace{2em} \text{(if discrete)} \newline
\mu = E(X) = \int_{-\infty}^{\infty} x f(x)  dx \hspace{2em} \text{(if continuous)}
```

  - Example: We have a bag containing 3 red balls and 4 blue balls. If we're going to take 3 balls at the same time, find the expected value of the number of blue balls in this attempt.
    - The probability distribution:

```math
f(x) = \frac{\text{ways to take } x \text{ blue balls from 4 blue balls} \times \text{ways to take } 3-x \text{ red balls from 3 red balls}}{\text{ways to take 3 balls from 7 balls}}
\newline \hspace{1em} \newline
= \frac{\binom{4}{x} \binom{3}{3-x}}{\binom{7}{3}}, \hspace{2em} x = 0,1,2,3 
```

- - The mathematical expectation:

```math
E(X) = \sum_{0}^{3} x f(x) = (0)f(0) + (1)f(1) + (2)f(2) + (3)f(3) = \frac{12}{7}
``` 