
# 前言

# 一些我认为比较重要的命题的证明

**证明:** 设无限集 $E$, 从 $E$ 中取出一个元素 $e_1$, 那么 $E\backslash\{e_1\}$ 仍是无限集, 所以又可以取出 $e_2$...那么得到集合

$$
\{e_1, e_2, e_3, \cdots\}
$$

且满足

$$
\overline{\overline{\{e_1,e_2,e_3,\cdots \}}}=\overline{\overline{\left\{ 1,2,3,\cdots \right\} }}
$$

同时 $E\backslash\{e_1,e_2,\cdots\}$ 仍是无限集, 还有

$$
\overline{\overline{E}}\geqslant \aleph _0
$$

证毕.

> **(Cantor-Bernstein-Schröder 定理)** 反对称性: 若同时成立 $\overline{\overline{E}}\geqslant \overline{\overline{F}}$ 和 $\overline{\overline{F}}\geqslant \overline{\overline{E}}$, 则必有 $\overline{\overline{E}}=\overline{\overline{F}}$.

**证明:** 构造双射

$$
\varphi : F_n\mapsto E_{n+1}\subseteq E\qquad\psi : E_n\mapsto F_{n+1}\subseteq F\qquad n=0,1,2,\cdots
$$

并记

$$
E_0=E\qquad F_0=F
$$

>> 引理1: $E\supseteq E_1\supseteq E_2\supseteq \cdots,\,F\supseteq F_1\supseteq F_2\supseteq \cdots $
>>

*证明: * 利用 $E_1\subseteq E$ 我们嵌套一次复合函数

$$
F_2=\psi \circ\varphi \left( F \right) =\psi \left( E_1 \right) \subseteq \psi \left( E \right) =F_1
$$

得到

$$
F_2\subseteq F_1 \tag{1}
$$

再次

$$
\psi\circ \varphi \left( F_2 \right) \subseteq \psi \circ \varphi \left( F_1 \right)
$$

得到

$$
F_4\subseteq F_3
$$

反复运用这个手法就有

$$
F_{2n+2}\subseteq F_{2n+1}
$$

利用 $F_1\subseteq F$ 我们嵌套一次复合函数

$$
\psi \circ \varphi \left( F_1 \right) \subseteq \psi \circ \varphi \left( F \right)
$$

得到

$$
F_3\circ F_2
$$

反复运用这个手法就有

$$
F_{2n+1}\subseteq F_{2n}\tag{2}
$$

结合(1)(2)就有

$$
F\supseteq F_1\supseteq F_2\supseteq \cdots
$$

关于 $E$ 的陈述同理可证.

>> 引理2: $\psi \circ \varphi $ 是 $F_n\backslash F_{n+1}$ 到 $F_{n+2}\backslash F_{n+3}$ 的双射.
>>

*证明: * 因为 $\psi \circ \varphi$ 是 $F_n$ 到 $F_{n+2}$ 的双射, 我们只要对以下两个双射做差集即可

$$
F_n \mapsto F_{n+2}
$$

$$
F_{n+1} \mapsto F_{n+3}
$$

下面考究原命题. 注意到

$$
F=\left( \bigcap_{k=1}^{\infty}{F_k} \right) \bigcup{\left( F\backslash F_1 \right) \bigcup{\left( F_1\backslash F_2 \right) \bigcup{\left( F_2\backslash F_3 \right) \bigcup{\left( F_3\backslash F_4 \right) \bigcup{\cdots}}}}}
$$

$$
\begin{align*}
F_1=\left( \bigcap_{k=1}^{\infty}{F_k} \right) \bigcup{\left( F_1\backslash F_2 \right) \bigcup{\left( F_2\backslash F_3 \right) \bigcup{\left( F_3\backslash F_4 \right) \bigcup{\left( F_4\backslash F_5 \right) \bigcup{\cdots}}}}}
\\
=\left( \bigcap_{k=1}^{\infty}{F_k} \right) \bigcup{\left( F_2\backslash F_3 \right) \bigcup{\left( F_1\backslash F_2 \right) \bigcup{\left( F_3\backslash F_4 \right) \bigcup{\left( F_4\backslash F_5 \right) \bigcup{\cdots}}}}}
\end{align*}
$$

