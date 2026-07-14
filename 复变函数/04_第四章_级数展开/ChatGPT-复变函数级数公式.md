# 复变函数级数公式

**User:** Anonymous  
**Created:** 7/3/2026 17:20:57  
**Updated:** 7/3/2026 17:22:54  
**Exported:** 7/3/2026 17:43:23  
**Link:** [https://chatgpt.com/c/6a477edc-61b0-83ee-af64-ee9fe978c8af?mweb_fallback=1](https://chatgpt.com/c/6a477edc-61b0-83ee-af64-ee9fe978c8af?mweb_fallback=1)  

## Response:
2026/7/3 17:20:55

下面按**复变函数“级数”章节**整理成：**默写模板版** + **答案版**。适合期末前直接背公式、刷题时套用。

# 一、默写模板版

## 0. 级数部分总框架

复变函数级数主要分为：

$$
\boxed{
\text{复数项级数}
\rightarrow
\text{函数项级数}
\rightarrow
\text{幂级数}
\rightarrow
\text{Taylor 级数}
\rightarrow
\text{Laurent 级数}
}
$$

核心问题：

$$
\boxed{
\text{收敛性}
+
\text{收敛半径}
+
\text{展开}
+
\text{逐项运算}
+
\text{奇点判断}
}
$$

---

# 1. 复数项级数

## 1.1 复数项级数定义

设

$$
\sum_{n=1}^{\infty} z_n
$$

其中 $z_n\in \mathbb C$。若部分和

$$
S_N=\underline{\qquad}
$$

存在有限极限 $S$，则称级数收敛，且

$$
\sum_{n=1}^{\infty}z_n=\underline{\qquad}
$$

---

## 1.2 收敛的必要条件

若

$$
\sum_{n=1}^{\infty}z_n
$$

收敛，则必须有

$$
\lim_{n\to\infty}z_n=\underline{\qquad}
$$

---

## 1.3 绝对收敛

若

$$
\sum_{n=1}^{\infty}|z_n|
$$

收敛，则称

$$
\sum_{n=1}^{\infty}z_n
$$

$$
\underline{\qquad}
$$

且绝对收敛必然推出：

$$
\sum z_n \ \underline{\qquad}
$$

---

## 1.4 复级数与实部虚部

设

$$
z_n=x_n+iy_n
$$

则

$$
\sum z_n \text{ 收敛}
\Longleftrightarrow
\underline{\qquad}
$$

并且

$$
\sum z_n=
\underline{\qquad}
$$

---

## 1.5 比值判别法

设

$$
\lim_{n\to\infty}\left|\frac{z_{n+1}}{z_n}\right|=\rho
$$

则：

$$
\rho<1 \Rightarrow \underline{\qquad}
$$

$$
\rho>1 \Rightarrow \underline{\qquad}
$$

$$
\rho=1 \Rightarrow \underline{\qquad}
$$

---

## 1.6 根值判别法

设

$$
\limsup_{n\to\infty}\sqrt[n]{|z_n|}=\rho
$$

则：

$$
\rho<1 \Rightarrow \underline{\qquad}
$$

$$
\rho>1 \Rightarrow \underline{\qquad}
$$

$$
\rho=1 \Rightarrow \underline{\qquad}
$$

---

# 2. 函数项级数

## 2.1 函数项级数

函数项级数为：

$$
\sum_{n=1}^{\infty}f_n(z)
$$

其部分和为：

$$
S_N(z)=\underline{\qquad}
$$

若对每个 $z\in D$，都有

$$
S_N(z)\to S(z)
$$

则称级数在 $D$ 上：

$$
\underline{\qquad}
$$

---

## 2.2 一致收敛定义

若

$$
\forall \varepsilon>0,\exists N,\forall n>N,\forall z\in D
$$

都有

$$
|S_n(z)-S(z)|<\underline{\qquad}
$$

则称

$$
S_n(z)\to S(z)
$$

在 $D$ 上：

$$
\underline{\qquad}
$$

---

## 2.3 Weierstrass 判别法

若存在正项数列 $M_n$，使得

$$
|f_n(z)|\le M_n,\quad z\in D
$$

且

$$
\sum_{n=1}^{\infty}M_n
$$

$$
\underline{\qquad}
$$

则

$$
\sum_{n=1}^{\infty}f_n(z)
$$

在 $D$ 上：

$$
\underline{\qquad}
$$

---

## 2.4 一致收敛与连续性

若 $f_n(z)$ 在 $D$ 上连续，且

$$
\sum f_n(z)
$$

在 $D$ 上一致收敛于 $f(z)$，则

$$
f(z)
$$

在 $D$ 上：

$$
\underline{\qquad}
$$

---

## 2.5 一致收敛与解析性

若 $f_n(z)$ 在区域 $D$ 内解析，且

$$
\sum f_n(z)
$$

在 $D$ 的任意闭子区域上一致收敛，则和函数 $f(z)$ 在 $D$ 内：

$$
\underline{\qquad}
$$

并且可以：

$$
\underline{\qquad}
$$

---

# 3. 幂级数

## 3.1 幂级数标准形式

以 $z_0$ 为中心的幂级数：

$$
\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

其中 $a_n\in\mathbb C$。

---

## 3.2 收敛圆

幂级数的收敛区域是：

$$
|z-z_0|<\underline{\qquad}
$$

发散区域是：

$$
|z-z_0|>\underline{\qquad}
$$

边界：

$$
|z-z_0|=\underline{\qquad}
$$

需要：

$$
\underline{\qquad}
$$

---

## 3.3 Cauchy-Hadamard 公式

收敛半径 $R$ 满足：

$$
\frac{1}{R}
=
\limsup_{n\to\infty}\sqrt[n]{|a_n|}
$$

所以

$$
R=
\underline{\qquad}
$$

特殊约定：

$$
\limsup\sqrt[n]{|a_n|}=0
\Rightarrow R=\underline{\qquad}
$$

$$
\limsup\sqrt[n]{|a_n|}=+\infty
\Rightarrow R=\underline{\qquad}
$$

---

## 3.4 比值法求收敛半径

若

$$
\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|
$$

存在，则

$$
R=
\underline{\qquad}
$$

也可由：

$$
\lim_{n\to\infty}
\left|
\frac{a_{n+1}(z-z_0)^{n+1}}
{a_n(z-z_0)^n}
\right|
<1
$$

得到：

$$
|z-z_0|<\underline{\qquad}
$$

---

## 3.5 根值法求收敛半径

由

$$
\limsup_{n\to\infty}
\sqrt[n]{|a_n(z-z_0)^n|}
<1
$$

得到：

$$
|z-z_0|
\limsup_{n\to\infty}\sqrt[n]{|a_n|}
<1
$$

所以：

$$
R=\underline{\qquad}
$$

---

## 3.6 幂级数的解析性

若

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

在

$$
|z-z_0|<R
$$

内收敛，则 $f(z)$ 在该圆内：

$$
\underline{\qquad}
$$

---

## 3.7 幂级数逐项求导

若

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

则

$$
f'(z)=
\underline{\qquad}
$$

更一般地：

$$
f^{(k)}(z)=
\underline{\qquad}
$$

---

## 3.8 幂级数逐项积分

$$
\int_{z_0}^{z} f(\zeta)d\zeta
=
\underline{\qquad}
$$

---

## 3.9 系数与导数关系

若

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

则

$$
a_n=
\underline{\qquad}
$$

---

# 4. 常用初等函数 Taylor 展开

## 4.1 指数函数

$$
e^z=
\underline{\qquad}
$$

收敛半径：

$$
R=\underline{\qquad}
$$

---

## 4.2 正弦函数

$$
\sin z=
\underline{\qquad}
$$

收敛半径：

$$
R=\underline{\qquad}
$$

---

## 4.3 余弦函数

$$
\cos z=
\underline{\qquad}
$$

收敛半径：

$$
R=\underline{\qquad}
$$

---

## 4.4 几何级数

$$
\frac{1}{1-z}
=
\underline{\qquad}
$$

成立条件：

$$
\underline{\qquad}
$$

---

## 4.5 推广几何级数

$$
\frac{1}{1+z}
=
\underline{\qquad}
$$

成立条件：

$$
\underline{\qquad}
$$

---

## 4.6 对数函数

$$
\log(1+z)=
\underline{\qquad}
$$

成立条件：

$$
\underline{\qquad}
$$

---

## 4.7 二项式展开

$$
(1+z)^\alpha
=
\underline{\qquad}
$$

其中

$$
\binom{\alpha}{n}
=
\underline{\qquad}
$$

成立条件：

$$
\underline{\qquad}
$$

---

# 5. Taylor 级数

## 5.1 Taylor 展开定理

若 $f(z)$ 在圆盘

$$
|z-z_0|<R
$$

内解析，则

$$
f(z)=
\underline{\qquad}
$$

其中

$$
a_n=
\underline{\qquad}
$$

---

## 5.2 Cauchy 积分公式求系数

若 $C$ 是圆盘内围绕 $z_0$ 的正向简单闭曲线，则

$$
a_n=
\underline{\qquad}
$$

---

## 5.3 Taylor 展开唯一性

若

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
=
\sum_{n=0}^{\infty}b_n(z-z_0)^n
$$

则

$$
\underline{\qquad}
$$

---

## 5.4 Taylor 级数收敛半径与奇点距离

若 $f$ 在 $z_0$ 附近解析，则 Taylor 级数收敛半径等于：

$$
\underline{\qquad}
$$

---

# 6. Laurent 级数

## 6.1 Laurent 级数形式

在环域

$$
r<|z-z_0|<R
$$

内，Laurent 级数为：

$$
f(z)=
\underline{\qquad}
$$

也可写成：

$$
f(z)=
\underline{\qquad}
+
\underline{\qquad}
$$

---

## 6.2 Laurent 系数公式

$$
a_n=
\underline{\qquad}
$$

其中 $C$ 是环域内围绕 $z_0$ 的正向闭曲线。

---

## 6.3 正幂部分

$$
\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

称为：

$$
\underline{\qquad}
$$

---

## 6.4 负幂部分

$$
\sum_{n=1}^{\infty}a_{-n}(z-z_0)^{-n}
$$

称为：

$$
\underline{\qquad}
$$

---

## 6.5 Laurent 展开的唯一性

若 $f$ 在同一环域内有两个 Laurent 展开：

$$
\sum_{n=-\infty}^{\infty}a_n(z-z_0)^n
=
\sum_{n=-\infty}^{\infty}b_n(z-z_0)^n
$$

则：

$$
\underline{\qquad}
$$

---

# 7. Laurent 级数与孤立奇点

## 7.1 可去奇点

若 $f$ 在 $z_0$ 的去心邻域解析，Laurent 展开中负幂项：

$$
\underline{\qquad}
$$

则 $z_0$ 是：

$$
\underline{\qquad}
$$

等价条件：

$$
\lim_{z\to z_0} f(z)
$$

$$
\underline{\qquad}
$$

---

## 7.2 极点

若 Laurent 展开中负幂项有限，最高负幂为：

$$
\frac{a_{-m}}{(z-z_0)^m},\quad a_{-m}\ne0
$$

则 $z_0$ 是：

$$
\underline{\qquad}
$$

等价地：

$$
f(z)=\frac{\varphi(z)}{(z-z_0)^m}
$$

其中：

$$
\varphi(z_0)\underline{\qquad}0
$$

---

## 7.3 本性奇点

若 Laurent 展开中负幂项：

$$
\underline{\qquad}
$$

则 $z_0$ 是：

$$
\underline{\qquad}
$$

---

## 7.4 留数

Laurent 展开中：

$$
f(z)=\sum_{n=-\infty}^{\infty}a_n(z-z_0)^n
$$

则 $f$ 在 $z_0$ 的留数为：

$$
\operatorname{Res}(f,z_0)=
\underline{\qquad}
$$

也就是：

$$
\underline{\qquad}
$$

的系数。

---

# 8. 常见 Laurent 展开模板

## 8.1 几何级数展开核心公式

$$
\frac{1}{1-w}
=
\underline{\qquad}
$$

成立条件：

$$
\underline{\qquad}
$$

---

## 8.2 外部区域展开

当 $|z|>1$ 时：

$$
\frac{1}{z-1}
=
\underline{\qquad}
$$

---

## 8.3 内部区域展开

当 $|z|<1$ 时：

$$
\frac{1}{z-1}
=
\underline{\qquad}
$$

---

## 8.4 以 $z_0$ 为中心展开的换元

若要在 $z=z_0$ 附近展开，通常令：

$$
w=\underline{\qquad}
$$

然后把函数化成关于 $w$ 的：

$$
\underline{\qquad}
$$

---

# 二、答案版

# 1. 复数项级数

## 1.1 定义

$$
S_N=\sum_{n=1}^{N}z_n
$$

若

$$
\lim_{N\to\infty}S_N=S
$$

则

$$
\sum_{n=1}^{\infty}z_n=S
$$

---

## 1.2 必要条件

若

$$
\sum z_n
$$

收敛，则

$$
\boxed{
\lim_{n\to\infty}z_n=0
}
$$

注意：

$$
z_n\to0
$$

只是必要条件，不是充分条件。

---

## 1.3 绝对收敛

若

$$
\sum |z_n|
$$

收敛，则

$$
\sum z_n
$$

绝对收敛。

并且：

$$
\boxed{
\text{绝对收敛} \Rightarrow \text{收敛}
}
$$

---

## 1.4 实部虚部判别

设

$$
z_n=x_n+iy_n
$$

则

$$
\boxed{
\sum z_n \text{ 收敛}
\Longleftrightarrow
\sum x_n \text{ 收敛且 } \sum y_n \text{ 收敛}
}
$$

并且：

$$
\boxed{
\sum z_n
=
\sum x_n+i\sum y_n
}
$$

---

## 1.5 比值判别法

若

$$
\lim_{n\to\infty}
\left|
\frac{z_{n+1}}{z_n}
\right|
=
\rho
$$

则：

$$
\boxed{
\rho<1 \Rightarrow \sum z_n \text{ 绝对收敛}
}
$$

$$
\boxed{
\rho>1 \Rightarrow \sum z_n \text{ 发散}
}
$$

$$
\boxed{
\rho=1 \Rightarrow \text{无法判断}
}
$$

---

## 1.6 根值判别法

若

$$
\limsup_{n\to\infty}
\sqrt[n]{|z_n|}
=
\rho
$$

则：

$$
\boxed{
\rho<1 \Rightarrow \sum z_n \text{ 绝对收敛}
}
$$

$$
\boxed{
\rho>1 \Rightarrow \sum z_n \text{ 发散}
}
$$

$$
\boxed{
\rho=1 \Rightarrow \text{无法判断}
}
$$

---

# 2. 函数项级数

## 2.1 函数项级数

$$
\sum_{n=1}^{\infty}f_n(z)
$$

部分和：

$$
\boxed{
S_N(z)=\sum_{n=1}^{N}f_n(z)
}
$$

若对每个 $z\in D$，有

$$
S_N(z)\to S(z)
$$

则称函数项级数在 $D$ 上逐点收敛于 $S(z)$。

---

## 2.2 一致收敛

若

$$
\forall \varepsilon>0,\exists N,\forall n>N,\forall z\in D
$$

都有

$$
|S_n(z)-S(z)|<\varepsilon
$$

则称

$$
S_n(z)\to S(z)
$$

在 $D$ 上一致收敛。

---

## 2.3 Weierstrass 判别法

若

$$
|f_n(z)|\le M_n,\quad z\in D
$$

且

$$
\sum M_n
$$

收敛，则

$$
\boxed{
\sum f_n(z)
\text{ 在 }D\text{ 上一致收敛且绝对收敛}
}
$$

---

## 2.4 一致收敛与连续性

若 $f_n(z)$ 在 $D$ 上连续，且

$$
\sum f_n(z)
$$

在 $D$ 上一致收敛于 $f(z)$，则：

$$
\boxed{
f(z)\text{ 在 }D\text{ 上连续}
}
$$

---

## 2.5 一致收敛与解析性

若 $f_n(z)$ 在区域 $D$ 内解析，且

$$
\sum f_n(z)
$$

在 $D$ 的任意闭子区域上一致收敛，则和函数 $f(z)$ 在 $D$ 内解析，并且可以逐项求导：

$$
\boxed{
f'(z)=\sum_{n=1}^{\infty}f_n'(z)
}
$$

---

# 3. 幂级数

## 3.1 标准形式

$$
\boxed{
\sum_{n=0}^{\infty}a_n(z-z_0)^n
}
$$

其中：

$$
z_0：\text{中心}
$$

$$
a_n：\text{系数}
$$

---

## 3.2 收敛圆

存在 $R\in[0,+\infty]$，使得：

$$
\boxed{
|z-z_0|<R \Rightarrow \text{绝对收敛}
}
$$

$$
\boxed{
|z-z_0|>R \Rightarrow \text{发散}
}
$$

$$
\boxed{
|z-z_0|=R \Rightarrow \text{逐点单独判断}
}
$$

这里 $R$ 称为收敛半径。

---

## 3.3 Cauchy-Hadamard 公式

$$
\boxed{
\frac{1}{R}
=
\limsup_{n\to\infty}
\sqrt[n]{|a_n|}
}
$$

所以：

$$
\boxed{
R=
\frac{1}
{\limsup\limits_{n\to\infty}\sqrt[n]{|a_n|}}
}
$$

特殊情况：

$$
\limsup_{n\to\infty}\sqrt[n]{|a_n|}=0
\Rightarrow
\boxed{R=+\infty}
$$

$$
\limsup_{n\to\infty}\sqrt[n]{|a_n|}=+\infty
\Rightarrow
\boxed{R=0}
$$

---

## 3.4 比值法求收敛半径

若极限存在，则：

$$
\boxed{
R=
\lim_{n\to\infty}
\left|
\frac{a_n}{a_{n+1}}
\right|
}
$$

因为：

$$
\left|
\frac{a_{n+1}(z-z_0)^{n+1}}
{a_n(z-z_0)^n}
\right|
=
\left|
\frac{a_{n+1}}{a_n}
\right|
|z-z_0|
$$

要求：

$$
\left|
\frac{a_{n+1}}{a_n}
\right|
|z-z_0|<1
$$

所以：

$$
|z-z_0|
<
\lim_{n\to\infty}
\left|
\frac{a_n}{a_{n+1}}
\right|
$$

---

## 3.5 根值法求收敛半径

$$
\limsup_{n\to\infty}
\sqrt[n]{|a_n(z-z_0)^n|}
=
|z-z_0|
\limsup_{n\to\infty}
\sqrt[n]{|a_n|}
$$

收敛要求：

$$
|z-z_0|
\limsup_{n\to\infty}
\sqrt[n]{|a_n|}
<1
$$

所以：

$$
\boxed{
R=
\frac{1}
{\limsup\limits_{n\to\infty}\sqrt[n]{|a_n|}}
}
$$

---

## 3.6 幂级数的解析性

若

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

在

$$
|z-z_0|<R
$$

内收敛，则：

$$
\boxed{
f(z)\text{ 在收敛圆内解析}
}
$$

---

## 3.7 逐项求导

$$
\boxed{
f'(z)
=
\sum_{n=1}^{\infty}
n a_n (z-z_0)^{n-1}
}
$$

更一般地：

$$
\boxed{
f^{(k)}(z)
=
\sum_{n=k}^{\infty}
n(n-1)\cdots(n-k+1)
a_n(z-z_0)^{n-k}
}
$$

逐项求导后的收敛半径仍为：

$$
\boxed{R}
$$

---

## 3.8 逐项积分

$$
\boxed{
\int_{z_0}^{z} f(\zeta)d\zeta
=
\sum_{n=0}^{\infty}
\frac{a_n}{n+1}(z-z_0)^{n+1}
}
$$

逐项积分后的收敛半径仍为：

$$
\boxed{R}
$$

---

## 3.9 系数与导数关系

若

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

则：

$$
\boxed{
a_n=
\frac{f^{(n)}(z_0)}{n!}
}
$$

---

# 4. 常用初等函数 Taylor 展开

这些是级数题最常用的公式，必须熟练。

## 4.1 指数函数

$$
\boxed{
e^z
=
\sum_{n=0}^{\infty}
\frac{z^n}{n!}
}
$$

即：

$$
e^z
=
1+z+\frac{z^2}{2!}
+\frac{z^3}{3!}
+\cdots
$$

收敛半径：

$$
\boxed{R=+\infty}
$$

---

## 4.2 正弦函数

$$
\boxed{
\sin z
=
\sum_{n=0}^{\infty}
(-1)^n
\frac{z^{2n+1}}{(2n+1)!}
}
$$

即：

$$
\sin z
=
z-\frac{z^3}{3!}
+\frac{z^5}{5!}
-\frac{z^7}{7!}
+\cdots
$$

收敛半径：

$$
\boxed{R=+\infty}
$$

---

## 4.3 余弦函数

$$
\boxed{
\cos z
=
\sum_{n=0}^{\infty}
(-1)^n
\frac{z^{2n}}{(2n)!}
}
$$

即：

$$
\cos z
=
1-\frac{z^2}{2!}
+\frac{z^4}{4!}
-\frac{z^6}{6!}
+\cdots
$$

收敛半径：

$$
\boxed{R=+\infty}
$$

---

## 4.4 几何级数

$$
\boxed{
\frac{1}{1-z}
=
\sum_{n=0}^{\infty}z^n
}
$$

成立条件：

$$
\boxed{
|z|<1
}
$$

---

## 4.5 推广几何级数

$$
\boxed{
\frac{1}{1+z}
=
\frac{1}{1-(-z)}
=
\sum_{n=0}^{\infty}(-1)^n z^n
}
$$

成立条件：

$$
\boxed{
|z|<1
}
$$

---

## 4.6 对数函数

$$
\boxed{
\log(1+z)
=
\sum_{n=1}^{\infty}
(-1)^{n-1}
\frac{z^n}{n}
}
$$

即：

$$
\log(1+z)
=
z-\frac{z^2}{2}
+\frac{z^3}{3}
-\frac{z^4}{4}
+\cdots
$$

成立条件：

$$
\boxed{
|z|<1
}
$$

---

## 4.7 $\log(1-z)$

$$
\boxed{
\log(1-z)
=
-\sum_{n=1}^{\infty}
\frac{z^n}{n}
}
$$

即：

$$
\log(1-z)
=
-z-\frac{z^2}{2}
-\frac{z^3}{3}
-\cdots
$$

成立条件：

$$
\boxed{
|z|<1
}
$$

---

## 4.8 二项式展开

$$
\boxed{
(1+z)^\alpha
=
\sum_{n=0}^{\infty}
\binom{\alpha}{n}z^n
}
$$

其中：

$$
\boxed{
\binom{\alpha}{n}
=
\frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!}
}
$$

