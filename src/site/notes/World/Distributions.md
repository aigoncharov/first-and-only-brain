---
{"dg-publish":true,"permalink":"/world/distributions/","created":"","updated":""}
---

#probability 
For PMF see [[World/Discrete random variables\|Discrete random variables]]

## Poisson distribution

$$X \sim Pois(\lambda)$$
### PMF, E, Var
$$P(X = k) = \frac{e^{-\lambda}\lambda^{k}}{k!}$$ 
where k = 0,1,2,...
$$E(X) = \lambda$$
$$Var(X) = \lambda$$


### Poisson process
Process of arrivals in continuous time. Conditions:
1. Number of arrivals occurring in interval t is $Pois(\lambda t)$
2. Numbers of arrivals in disjoint intervals are independent.

### Count-time duality

$$P(T_{1} > t) = P(N_{t} = 0) = \frac{e^{-\lambda t}(\lambda t)^{0}}{0!} = e^{-\lambda t}$$
where $N_{t}$ - number of events before time t (inclusive), $T_{x}$ - time to event x.
It follows that $P(T_{1} \leq t) = 1 - P(T_{1} > t) = 1 - e^{-\lambda t}$, therefore $T_{1} \sim Expo(\lambda)$.

### Poisson approximation
Let $A_{1},A_{2}, \dots, A_{j}$ be events with $p_{j} = P(A)$, where n is large, $p_{j}$ are small, $A_{j}$ are independent or weakly dependent. Let $X = \sum\limits_{j=1}^{n}I(A_{j})$ count how many $A_{j}$ occur. Then $X$ is approximately $Pois(\lambda)$, where $\lambda = \sum\limits_{j=1}^{n}p_{j}$.
### Sum of independent Poissons
If $X \sim Pois(\lambda_{1})$, $Y \sim Pois(\lambda_{2})$, X and Y are independent, then $X + Y \sim Pois(\lambda_{1} + \lambda_{2})$.

## Bernoulli distribution
$$X \sim Bern(p)$$
$P(X = 1) = p$, $P(X = 0) = 1 - p$, where p is the parameter of the distribution, 0 < p < 1. Sample space - $\{0,1\}$.

**Bernoulli trial** - experiment that result in a success of failure (1 or 0).

## Binomial distribution

$$X \sim Bin(n,p)$$
where n - number of independent Bernoulli trials, p - success probability of each trial, X - number of successes.

If $X \sim Bin(n,p)$, then $X = X_{1} + X_{2} + \dots + X_{n}$, where $X_{i}$ are i.i.d. ([[World/Random variable\|Random variable]]) $Bern(p)$.

If $X \sim Bin(n,p)$, $Y \sim Bin(m , p)$, X and Y are independent, then $X + Y \sim Bin(n + m, p)$

### PMF, E, Var
$$P(X = k) = {n \choose k}p^{k}(1-p)^{n-k}$$
$$E(X) = np$$
$$Var(X) = np(1-p)$$

## Hypergeometric
$$X \sim HGeom(w,b,n)$$
where $w$ and $b$ are numbers of different opposing outcomes, n - number of trials **without** replacement.

> Binomial with dependent trials

### Story
Consider an urn with $w$ white balls and $b$ black balls. We draw $n$ balls out of the urn at random **without** replacement, such that ${w+b} \choose n$ are equally likely. Let X be the number of white balls in the sample. Then X is said to have Hypergeometric distribution.

### PMF, E

$P(X=k)=\frac{{w \choose k}{b \choose {n - k}}}{{w + b} \choose n}$
for k satisfying $0 \leq k \leq w$, $0 \leq n - k \leq b$.

See Vandermonde's identity in [[World/Sampling\|Sampling]]

$$E(X) = \frac{nw}{w + b}$$

## Geometric
$$X \sim Geom(p)$$
Sequence of Bernoulli trials until success occurs.

### PMF, E, Var
$$P(X = k) = q^{k}p$$
$$E(X) = \frac{q}{p}$$
$$Var(X) = \frac{q}{p^{2}}$$

### First success distribution
By various conventions, Geometric could include or not include the first success. We are not including first success. To include it, we introduce "First Success" distribution.
$$ X \sim FS(p)$$
If $Y \sim FS(p)$, then $Y - 1 \sim Geom(p)$.
$$E(Y) = \frac{1}{p}$$
$$Var(X) = \frac{q}{p^{2}}$$

## Negative binomial
$$X \sim NBin(r, p)$$
Sequence of independent Bernoulli trials with probability p, if X is the number of failures before r successes.