两式右侧每一项对应为双射, 那么

$$
F\sim F_1
$$

又

$$
F_1\sim E
$$

所以

$$
F\sim E
$$

证毕.

> $(0,1)$, $[0,1]$ 与 $\mathbb{R}$ 等势, 它们的势都记作 $\aleph$, 称为**连续统**.

**证明:** 先证明 $(0,1)$ 与 $[0,1]$ 等式, 记

$$
A_1 = \left\{ 0,1,\frac{1}{2},\frac{1}{3},\frac{1}{4}\cdots \right\}
$$

$$
A_2 = \left\{ \frac{1}{2},\frac{1}{3},\frac{1}{4}\cdots \right\}
$$

$$
B=[0,1]\backslash A_1
$$

于是

$$
f(x)=\begin{cases}
	x&		x\in B\\
	\displaystyle\frac{1}{1/x-2}&		x\in A_2, x\ne \dfrac{1}{2}\\
	0		& 		x=\dfrac{1}{2}
\end{cases}
$$

就是一个 $(0,1)$ 到 $[0,1]$ 的双射.

构造

$$
\displaystyle
g\left( x \right) =\begin{cases}
	\ln 2x&		x\in \left( 0,\dfrac{1}{2} \right)\\
	-\ln \left( 2-2x \right)&		x\in \left( \dfrac{1}{2},1 \right)\\
	0&		x=\dfrac{1}{2}\\
\end{cases}
$$

就是一个 $(0,1)$ 到 $\mathbb{R}$ 的双射.

# 课后习题

## A组

> 1. 设 $a_0,a_1,\cdots ,a_n$ 为复常数, 且对任何的 $x\in\mathbb{R}$ 成立
>
> $$
> a_nx^n+a_{n-1}x^{n-1}+\cdots+a_1x+a_0=0
> $$
>
> 证明: $a_0=a_1=\cdots=a_0=0$.

**证明:** 先给出一个不太严谨的证法. 代入 $x=0$ 立刻得到

$$
a_0=0
$$

于是

$$
a_nx^n+a_{n-1}x^{n-1}+\cdots+a_1x+a_0=a_nx^n+a_{n-1}x^{n-1}+\cdots+a_1x=0
$$

约去 $x$

$$
a_nx^{n-1}+a_{n-1}x^{n-2}+\cdots+a_1=0\qquad (x\ne0)
$$

尽管 $x\ne0$, 但不严谨地, 我们反复运用这个手法就可以得到结果. 下面给出一个更加严格的证法, 这个证法经过考究存在学名"Lagrange 插值(Interpolation)法".

对于式子

$$
a_nx^n+a_{n-1}x^{n-1}+\cdots+a_1x=0
$$

让 $x$ 取遍 $n$ 个不同的非零值 $x_i(i=1,2,3,\cdots,n)$ 得到

$$
\begin{cases}
	a_1x_1+a_2x_{1}^{2}+\cdots +a_nx_{1}^{n}=0\\
	a_1x_2+a_2x_{2}^{2}+\cdots +a_nx_{2}^{n}=0\\
	\cdots\\
	a_1x_n+a_2x_{n}^{2}+\cdots +a_nx_{n}^{n}=0\\
\end{cases}
$$

视其为关于 $a_1,a_2,\cdots,a_n$ 的线性方程组, 其系数行列式为

$$
\left| \begin{matrix}
	x_1&		x_{1}^{2}&		\cdots&		x_{1}^{n}\\
	x_2&		x_{2}^{2}&		\cdots&		x_{2}^{n}\\
	\vdots&		\vdots&		\cdots&		\vdots\\
	x_n&		x_{n}^{2}&		\cdots&		x_{n}^{n}
\end{matrix} \right|=\prod_{i=1}^n{x_i}\left| \begin{matrix}
	1&		x_1&		\cdots&		x_{1}^{n-1}\\
	1&		x_2&		\cdots&		x_{2}^{n-1}\\
	\vdots&		\vdots&		\cdots&		\vdots\\
	1&		x_n&		\cdots&		x_{n}^{n-1}
