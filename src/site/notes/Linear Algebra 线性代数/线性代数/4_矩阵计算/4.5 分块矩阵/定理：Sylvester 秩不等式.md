---
{"dg-publish":true,"permalink":"/Linear Algebra 线性代数/线性代数/4_矩阵计算/4.5 分块矩阵/定理：Sylvester 秩不等式/","tags":["线代","定理"]}
---

#### Sylvester 秩不等式
$rank(AB) \geq rank(A)  + rank(B) - n$

**证明：**

> [!NOTE] 思路
> 通过以下的方式
> $$
> rank(A) + rank(B) = rank
> \begin{pmatrix} 
 A & 0  \\
0 & B
\end{pmatrix}
> $$
> 对矩阵做初等行列变换，直到矩阵内部出现题目所要求证明的矩阵

移项
$$
rank(AB) + n \geq rank(A)  + rank(B)
$$
因为$rank(I_{n}) = n$
因此
$$
rank(A) + n =rank\begin{pmatrix}
AB & 0 \\
0 & I_{n}
\end{pmatrix}
$$
$$
\begin{align}
\begin{pmatrix}
AB & 0 \\
0 & I_{n}
\end{pmatrix} 
 & = 
\begin{pmatrix}
AB & A \\
0 & I_{n}
\end{pmatrix}  \\
 & =
\begin{pmatrix}
0 & A \\
B & I_{n}
\end{pmatrix}
\end{align}
$$
设$rank(A) = s, rank(B) = t$
则$A$和$B$分别存在一个$s$阶子式$|A_{1}|$和$t$阶子式$|B_{1}|$不为零

那么矩阵
$$
\begin{pmatrix}
0 & A \\
B & I_{n}
\end{pmatrix}
$$
也存在一个$s+t$阶子式，使得
$$
\begin{vmatrix}
0 & A_{1} \\
B_{1} & C_{1} 
\end{vmatrix}
=|A||B| \ne 0
$$
又因为初等行列变化不改变矩阵的秩
因此
$$
\begin{align}
rank\begin{pmatrix}
AB & 0 \\
0 & I_{n}
\end{pmatrix}  
 & \geq 
s + t \\
rank(AB) + n  & \geq rank(A)+rank(B) \\
rank(AB)   & \geq rank(A)+rank(B) - n
\end{align}
$$
