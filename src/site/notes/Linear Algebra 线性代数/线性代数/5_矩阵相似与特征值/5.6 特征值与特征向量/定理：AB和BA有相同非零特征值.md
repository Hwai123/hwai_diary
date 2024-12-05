---
{"dg-publish":true,"permalink":"/Linear Algebra 线性代数/线性代数/5_矩阵相似与特征值/5.6 特征值与特征向量/定理：AB和BA有相同非零特征值/","tags":["线代"]}
---

1. 证明 $AB$ 和 $BA$ 有相同的非零特征值
2. 证明 $AB$ 和 $BA$ 相同的非零特征值的重数也相同

**证明相同非零特征值**

假设有一个$\lambda_{0}$能让$|\lambda_{0}I - AB| = 0$

> [!NOTE] 思路
> 证明两者有同样的特征值
> 也就是证明$|\lambda_{0}I - AB| = |\lambda_{0}I - BA| = 0$
> 可以看出这个行列式的形式类似于[[Linear Algebra 线性代数/线性代数/4_矩阵计算/4.5 分块矩阵/定理：I - AB = I - BA\|定理：I - AB = I - BA]]
> 尝试去用这个定理证明

设$A$为$n\times s$矩阵，$B$为$s\times n$矩阵
$$
\begin{align}
|\lambda_{0}I_{n} - AB|  & = \lambda_{0}^{n}|I_{n} - \frac{1}{\lambda_{0}}AB|  \\
 & = \lambda_{0}^{n}|I_{s} - B\frac{1}{\lambda_{0}}A| \\
 & = \lambda_{0}^{n-s}|\lambda_{0}I_{s} - BA|
\end{align}
$$
因此$AB$ 和 $BA$ 有相同的非零特征值

**证明重数相同**

> [!NOTE] 思路
> 证明重数相同
> $\to$ 证明特征多项式有都有同样的 $l$ 重因式$(\lambda - \lambda_{0})^{l}$

把特征多项式因式分解
$$
|\lambda I_{n} - AB| = (\lambda - \lambda_{0})^{l_{0}}(\lambda - \lambda_{1})^{l_{1}}\dots(\lambda - \lambda_{m})^{l_{m}}
$$
把他带入上一个公式
$$
\begin{align}
|\lambda I_{n} - AB|  & = \lambda ^{n-s}|\lambda I_{s} - BA| \\
\lambda^{n}|\lambda I_{s} - BA|  & = (\lambda - \lambda_{0})^{l_{0}}(\lambda - \lambda_{1})^{l_{1}}\dots(\lambda - \lambda_{m})^{l_{m}}\lambda^{s} \\
\end{align}
$$
因此$\lambda_{0}$在都是$AB$和$BA$的$l_{0}$重特征值