\end{matrix} \right|=\prod_{i=1}^n{x_i}\prod_{1\leqslant i \lt j\leqslant n}{\left( x_i-x_j \right)}\ne 0
$$

上面的展开运用了 Vandermonde 行列式的性质. 由于系数行列式恒为 0, 所以

$$
a_i=0\qquad i=1,2,3\cdots,n
$$

> 2. 试构造区间 $(0,1)$ 到 $[0,1]$ 的一个双射.

见前文.

> 3. 说明以下映射为有理数集到整数集的单射
>
> $$
> T\left( q \right) =\begin{cases}
>   \left( m+n \right) ^2+n&		q=\dfrac{n}{m}&		n,m\text{为既约正整数}\\
>   0&		q=0&		\,\,\\
>   -(m+n)^2=n&		q=-\dfrac{n}{m}&		n,m\text{为既约正整数}\\
> \end{cases}
> $$

**证明:** 只需证明整数情形即可, 设

$$
q_1=\dfrac{n_1}{m_1}\qquad q_2=\dfrac{n_2}{m_2}
$$

且 $n_1,m_1$ 既约, $n_2,m_2$ 既约, $q_1,q_2>0$, $q_1\ne q_2$, 下面试图通过等式

$$
(m_1+n_1)^2+n_1=(m_2+n_2)^2+n_2
$$

导出矛盾. 容易验证, 若 $m_1=m_2$ 或 $n_1=n_2$ 成立其一, 可以导出另外一个, 下面讨论更一般情形 $m_1\ne m_2$ 且 $n_1\ne n_2$, 不失一般性, 令 $n_1>n_2$, 于是

$$
m_1+n_1<m_2+n_2
$$

由于都是正整数, 所以

$$
(m_2+n_2)-(m_1+n_1)>1
$$

于是

$$
\begin{align*}
(m_2+n_2)^2-(m_1+n_1)^2-n_1&=\left[ \left( m_1+n_1 \right) +\left( m_2+n_2 \right) -\left( m_1+n_1 \right) \right] ^2-\left( m_1+n_1 \right) ^2-n_1
\\
&=2\left( m_1+n_1 \right) \left[ \left( m_2+n_2 \right) -\left( m_1+n_1 \right) \right] +\left[ \left( m_2+n_2 \right) -\left( m_1+n_1 \right) \right] ^2-n_1
\\
&>2\left( m_1+n_1 \right) +\left[ \left( m_2+n_2 \right) -\left( m_1+n_1 \right) \right] ^2-n_1
\\
&>0
\end{align*}
$$

所以

$$
(m_1+n_1)^2+n_1<(m_2+n_2)^2+n_2
$$

矛盾! 所以原函数在 $q>0$ 时是单射, 证毕.

> 4. 证明代数数集是可列集.

**证明:** 显然给定一个整系数多项式, 它的系数构成的集合是可列的. 又对于给定的 $n\in\mathbb{N}$, $n$ 次多项式构成的集合是克列的, 所以整系数多项式构成的集合是可列的. 对于 $n$ 次整系数多项式, 其根构成的集合是可列的, 所以代数数集是可列的.

> 5. 证明: 存在常数 $A>0$ 使得对于任何整数 $q$ 和正整数 $p$, 成立
>
> $$
> \left| \sqrt{3}-\frac{q}{p} \right|>\frac{A}{p^2}
> $$

**证明:** 注意到 $x=\sqrt{3}$ 是以下方程的一个根

$$
x^2-3=0
$$

根据 Diophantus 逼近的 Liouville 定理, 立刻得证.

## B组

> 1. 设 $P$ 为首系数不为零的 $n$ 次复系数多项式, $x_1$ 是它的一个零点. 则首项系数不为零的 $n-1$ 次多项式 $Q$ 使得
>
> $$
> P(x)=(x-x_1)Q(x)
> $$

