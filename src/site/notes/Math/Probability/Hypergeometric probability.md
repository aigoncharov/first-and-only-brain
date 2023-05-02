---
{"dg-publish":true,"permalink":"/math/probability/hypergeometric-probability/","created":"","updated":""}
---

#probability 
Say, we have a random sample $n$ out of $N$ items ($N \choose n$). Then we select a new sample $m$ out of $N$ items ($N \choose m$). The probability that **exactly** $k$ of $m$ items were in the first sample $n$ is: 

$$
\frac{{n \choose k} {N - n \choose m - k}}{{N \choose m}}
$$