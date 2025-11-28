# Problem Description

This project implements a 5-armed bandit environment and compares two action-selection strategies:
- Greedy
- ε-Greedy (with ε = 0.4)

The goal is to evaluate which method performs better over 100 time steps across 200 independent runs.
You may define any reward distributions or parameters for the bandit arms.

For background, refer to Section 2.3 of Sutton & Barto’s Reinforcement Learning (10-armed testbed example).
A common way to visualize performance is by reproducing one of the plots from Figure 2.2, but any clear comparison—plots, tables, or qualitative explanation—is acceptable.

Below is the ε-greedy action-selection algorithm for the k-armed bandit problem (Section 2.4), which serves as the basis for this implementation.


```latex
# A simple bandit algorithm

Initialize, for a = 1 to k:
    Q(a) <- 0
    N(a) <- 0

Repeat forever:

    A <- | argmax a Q(a) with probability 1 - e (breaking ties randomly)
         | random action with probability e
    R <- bandit(A)
    N(A) <- N(A) + 1
    Q(A) <- Q(A) + 1/N(A)[R - Q(A)]
```
