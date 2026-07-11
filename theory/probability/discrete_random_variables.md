## Random Variable: 
A random variable is defined as a function that assigns a real number to each possible outcome in the sample space of a random experiment. It provides a way toquantify the outcomes of the experiment and allows us to analyze and model random phenomena mathematically.

If $S$ is the sample space of a random experiment and $\tau$ is an outcome in $S$, then a random variable $X$ is a function that maps each outcome $\tau$ to a real number $X(\tau)$. The set of all possible values that the random variable can take is called the *range* or *support* of the random variable.

## Discrete Random Variable:
A discrete random variable is a type of random variable that can take on a countable number of distinct values. These values can be finite or countably infinite. Discrete random variables are often associated with experiments that have a finite or countably infinite number of possible outcomes, such as rolling a die


## Probability Mass Function (PMF):
The probability mass function (PMF) of a discrete random variable $X$ is a function that gives the probability that $X$ takes on a specific value. Formally, the PMF is defined as:

$$
P(X = x) = p(x)
$$

where $p(x)$ is the probability that the random variable $X$ equals the value $x$. The PMF must satisfy the following properties:

1. Non-negativity: $p(x) \geq 0$ for all $x$ in the range of $X$.
2. Normalization: The sum of the probabilities over all possible values of $X$ must equal 1:
3. The probability of any event can be calculated by summing the probabilities of the individual outcomes that make up that event. 

i.e
$$
P(X \in A) = \sum_{x \in A} p(x)
$$

## Expected Value & Moments:

The expected value of a discrete random variable $X$, denoted as $E[X]$ or $\mu_X$, is defined as the weighted sum of all possible values that the random variable can take. 
The weights are the probability masses of those values. For a discrete random variable, the expected value is given by:

$$
E[X] = \sum_{x \in \text{range of } X} x \cdot p(x)  \tag{1}
$$

## Properties of Expected Value:
1. Linearity: For any two discrete random variables $X$ and $Y$, and any constants $a$ and $b$, the expected value satisfies:
   $$
   E[aX + bY] = aE[X] + bE[Y]
   $$

2. Expected value of functions: If $g(X)$ is a function of the random variable $X$, then the expected value of $g(X)$ is given by:
   $$
   E[g(X)] = \sum_{x \in \text{range of } X} g(x) \cdot p(x)
   $$


## Variance of a Discrete Random Variable:

The deviation of a discrete random variable $X$ from its expected value is a measure of how much the values of $X$ differ from the mean.
The deviation can be either positive or negative, depending on whether the value of $X$ is above or below the expected value. 
To quantify the spread of the random variable's values around the mean, we consider the squared deviation, which is always non-negative.
The variance is defined as the expected value of the squared deviation of the random variable from its mean. It measures the spread or dispersion of the random variable's values around the expected value. The variance of a discrete random variable $X$, denoted as $\text{Var}(X)$ or $\sigma_X^2$, is given by:

$$
\text{Var}(X) = E[(X - E[X])^2] = \sum_{x \in \text{range of } X} (x - E[X])^2 \cdot p(x)  \tag{2}
$$

## TODO: Expected Value and Variance of the common discrete random variables (Bernoulli, Binomial, Geometric, Poisson, etc.):


## Conditional Probability Mass Function (Conditional PMF):

- How does the PMF of a discrete random variable change when we have additional information about the outcome of another random variable? 

This is where the concept of conditional probability mass function (conditional PMF) comes into play.

