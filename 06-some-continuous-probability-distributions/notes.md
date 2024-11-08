# Ch. 6: Some Continuous Probability Distribution


## Continuous Uniform Distributions

![Continuous Uniform Distributions](https://upload.wikimedia.org/wikipedia/commons/9/96/Uniform_Distribution_PDF_SVG.svg)

- Density function of the continuous uniform random variable $X$ on the interval $[A, B]$

```math
f(x; A, B) = 
\begin{cases}
    \frac{1}{B-A},& A \leq x \leq B \\
    0,              & \text{elsewhere}
\end{cases}
```

- Example: Suppose that a large conference room at a certain company can be reserved for no more than 4 hours. Both long and short conference occur quite often. In fact, it can be assumed that the length $X$ of a conference has a uniform distribution on the interval [0, 4].
  - What is the probability density function?

```math
f(x) = 
\begin{cases}
    \frac{1}{4},& 0 \leq x \leq 4 \\
    0,              & \text{elsewhere}
\end{cases}
```

-  - What is the probability that any given conference last at least 3 hours?

```math
P[X \geq 3] = \int_{3}^{4} \frac{1}{4} dx = \frac{1}{4}
```

- Mean of continuous uniform distributions

```math
\mu = \frac{A+B}{2}
```

- Variance of continuous uniform distributions

```math
\sigma^{2} = \frac{(B-A)^2}{12}
```

## Normal Distributions

![Normal Distribution](https://upload.wikimedia.org/wikipedia/commons/7/74/Normal_Distribution_PDF.svg)

- The most important continuous probability distribution in statistic: Normal Distribution
  - Approximately describes many phenomena that occur in nature, industry, and research
  - Equation of normal curve was first developed by Abraham DeMoivre
  - Often referred as Gaussian distribution in honor of Karl Friedrich Gauss (1777-1855) who derived its equation from a study of errors in repeated measurements of the same quantity
  - Enormous application as limiting distribution
- Density of the normal random variable $X$, with mean $\mu$ and variance $\sigma^2$:

```math
n(x;\mu, \sigma) = \frac{1}{\sqrt{2 \pi} \sigma} e^{-\frac{1}{2 \sigma^2} \left(x - \mu \right)^2}, \hspace{1em} - \infty < x < \infty
```

- Mean of normal distributions

```math
\mu
```

- Variance of normal distributions

```math
\sigma^{2}
```

## Areas under Normal Curve

- This integral is difficult to solve

```math
P\left( x_{1} \leq X \leq x_{2} \right) = \int_{x_1}^{x_2} n(x; \mu, \sigma) dx = \frac{1}{\sqrt{2 \pi} \sigma} \int_{x_1}^{x_2} e^{-\frac{1}{2 \sigma^2} (x- \mu)^2} dx
```

so we need a _tabulation of normal curve areas_ for quick reference.

- For any normal random variable $X$, we can transform it into a new normal random variable $Z$ with mean 0 and variance 1

```math
Z = \frac{X - \mu}{\sigma}
```

Therefore,

```math
P\left( x_{1} \leq X \leq x_{2} \right) = \int_{z_1}^{z_2} e^{-\frac{1}{2} z^2} dz = \int_{z_1}^{z_2} n(z; 0, 1) dz = P\left( z_{1} \leq Z \leq z_{2} \right)
```

- Standard Normal Distribution: the distribution of a normal random variable with mean 0 and variance 1
- Example: An electrical firm manufactures light bulbs that have a life, before burn-out, that is normally distributed with mean equal to 800 hours and a standard deviation of 40 hours. Find the probability that a bulb burns between 778 and 834 hours.

```math
\mu = 800; \sigma 40; x_1 = 778; x_2 = 834; z_1 = \frac{774-800}{40} = -0.55; z_2 = \frac{834-800}{40} = 0.85
```

Hence by looking up the value of area under normal curve with z < -0.55 and z < 0.85,

```math
P( 778 < X < 834) = P(-0.55 < Z < 0.85) = P(Z < 0.85) - P(Z < -0.55) = 0.8023 - 0.2912 = 0.5111 \approx 51\%
```

## Normal Approximation to Binomial

- If $X$ is a binomial random variable with mean $\mu = np$ and variance $\sigma^2 = npq$, then the limiting distribution of $Z = \frac{X - np}{\sqrt{npq}}$ as $n \rightarrow \infty$, is the _standard normal distribution_ $n(z;0, 1)$
- Let $X$ be a binomial random variable with parameters $n$ and $p$. For large $n$, $X$ has approximately a normal distribution with $\mu = np$ and $\sigma^2 = npq = np(1-p)$ and

```math
P(X \leq x) = \sum_{k=0}^{x} b(k;n,p) \approx \text{ area under normal curve to the left of } x + 0.5 = P \left(Z \leq \frac{x + 0.5 - np}{\sqrt{npq}} \right)
```

and the approximation will be good if $np$ and $n(1-p)$ are greater than or equal to 5

## Gamma and Exponential Distributions

### Gamma Distribution

![Gamma Distributions](https://upload.wikimedia.org/wikipedia/commons/e/e6/Gamma_distribution_pdf.svg)

- Exponential and gamma distributions play an important role in both queuing theory and reliability problems
  - Example: time between arrivals at service facilities, time to failure of component parts, etc
- Gamma function

```math
\Gamma (\alpha) = \int_{0}^{\infty} x^{\alpha - 1} e^{-x} dx, \hspace{1em} \text{for } \alpha > 0
```

- Properties of gamma function
  1. $\Gamma (n) = (n-1)(n-2) \cdots (1) \Gamma(1)$
  2. $\Gamma (n) = (n-1)!$ for a positive integer $n$
  3. $\Gamma (1) = 1$
  4. $\Gamma (1/2) = \sqrt{\pi}$

- The continuous random variable $X$ has a gamma distribution, with parameters $\alpha$ and $\beta$, if its density function is given by 

```math
f(x; \alpha, \beta) = \begin{cases}
\frac{1}{\beta^\alpha \Gamma(\alpha)} x^{\alpha - 1} e^{-x/\beta},& x > 0 \\
0,& \text{elsewhere}
\end{cases}
```

where $\alpha > 0$ and $\beta > 0$.

- Mean of gamma distribution

```math
\mu = \alpha \beta
```

- Variance of gamma distribution

```math
\sigma^{2} = \alpha \beta^2
```

### Exponential Distribution

- Exponential distribution: gamma distribution which $\alpha = 1$
- The continuous random variable $X$ has an exponential distribution, with parameter $\beta$, if its density function is given by 

```math
f(x; \beta) = \begin{cases}
\frac{1}{\beta} e^{-x/\beta},& x > 0 \\
0,& \text{elsewhere}
\end{cases}
```

where $\beta > 0$.

- Mean of beta distribution

```math
\mu = \beta
```

- Variance of beta distribution

```math
\sigma^{2} = \beta^2
```

### Relationship to Poisson Process

- The probability of no events occuring in the span up to time $t$ is given by this Poisson distribution

```math
p(0;\lambda t) = \frac{e^{-\lambda t} (\lambda t)^0}{0!} = e^{-\lambda t}
```

- This is the same as the probability of a first Poisson event occurance where the time $X$ exceed $x$, the time when no events occurs

```math
P(X > x) = e^{-\lambda x}
```

- Thus, the cumulative distribution function for $X$ is given by

```math
P(0 \leq X \leq x) = 1 - e^{-\lambda x}
```

- To obtain the exponential distribution form, we differentiate the cumulative distribution function

```math
f(x) = \frac{d \left(1 - e^{-\lambda x} \right)}{dx} = \lambda e^{-\lambda x}
```

which is the same as the density function of the exponential distribution with $\lambda = 1/\beta$

### Application of the Exponential and Gamma Distributions

- Cases examples
  - In reliability theory, where equipment failure often conforms to this Poisson process, $\beta$ is called mean time between failures
  - In analyzing equipment breakdowns, which follows Poisson process
  - In biomedical experiments, to analyze survival time
  - In analyzing computer response time

### The Memoryless Property and Its Effect on the Exponential Distribution

- Analogy: "If the component 'makes it' to $t_0$ hours, the probability of lasting an additional $t$ hours is the same as the probability of lasting $t$ hours. There is no 'punishment' through wear that may have ensued for lasting the first $t_0$ hours"
- If gradual or slow wear happens, then the exponential does not apply
  - Use gamma or Weibull distribution instead