并且：

$$
\binom{\alpha}{0}=1
$$

成立条件：

$$
\boxed{
|z|<1
}
$$

---

## 4.9 常见特例

$$
\boxed{
\frac{1}{(1-z)^2}
=
\sum_{n=1}^{\infty}n z^{n-1}
=
\sum_{n=0}^{\infty}(n+1)z^n
}
$$

$$
\boxed{
\frac{1}{(1-z)^3}
=
\sum_{n=0}^{\infty}
\frac{(n+1)(n+2)}{2}z^n
}
$$

$$
\boxed{
\frac{1}{1-z^m}
=
\sum_{n=0}^{\infty}z^{mn}
}
$$

成立条件都是：

$$
\boxed{|z|<1}
$$

---

# 5. Taylor 级数

## 5.1 Taylor 展开定理

若 $f(z)$ 在

$$
|z-z_0|<R
$$

内解析，则：

$$
\boxed{
f(z)
=
\sum_{n=0}^{\infty}
\frac{f^{(n)}(z_0)}{n!}
(z-z_0)^n
}
$$

其中：

$$
\boxed{
a_n=
\frac{f^{(n)}(z_0)}{n!}
}
$$

---

## 5.2 Cauchy 积分公式求 Taylor 系数

$$
\boxed{
a_n
=
\frac{1}{2\pi i}
\int_C
\frac{f(\zeta)}
{(\zeta-z_0)^{n+1}}
d\zeta
}
$$