$$
\begin{align*}
f\left( x \right) &=a_nx^n+a_{n-1}x^{n-1}+\cdots +a_1x+a_0
\\
&=a_n\left( x^n-x_{1}^{n} \right) +a_{n-1}\left( x^{n-1}-x_{1}^{n-1} \right) +\cdots +a_1\left( x-x_1 \right) +a_0+a_nx_{1}^{n}+a_{n-1}x_{1}^{n-1}+\cdots +a_1x_1
\\
&=a_n\left( x^n-x_{1}^{n} \right) +a_{n-1}\left( x^{n-1}-x_{1}^{n-1} \right) +\cdots +a_1\left( x-x_1 \right) +f\left( x_1 \right) 
\\
&=a_n\left( x^n-x_{1}^{n} \right) +a_{n-1}\left( x^{n-1}-x_{1}^{n-1} \right) +\cdots +a_1\left( x-x_1 \right) 
\\
&=a_n\left( x-x_1 \right) \left( x^{n-1}+x_1x^{n-2}+\cdots +x_{1}^{n-2}x+x_{1}^{n-1} \right) +a_{n-1}\left( x-x_1 \right) \left( x^{n-2}+x_1x^{n-3}+\cdots +x_{1}^{n-3}x+x_{1}^{n-2} \right) +\cdots +a_1\left( x-x_1 \right) 
\\
&=\left( x-x_1 \right) \left( a_n\left( x^{n-1}+x_1x^{n-2}+\cdots +x_{1}^{n-2}x+x_{1}^{n-1} \right) +a_{n-1}\left( x^{n-2}+x_1x^{n-3}+\cdots +x_{1}^{n-3}x+x_{1}^{n-2} \right) +\cdots +a_1 \right) 
\\
&=\left( x-x_1 \right) \left( a_nx^{n-1}+\left( a_nx_1+a_{n-1} \right) x^{n-2}+\cdots +a_1 \right) 
\end{align*}
$$

> 2. **(代数基本定理)** 设 $a_0,a_1,\cdots,a_n$ 为复常数, $a_n\ne 0$. 证明: 多项式
>
> $$
> P(x)=a_nx^n+a_{n-1}x^{n-1}+\cdots+a_1x+a_0
> $$
>
> 至多有 $n$ 个复零点(含重数).

实际上这个题目的严格证明以及远远超出了目前的知识水平. 我本人没有能力解答, 答案也看不明白, 泪. 

> 3. 证明 Vièta 定理: 设 $a_n\ne0$, $x_1,x_2,\cdots,x_n$ 为
>
> $$
> P(x)=a_nx^n+a_{n-1}x^{n-1}+\cdots+a_1x+a_0
> $$
>
> 的 $n$ 个复零点(含重根), 则对于 $1\leqslant k\leqslant n$, 成立
>
> $$
> \sum_{1\leqslant m_1<m_2<\cdots <m_k\leqslant n}{\prod_{j=1}^k{x_{m_j}=\left( -1 \right) ^k\frac{a_{n-k}}{a_n}}}
> $$

**证明: ** 把 $P(x)$ 写成零点式

$$
P(x)=a_n(x-x_1)(x-x_2)\cdots (x-x_n)
$$

得到

$$
(x-x_1)(x-x_2)\cdots (x-x_n)=x^n+\frac{a_{n-1}}{a_n}x^{n-1}+\cdots +\frac{a_1}{a_n}x+\frac{a_0}{a_n}
$$

展开左边并比较两边系数即可证明.

> 4. 称关于 $x_1,x_2,\cdots,x_n$ 的 $m$ 次 $n$ 元多项式 $R(x_1,x_2,\cdots,x_n)$ 是 **可轮换的**, 如果对任何 $1\leqslant k<j\leqslant n$, 将 $R(x_1,x_2,\cdots,x_n)$ 中的 $x_k,x_j$ 分别替换成 $x_j,x_k$ 后多项式保持不变. 证明: 
>    (1) 若 $R(x_1,x_2,\cdots,x_n)$ 是可轮换的一次齐次多项式, 则它是 $x_1+x_2+\cdots x_n$ 的常数倍.
>    (2) 若 $R(x_1,x_2,\cdots,x_n)$ 是可轮换的二次齐次多项式, 则有常数 $C_1,C_2$, 使得
>
> $$
> R\left( x_1,x_2,\cdots ,x_n \right) \equiv C_1\left( x_{1}^{2}+x_{2}^{2}+\cdots +x_{n}^{2} \right) +C_2\sum_{1\leqslant i<j\leqslant n}{x_ix_j}
> $$
>
> (3) 归纳证明, 若 $R(x_1,x_2,\cdots,x_n)$ 是可轮换的 $k$ 次多项式, 而 $x_1,x_2,\cdots,x_n$ 是某首项系数不为零的 $n$ 次有理系数多项式的零点, 则 $R(x_1,x_2,\cdots,x_n)$ 为有理数.

