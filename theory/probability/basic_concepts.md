## Random Experiment

A random experiment is an experiment in which the outcome varies in an unpredictable manner whenever it is repeated under the same conditions.

It is specified by: 
- An experimental procedure that can be repeated,
- A set of one or more possible outcomes

Examples of random experiments are: 
- 


## Samples - L1

An outcome or sample point of an experiment is a result that cannot be decomposed into simpler components. 
For example, in a coin toss, the outcome can be either heads or tails. In a dice roll, the outcome can be any of the numbers 1 through 6.

The set of all possible outcomes of a random experiment is called the *Sample Space*. It is usually denoted by the symbol S.

A sample space can either be finite, countably infinite, or uncountably infinite.

## Events - L2

An event is defined as a subset of the sample space. 
It is a collection of one or more outcomes of a random experiment. 
For example, in a dice roll, the event "rolling an even number" consists of the outcomes {2, 4, 6}.

TODO: Certain event and null event.

## Event classes - L3
 An event class is a collection of events that share certain properties or characteristics. Essentially, it is a "set of sets"! 
 Q: What are the events to which a probability can be assigned and satisfy the axioms of probability?
 A: The events to which a probability can be assigned and satisfy the axioms of probability are called *measurable events*. These events form a σ-algebra (sigma-algebra) over the sample space, which is a collection of subsets of the sample space that includes the sample space itself, is closed under complementation, and is closed under countable unions.
 Todo: 
  - Need to understand more about σ-algebra and measurable events.
  - Need to understand the Banach-Tarski paradox and how it motivates the study of measure theory.
  - The need for measure theory and other advanced concepts arises from the fact that sometimes the sample space can be uncountably infinite, and we need a rigorous way to assign probabilities to events in such cases. For the countablly finite and countably infinite cases, we can assign probabilities to all events in the sample space. However, for uncountably infinite sample spaces, we need to restrict ourselves to a σ-algebra of events to ensure that the probability measure is well-defined and satisfies the axioms of probability.

## Axioms of Probability: 

Given a sample space S and a σ-algebra of events F, a probability measure P is a function that assigns a probability to each event in F, satisfying the following axioms:

Axiom #1: Non-negativity: For any event A, the probability of A is greater than or equal to 0. P(A) ≥ 0.

Axiom #2: Normalization: The probability of the sample space S is 1. P(S) = 1.

Axiom #3: Additivity: For any countable sequence of mutually exclusive events A1, A2, A3, ..., the probability of their union is equal to the sum of their individual probabilities.

$$
P(A1 ∪ A2 ∪ A3 ∪ ...) = P(A1) + P(A2) + P(A3) + ...    \tag{Eq.1}
$$

A lot of corollaries can be derived from these axioms, such as the probability of the empty set being 0, the probability of the complement of an event, and the probability of the union of two events etc.

## Discrete Sample Spaces

- Countably finite: 

- Countably infinite:

  Experiment where we toss a coin repeatedly and observe the number of coin tosses until we get a heads. The sample space is {1, 2, 3, ...}, which is countably infinite.

## Continuous Sample Spaces

- Borel Field: For the real line, the Borel field contains all open and closed intervals, as well as countable unions and intersections of these intervals.

- In continuous sample spaces, we often deal with probability density functions (PDFs) instead of discrete probabilities. The PDF describes the likelihood of a random variable taking on a particular value within a continuous range.

- The probability of a single point in a continuous sample space is zero. Does that mean that the event is impossible? No, it means that the probability of observing that exact value is infinitesimally small, but it does not imply that the event cannot occur. In continuous sample spaces, we are more interested in the event of the random variable falling within a certain interval, rather than taking on a specific value.