其中 $C$ 是围绕 $z_0$ 的正向简单闭曲线。

---

## 5.3 Taylor 级数唯一性

若

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
=
\sum_{n=0}^{\infty}b_n(z-z_0)^n
$$

则：

$$
\boxed{
a_n=b_n,\quad n=0,1,2,\cdots
}
$$

---

## 5.4 Taylor 收敛半径与奇点距离

Taylor 级数的收敛半径通常等于：

$$
\boxed{
z_0 \text{ 到最近奇点的距离}
}
$$

即：

$$
\boxed{
R=
\min\{|z_0-a|:a\text{ 是 }f\text{ 的奇点}\}
}
$$

---

# 6. Laurent 级数

## 6.1 Laurent 级数形式

若 $f(z)$ 在环域

$$
r<|z-z_0|<R
$$

内解析，则：

$$
\boxed{
f(z)
=
\sum_{n=-\infty}^{\infty}
a_n(z-z_0)^n
}
$$

也可拆成：

$$
\boxed{
f(z)
=
\sum_{n=0}^{\infty}a_n(z-z_0)^n
+
\sum_{n=1}^{\infty}
a_{-n}(z-z_0)^{-n}
}
$$

即：

$$
\boxed{
f(z)=\text{正则部分}+\text{主要部分}
}
$$

