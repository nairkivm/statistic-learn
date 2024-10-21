# Ch. 4: Mathematical Expectation

- [Ch. 4: Mathematical Expectation](#ch-4-mathematical-expectation)
  - [Mean of a Random Variable](#mean-of-a-random-variable)
  - [Variance and Covariance of Random Variables](#variance-and-covariance-of-random-variables)
  - [Means and Variance of Linear Combination of Random Variables](#means-and-variance-of-linear-combination-of-random-variables)
  - [Chebyshev's Theorem](#chebyshevs-theorem)

## Mean of a Random Variable

- Expected Value of $X$:
  - Let $X$ be a random variable with a probability distribution $f(x)$. The *mean* or *expected value*:

```math
\mu = E(X) = \sum_{x} x f(x) \hspace{2em} \text{(discrete)}
```

```math
\mu = E(X) = \int_{-\infty}^{\infty} x f(x)  dx \hspace{2em} \text{(continuous)}
```

  - Example: We have a bag containing 3 red balls and 4 blue balls. If we're going to take 3 balls at the same time, find the expected value of the number of blue balls in this attempt.
    - The probability distribution:

```math
f(x) = \frac{\text{ways to take } x \text{ blue balls from 4 blue balls} \times \text{ways to take } 3-x \text{ red balls from 3 red balls}}{\text{ways to take 3 balls from 7 balls}}
```

```math
= \frac{\binom{4}{x} \binom{3}{3-x}}{\binom{7}{3}}, \hspace{2em} x = 0,1,2,3 
```

- - The mathematical expectation:

```math
E(X) = \sum_{0}^{3} x f(x) = (0)f(0) + (1)f(1) + (2)f(2) + (3)f(3) = \frac{12}{7}
``` 

- Expected value of $g(X)$:

```math
\mu_{g(X)} = E[g(X)] = \sum_{x} g(x) f(x) \hspace{2em} \text{(discrete)}
```

```math
\mu_{g(X)} = E[g(X)] = \int_{-\infty}^{\infty} g(x) f(x)  dx \hspace{2em} \text{(continuous)}
```

- Expected value of $g(X, Y)$:

```math
\mu_{g(X, Y)} = E[g(X, Y)] = \sum_{x}\sum_{y} g(x, y) f(x, y) \hspace{2em} \text{(discrete)}
```

```math
\mu_{g(X, Y)} = E[g(X, Y)] = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x, y) f(x, y)  dx dy \hspace{2em} \text{(continuous)}
```

## Variance and Covariance of Random Variables

- Variance of the probability distribution of $X$
  - Symbol: $\text{Var} X$, $\sigma_{X}^{2}$, $\sigma^{2}$
  - Let $X$ be a random variable with a probability distribution $f(x)$ and mean $\mu$. The *variance* of $X$:

```math
\sigma^{2} = E \left[ \left(X - \mu \right)^{2} \right] = \sum_{x} \left(x - \mu \right)^{2} f(x)  \hspace{2em} \text{(discrete)}
```

```math
\sigma^{2} = E \left[ \left(X - \mu \right)^{2} \right] = \int_{-\infty}^{\infty} \left(x - \mu \right)^{2} f(x) dx  \hspace{2em} \text{(continuous)}
```

  -  Alternative: 

```math
\sigma^{2} = E(X^2) - \mu^2
```

- Variance of $g(X)$

```math
\sigma_{g(X)}^{2} = E \left\{ \left[g(X) - \mu_{g(X)} \right]^{2} \right\} = \sum_{x} \left[g(x) - \mu_{g(x)} \right]^{2} f(x)  \hspace{2em} \text{(discrete)}
```

```math
\sigma_{g(X)}^{2} = E \left\{ \left[g(X) - \mu_{g(X)} \right]^{2} \right\} = \int_{-\infty}^{\infty} \left[g(x) - \mu_{g(x)} \right]^{2} f(x) dx  \hspace{2em} \text{(continuous)}
```

- Covariance of $(X, Y)$

```math
\sigma_{XY} = E \left[ \left(X - \mu_{X} \right) \left(Y - \mu_{Y} \right) \right] = \sum_{x} \sum_{y} \left(x - \mu_{X} \right) \left(y - \mu_{Y} \right) f(x, y)  \hspace{2em} \text{(discrete)}
```

```math
\sigma_{XY} = E \left[ \left(X - \mu_{X} \right) \left(Y - \mu_{Y} \right) \right] = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} \left(x - \mu_{X} \right) \left(y - \mu_{Y} \right) f(x, y) dx dy  \hspace{2em} \text{(continuous)}
```

- - Covariance is a measure of the nature of the association between two random variables
    - Positive -> larger X, results in larger Y
    - Negative -> larger X, results in smaller Y
    - Zero -> statistically independent or non linear relationship
- - Alternative:

```math
\sigma_{XY} = E(XY) - \mu_{X} \mu_{Y}
```

- Correlation coefficient ($\rho_{XY}$)
  - Scale-free version of the covariance -> measure the strength of the relationship
  - Range: $-1 \leq \rho_{XY} \leq 1$

```math
\rho_{XY} = \frac{\sigma_{XY}}{\sigma_{X} \sigma_{Y}}
```

## Means and Variance of Linear Combination of Random Variables

- Type I:

```math
E(aX + b) = a E(X) + b
```

- Type II:

```math
E \left[ g(X) \pm h(X) \right] = E \left[ g(X) \right] \pm E \left[ h(X) \right]
```

- Type III:

```math
E \left[ g(X, Y) \pm h(X, Y) \right] = E \left[ g(X, Y) \right] \pm E \left[ h(X, Y) \right]
```

- Type IV:

```math
E \left[ g(X) \pm h(Y) \right] = E \left[ g(X) \right] \pm E \left[ h(Y) \right]
```

- Type V:

```math
E(XY) = E(X) E(Y)
```

- Linear combination on variance

```math
\sigma_{aX+bY+c}^{2} = a^2 \sigma_{X}^{2} + b^2 \sigma_{Y}^{2} + 2ab \sigma_{XY}
```

- Approximation of $E[g(X)]$

```math
E[g(X)] \approx g(\mu_{X}) + \left. \frac{\partial^{2} g(x)}{\partial x^2} \right|_{x= \mu_{X}} \frac{\sigma_{X}^{2}}{2}
```

- Approximation of $Var[g(X)]$

```math
Var[g(X)] \approx \left[ \frac{\partial g(x)}{\partial x} \right]_{x= \mu_{X}}^{2} \sigma_{X}^{2}
```

## Chebyshev's Theorem

> The probability that any random variable $X$ will assume a value within $k$ standard deviations of the mean is at least $1 - 1/k^2$. That is,

```math
P \left( \mu - k \sigma < X < \mu + k \sigma \right) \geq 1 - \frac{1}{k^2}
```

- This theorem helps us to estimate a mean without knowledge of distribution function shape