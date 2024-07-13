---
{"dg-publish":true,"permalink":"/world/definition-of-probability/"}
---

#probability 

**Naive**: $P_{naive}(A) = \frac{|A|}{|S|} = \frac{number\:of\:outcomes favorable\:to\:A}{total\:number\:of\:outsomes\:in\:S}$

**General:** 
Given that: 

1. $P(\emptyset) = 0$, $P(S) = 1$ 
2. if $A_1,A_2,\dots$ are disjoint (mutually exclusive) events

then 
$$P(\bigcup\limits_{j=1}^{\infty}A_{j})= \sum\limits_{j=1}^{\infty}P(A_j)$$
where S - sample space, A - event ($A \subseteq S$)

## Sample space
Set of all possible outcomes of the experiment. Can be finite or infinite.

## Event
Event A is a susbet of the sample space.
A occurred if the actual outcome is A.
$A^c$ - complement of A, event that occurs only if A does not occur. 

## De Morgan's laws
$(A \cup B)^{c} = A^{c} \cap B^c$
$(A \cap B)^{c} = A^{c}\cup B^c$

## Properties
1. $P(A^{c)} = 1 - P(A)$, where $A^c$ is A complement
2. If $A \subseteq B$, then $P(A) \le P(B)$
3. $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
	1. $P(A \cup B \cup C) = P(A) + P(B) + P(C) - P(A \cap B) - P(A \cap C) - P(B \cap C) + P(A \cap B \cap C)$