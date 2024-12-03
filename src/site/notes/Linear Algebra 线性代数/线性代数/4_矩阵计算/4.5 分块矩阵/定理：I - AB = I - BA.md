---
{"dg-publish":true,"permalink":"/Linear Algebra 线性代数/线性代数/4_矩阵计算/4.5 分块矩阵/定理：I - AB = I - BA/","tags":["定理","线代"]}
---

设$A$为$n\times s$矩阵，$B$为$s\times n$矩阵
1. 证明
$$
\begin{vmatrix}
I_{s}  & B \\
A & I_{n}
\end{vmatrix}
=
\begin{vmatrix}
I_{n} - AB
\end{vmatrix}
$$
2. 证明$|I_{n} - AB| = |I_{s} - BA|$


> [!NOTE] 思路
> 分块矩阵常用的解行列式思路：
> 1. 做初等行列变换，把其中一个矩阵清零
> 2. 拉普拉斯展开求行列式

$$
\begin{pmatrix}
I_{s} & B \\
A & I_{n}
\end{pmatrix}
=_{(2) - (1)B}
\begin{pmatrix}
I_{s} & 0 \\
A & I_{n} - AB
\end{pmatrix}
$$
变为行列式计算
$$
\begin{align}
\begin{vmatrix}
I_{s} & B \\
A & I_{n}
\end{vmatrix} 
\begin{vmatrix}
I_{s} & -B \\
0 & I_{n}
\end{vmatrix}  
 & = 
\begin{vmatrix}
I_{s} & 0 \\
A & I_{n}-AB
\end{vmatrix} \\ 

\begin{vmatrix}
I_{s} & B \\
A & I_{n}
\end{vmatrix}  
|I_{s}||I_{n}|   
& =  
|I_{s}| 
\begin{vmatrix}
I_{n} - AB
\end{vmatrix} \\

\begin{vmatrix}
I_{s} & B \\
A & I_{n}
\end{vmatrix}   
 & =  
\begin{vmatrix}
I_{n} - AB
\end{vmatrix} 
\end{align}
$$
---
用同样方式证明
$$
\begin{vmatrix}
I_{s}  & B \\
A & I_{n}
\end{vmatrix}
=
\begin{vmatrix}
I_{s} - BA
\end{vmatrix}
$$

$$
\begin{pmatrix}
I_{s} & B \\
A & I_{n}
\end{pmatrix}
=_{(1) - (2)A}
\begin{pmatrix}
I_{s} - BA & B \\
0 & I_{n}
\end{pmatrix}
$$
$$
\begin{align}
\begin{vmatrix}
I_{s} & B \\
A & I_{n}
\end{vmatrix} 
\begin{vmatrix}
I_{s} & 0 \\
-A & I_{n}
\end{vmatrix}  
 & = 
\begin{vmatrix}
I_{s} - BA & B \\
0 & I_{n}
\end{vmatrix} \\ 

\begin{vmatrix}
I_{s} & B \\
A & I_{n}
\end{vmatrix}  
|I_{s}||I_{n}|   
& =  
\begin{vmatrix}
I_{s} - BA
\end{vmatrix} 
|I_{n}|  \\

\begin{vmatrix}
I_{s} & B \\
A & I_{n}
\end{vmatrix}   
 & =  
\begin{vmatrix}
I_{s} - BA
\end{vmatrix} 
\end{align}
$$
由此证明
$$
\begin{vmatrix}
I_{n} - AB
\end{vmatrix} 
=\begin{vmatrix}
I_{s} - BA
\end{vmatrix} 
$$