---

## 6.2 Laurent 系数公式

$$
\boxed{
a_n
=
\frac{1}{2\pi i}
\int_C
\frac{f(\zeta)}
{(\zeta-z_0)^{n+1}}
d\zeta
}
$$

其中 $n\in\mathbb Z$。

注意：Taylor 系数公式和 Laurent 系数公式形式一样，但 Taylor 中 $n\ge0$，Laurent 中 $n\in\mathbb Z$。

---

## 6.3 正则部分

$$
\boxed{
\sum_{n=0}^{\infty}a_n(z-z_0)^n
}
$$

称为正则部分，也叫解析部分。

---

## 6.4 主要部分

$$
\boxed{
\sum_{n=1}^{\infty}a_{-n}(z-z_0)^{-n}
}
$$

称为主要部分，也叫负幂部分。

---

## 6.5 Laurent 展开唯一性

若在同一环域中：

$$
\sum_{n=-\infty}^{\infty}a_n(z-z_0)^n
=
\sum_{n=-\infty}^{\infty}b_n(z-z_0)^n
$$

则：

$$
\boxed{
a_n=b_n,\quad n\in\mathbb Z
}
$$

---

# 7. Laurent 级数与孤立奇点

## 7.1 可去奇点

若 Laurent 展开中没有负幂项，即：

