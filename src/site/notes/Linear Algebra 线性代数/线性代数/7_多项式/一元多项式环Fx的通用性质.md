---
{"dg-publish":true,"permalink":"/Linear Algebra 线性代数/线性代数/7_多项式/一元多项式环Fx的通用性质/","tags":["线代","定理"]}
---

设$K$是一个数域，$R$是有单位元$e$的交换[[Linear Algebra 线性代数/线性代数/7_多项式/环\|环]]且$K$到$R$的一个子环$R^{\prime}$(含有单位元$e$)有一个 [[Linear Algebra 线性代数/线性代数/7_多项式/环的同构映射\|环的同构映射]]$\sigma_{t}$，使得
$$
\begin{align}
K[x] \to R \\
f(x) = \sum_{i = 0}^{n}a_{i}x^{i} \to \sum_{i=0}^{n}a_{i}t^{i}
\end{align}
$$
则$\sigma_{t}$**是$K$到$R$的映射**，$\sigma_{t}(x) = t$，
$\sigma_{t}$保持加法和乘法运算，即
$$
\begin{align}
f(x) + g(x) = h(x),f(x)g(x) = P(x) \\
f(t) + g(t) = h(t),f(t)g(t) = P(t) \\

\end{align}
$$
称$\sigma_{t}$**是$x$的通用代入**