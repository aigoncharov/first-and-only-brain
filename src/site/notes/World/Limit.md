---
{"dg-publish":true,"permalink":"/world/limit/"}
---

#math #limits 
## Series (последовательность)
### Определение
Число $a \in R$ - предел последовательности $\{a_{n}\}$ (записывается $a = \lim_{n\to \infty} a_{n}$), если:
$$\forall \epsilon > 0, \exists N(\epsilon) \in N : \forall n \geq N(\epsilon) -> |a-a_{n}| < \epsilon$$
($N(\epsilon)$ - значит N зависит от $\epsilon$)
Другими словами, для любой сколь угодно малой окрестности $\epsilon$ всегда найдется номер, начиная с которого все члены последовательности лежат в окрестности.

**Пример**
Докажем, что предел последовательности $\{a_{n}\} = \frac{1}{n}$ равен 0. Для этого найдем такое $N(\epsilon)$ начиная с которого будет выполняться неравенство $|a-\frac{1}{n}| < \epsilon$

$$|0-\frac{1}{n}| < \epsilon$$
$$\frac{1}{n} < \epsilon$$
$$\frac{1}{\epsilon} > n$$
$$\lceil\frac{1}{\epsilon}\rceil > n$$
$$\lceil\frac{1}{\epsilon}\rceil + 1 \geq n$$
 Мы нашли n начиная с которого все члены последовательности в окрестности -> предел последовательности 0.

### Сходящаяся последовательность 
Последовательность у которой есть конечный предел

### Расходящаяся последовательность 
Последовательность у которой предела нет или предел бесконечен.
### Ratio test
$\lim_{n \to \infty} |\frac{a_{n+1}}{a_{n}}| = L$
If L < 1, series converges.
If L > 1, series diverges
If L = 1, i tis inconclusive

### Root test
Consider series $\sum\limits_{n=1}^{\infty} a_{n}$, such that $\lim_{n \to \infty} \sqrt[n]{|a_{n}|} = p$ for some real p. Then for N sufficiently large $|a_{N}| = p^{N}$. Therefore, we can approximate $\sum\limits_{n=N}^{\infty} |a_{n}| = p^{N} + p^{N+1} + \dots$. It is a geometric series.
If p < 1, series converges.
If p = 1, it is inconclusive.
If p > 1, the series diverges.

### Root and ratio test relation
$$
\lim\inf\limits_{n\rightarrow \infty} \frac{A_{n+1}}{A_n} 
\leq 
\lim\inf\limits_{n\rightarrow \infty} (A_n)^{1/n} 
\leq 
\lim\sup\limits_{n\rightarrow \infty} (A_n)^{1/n} \leq \lim\sup\limits_{n\rightarrow \infty} \frac{A_{n+1}}{A_n}
$$
### Бесконечно большие и бесконечно малые последовательности
$\lim_{n \to \infty} a_{n} = +\infty, \forall \epsilon > 0, \exists n_{\epsilon} \in N : \forall n \geq n_{\epsilon} \rightarrow a_{n} > \epsilon$
Для $\lim_{n \to \infty} a_{n} = -\infty$ определение аналогичное.

Последовательность **бесконечно большая**: $\forall \epsilon > 0, \exists n_{\epsilon} \in N : \forall n \geq n_{\epsilon} \rightarrow |a_{n}| > \epsilon$
Последовательность **бесконечно малая**: $|a_{n}| < \epsilon$
### Теорема (Вейерштрасса) о существовании предела монотонной ограниченной последовательности
Монотонная ограниченная последовательность имеет предел равный ее точной верхней грани, если она возрастает, и нижней грани, если убывает.