$$
\boxed{
a_{-1}=a_{-2}=a_{-3}=\cdots=0
}
$$

则 $z_0$ 是可去奇点。

等价条件：

$$
\boxed{
\lim_{z\to z_0}f(z)
\text{ 存在且有限}
}
$$

或者：

$$
\boxed{
f(z)\text{ 在 }z_0\text{ 附近有界}
}
$$

---

## 7.2 极点

若 Laurent 展开中负幂项有限，且最高负幂为：

$$
\frac{a_{-m}}{(z-z_0)^m},
\quad a_{-m}\ne0
$$

则：

$$
\boxed{
z_0\text{ 是 }m\text{ 阶极点}
}
$$

等价地：

$$
\boxed{
f(z)=
\frac{\varphi(z)}
{(z-z_0)^m}
}
$$

其中：

$$
\boxed{
\varphi(z)\text{ 在 }z_0\text{ 解析，且 }\varphi(z_0)\ne0
}
$$

还有：

$$
\boxed{
\lim_{z\to z_0}f(z)=\infty
}
$$

---

## 7.3 本性奇点

若 Laurent 展开中负幂项有无限多项，则：

$$
\boxed{
z_0\text{ 是本性奇点}
}
$$

典型例子：

$$
\boxed{
e^{1/z}
=
\sum_{n=0}^{\infty}
\frac{1}{n!z^n}
=
1+\frac{1}{z}
+\frac{1}{2!z^2}
+\cdots
}
$$

