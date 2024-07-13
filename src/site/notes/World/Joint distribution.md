---
{"dg-publish":true,"permalink":"/world/joint-distribution/"}
---

#probability 

Joint CDF $F_{X,Y}(x,y) = P(X \leq x, Y \leq y)$
Joint PMF $p_{X,Y}(x,y) = P(X = x, Y = y)$

Joint PMF must also sum to 1: $\sum\limits_{x}\sum\limits_{y}P(X=x,Y=y)=1$
![joint_pmf.png](/img/user/Files/joint_pmf.png)

Marginal (unconditional) PMF (how to get PMF of X when we have PMF of X,Y): $P(X=x) = \sum\limits_{y}P(X=x,Y=y)$ or $P(X = x) = \sum\limits_{y}P(X=x|Y=y)P(Y=y)$
Conditional PMF: $P(Y=y|X=x) = \frac{P(X=x, Y=y)}{P(X=x)}$
![conditional_pmf.png](/img/user/Files/conditional_pmf.png)

## Covariance
$$Cov(X,Y) = E((X - EX)(Y - EY)) = E(XY) - E(X)E(Y)$$
If X and Y are independent, Cov = 0.

### Properties
1. $Cov(X,X) = Var(X)$
2. $Cov(X,Y) = Cov(Y,X)$
3. $Cov(X,c) = 0$ for any constant c
4. $Cov(aX, Y) = aCov(X,Y)$
5. $Cov(X+Y,Z) = Cov(X,Z) + Cov(Y,Z)$
6. $Cov(X+Y,Z+W) = Cov(X,Z) + Cov(X,W) + Cov(Y,Z) + Cov(Y,W)$
7. $Var(X,Y) = Var(X) + Var(Y) + 2Cov(X,Y)$
8. $Var(X_1,\dots,X_{n})= Var(X_{1)}+ \dots + Var(X_{n}) + 2\sum\limits_{i<j}Cov(X_{i}, Y_{j})$

## Correlation
$$Corr(X,Y) = \frac{Cov(X,Y)}{\sqrt{Var(X)Var(Y)}}$$
Acts as covariance normalized from -1 to 1.
$$-1 \leq Corr(X,Y) \leq 1$$
