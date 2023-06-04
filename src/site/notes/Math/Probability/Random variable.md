---
{"dg-publish":true,"permalink":"/math/probability/random-variable/","created":"","updated":""}
---

#probability 

**Random variable** - function mapping the sample space ([[Math/Probability/Definition of probability\|Definition of probability]]) to the real numbers.

## Function of a random variable

Given r.v. X, sample space S, function $g: \mathbb{R} \to \mathbb{R}$,  $g(X)$ is the r.v. that maps s to g(X(s)) for all $s \in S$

## Independence of 2 r.v.s

R.V.s X and Y are independent if
$$P(X \leq x, Y \leq y) = P(X \leq x)P(y \leq y)$$
for all $x,y \in \mathbb{R}$

**In the discrete case** this is equivalent to 
$$P(X = x, Y = y) = P(X = x)P(Y = y)$$

for all x,y in the support of X and Y correspondingly.

## Independent and Identically distributed R.V.s
Independent and identically distributed (**i.i.d.**) R.V.s - R.V.s that are independent and have the same distribution

## Conditional independence of R.V.s
> Independence of r.v.s does not imply their conditional independence and vice versa.

R.V.s X and Y and conditionally independent given a r.v. Z if for all $x,y \in \mathbb{R}$ and z in the support of Z
$$
P(X \leq x, Y \leq y | Z=z)=P(X \leq x |Z = z)P(Y \leq y | Z = z)
$$

**In the discrete case** this is equivalent to
$$
P(X = x, Y = y | Z=z)=P(X = x |Z = z)P(Y = y | Z = z)
$$

### Conditional PMF
For any discrete r.v.s X and Z, the function $P(X = x | Z = z)$, when considered as a function of x for fixed z, is called the conditional PMF of X given Z = z.