所以 $z=0$ 是 $e^{1/z}$ 的本性奇点。

---

## 7.4 留数

若

$$
f(z)=\sum_{n=-\infty}^{\infty}a_n(z-z_0)^n
$$

则：

$$
\boxed{
\operatorname{Res}(f,z_0)=a_{-1}
}
$$

也就是说：

$$
\boxed{
\text{留数就是 Laurent 展开中 }(z-z_0)^{-1}\text{ 的系数}
}
$$

---

# 8. 常见 Laurent 展开模板

Laurent 展开最核心是把函数化成几何级数：

$$
\frac{1}{1-w}
=
\sum_{n=0}^{\infty}w^n,
\quad |w|<1
$$

---

## 8.1 内部区域展开

例如：

$$
\frac{1}{z-1}
=
-\frac{1}{1-z}
$$

当

$$
|z|<1
$$

时：

$$
\boxed{
\frac{1}{z-1}
=
-\sum_{n=0}^{\infty}z^n
}
$$

即：

$$
\frac{1}{z-1}
=
-1-z-z^2-z^3-\cdots
$$

---

## 8.2 外部区域展开

$$
\frac{1}{z-1}
=
\frac{1}{z}\cdot\frac{1}{1-\frac{1}{z}}
$$

当

$$
\left|\frac{1}{z}\right|<1
$$

