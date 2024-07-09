# 泛函分析中的 Euler 方程与最小作用量原理的联系

## 变分算符 $\delta$

对于性质良好的函数
$$
y=y(x)
$$
$\delta y$ 表示任意性质良好的保端点小值函数，其中，保端点的意思是
$$
\left.\delta y\right|_{x=a}\equiv\left.\delta y\right|_{x=b}\equiv0
$$
对于泛函
$$
F(y,y',y'',\cdots,y^{(n)},x)
$$
作用在其上的变分算符 $\delta$ 满足链式法则
$$
\delta F=\sum_{i=0}^n{\frac{\partial F}{\partial y^{\left( i \right)}}\delta y^{\left( i \right)}}=\frac{\partial F}{\partial y}\delta y+\frac{\partial F}{\partial y'}\delta y'+\frac{\partial F}{\partial y''}\delta y''+\cdots +\frac{\partial F}{\partial y^{\left( n \right)}}\delta y^{\left( n \right)}
$$


## Euler 方程

对于如下所示的泛函
$$
S\left[ y \right] =\int_a^b{F\left( y,y',x \right) \mathrm{d}x}
$$
为求得其极值，对其做一次变分
$$
\begin{align*}
\delta S&=\int_a^b{\left( \frac{\partial F}{\partial y}\delta y+\frac{\partial F}{\partial y'}\delta y' \right) \mathrm{d}x}
\\\\
&=\int_a^b{\left( \frac{\partial F}{\partial y}\delta y+\frac{\partial F}{\partial y‘}\delta \left( \frac{\mathrm{d}y}{\mathrm{d}x} \right) \right) \mathrm{d}x}
\\\\
&=\int_a^b{\left( \frac{\partial F}{\partial y}\delta y\mathrm{d}x+\frac{\partial F}{\partial y’}\delta \left( \mathrm{d}y \right) \right)}
\\\\
&=\int_a^b{\left( \frac{\partial F}{\partial y}\delta y\mathrm{d}x+\frac{\partial F}{\partial y‘}\mathrm{d}\left( \delta y \right) \right)}
\\\\
&=\int_a^b{\left( \frac{\partial F}{\partial y}\delta y\mathrm{d}x+\mathrm{d}\left( \frac{\partial F}{\partial y’}\delta y \right) -\delta y\mathrm{d}\left( \frac{\partial F}{\partial y’} \right) \right)}
\\\\
&=\int_a^b{\left( \frac{\partial F}{\partial y}\delta y\mathrm{d}x-\delta y\mathrm{d}\left( \frac{\partial F}{\partial y‘} \right) \right)}+\left. \frac{\partial F}{\partial y‘}\delta y \right|_{a}^{b}
\\\\
&=\int_a^b{\left( \frac{\partial F}{\partial y}\delta y\mathrm{d}x-\delta y\mathrm{d}\left( \frac{\partial F}{\partial y’} \right) \right)}
\\\\
&=\int_a^b{\left( \frac{\partial F}{\partial y}-\frac{\mathrm{d}}{\mathrm{d}x}\frac{\partial F}{\partial y’} \right)}\delta y\mathrm{d}x
\end{align*}
$$
可以看到，泛函取得极值的一个必要条件是
$$
\begin{equation}
\frac{\partial F}{\partial y}-\frac{\mathrm{d}}{\mathrm{d}x}\frac{\partial F}{\partial y’}=0
\end{equation}
$$

## 最小作用量原理

最小作用量原理又称 Hamilton 原理，原理指出，每一个力学系统都可以由一个确定的函数
$$
L(q,\dot{q},t)
$$
表征，称为 Lagrange 函数，其中
$$
q=(q_1,q_2,\cdots,q_s)
$$
$s\in\mathbb{N_+}$ 表示系统的自由度. Lagrange 函数的具体形式将由以下条件给出
$$
S=\int_{t_1}^{t_2}L\,\mathrm{d}t
$$

$$
\delta S=0
$$

$S$ 称为系统的作用量，$\delta S=0$ 意思是 Lagrange 函数的具体形式使得作用量取最小值. 显然作用量是无法取得极大值的，而对于取得的极小值是最小值这一论述，则不太好说明.

## 练习

**试导出最速降线方程.**

**解：**根据功能关系，我们知道下降 $y$ 后质点获得的速度为
$$
v=\sqrt{2gy}
$$
弧微元被表示为
$$
\mathrm{d}s=\sqrt{1+y'^2}\mathrm{d}x
$$
所以时间微元可以写作
$$
\mathrm{d}t=\frac{\sqrt{1+y'^2}}{\sqrt{2gy}}\mathrm{d}x
$$
我们所关心的全时长是路径函数的泛函
$$
t=\int_0^{x_0}{\frac{\sqrt{1+y'^2}}{\sqrt{2gy}}\mathrm{d}x}
$$
记
$$
K=\frac{ \sqrt{1+y'^2}   }{\sqrt{2gy}}
$$
直接套用 Euler 方程得到的是一个十分复杂的微分方程(读者可以自行尝试)，为改善这一点，我们可以利用 $K$ 不显含 $x$ 这一性质，以下是对 Euler 方程的一些变形.

首先，做如下考量
$$
\begin{align*}
\frac{\mathrm{d}F}{\mathrm{d}y}&=\frac{\partial F}{\partial y}+\frac{\partial F}{\partial y'}\frac{\mathrm{d}y'}{\mathrm{d}y}+\frac{\partial F}{\partial x}\frac{\mathrm{d}x}{\mathrm{d}y}
\\\\
&=\frac{\partial F}{\partial y}+\frac{\partial F}{\partial y'}\frac{\mathrm{d}y'}{\mathrm{d}y}
\end{align*}
$$
上式第二个等号的成立要求 $F$ 不显含 $x$，这样就有
$$
\frac{\partial F}{\partial x}=0
$$
这样得到
$$
\frac{\partial F}{\partial y}=\frac{\mathrm{d}F}{\mathrm{d}y}-\frac{\partial F}{\partial y'}\frac{\mathrm{d}y'}{\mathrm{d}y}
$$
代回 Euler 方程
$$
\frac{\mathrm{d}F}{\mathrm{d}y}-\frac{\partial F}{\partial y\prime}\frac{\mathrm{d}y\prime}{\mathrm{d}y}-\frac{\mathrm{d}}{\mathrm{d}x}\frac{\partial F}{\partial y’}=0
$$
下面做一个求导算子的恒等变形
$$
\frac{\mathrm{d}}{\mathrm{d}x}=\frac{\mathrm{d}y}{\mathrm{d}x}\frac{\mathrm{d}}{\mathrm{d}y}=y'\frac{\mathrm{d}}{\mathrm{d}y}
$$
代回 Euler 方程
$$
\frac{\mathrm{d}F}{\mathrm{d}y}-\frac{\partial F}{\partial y\prime}\frac{\mathrm{d}y\prime}{\mathrm{d}y}-y'\frac{\mathrm{d}}{\mathrm{d}y}\frac{\partial F}{\partial y’}=0
\\\\
\frac{\mathrm{d}F}{\mathrm{d}y}-\frac{\mathrm{d}}{\mathrm{d}y}\left( y'\frac{\partial F}{\partial y'} \right) =0
\\\\
\frac{\mathrm{d}}{\mathrm{d}y}\left( F-y'\frac{\partial F}{\partial y'} \right) =0
$$

$$
\begin{equation}
F-y'\frac{\partial F}{\partial y'}=C
\end{equation}
$$

将上式用于本题得到
$$
K-y'\frac{\partial K}{\partial y'}=C
$$

$$
\frac{ \sqrt{1+y'^2}   }{\sqrt{2gy}}-y'\frac{1}{2}\frac{2y'}{\sqrt{2gy}\sqrt{1+y'^2}}=C
$$

$$
\frac{1}{\sqrt{1+y'^2}\sqrt{2gy}}=C
$$

$$
y(1+y'^2)=C
$$

这个微分方程可分离变量，是好解的，解是摆线方程
$$
\begin{cases}
	x=C\left( \theta -\sin \theta \right)\\\\
	y=C\left( 1-\cos \theta \right)\\
\end{cases}
$$

## 后记

本文的 markdown 格式源代码以上传至 Github, 复制以下代码到终端可下载源文件

```bash
git clone https://github.com/SweetPastry/Markdown
```