**Пример применения**
Последовательность $\{x_{n}\}$ задана как: $x_{1} = \sqrt{2}, x_{n+1} = \sqrt{2 + x_{n}}$
Исследуем на монотонность. Eсли $x_{n+1} > x_{n}$ , то $\sqrt{2 + x_{n}} > x_{n}$ -> $2+x_{n} > x_{n}^{2}$. Выполняется для $x \in (0,2)$.
Покажем, что последовательность ограничена сверху. Если $x_{n} < 2$, то $x_{n} + 2 < 4$ -> $\sqrt{2 + x_{n}} < 2$. Т.к. $x_{1} = \sqrt{2} < 2$ -> $x_{n+1} < 2, n \in N$
По теореме Вейерштрасса, если последовательность монотонно возрастает и она ограничена, то у нее есть предел. 
$\lim_{n \to \infty} x_{n+1} = \lim_{n \to \infty} x_{n} = A$
$A = \sqrt{2 + A}$
$A^{2} - A - 2 = 0$
Ответ: A=2 (A=-1 не подходит, т.к. все члены >0).

### Свойства пределов
1. $\lim_{n \to \infty} (a_{n} \pm b_{n}) = a \pm b$, если $\exists \lim_{n \to \infty} a_{n}$, $\exists \lim_{n \to \infty} b_{n}$, пределы конечны
2. $\lim_{n \to \infty} (a_{n}b_{n}) = ab$, если $\exists \lim_{n \to \infty} a_{n}$, $\exists \lim_{n \to \infty} b_{n}$, пределы конечны
3. $\lim_{n \to \infty} (\frac{a_{n}}{b_{n}}) = \frac{a}{b}$, если $b_{n} \neq 0 \forall n \in N, b \neq 0$б , $\exists \lim_{n \to \infty} a_{n}$, $\exists \lim_{n \to \infty} b_{n}$, пределы конечны
4. $lim_{x \to \infty} (a_{n})^{n} = (lim_{x \to \infty} a_{n})^{n}$
## Function

$f(x)$ has limit $b$ as $x$ approaches $a$ if for each $\epsilon > 0$ exists $\sigma$ such that when $0 < |x - a| < \sigma$ then $|y - b| < \epsilon$ 

$\lim_{x \to a} f(x)$ exists if $lim_{x \to a^{+}} f(x) = lim_{x \to a^{-}}f(x)$

### Basics
$$lim_{x \to a} C = C$$
$$lim_{x \to a} x = a$$
$$lim_{x \to 0^{-}} \frac{1}{x}= -\infty$$
$$lim_{x \to 0^{+}} \frac{1}{x}= +\infty$$
### Properties
Gien that:
$$lim_{x \to a} f(x) = L_1$$
$$lim_{x \to a} g(x) = L_2$$
Properties:
1. $$lim_{x \to a} [f(x) \pm g(x)] = lim_{x \to a} f(x) \pm lim_{x \to a} g(x)$$
2. $$lim_{x \to a} [f(x) \times g(x)] = lim_{x \to a} f(x) \times lim_{x \to a} g(x)$$
3. $$lim_{x \to a} [\frac{f(x)}{g(x)}] = \frac{lim_{x \to a} f(x)}{lim_{x \to a} g(x)}$$
   where $lim_{x \to a} g(x) \neq 0$
4. $$lim_{x \to a} [f(x)]^n = [lim_{x \to a} f(x)]^n$$
5. $$lim_{x \to a} P(x) = P(a)$$
   where P(x) is a polynomial ([[World/Function\|Function]])
6. $$lim_{x \to a} f\circ{g}(x) = f(lim_{x \to a} g(x)) $$
   if f(x) is continuous

### Sign analysis

1. Mark points where numerator = 0 and denominator = 0
2. Pick a point in the interval to the left of where denominator = 0.
3. If function at that point is negative, then limit from the left is $-\inf$ (and vice versa for positive).
4. Do the same for a point to the right.
5. If limits from the left and limit from the right are same, limit exists.
### $\pm \inf$
If approaches a number as $x \to \pm\inf$ then $\lim_{x \to \pm\inf} f(x)$ exists.
$f(x)$ is going to have a horizontal asymptote at that limit.

#### Example
$$\lim_{x \to \inf} \frac{5x-2}{3x+9} = \lim_{x \to \inf} \frac{x-\frac{2}{x}}{3+\frac{9}{x}} = \frac{5}{3}$$
Divide every term by the largest power of x in the denominator.