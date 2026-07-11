# Sequential Experiments


## Binomial Probaility Law:

- In a sequence of n independent Bernoulli trials, where each trial has two possible outcomes (success or failure) and the probability of success is p, the probability of obtaining exactly k successes in n trials is given by the binomial probability formula:

$$
P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k} \quad \text{for } k = 0, 1, 2, ..., n  \tag{Eq.1}
$$

### Side Note: 
- Binomial Theorem: The binomial theorem states that for any positive integer n and any real numbers a and b, the expansion of $(a + b)^n$ can be expressed as:

$$
(a + b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^k    \tag{Eq.2}
$$

Q: Who came up with the binomial theorem?
A: Its a bit complicated. But the generalized version of the binomial theorem was first discovered by Sir Isaac Newton in the 17th century. However, the basic form of the binomial theorem was known to mathematicians in ancient India and Greece. The Indian mathematician Pingala (circa 3rd century BCE) is credited with discovering the binomial coefficients, which are used in the binomial theorem. The Greek mathematician Euclid (circa 300 BCE) also studied the binomial coefficients and their properties.



## Multinomial Probability Law:

Generalizing the binomial probability law, the multinomial probability law describes the probability of obtaining a specific combination of outcomes in a sequence of n independent trials, where each trial can result in one of k possible outcomes. The probability of obtaining counts $x_1, x_2, ..., x_k$ for each outcome is given by the multinomial probability formula:


## Geomteric Probability Law:

## Markov Chains

Consider the case when the sequence of experiments are not independent!