While Binomial counts numbers of successes in a fixed number of trials, negative binomial counts number of failures until a fixed number of successes reached.

### PMF, E, Var
$$P(X = n) = {{n + r - 1} \choose {r -1}}p^{r}q^{n}$$
$$E(X) = r\frac{q}{p}$$
$$Var(X) = r\frac{q}{p^{2}}$$
### Sum of Geometric
If $X \sim NBin(r,p)$, then $X = \sum\limits_{i=1}^{r} X_{i}$, where $X_{i}$ are i.i.d. $Geom(p)$.

## Discrete uniform
$$X \sim DUnif(C)$$
where C is a finite nonempty set of numbers and we choose one of them uniformly at random

### PMF
$$P(X = x) = \frac{1}{|C|}$$
for $x \in C$

## Continuous uniform
$$X \sim Unif(a, b)$$
Uniform distribution on the interval $(a,b)$

**Standard uniform** is $Unif(0, 1)$

### PDF

$$
\begin{equation}
f(x) =
\begin{cases} \\
\frac{1}{b-a} & \text{if a < x < b} \\
0 & \text{otherwise}
\end{cases}       
\end{equation}
$$
### CDF
$$
\begin{equation}
F(x) =
\begin{cases} \\
0 & x \leq a \\
\frac{x-a}{b-a} & a < x < b \\
1 & x \geq b
\end{cases}       
\end{equation}
$$
It **follows** that $P(U \leq u) = u$ where $u \in (0,1)$.

### E, Var
$$E(X)=\frac{a+b}{2}$$
$$Var(U) = \frac{(b-a)^{2}}{12}$$

### Location-scale transformation
Let X be an r.v. and $Y = \sigma X + \mu$, where $\sigma$ and $\mu$ are constants with $\sigma > 0$. Then we say that Y has been obtained as a _location-scale transformation_ of X. Here $\mu$ controls how the location is changed and $\sigma$ controls how the scale is changed.

*TODO: How to scale PDF, CDF?*

### Universality (Probability Integral Transform)
Let F be a CDF which is a continuous function and strictly increasing on the support of the distribution. This ensures that the inverse function $F^{-1}$ exists, as a function from (0,1) to $\mathbb{R}$. We then have the following results.
1. 1. Let $U \sim Unif(0,1)$ and $X = F^{-1}(U)$. Then X is an r.v. with CDF F.
2. 1. Let X be an r.v. with CDF F. Then $F(X) \sim U(0,1)$.
#### Proof
1. $$
   P(X \leq x) = 
   P(F^{-1}(U) \leq x) = 
   P(U \leq F(x)) =
   F(x)
   $$
   because $P(U \leq u) = u$ where $u \in (0,1)$
2. Find CDF of $Y = F(X)$
    $$
   P(Y \leq y) =
   P(F(X) \leq y) = 
   P(X \leq F^{-1}(y)) = 
   F(F^{-1}(y)) = 
   y
   $$
   It follows that $Y \sim U(0, 1)$

#### Example (percentiles)
Let X be the score of a random student on an exam. Say median score is 60, i.e. F(60) = 1/2. If Jimmy scores a 72 on the exam, then his _percentile_ is the fraction of students who score below a 72. This is F(72).  A percentile is also called a _quantile_, which is why $F^{-1}$ is called the quantile function. The function $F$ converts scores to quantiles, and the function $F^{-1}$ converts quantiles to scores.
The strange operation of plugging X into its own CDF now has a natural interpretation: F(X) is the percentile attained by a random student. While distribution of scores is usually non-Uniform, the distripbution of percentiles is.
For example, 50% of the students have a percentile of at least 0.5. Universality of the Uniform is expressing the fact that 10% of the students have a percentile between 0 and 0.1, 10% have a percentile between 0.1 and 0.2, 10% have a percentile between 0.2 and 0.3, and so on.

#### Application

Logistic CDF is $F(x) = \frac{e^x}{1+e^x}$
$$F^{-1}(U) = \ln(\frac{U}{1 - U})$$
$$
P(\ln{\frac{U}{1 -U}} \leq x) =
P(\frac{U}{1-U} \leq e^{x)} =
P(U \leq e^{x} - e^{x}U) =
P(U(1 + e^{x}) \leq e^{x}) =
P(U \leq \frac{e^{x}}{1 + e^{x}})= 
\frac{e^{x}}{1 + e^{x}} =
F(x)
$$
## Normal
$X \sim N(\mu, \sigma^2)$
where $\mu$ is mean, $\sigma^2$ is variance.