**证明: ** (1) 依题意设

$$
R\left( x_1,x_2,\cdots ,x_n \right) =a_1x_1+a_2x_2+\cdots +a_nx_n
$$

那么

$$
R\left( x_1,\cdots ,x_k,\cdots ,x_j,\cdots ,x_n \right) -R\left( x_1,\cdots ,x_j,\cdots ,x_k,\cdots ,x_n \right) =a_k\left( x_k-x_j \right) +a_j\left( x_j-x_k \right) =\left( x_k-x_j \right) \left( a_k-a_j \right) =0
$$

所以

$$
a_k=a_j
$$

因为 $k,j$ 是取遍 $\{1,2,\cdots,n\}$ 的正整数对, 所以

$$
a_1=a_2=\cdots=a_n
$$

(2) 采用相同的方法, 依题意, 设

$$
R\left( x_1,x_2,\cdots ,x_n \right) =a_1x_{1}^{2}+a_2x_{2}^{2}+\cdots +a_nx_{n}^{2}+b_{12}x_1x_2+b_{13}x_1x_3+\cdots +b_{1n}x_1x_n+b_{23}x_2x_3+\cdots +b_{n-1,n}x_{n-1}x_n
$$

那么

$$
\begin{align*}
&R\left( x_1,\cdots ,x_k,\cdots ,x_j,\cdots ,x_n \right) -R\left( x_1,\cdots ,x_j,\cdots ,x_k,\cdots ,x_n \right) \\
&=\left( a_k-a_j \right) \left( x_k+x_j \right) \left( x_k-x_j \right) +\sum_{\begin{array}{c}
	i=1\\
	i\ne k\\
\end{array}}^n{b_{ki}x_i\left( x_k-x_j \right)}-\sum_{\begin{array}{c}
	i=1\\
	i\ne j\\
\end{array}}^n{b_{ji}x_i\left( x_k-x_j \right)}
\\
&=\left( x_k-x_j \right) \left( \left( a_k-a_j \right) \left( x_k+x_j \right) +\sum_{\begin{array}{c}
	i=1\\
	i\ne k\\
\end{array}}^n{b_{ki}x_i-\sum_{\begin{array}{c}
	i=1\\
	i\ne j\\
\end{array}}^n{b_{ji}x_i}} \right) 
\\
&=\left( x_k-x_j \right) \left( \left( b_{k1}-b_{j1} \right) x_1+\left( b_{k2}-b_{j2} \right) x_2+\cdots +\left( a_k-b_{jk} \right) x_k+\cdots +\left( b_{kj}-a_j \right) x_j+\cdots +\left( b_{kn}-b_{jn} \right) x_n \right) 
\\
&=0
\end{align*}
$$

就此推得所有的 $b$ 都是相同的, 且

$$
a_kx_k-a_jx_j+b_{jk}\left( x_j-x_k \right) =0
$$

只有 $a_k=a_j$ 时才能实现. 所以所有的 $a$ 都相同. 

(3) 本题实际上是要证明**对称多项式基本定理**, 之后利用 Viète 定理立刻得证, 以下是定理的叙述与证明(证明来自 ChatGPT-4o): 


### 定理陈述

对于任意一个对称多项式 $f(x_1, x_2, \ldots, x_n)$, 都存在一个多项式 $g$ 满足

$$
f(x_1, x_2, \ldots, x_n) = g(e_1, e_2, \ldots, e_n)
$$

其中 $e_i$ 是 $x_1, x_2, \ldots, x_n$ 的初等对称多项式. 

### 初等对称多项式定义

初等对称多项式 $e_i(x_1, x_2, \ldots, x_n)$ 定义为: 

