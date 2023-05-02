---
{"dg-publish":true,"permalink":"/math/probability/inclusion-exclusion-theorem/","created":"","updated":""}
---

#probability 
$$
P(\bigcup\limits_{i=1}^{n}A_{i}) =
\sum\limits_{i}^{n}P(A_{i}) -
\sum\limits_{j=i+1}^{n}P(A_{i} \cap A{j}) +
\sum\limits_{k=j+1}^{n}P(A_{i} \cap A{j} \cap A_{k}) -
\dots +
(-1)^{n+1}P(A_1 \cap\dots \cap A_n)
$$
Famous application: de Montmort's matching problem