**Standard normal**: $X \sim N(0, 1)$. Often denoted as $Z$.

![std_normal.png](/img/user/Files/std_normal.png)

### Convert from std to general
$$
X = \mu + \sigma Z
$$

Also $$\frac{X - \mu}{\sigma} \sim N(0,1)$$

### PDF
#### Standard
$$\phi(z) = \frac{1}{\sqrt{2\Pi}}e^{-\frac{z^2}{2}}$$
where $-\infty < z < \infty$
#### General
$$f(x) = \phi(\frac{x - \mu}{\sigma})\frac{1}{\sigma}$$
or
$$
f(x) = \frac{1}{\sqrt{2\Pi}\sigma}e^{-\frac{{(x-\mu)}^2}{2\sigma^2}}
$$

### CDF
No closed form. Integrate. Named $\Phi$.

### Properties
1. Symmetry of PDF. $\phi(z) = \phi(-z)$
2. Symmetry of tail areas. $\Phi(z) = 1 - \Phi(-z)$
3. Symmetry of $Z$ and $-Z$. If $Z \sim N(0,1)$, then $-Z \sim N(0,1)$.
4. Sum of independent normals is a normal. If $X_{1}\ sim N(\mu_{1},\sigma_{1}^{2}), X_{2} \sim N(\mu_{2},\sigma_{2}^{2})$, then 
   $$
   X_{1}+ X_{2} \sim N(\mu_{1} + \mu_{2}, \sigma_{1}^{2} + \sigma_{2}^{2})
  $$
  $$
  X_{1} - X_{2} \sim N(\mu_{1} - \mu_{2}, \sigma_{1}^{2} + \sigma_{2}^{2})
  $$

### 68-95-99.7 rule

If $X \sim N(\mu, \sigma^{2})$, then
1. $P(|X - \mu| < \sigma) \approx 0.68$
2. $P(|X - \mu| < 2\sigma) \approx 0.95$
3. $P(|X - \mu| < 3\sigma) \approx 0.997$

## Exponential
$$
X \sim Expo(\lambda)
$$

Widely used as a simple model for the waiting time for a certain kind of event to occur, e.g., the time until the next email arrives.

### PDF
$$f(x) = \lambda e^{-\lambda x}$$
where x > 0

### CDF
$$F(x) = 1 - e^{-\lambda x}$$
![expo_cdf_pdf.png](/img/user/Files/expo_cdf_pdf.png)

### E, Var
$$E(X) = \frac{1}{\lambda}$$
$$Var(X) = \frac{1}{\lambda^{2}}$$
### Transformations

If $X \sim Expo(1)$, then $Y = \frac{X}{\lambda} \sim Expo(\lambda)$

Proof: 
$$
P(Y \leq y) =
P\left(\frac{X}{\lambda} \leq y\right)= 
P(X \leq \lambda y) = F(\lambda y)
$$

### Properties
1. Memoryless. If the waiting time for a certain event to occur is Exponential, then the memoryless property says that no matter how long you have waited so far, your additional waiting time is still Exponential (with the same parameter). $P(X \geq s + t | X \geq s) = P(X \geq t)$.

### Minimum of independent expos
Let $X_{1}, X_{2}, \dots, X_{n}$ be independent with $X_{j} \sim Expo(\lambda)$. Let $L = min(X_{1}, X_{2}, \dots, X_{n})$. 
Then $L \sim Expo(\sum\limits_{i=1}^{n}\lambda_{i} )$
Proof:
We can find the distribution of by considering its _survival function_ , since the survival function is 1 minus the CDF.
$$
P(L > t) = P(min(X_{1}, X_{2}, \dots, X_{n}) > t) = 
P(X_{1} > t, X_{2} > t, \dots, X_{n} > t) = 
P(X_{1} > t)P(X_{2} > t) \dots P(X_{n} > t) = 
e^{-\lambda_{1}t} e^{-\lambda_{2}t} \dots e^{-\lambda_{n}t} =
e^{-(\lambda_{1} + \lambda_{2} + \dots + \lambda_{n})t}
$$
#### Survival function
$P(X > t) = 1 - F(t)$, where F - CDF of Expo.

## Cauchy
If X and Y are i.i.d. N(0, 1), then $\frac{X}{Y} \sim Cauchy$.

$$f(x) = \frac{1}{\Pi(1 + x^{2})}$$
**Properties**:
1. No finite mean or variance.
2. Sample mean of n Cauchy is still Cauchy. Central Limit Theorem does not apply!
3. No true mean. Law of large numbers does not apply!