## Summary of Probability Models: 

  We are given an experimental procedure and a set of measurements and observations. These measurements and observations determine the set of all possible outcomes and hence the sample space S.

  An initial probability assignment that specifies the probability of some elementary events must be determined next. This probability assignment must satisfy the axioms of probability. If S is discrete, then it suffices to specify the probabilities of elementary events. If S is continuous, it suffices to specify the probabilities of intervals of the real line or regions of the plane. The probability of other events of interest can then be determined from the initial probability assignment and the axioms of probability and their corollaries. Many probability assignments are possible, so the choice of probability assignment must reflect experimental observations and/or previous experience.

## Computing probabilities using counting methods: 
- This is where all the permutations and combinations come into play. We can use combinatorial methods to count the number of favorable outcomes and the total number of outcomes in the sample space, and then compute probabilities as the ratio of favorable outcomes to total outcomes.
- Super interesting topic and fun to explore! But since its not directly relevant to generative modeling at the moment, we will not go into details here. Will come back to this topic later if its deemed relevant to generative modeling.

## Conditional Probability

- Intuition: Suppose we have a sample space S and two events A and B. If we know that event B has occured, think of it as if our whole sample space has been reduced to event B. Now, we want to know the probability of event A within this reduced sample space. This is called conditional probability and is denoted as P(A|B).

- Fomula: The conditional probability of A given B is defined as:

$$
P(A|B) = \frac{P(A ∩ B)}{P(B)} \quad \text{if } P(B) > 0    \tag{Eq.2}
$$


<svg xmlns="http://www.w3.org/2000/svg" width="420" height="260">
  <rect x="10" y="10" width="400" height="240" rx="12" style="fill:#f0f0f0;stroke:#888;stroke-width:2"/>
  <text x="28" y="36" style="font-size:18px;font-style:italic;fill:#555;font-family:serif">S</text>
  <circle cx="165" cy="130" r="90" style="fill:steelblue;fill-opacity:0.5;stroke:#2255aa;stroke-width:2"/>
  <circle cx="255" cy="130" r="90" style="fill:orange;fill-opacity:0.5;stroke:#cc5500;stroke-width:2"/>
  <text x="100" y="134" style="font-size:22px;font-style:italic;fill:#1a3a6b;font-family:serif">A</text>
  <text x="300" y="134" style="font-size:22px;font-style:italic;fill:#7a2800;font-family:serif">B</text>
  <text x="182" y="178" style="font-size:13px;fill:#333;font-family:serif">A &#x2229; B</text>
</svg>

## Theorem of Total Probability


## Bayes' Theorem

- Motivation: Suupose we have a random experiment in which the events of interest form a partition. The “a priori probabilities” of
these events, $P(B_j)$, are the probabilities of the events before the experiment is performed. Now suppose that the experiment is performed, and we are informed that
event $A$ occurred; the “a posteriori probabilities” are the probabilities of the events in the partition, $P(B_j \mid A)$, given this additional information.

$$
P(B_j \mid A) = \frac{P(A \mid B_j) P(B_j)}{\sum_{i=1}^{n} P(A \mid B_i) P(B_i)} \quad \text{for } j = 1, 2, ..., n  \tag{Eq.3}
$$

- Examples: TODO

## Independence of Events

- Questions:  
  - Is independence of events the same as mutual exclusivity? ❌
    - No, independence of events is not the same as mutual exclusivity. Two events A and B are mutually exclusive if they cannot occur at the same time, meaning that $P(A ∩ B) = 0$. On the other hand, two events A and B are independent if the occurrence of one event does not affect the probability of the other event occurring, which is defined as $P(A ∩ B) = P(A) \cdot P(B)$. Therefore, mutually exclusive events are not independent, and independent events are not mutually exclusive.
  - Is independence of events directional? That is, if A is independent of B, is B independent of A? ✅
  - What is the formal definition of independence of events? How does it relate to conditional probability?
    - Defined as: Two events A and B are independent if and only if $P(A ∩ B) = P(A) \cdot P(B)$. This means that the occurrence of one event does not affect the probability of the other event occurring.
                  Using the definition of conditional probability, this also means that independence is bidirectional, since $P(A|B) = P(A)$ and $P(B|A) = P(B)$ if A and B are independent.