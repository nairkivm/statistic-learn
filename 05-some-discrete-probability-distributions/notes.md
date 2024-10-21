# Ch. 5: Some Discrete Probability Distribution

```mermaid
mindmap
    root(Discrete Probability Distributions)
        Binomial
        Multinomial
        Hypergeometric
        Negative binomial
        Geometric
        Poisson
```

## Binomial and Multinomial Distributions

### Binomial Distributions

- Bernoulli process (process that results in one of two outcomes: success or failure)
  - The experiment consists of repeated trials
  - Each trial results in an outcome that may be classified as a success or failure
  - The probability of success ($p$) remains constants from trial to trial
  - The repeated trials are independent
- Binomial distributions
  - A Bernoulli trial can result in a sucess with probability $p$ and a failure with $q = 1 - p$
  - Then the probability distributions of the binomial random variable $X$, the number of successes in $n$ independent trials, is

```math
b(x; n, p) = \binom{n}{x} p^{x} q^{n-x}, \hspace{2em} x = 0, 1, 2, \cdots, n
```

- Binomial sum ($P (X < r)$)

```math
B(r; n, p) = \sum_{x=0}^{r} b(x; n, p)
```

- Example: A large chain retailer purchases a certain kind of electronic device from a manufacturer. The manufacturer indicates that the defective rate of the device is 3%. The inspector randomly picks 20 items from a shipment. What is the probability that there will be at least one defective item among these 20?

```math
P(X \geq 1) = 1 - P(X = 0) = 1 - b(0; 20, 0.03) = 0.4562
```

- Mean of the binomial distribution $b(x; n, p)$

```math
\mu = np
```

- Variance of the binomial distribution $b(x; n, p)$

```math
\sigma^2 = npq
```

### Multinomial distributions

- Multinomial distributions
  - If a given trial can result in the $k$ outcomes $E_1, E_2, \cdots, E_k$ with probabilities $p_1, p_2, \cdots, p_k$, then the probability distribution of the random variable $X_1, X_2, \cdots, X_k$, representing the number of the occurences in $n$ independent trials is

```math
f(x_1, x_2, \cdots, x_k; p_1, p_2, \cdots, p_k) = \binom{n}{x_1, x_2, \cdots, x_k} p_{1}^{x_{1}} p_{2}^{x_{2}} \cdots p_{k}^{x_{k}}
```

```math
\text{with } \sum_{i=1}^{k} x_{i} = n \text{ and } \sum_{i=1}^{k} p_{i} = 1
```


- Example: For a certain airport with three runaways, it is known that in the ideal setting the following are the probabilities that the individual runways are accessed by a randomly arriving commercial jet.
  - Runway 1: $p_1 = 2/9$
  - Runway 2: $p_2 = 1/6$
  - Runway 3: $p_3 = 11/18$

- What is the probability that 6 randomly arriving airplanes are distributed in the following manners.
  - Runway 1: 2 airplanes
  - Runway 2: 1 airplanes
  - Runway 3: 3 airplanes

```math
f \left( 2, 1, 3 ; \frac{2}{9} \frac{1}{6} \frac{11}{18} \right) = 0.1127
```

##