即

$$
|z|>1
$$

时：

$$
\boxed{
\frac{1}{z-1}
=
\sum_{n=0}^{\infty}\frac{1}{z^{n+1}}
}
$$

即：

$$
\frac{1}{z-1}
=
\frac{1}{z}
+\frac{1}{z^2}
+\frac{1}{z^3}
+\cdots
$$

---

## 8.3 以 $z_0$ 为中心展开

令：

$$
\boxed{
w=z-z_0
}
$$

然后把函数写成关于 $w$ 的形式，再用：

$$
\boxed{
\frac{1}{1-w}
=
\sum_{n=0}^{\infty}w^n
}
$$

或者：

$$
\boxed{
\frac{1}{1-\frac{a}{w}}
=
\sum_{n=0}^{\infty}
\left(\frac{a}{w}\right)^n
}
$$

---

# 9. 常见展开套路

## 9.1 遇到 $\frac{1}{z-a}$

若以 $z_0$ 为中心展开，令：

$$
w=z-z_0
$$

则：

$$
z-a
=
(z-z_0)+(z_0-a)
=
w+(z_0-a)
$$

然后根据题目给的区域判断用哪种几何级数。

---

## 9.2 遇到 $\frac{1}{1-z}$

直接用：

$$
\boxed{
\frac{1}{1-z}
=
\sum_{n=0}^{\infty}z^n,
\quad |z|<1
}
$$

---

## 9.3 遇到 $\frac{1}{z-a}$ 且区域在外部

通常化成：

$$
\frac{1}{z-a}
=
\frac{1}{z}\cdot
\frac{1}{1-\frac{a}{z}}
$$

于是：

$$
\boxed{
\frac{1}{z-a}
=
\sum_{n=0}^{\infty}
\frac{a^n}{z^{n+1}},
\quad |z|>|a|
}
$$

---

## 9.4 遇到 $\frac{1}{z-a}$ 且区域在内部

$$
\frac{1}{z-a}
=
-\frac{1}{a}
\cdot
\frac{1}{1-\frac{z}{a}}
$$

所以：

$$
\boxed{
\frac{1}{z-a}
=
-\sum_{n=0}^{\infty}
\frac{z^n}{a^{n+1}},
\quad |z|<|a|
}
$$

---

# 10. 级数题常用结论汇总

## 10.1 判断收敛半径

对于：

$$
\sum a_n(z-z_0)^n
$$

优先用：

$$
\boxed{
R=
\lim_{n\to\infty}
\left|
\frac{a_n}{a_{n+1}}
\right|
}
$$

若比值不好算，用：

$$
\boxed{
R=
\frac{1}
{\limsup\limits_{n\to\infty}\sqrt[n]{|a_n|}}
}
$$

---

## 10.2 判断边界点

先求：

$$
|z-z_0|=R
$$

然后把边界点代入原级数：

$$
\sum a_n(z-z_0)^n
$$

变成普通复数项级数，逐点判断。

---

## 10.3 Taylor 展开题

步骤：

$$
\boxed{
\text{找中心}
\rightarrow
\text{化成标准公式}
\rightarrow
\text{确定收敛半径}
}
$$

常用标准公式：

