---
{"dg-publish":true,"permalink":"/math/linear-algebra/inverse-matrix/","created":"","updated":""}
---

#linear_algebra 

[[Math/Linear algebra/Matrix multiplication\|Matrix multiplication]]

$Ax=b$, then $x=A^{-1}b$

Example:
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
