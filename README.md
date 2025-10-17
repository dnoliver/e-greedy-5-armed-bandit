# Programming Assignment

## Instructions

You can use any programming languages. You may work in a group of two. It’s due is October 30 at the beginning of the
class.

You have to submit a hardcopy of your program, the results with a detailed explanation including all the selected
parameters

## Problem

Implement a 5 armed bandit problem with greedy and e-greedy action selection algorithms. Compare the results of e-greedy
action selection method (e=0.4) with the greedy one. Which one works better over 100 time-steps in 200 runs? You can
choose any distribution/values for your reward function and/or other parameters.

Section 2.3 of our book is an example for one 10 armed testbed. One way to show the performance of e greedy method vs
the greedy method is by producing one of the graphs in Figure 2.2. However you may explain/show or compare the
performance of two approaches in different ways.

The following algorithm is an example for e-greedy action selection in k armed bandit problem (section 2.4).

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

## Output

Code, results, and the detailed explanation of your approach.