$$
\begin{align*}
e_0 &= 1\\
e_1 &= x_1 + x_2 + \cdots + x_n\\
e_2 &= \sum_{1 \leq i < j \leq n} x_i x_j\\
&\vdots\\
e_n &= x_1 x_2 \cdots x_n\\
\end{align*}
$$

### 证明

**步骤 1: 单项式表达**

首先, 我们考虑对称多项式 $f(x_1, x_2, \ldots, x_n)$ 的单项式表达. 假设 $f$ 可以表示为: 

$$
f(x_1, x_2, \ldots, x_n) = \sum_{\alpha} c_{\alpha} x_1^{\alpha_1} x_2^{\alpha_2} \cdots x_n^{\alpha_n}
$$

其中 $\alpha = (\alpha_1, \alpha_2, \ldots, \alpha_n)$ 是一个多重指数,  $c_{\alpha}$ 是常数系数. 

**步骤 2: 对称性**

由于 $f$ 是对称多项式, 对于任意置换 $\sigma \in S_n$ 有: 

$$
f(x_{\sigma(1)}, x_{\sigma(2)}, \ldots, x_{\sigma(n)}) = f(x_1, x_2, \ldots, x_n)
$$

因此, 单项式 $x_1^{\alpha_1} x_2^{\alpha_2} \cdots x_n^{\alpha_n}$ 的系数 $c_{\alpha}$ 必须在所有不同排列下相同. 

**步骤 3: 对称多项式基底**

接下来, 我们使用初等对称多项式 $e_1, e_2, \ldots, e_n$ 作为基底. 我们希望找到一个多项式 $g$, 使得: 

$$
f(x_1, x_2, \ldots, x_n) = g(e_1, e_2, \ldots, e_n)
$$

考虑多项式环 $\mathbb{R}[x_1, x_2, \ldots, x_n]$ 中的理想 $I$, 由初等对称多项式生成: 

$$
I = \langle e_1, e_2, \ldots, e_n \rangle
$$

对于任意对称多项式 $f$, 存在一个多项式 $h$, 使得: 

$$
f(x_1, x_2, \ldots, x_n) \in I
$$

这意味着 $f$ 可以表示为初等对称多项式 $e_i$ 的多项式: 

$$
f(x_1, x_2, \ldots, x_n) = h(e_1, e_2, \ldots, e_n)
$$

**步骤 4: 构造 $g$**

由于 $e_i$ 是 $x_i$ 的多项式, 因此 $f$ 是 $e_i$ 的多项式. 我们将 $f$ 写作 $g(e_1, e_2, \ldots, e_n)$, 并证明存在这样的 $g$. 

考虑 $f$ 的每一项 $x_1^{\alpha_1} x_2^{\alpha_2} \cdots x_n^{\alpha_n}$: 

1. 对于 $\alpha$ 中所有的 $\alpha_i$ 都相同的项(如 $x_1^k x_2^k \cdots x_n^k$), 它们可以直接表示为 $e_i$ 的幂次. 
2. 对于混合项, 我们通过初等对称多项式的展开表示这些项为 $e_i$ 的组合. 

因此, 所有对称多项式 $f$ 都可以表示为初等对称多项式的多项式 $g(e_1, e_2, \ldots, e_n)$. 



> 5. 设 $P,Q$ 分别是 $m,n$ 阶首系数为 1 的有理系数多项式.
> $$P\left( x \right) =\prod_{k=1}^m{\left( x-x_k \right) ,\qquad Q\left( x \right) =\prod_{k=1}^n{\left( x-y_k \right)}}$$
> 证明: 
> (1) 多项式 $=R\left( x \right) =\displaystyle\prod_{k=1}^m{\prod_{j=1}^n{\left( x-x_k-y_j \right)}}$ 是有理系数多项式.
> (2) 多项式 $S\left( x \right) =\prod_{k=1}^m{\prod_{j=1}^n{\left( x-x_ky_j \right)}}$ 是有理系数多项式.

> 6. 证明 Liouville 定理.

> 7. 证明一个复数是代数数当且仅当它的实部和虚部都是代数数.

