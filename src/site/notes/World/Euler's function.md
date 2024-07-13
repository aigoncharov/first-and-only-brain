---
{"dg-publish":true,"permalink":"/world/euler-s-function/"}
---

#math #prime_numbers
$\phi(N) = \prod{(p_{i}^{\alpha_{i}} - p_{i}^{\alpha_{i - 1}})}$
Количество натуральных чисел <= N и взаимно простых с ним.

See [[World/Fundamental theorem of arithmetic\|Fundamental theorem of arithmetic]]

$\phi(p) = p - 1$

$\phi(p^{\alpha}) = p^{\alpha} - \frac{p^{\alpha}}{p} = p^{\alpha} - p^{\alpha - 1}$ - убираем все числа делящиеся на p

$\phi(p^{\alpha} \cdot q^{\beta}) = p^{\alpha} \cdot q^{\beta} - \frac{p^{\alpha} \cdot q^{\beta}}{p} - \frac{p^{\alpha} \cdot q^{\beta}}{q} + \frac{p^{\alpha} \cdot q^{\beta}}{pq} = (p^{\alpha} - p^{\alpha - 1})(q^{\beta} - q^{\beta - 1})$
