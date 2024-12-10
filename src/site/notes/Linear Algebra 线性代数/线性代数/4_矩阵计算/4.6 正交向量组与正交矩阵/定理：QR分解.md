---
{"dg-publish":true,"permalink":"/Linear Algebra 线性代数/线性代数/4_矩阵计算/4.6 正交向量组与正交矩阵/定理：QR分解/","tags":["线代","定理"]}
---


> [!Question] 问题
> 设$A$为$m\times n$矩阵，其中$m > n$，如果$A$是列满秩矩阵（$A$的列向量线性无关），那么$A$一定可以被唯一地分解为$A = QR$
> 其中$Q$为$m\times n$，列向量为正交单位向量组，$R$为可逆上三角矩阵


> [!NOTE] 步骤整理
> 1. 利用线性无关的向量组能被正交化的特性，把列向量写成正交向量组的线性组合
> 2. 把矩阵的正交向量组和线性组合的矩阵分解出来
> 3. 再通过把正交向量组单位化，分解出正交单位向量组

设$A$的列向量组为$\alpha_{1},\alpha_{2},\dots,\alpha_{n}$
因为它们是线性无关的，所有它们可[[Linear Algebra 线性代数/线性代数/4_矩阵计算/4.6 正交向量组与正交矩阵/工具箱：标准正交化\|工具箱：标准正交化]]
先做正交化
$$
\begin{align}
\beta_{1} & = a_{1} \\
\beta_{2} & = a_{2} -  \frac{[\beta_{1},a_{2}]}{[\beta_{1},\beta_{2}]}\beta_{1} \\
\beta_{3}  & =a_{3} - \frac{[\beta_{2},a_{3}]}{[\beta_{2},\beta_{2}]}\beta_{2} - \frac{[\beta_{1},a_{3}]}{[\beta_{1},\beta_{2}]}\beta_{1} \\
\dots \\
\beta_{n}  & = a_{n}- \sum_{i=1}^{n} \frac{[\beta_{i} , a_{n}]}{[\beta_{i},\beta_{i}]}\beta_{i}
\end{align}
$$
因此
$$
\begin{align}
a_{1} & =  \beta_{1}\\
 a_{2}& = \frac{[\beta_{1},a_{2}]}{[\beta_{1},\beta_{2}]}\beta_{1} + \beta_{2} \\
a_{3}  & =  \frac{[\beta_{1},a_{3}]}{[\beta_{1},\beta_{2}]}\beta_{1} + \frac{[\beta_{2},a_{3}]}{[\beta_{2},\beta_{2}]}\beta_{2}  + \beta_{3}\\
\dots \\
a_{n}  & =  \sum_{i=1}^{n} \frac{[\beta_{i} , a_{n}]}{[\beta_{i},\beta_{i}]}\beta_{i} + \beta_{n}
\end{align}
$$

令
$b_{ij} = \frac{[\beta_{i} , a_{j}]}{[\beta_{i},\beta_{i}]}$
则
$$
\begin{align}
\begin{pmatrix}
\alpha_{1} & \alpha_{2} & \alpha_{3} & \dots & \alpha_{n}
\end{pmatrix}  
 & = \begin{pmatrix}
\beta_{1} & \beta_{2} & \beta_{3} & \dots & \beta_{n}
\end{pmatrix}
\begin{pmatrix}
1 & b_{12} & b_{13} & \dots & b_{1n} \\ 
0  & 1 & b_{23} & \dots & b_{2n} \\
0  & 0 & 1 & \dots & b_{23n}\\
\dots  & \dots & \dots & \dots & \dots\\
0 & 0 & 0 & \dots & 1
\end{pmatrix} \\
\end{align}
$$
又因为$\beta_{i}$可以被单位化
$$
\begin{align}
\eta_{i} = \frac{1}{|\beta_{i}|}\beta_{i} \\
\beta_{i} = |\beta_{i}|\eta_{i}
\end{align}
$$
$$
\begin{align} \\
 & \begin{pmatrix}
\alpha_{1} & \alpha_{2} & \alpha_{3} & \dots & \alpha_{n}
\end{pmatrix}   \\
 & = \begin{pmatrix}
|\beta_{1}|\eta_{1} & |\beta_{2}|\eta_{2} & |\beta_{3}|\eta_{3}& \dots & |\beta_{n}|\eta_{n}
\end{pmatrix}
\begin{pmatrix}
1 & b_{12} & b_{13} & \dots & b_{1n} \\ 
0  & 1 & b_{23} & \dots & b_{2n} \\
0  & 0 & 1 & \dots & b_{23n}\\
\dots  & \dots & \dots & \dots & \dots\\
0 & 0 & 0 & \dots & 1
\end{pmatrix} \\
 & = 
\begin{pmatrix}
\eta_{1} & \eta_{2} & \eta_{3}& \dots & \eta_{n}
\end{pmatrix} 
\begin{pmatrix}
|\beta_{1}| & 0 & 0 & \dots & 0 \\
0 & |\beta_{2}| & 0 & \dots & 0 \\
0 & 0 & |\beta_{3}| & \dots & 0 \\
\dots & \dots & \dots & \dots & \dots \\
0 & 0 & 0 & \dots & |\beta_{n}|
\end{pmatrix}
\begin{pmatrix}
1 & b_{12} & b_{13} & \dots & b_{1n} \\ 
0  & 1 & b_{23} & \dots & b_{2n} \\
0  & 0 & 1 & \dots & b_{23n}\\
\dots  & \dots & \dots & \dots & \dots\\
0 & 0 & 0 & \dots & 1
\end{pmatrix}  \\
 & =\begin{pmatrix}
\eta_{1} & \eta_{2} & \eta_{3}& \dots & \eta_{n}
\end{pmatrix}  
\begin{pmatrix}
|\beta_{1}| & |\beta_{1}|b_{12} &|\beta_{1}| b_{13} & \dots & |\beta_{1}|b_{1n} \\ 
0  & |\beta_{2}|  & |\beta_{2}|b_{23} & \dots & |\beta_{2}|b_{2n} \\
0  & 0 & |\beta_{3}|  & \dots & |\beta_{3}|b_{23n}\\
\dots  & \dots & \dots & \dots & \dots\\
0 & 0 & 0 & \dots & |\beta_{n}| 
\end{pmatrix} 
\end{align}
$$

