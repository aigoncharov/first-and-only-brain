---
{"dg-publish":true,"permalink":"/world/matrix/","created":"","updated":""}
---

#linear_algebra 

## Identity

$I=\begin{bmatrix} 1&0&0&\dots&0 \\ 0&1&0&\dots&0 \\ 0&0&1&\dots&0 \\ \dots&\dots&\dots&\dots&\dots \\ 0&0&0&\dots&1 \end{bmatrix}$

$Ix=x$ - always!

## Inverse

$Ax=b$, then $x=A^{-1}b$

### Example
$$
Ax= \begin{bmatrix} 1&0&0 \\ -1&1&0 \\ 0&-1&1 \end{bmatrix} \begin{bmatrix}x_1 \\ x_2 \\ x_3 \end{bmatrix} =
\begin{bmatrix} x_1 \\ x_{2}-x_1 \\ x_3-x_2\end{bmatrix} =
\begin{bmatrix}b_1 \\ b_2 \\ b_3\end{bmatrix}
$$
$$
\begin{bmatrix}x_1 \\ x_2 \\ x_3\end{bmatrix}=
\begin{bmatrix}b_1 \\ b_{1}+ b_2 \\ b_1+b_2+b_3\end{bmatrix}
$$
$$
x=\begin{bmatrix}1 & 0 & 0 \\ 1 & 1 & 0 \\ 1 & 1 & 1\end{bmatrix}\begin{bmatrix}b_1 \\ b_2 \\ b_3\end{bmatrix}
$$
$$
A= \begin{bmatrix} 1&0&0 \\ -1&1&0 \\ 0&-1&1 \end{bmatrix}
$$
$$A^{-1}=\begin{bmatrix}1 & 0 & 0 \\ 1 & 1 & 0 \\  1 & 1 & 1\end{bmatrix}$$


## Multiplication
As a linear combination of [[World/Vector\|Vector]]:

$$\begin{bmatrix}2 & 5\\1&3\end{bmatrix}\begin{bmatrix}1\\2\end{bmatrix} = 1\begin{bmatrix}2\\1\end{bmatrix} + 2\begin{bmatrix}5\\3\end{bmatrix} = \begin{bmatrix}2\\1\end{bmatrix} + \begin{bmatrix}10\\6\end{bmatrix} = \begin{bmatrix}12\\7\end{bmatrix}$$
In row form ([[World/Vector\|Vector]] dot product):
$$\begin{bmatrix} \begin{bmatrix}2\\5\end{bmatrix} \cdot \begin{bmatrix}1\\2\end{bmatrix} \\ \begin{bmatrix}1\\3\end{bmatrix} \cdot \begin{bmatrix}1\\2\end{bmatrix} \end{bmatrix}
=
\begin{bmatrix} 2*1+5*2 \\ 1*1+3*2 \end{bmatrix}
=
\begin{bmatrix}12\\7\end{bmatrix}$$
## Elimination

1. Eliminate row by row until reaching a triangular form.
2. Back substitution - solve row by row starting from the bottom 

Details: [[World/Метод Гаусса\|Метод Гаусса]]