$$
\boxed{
e^z,\sin z,\cos z,\frac{1}{1-z},\log(1+z),(1+z)^\alpha
}
$$

---

## 10.4 Laurent 展开题

步骤：

$$
\boxed{
\text{找展开中心}
\rightarrow
\text{令 }w=z-z_0
\rightarrow
\text{化成几何级数}
\rightarrow
\text{根据环域选展开形式}
}
$$

---

## 10.5 奇点判断

看 Laurent 展开负幂部分：

$$
\boxed{
\text{无负幂项}
\Rightarrow
\text{可去奇点}
}
$$

$$
\boxed{
\text{有限多个负幂项}
\Rightarrow
\text{极点}
}
$$

$$
\boxed{
\text{无限多个负幂项}
\Rightarrow
\text{本性奇点}
}
$$

---

# 11. 期末最该背的核心公式

按重要程度排序：

$$
\boxed{
\frac{1}{1-z}
=
\sum_{n=0}^{\infty}z^n,
\quad |z|<1
}
$$

$$
\boxed{
e^z=
\sum_{n=0}^{\infty}\frac{z^n}{n!}
}
$$

$$
\boxed{
\sin z=
\sum_{n=0}^{\infty}
(-1)^n\frac{z^{2n+1}}{(2n+1)!}
}
$$

$$
\boxed{
\cos z=
\sum_{n=0}^{\infty}
(-1)^n\frac{z^{2n}}{(2n)!}
}
$$

$$
\boxed{
\log(1+z)=
\sum_{n=1}^{\infty}
(-1)^{n-1}\frac{z^n}{n},
\quad |z|<1
}
$$

$$
\boxed{
(1+z)^\alpha
=
\sum_{n=0}^{\infty}
\binom{\alpha}{n}z^n,
\quad |z|<1
}
$$

$$
\boxed{
R=
\lim_{n\to\infty}
\left|
\frac{a_n}{a_{n+1}}
\right|
}
$$

$$
\boxed{
\frac{1}{R}
=
\limsup_{n\to\infty}
\sqrt[n]{|a_n|}
}
$$

$$
\boxed{
f(z)
=
\sum_{n=0}^{\infty}
\frac{f^{(n)}(z_0)}{n!}
(z-z_0)^n
}
$$

$$
\boxed{
f(z)
=
\sum_{n=-\infty}^{\infty}
a_n(z-z_0)^n
}
$$

$$
\boxed{
a_n=
\frac{1}{2\pi i}
\int_C
\frac{f(\zeta)}
{(\zeta-z_0)^{n+1}}
d\zeta
}
$$

$$
\boxed{
\operatorname{Res}(f,z_0)=a_{-1}
}
$$

---

# 12. 最常考的三类题模板

## 12.1 求收敛半径

题型：

$$
\sum a_n(z-z_0)^n
$$

做法：

$$
\boxed{
R=
\lim_{n\to\infty}
\left|
\frac{a_n}{a_{n+1}}
\right|
}
$$

若比值法不好用：

$$
\boxed{
R=
\frac{1}
{\limsup\limits_{n\to\infty}\sqrt[n]{|a_n|}}
}
$$

然后写：

$$
\boxed{
|z-z_0|<R
}
$$

最后边界：

$$
\boxed{
|z-z_0|=R\text{ 单独讨论}
}
$$

---

## 12.2 Taylor 展开

题型：

$$
\text{把 }f(z)\text{ 在 }z_0\text{ 处展开}
$$

做法：

$$
\boxed{
w=z-z_0
}
$$

把 $f(z)$ 改写成关于 $w$ 的函数，然后套：

$$
\boxed{
\frac{1}{1-w}
=
\sum_{n=0}^{\infty}w^n
}
$$

或：

$$
\boxed{
e^w,\sin w,\cos w,\log(1+w)
}
$$

---

## 12.3 Laurent 展开

题型：

$$
\text{在环域 }r<|z-z_0|<R\text{ 内展开}
$$

做法：

$$
\boxed{
w=z-z_0
}
$$

把分母变成：

$$
\boxed{
1-w
}
$$

或：

$$
\boxed{
1-\frac{a}{w}
}
$$

然后根据：

$$
|w|<|a|
$$

或

$$
|w|>|a|
$$

选择展开方式。

关键判断：

$$
\boxed{
|w|<|a| \Rightarrow \text{正幂展开}
}
$$

$$
\boxed{
|w|>|a| \Rightarrow \text{负幂展开}
}
$$

---

# 13. 一句话记忆

$$
\boxed{
\text{幂级数看收敛半径，Taylor 看导数，Laurent 看负幂，留数看 }(z-z_0)^{-1}\text{ 的系数。}
}
$$



---
Powered by [ChatGPT Exporter](https://www.chatgptexporter.com)