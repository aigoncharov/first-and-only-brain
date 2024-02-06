---
{"dg-publish":true,"permalink":"/world/conditional-probability/","created":"","updated":""}
---

#probability 
$$P(A|B) = \frac{P(A \bigcap B)}{P(B)}$$
$$P(A|B) \neq P(B|A)$$
$$P(A_{1}\bigcap A_{2} \dots A_{n})= P(A_1)P(A_2|A_1)P(A_3|A_1,A_{2})\dots P(A_n|A_1,\dots,A_{n-1})$$
## Bayes' rule
$$P(A|B)=\frac{P(B|A)P(A)}{P(B)}$$
With extra conditioning:
$$P(A|B,E) = \frac{P(B|A,E) P(A|E)}{P(B|E)}$$
## Law of total probability
If $A_1,\dots,A_n$ are disjoint events of sample space $S$ and $P(A_i)>0$, then
$$
P(B) = \sum\limits_{i=1}^{n} P(B|A_i)P(A_i)
$$
With extra conditioning:
$$P(B|E) = \sum_{i=1}^n P(B|A_i, E) P(A_i|E)$$
### Application
$$P(A|B) = \frac{P(B|A)P(A)}{P(B|A)P(A) + P(B|A^{c})P(A^{c})}$$
Even if P(B|A) is very high, but P(A) is very low, then the result is going to be fairly low as well
## Independence
A and B are independent if
$$P(A \bigcap B) = P(A)P(B)$$
equivalent to
$$P(A|B) = P(A)$$
equivalent to
$$P(B|A)=P(B)$$
### Pairwise independence
$$P(A \bigcap B) = P(A)P(B)$$
$$P(A \bigcap C) = P(A)P(C)$$
$$P(B \bigcap C) = P(B)P(C)$$
It does not always imply that
$$P(A \bigcap B \bigcap C) = P(A)P(B)P(C)$$
### Conditional independence
$$P(A \bigcap B|E)=P(A|E)P(B|E)$$
Conditional independence does not imply independence.
Independence does not imply conditional independence.

## Conditional PMF
$$
P_{X|Y=y}(x) = \frac{P_{XY}(x,y)}{P_Y(y)}
$$