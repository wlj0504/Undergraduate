# 复变函数级数总结

**User:** Anonymous  
**Created:** 7/4/2026 1:33:07  
**Updated:** 7/4/2026 1:35:33  
**Exported:** 7/4/2026 1:41:37  
**Link:** [https://chatgpt.com/c/6a47f232-d718-83e8-9209-0261dcab6a83?mweb_fallback=1](https://chatgpt.com/c/6a47f232-d718-83e8-9209-0261dcab6a83?mweb_fallback=1)  

## Response:
2026/7/4 01:33:06

我会按“题型—常用结论—典型试题—答案模板”整理，重点放在期末最常考的幂级数收敛域、Taylor 展开、逐项求导积分、级数求和和一致收敛。

# 复变函数：级数章常见试题与拓展结论总结

级数这一章期末最常考的不是“背定义”，而是下面几类：

1. **判断复数项级数收敛**
2. **求幂级数收敛半径、收敛圆、边界**
3. **判断函数项级数一致收敛**
4. **利用幂级数逐项求导、逐项积分**
5. **展开 Taylor 级数**
6. **用级数求和、求积分、求系数**
7. **由奇点判断 Taylor 级数收敛半径**
8. **级数与解析函数之间的关系**

---

# 一、核心知识框架

复变函数里的级数大致分为：

$$
\sum_{n=1}^{\infty} a_n
$$

这是**复数项级数**。

$$
\sum_{n=1}^{\infty} f_n(z)
$$

这是**函数项级数**。

$$
\sum_{n=0}^{\infty} a_n (z-z_0)^n
$$

这是**幂级数**。

$$
f(z)=\sum_{n=0}^{\infty} a_n(z-z_0)^n
$$

这是**Taylor 展开**。

这章的中心思想是：

$$
\boxed{
\text{幂级数在收敛圆内可以像多项式一样求导、积分、运算}
}
$$

---

# 二、必背结论

## 1. 复数项级数收敛

设

$$
a_n=\alpha_n+i\beta_n
$$

则

$$
\sum a_n \text{ 收敛}
$$

等价于

$$
\sum \alpha_n,\qquad \sum \beta_n
$$

都收敛。

如果

$$
\sum |a_n|
$$

收敛，则

$$
\sum a_n
$$

收敛，称为**绝对收敛**。

结论：

$$
\boxed{
\text{绝对收敛} \Rightarrow \text{收敛}
}
$$

但反过来不一定成立。

---

## 2. 幂级数收敛半径公式

对幂级数

$$
\sum_{n=0}^{\infty} a_n(z-z_0)^n
$$

收敛半径为

$$
\boxed{
R=\frac{1}{\limsup\limits_{n\to\infty}|a_n|^{1/n}}
}
$$

若极限存在，也可写成

$$
\boxed{
R=\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|
}
$$

常用判断：

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
|z-z_0|=R \Rightarrow \text{必须单独判断}
}
$$

注意：

边界不能只靠收敛半径判断。

---

## 3. 幂级数的基本性质

若

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

收敛半径为 $R$，则在

$$
|z-z_0|<R
$$

内：

### 可以逐项求导

$$
\boxed{
f'(z)=\sum_{n=1}^{\infty} n a_n(z-z_0)^{n-1}
}
$$

### 可以逐项积分

$$
\boxed{
\int f(z)\,dz
=
C+\sum_{n=0}^{\infty}\frac{a_n}{n+1}(z-z_0)^{n+1}
}
$$

### 求导和积分后收敛半径不变

$$
\boxed{
\text{求导、积分不改变幂级数收敛半径}
}
$$

---

## 4. Taylor 系数公式

若 $f$ 在 $z_0$ 的邻域解析，则

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

其中

$$
\boxed{
a_n=\frac{f^{(n)}(z_0)}{n!}
}
$$

也可以写成

$$
\boxed{
a_n=\frac{1}{2\pi i}
\int_C\frac{f(\zeta)}{(\zeta-z_0)^{n+1}}\,d\zeta
}
$$

其中 $C$ 是包围 $z_0$ 的正向简单闭曲线。

所以：

$$
\boxed{
\frac{f^{(n)}(z_0)}{n!}
=
\frac{1}{2\pi i}
\int_C\frac{f(\zeta)}{(\zeta-z_0)^{n+1}}\,d\zeta
}
$$

这是 Taylor 系数公式和 Cauchy 积分公式之间的联系。

---

## 5. 常用 Taylor 展开

### 几何级数

$$
\boxed{
\frac{1}{1-z}=\sum_{n=0}^{\infty}z^n,\qquad |z|<1
}
$$

推广：

$$
\boxed{
\frac{1}{1+z}=\sum_{n=0}^{\infty}(-1)^n z^n,\qquad |z|<1
}
$$

---

### 指数函数

$$
\boxed{
e^z=\sum_{n=0}^{\infty}\frac{z^n}{n!},\qquad R=+\infty
}
$$

---

### 三角函数

$$
\boxed{
\sin z=\sum_{n=0}^{\infty}(-1)^n\frac{z^{2n+1}}{(2n+1)!}
}
$$

$$
\boxed{
\cos z=\sum_{n=0}^{\infty}(-1)^n\frac{z^{2n}}{(2n)!}
}
$$

二者收敛半径都是

$$
R=+\infty
$$

---

### 对数函数

$$
\boxed{
\log(1+z)=\sum_{n=1}^{\infty}(-1)^{n-1}\frac{z^n}{n},
\qquad |z|<1
}
$$

$$
\boxed{
-\log(1-z)=\sum_{n=1}^{\infty}\frac{z^n}{n},
\qquad |z|<1
}
$$

---

### 二项式展开

$$
\boxed{
(1+z)^\alpha
=
\sum_{n=0}^{\infty}
\binom{\alpha}{n}z^n,
\qquad |z|<1
}
$$

其中

$$
\binom{\alpha}{n}
=
\frac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!}
$$

---

# 三、常见题型一：求幂级数收敛半径和收敛域

## 题 1

求

$$
\sum_{n=1}^{\infty} n^2 z^n
$$

的收敛半径和收敛域。

### 解

这里

$$
a_n=n^2
$$

用根值法：

$$
\lim_{n\to\infty}|a_n|^{1/n}
=
\lim_{n\to\infty}(n^2)^{1/n}=1
$$

所以

$$
R=\frac{1}{1}=1
$$

当

$$
|z|<1
$$

时收敛。

当

$$
|z|>1
$$

时发散。

边界：

$$
|z|=1
$$

此时通项

$$
n^2z^n
$$

的模长为

$$
|n^2z^n|=n^2
$$

不趋于 $0$，所以发散。

答案：

$$
\boxed{
R=1,\qquad \text{收敛域为 } |z|<1
}
$$

---

## 题 2

求

$$
\sum_{n=1}^{\infty}\frac{z^n}{n}
$$

的收敛域。

### 解

这里

$$
a_n=\frac{1}{n}
$$

根值法：

$$
\lim_{n\to\infty}\left|\frac{1}{n}\right|^{1/n}=1
$$

所以

$$
R=1
$$

当

$$
|z|<1
$$

绝对收敛。

当

$$
|z|>1
$$

发散。

边界：

$$
|z|=1
$$

需要单独讨论。

若 $z=1$，则

$$
\sum_{n=1}^{\infty}\frac{1}{n}
$$

发散。

若 $z\neq 1$，且 $|z|=1$，则

$$
\sum_{n=1}^{\infty}\frac{z^n}{n}
$$

由 Dirichlet 判别法收敛。

但不绝对收敛，因为

$$
\sum_{n=1}^{\infty}\left|\frac{z^n}{n}\right|
=
\sum_{n=1}^{\infty}\frac{1}{n}
$$

发散。

所以答案为：

$$
\boxed{
|z|<1 \text{ 收敛，且 } |z|=1,z\neq 1 \text{ 条件收敛}
}
$$

即

$$
\boxed{
\text{收敛域为 } \{z:|z|<1\}\cup\{z:|z|=1,z\neq 1\}
}
$$

---

## 题 3

求

$$
\sum_{n=1}^{\infty}\frac{(z-2)^n}{n^2}
$$

的收敛域。

### 解

这是以

$$
z_0=2
$$

为中心的幂级数。

系数：

$$
a_n=\frac{1}{n^2}
$$

根值法：

$$
\lim_{n\to\infty}|a_n|^{1/n}
=
\lim_{n\to\infty}\left(\frac{1}{n^2}\right)^{1/n}=1
$$

所以

$$
R=1
$$

当

$$
|z-2|<1
$$

绝对收敛。

当

$$
|z-2|>1
$$

发散。

边界：

$$
|z-2|=1
$$

此时

$$
\left|\frac{(z-2)^n}{n^2}\right|
=
\frac{1}{n^2}
$$

而

$$
\sum_{n=1}^{\infty}\frac{1}{n^2}
$$

收敛，所以边界上绝对收敛。

答案：

$$
\boxed{
R=1,\qquad \text{收敛域为 } |z-2|\le 1
}
$$

---

## 题 4

求

$$
\sum_{n=1}^{\infty} n! z^n
$$

的收敛半径。

### 解

$$
a_n=n!
$$

根值法：

$$
\lim_{n\to\infty}(n!)^{1/n}=+\infty
$$

所以

$$
R=\frac{1}{+\infty}=0
$$

答案：

$$
\boxed{
R=0
}
$$

这个级数只在

$$
z=0
$$

处收敛。

---

## 题 5

求

$$
\sum_{n=0}^{\infty}\frac{z^n}{n!}
$$

的收敛半径。

### 解

$$
a_n=\frac{1}{n!}
$$

根值法：

$$
\lim_{n\to\infty}|a_n|^{1/n}
=
\lim_{n\to\infty}\frac{1}{(n!)^{1/n}}=0
$$

所以

$$
R=\frac{1}{0}=+\infty
$$

答案：

$$
\boxed{
R=+\infty
}
$$

实际上

$$
\boxed{
\sum_{n=0}^{\infty}\frac{z^n}{n!}=e^z
}
$$

---

## 题 6

求

$$
\sum_{n=1}^{\infty}\frac{n^n}{n!}z^n
$$

的收敛半径。

### 解

$$
a_n=\frac{n^n}{n!}
$$

用 Stirling 公式：

$$
n!\sim \sqrt{2\pi n}\left(\frac{n}{e}\right)^n
$$

所以

$$
\frac{n^n}{n!}
\sim
\frac{n^n}{\sqrt{2\pi n}\left(\frac{n}{e}\right)^n}
=
\frac{e^n}{\sqrt{2\pi n}}
$$

因此

$$
|a_n|^{1/n}\to e
$$

所以

$$
R=\frac{1}{e}
$$

答案：

$$
\boxed{
R=\frac{1}{e}
}
$$

---

## 题 7

求

$$
\sum_{n=1}^{\infty}\left(\frac{z-1}{z+1}\right)^n
$$

的收敛域。

### 解

这是几何级数。

令

$$
w=\frac{z-1}{z+1}
$$

则级数为

$$
\sum_{n=1}^{\infty}w^n
$$

几何级数收敛条件为

$$
|w|<1
$$

所以

$$
\left|\frac{z-1}{z+1}\right|<1
$$

即

$$
|z-1|<|z+1|
$$

设

$$
z=x+iy
$$

则

$$
|z-1|^2=(x-1)^2+y^2
$$

$$
|z+1|^2=(x+1)^2+y^2
$$

所以

$$
(x-1)^2+y^2<(x+1)^2+y^2
$$

化简：

$$
x^2-2x+1<x^2+2x+1
$$

$$
-2x<2x
$$

$$
x>0
$$

答案：

$$
\boxed{
\operatorname{Re}z>0
}
$$

注意还要排除 $z=-1$，但 $z=-1$ 本来也不满足 $\operatorname{Re}z>0$。

---

# 四、常见题型二：一致收敛

## 必背判别法：Weierstrass 判别法

如果在区域 $D$ 上有

$$
|f_n(z)|\le M_n
$$

且

$$
\sum_{n=1}^{\infty}M_n
$$

收敛，则

$$
\sum_{n=1}^{\infty}f_n(z)
$$

在 $D$ 上一致收敛。

即：

$$
\boxed{
|f_n(z)|\le M_n,\quad \sum M_n \text{ 收敛}
\Rightarrow
\sum f_n(z) \text{ 一致收敛}
}
$$

---

## 题 8

证明

$$
\sum_{n=1}^{\infty}\frac{z^n}{n^2}
$$

在

$$
|z|\le 1
$$

上一致收敛。

### 解

当

$$
|z|\le 1
$$

时，

$$
\left|\frac{z^n}{n^2}\right|
\le
\frac{1}{n^2}
$$

而

$$
\sum_{n=1}^{\infty}\frac{1}{n^2}
$$

收敛。

由 Weierstrass 判别法可知：

$$
\boxed{
\sum_{n=1}^{\infty}\frac{z^n}{n^2}
\text{ 在 } |z|\le 1 \text{ 上一致收敛}
}
$$

---

## 题 9

证明

$$
\sum_{n=0}^{\infty} z^n
$$

在

$$
|z|\le r<1
$$

上一致收敛，但在

$$
|z|<1
$$

上不一致收敛。

### 解

在

$$
|z|\le r<1
$$

上，

$$
|z^n|\le r^n
$$

而

$$
\sum_{n=0}^{\infty}r^n
$$

收敛。

所以由 Weierstrass 判别法：

$$
\boxed{
\sum z^n \text{ 在 } |z|\le r<1 \text{ 上一致收敛}
}
$$

但是在整个单位圆盘

$$
|z|<1
$$

上不一致收敛。

因为

$$
\sum_{n=0}^{\infty}z^n=\frac{1}{1-z}
$$

部分和为

$$
S_N(z)=\frac{1-z^{N+1}}{1-z}
$$

余项为

$$
R_N(z)=\frac{z^{N+1}}{1-z}
$$

当 $z$ 趋近于 $1$ 时，余项不能一致趋于 $0$。

所以：

$$
\boxed{
\sum z^n \text{ 在 } |z|<1 \text{ 上不一致收敛}
}
$$

重要结论：

$$
\boxed{
幂级数在收敛圆内部的任意闭圆盘 |z-z_0|\le r<R 上一致收敛，
但不一定在整个收敛圆内一致收敛。
}
$$

---

# 五、常见题型三：逐项求导与逐项积分

## 题 10

设

$$
f(z)=\sum_{n=1}^{\infty}\frac{z^n}{n}
$$

求 $f'(z)$，并求 $f(z)$。

### 解

已知收敛半径为

$$
R=1
$$

所以在

$$
|z|<1
$$

内可以逐项求导。

$$
f'(z)
=
\sum_{n=1}^{\infty}z^{n-1}
$$

这是几何级数：

$$
\sum_{n=1}^{\infty}z^{n-1}
=
\sum_{k=0}^{\infty}z^k
=
\frac{1}{1-z}
$$

所以

$$
f'(z)=\frac{1}{1-z}
$$

积分得

$$
f(z)=-\log(1-z)+C
$$

又因为

$$
f(0)=0
$$

所以

$$
C=0
$$

答案：

$$
\boxed{
\sum_{n=1}^{\infty}\frac{z^n}{n}
=
-\log(1-z),\qquad |z|<1
}
$$

---

## 题 11

求

$$
\sum_{n=1}^{\infty}n z^{n}
$$

的和函数。

### 解

从几何级数出发：

$$
\sum_{n=0}^{\infty}z^n=\frac{1}{1-z},\qquad |z|<1
$$

两边求导：

$$
\sum_{n=1}^{\infty}n z^{n-1}
=
\frac{1}{(1-z)^2}
$$

两边乘以 $z$：

$$
\sum_{n=1}^{\infty}n z^n
=
\frac{z}{(1-z)^2}
$$

答案：

$$
\boxed{
\sum_{n=1}^{\infty}n z^n
=
\frac{z}{(1-z)^2},
\qquad |z|<1
}
$$

---

## 题 12

求

$$
\sum_{n=1}^{\infty}n^2 z^n
$$

的和函数。

### 解

已知

$$
\sum_{n=1}^{\infty}n z^n=\frac{z}{(1-z)^2}
$$

两边对 $z$ 求导：

$$
\sum_{n=1}^{\infty}n^2z^{n-1}
=
\frac{1+z}{(1-z)^3}
$$

两边乘以 $z$：

$$
\sum_{n=1}^{\infty}n^2 z^n
=
\frac{z(1+z)}{(1-z)^3}
$$

答案：

$$
\boxed{
\sum_{n=1}^{\infty}n^2 z^n
=
\frac{z(1+z)}{(1-z)^3},
\qquad |z|<1
}
$$

---

# 六、常见题型四：Taylor 展开

## 题 13

将

$$
\frac{1}{1-z}
$$

在 $z=0$ 展开成 Taylor 级数。

### 解

直接使用几何级数：

$$
\boxed{
\frac{1}{1-z}
=
\sum_{n=0}^{\infty}z^n,
\qquad |z|<1
}
$$

---

## 题 14

将

$$
\frac{1}{2-z}
$$

在 $z=0$ 展开。

### 解

先变形：

$$
\frac{1}{2-z}
=
\frac{1}{2}\cdot \frac{1}{1-\frac{z}{2}}
$$

用几何级数：

$$
\frac{1}{1-w}
=
\sum_{n=0}^{\infty}w^n
$$

令

$$
w=\frac{z}{2}
$$

得到

$$
\frac{1}{2-z}
=
\frac{1}{2}
\sum_{n=0}^{\infty}
\left(\frac{z}{2}\right)^n
$$

所以

$$
\boxed{
\frac{1}{2-z}
=
\sum_{n=0}^{\infty}
\frac{z^n}{2^{n+1}},
\qquad |z|<2
}
$$

---

## 题 15

将

$$
\frac{1}{z+2}
$$

在 $z=0$ 展开。

### 解

$$
\frac{1}{z+2}
=
\frac{1}{2}\cdot \frac{1}{1+\frac{z}{2}}
$$

而

$$
\frac{1}{1+w}
=
\sum_{n=0}^{\infty}(-1)^n w^n,\qquad |w|<1
$$

令

$$
w=\frac{z}{2}
$$

得到

$$
\frac{1}{z+2}
=
\frac{1}{2}
\sum_{n=0}^{\infty}
(-1)^n\left(\frac{z}{2}\right)^n
$$

所以

$$
\boxed{
\frac{1}{z+2}
=
\sum_{n=0}^{\infty}
\frac{(-1)^n z^n}{2^{n+1}},
\qquad |z|<2
}
$$

---

## 题 16

将

$$
\frac{1}{z-1}
$$

在 $z=0$ 展开。

### 解

$$
\frac{1}{z-1}
=
-\frac{1}{1-z}
$$

所以

$$
\frac{1}{z-1}
=
-\sum_{n=0}^{\infty}z^n
$$

答案：

$$
\boxed{
\frac{1}{z-1}
=
-\sum_{n=0}^{\infty}z^n,
\qquad |z|<1
}
$$

---

## 题 17

将

$$
\frac{1}{z-a}
$$

在 $z=0$ 展开，其中 $a\neq 0$。

### 解

$$
\frac{1}{z-a}
=
-\frac{1}{a}\cdot \frac{1}{1-\frac{z}{a}}
$$

所以

$$
\boxed{
\frac{1}{z-a}
=
-\sum_{n=0}^{\infty}\frac{z^n}{a^{n+1}},
\qquad |z|<|a|
}
$$

这个公式很常用。

---

## 题 18

将

$$
\frac{1}{z^2-1}
$$

在 $z=0$ 展开。

### 解

先部分分式分解：

$$
\frac{1}{z^2-1}
=
\frac{1}{(z-1)(z+1)}
$$

设

$$
\frac{1}{z^2-1}
=
\frac{A}{z-1}+\frac{B}{z+1}
$$

解得

$$
A=\frac12,\qquad B=-\frac12
$$

所以

$$
\frac{1}{z^2-1}
=
\frac{1}{2}\cdot\frac{1}{z-1}
-
\frac{1}{2}\cdot\frac{1}{z+1}
$$

利用前面的展开：

$$
\frac{1}{z-1}
=
-\sum_{n=0}^{\infty}z^n
$$

$$
\frac{1}{z+1}
=
\frac{1}{1+z}
=
\sum_{n=0}^{\infty}(-1)^nz^n
$$

于是

$$
\frac{1}{z^2-1}
=
-\frac12\sum_{n=0}^{\infty}z^n
-
\frac12\sum_{n=0}^{\infty}(-1)^nz^n
$$

也可以直接写：

$$
\frac{1}{z^2-1}
=
-\frac{1}{1-z^2}
=
-\sum_{n=0}^{\infty}z^{2n}
$$

所以答案：

$$
\boxed{
\frac{1}{z^2-1}
=
-\sum_{n=0}^{\infty}z^{2n},
\qquad |z|<1
}
$$

---

# 七、常见题型五：由奇点判断 Taylor 收敛半径

这是考试非常喜欢的题型。

## 核心结论

如果 $f$ 在 $z_0$ 附近解析，那么它在 $z_0$ 的 Taylor 级数的收敛半径等于：

$$
\boxed{
z_0 \text{ 到最近奇点的距离}
}
$$

也就是说：

$$
\boxed{
R=\min\{|z_0-a|:a \text{ 是 } f \text{ 的奇点}\}
}
$$

---

## 题 19

求

$$
f(z)=\frac{1}{1+z^2}
$$

在 $z=0$ 的 Taylor 级数收敛半径。

### 解

奇点由

$$
1+z^2=0
$$

得到：

$$
z=\pm i
$$

它们到 $0$ 的距离为

$$
|i-0|=1,\qquad |-i-0|=1
$$

所以最近奇点距离为 $1$。

答案：

$$
\boxed{
R=1
}
$$

并且

$$
\frac{1}{1+z^2}
=
\sum_{n=0}^{\infty}(-1)^n z^{2n},
\qquad |z|<1
$$

---

## 题 20

求

$$
f(z)=\frac{1}{z^2+4}
$$

在 $z=1$ 处 Taylor 展开的收敛半径。

### 解

奇点由

$$
z^2+4=0
$$

得到

$$
z=\pm 2i
$$

中心为

$$
z_0=1
$$

计算距离：

$$
|1-2i|=\sqrt{1^2+(-2)^2}=\sqrt5
$$

$$
|1+2i|=\sqrt{1^2+2^2}=\sqrt5
$$

所以

$$
R=\sqrt5
$$

答案：

$$
\boxed{
R=\sqrt5
}
$$

---

## 题 21

求

$$
f(z)=\frac{1}{(z-2)(z+3)}
$$

在 $z=0$ 处 Taylor 展开的收敛半径。

### 解

奇点为

$$
z=2,\qquad z=-3
$$

它们到 $0$ 的距离：

$$
|2|=2,\qquad |-3|=3
$$

最近的是 $z=2$。

所以

$$
\boxed{
R=2
}
$$

---

## 题 22

求

$$
f(z)=\frac{1}{z^2-2z+2}
$$

在 $z=0$ 处 Taylor 级数的收敛半径。

### 解

先求奇点：

$$
z^2-2z+2=0
$$

$$
z=1\pm i
$$

到 $0$ 的距离：

$$
|1+i|=\sqrt2
$$

$$
|1-i|=\sqrt2
$$

所以

$$
\boxed{
R=\sqrt2
}
$$

---

# 八、常见题型六：求 Taylor 系数

## 题 23

设

$$
f(z)=\frac{1}{1-z}
$$

求它在 $z=0$ 处 Taylor 展开中的 $z^n$ 的系数。

### 解

已知

$$
\frac{1}{1-z}
=
\sum_{n=0}^{\infty}z^n
$$

所以每一项系数都是 $1$。

答案：

$$
\boxed{
a_n=1
}
$$

---

## 题 24

求

$$
\frac{1}{(1-z)^2}
$$

在 $z=0$ 处的 Taylor 系数。

### 解

由

$$
\frac{1}{1-z}
=
\sum_{n=0}^{\infty}z^n
$$

两边求导：

$$
\frac{1}{(1-z)^2}
=
\sum_{n=1}^{\infty}n z^{n-1}
$$

令 $m=n-1$，则

$$
n=m+1
$$

所以

$$
\frac{1}{(1-z)^2}
=
\sum_{m=0}^{\infty}(m+1)z^m
$$

写成 $n$：

$$
\boxed{
\frac{1}{(1-z)^2}
=
\sum_{n=0}^{\infty}(n+1)z^n,
\qquad |z|<1
}
$$

所以系数为

$$
\boxed{
a_n=n+1
}
$$

---

## 题 25

求

$$
\frac{1}{(1-z)^3}
$$

在 $z=0$ 处的 Taylor 系数。

### 解

已知

$$
\frac{1}{(1-z)^2}
=
\sum_{n=0}^{\infty}(n+1)z^n
$$

两边求导：

$$
\frac{2}{(1-z)^3}
=
\sum_{n=1}^{\infty}n(n+1)z^{n-1}
$$

令 $m=n-1$，得

$$
\frac{2}{(1-z)^3}
=
\sum_{m=0}^{\infty}(m+1)(m+2)z^m
$$

所以

$$
\frac{1}{(1-z)^3}
=
\sum_{m=0}^{\infty}\frac{(m+1)(m+2)}{2}z^m
$$

答案：

$$
\boxed{
\frac{1}{(1-z)^3}
=
\sum_{n=0}^{\infty}
\frac{(n+1)(n+2)}{2}z^n
}
$$

即

$$
\boxed{
a_n=\frac{(n+1)(n+2)}{2}
}
$$

---

# 九、常见题型七：用级数计算积分

## 核心结论

如果

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
$$

在闭曲线 $C$ 内解析，则

$$
\int_C f(z)\,dz=0
$$

但如果 integrand 里有

$$
\frac{1}{z-z_0}
$$

这一类项，就要找系数。

尤其：

$$
\boxed{
\int_C \frac{f(z)}{z-z_0}\,dz
=
2\pi i f(z_0)
}
$$

这和 Taylor 级数联系为：

$$
f(z)=a_0+a_1(z-z_0)+a_2(z-z_0)^2+\cdots
$$

则

$$
\frac{f(z)}{z-z_0}
=
\frac{a_0}{z-z_0}+a_1+a_2(z-z_0)+\cdots
$$

闭路积分只有

$$
\frac{a_0}{z-z_0}
$$

有贡献。

所以：

$$
\boxed{
\int_C \frac{f(z)}{z-z_0}\,dz=2\pi i a_0=2\pi i f(z_0)
}
$$

---

## 题 26

设 $C:|z|=2$，正向，求

$$
\int_C \frac{e^z}{z}\,dz
$$

### 解

利用

$$
e^z=\sum_{n=0}^{\infty}\frac{z^n}{n!}
$$

所以

$$
\frac{e^z}{z}
=
\frac{1}{z}
+
1+\frac{z}{2!}+\frac{z^2}{3!}+\cdots
$$

闭路积分中只有

$$
\frac{1}{z}
$$

项有贡献：

$$
\int_C \frac{1}{z}\,dz=2\pi i
$$

所以

$$
\boxed{
\int_C \frac{e^z}{z}\,dz=2\pi i
}
$$

---

## 题 27

设 $C:|z|=1$，正向，求

$$
\int_C \frac{\sin z}{z^3}\,dz
$$

### 解

展开：

$$
\sin z
=
z-\frac{z^3}{3!}+\frac{z^5}{5!}-\cdots
$$

所以

$$
\frac{\sin z}{z^3}
=
\frac{1}{z^2}
-\frac{1}{3!}
+\frac{z^2}{5!}
-\cdots
$$

这里没有

$$
\frac{1}{z}
$$

项。

所以积分为

$$
\boxed{
0
}
$$

也可以用 Cauchy 公式：

$$
\int_C \frac{f(z)}{z^{n+1}}\,dz
=
\frac{2\pi i}{n!}f^{(n)}(0)
$$

这里

$$
\frac{\sin z}{z^3}
=
\frac{f(z)}{z^{2+1}}
$$

所以 $n=2$，$f(z)=\sin z$。

$$
f''(z)=-\sin z
$$

$$
f''(0)=0
$$

故积分为

$$
0
$$

---

## 题 28

设 $C:|z|=1$，正向，求

$$
\int_C \frac{e^z-1-z}{z^3}\,dz
$$

### 解

展开：

$$
e^z
=
1+z+\frac{z^2}{2!}+\frac{z^3}{3!}+\cdots
$$

所以

$$
e^z-1-z
=
\frac{z^2}{2!}+\frac{z^3}{3!}+\cdots
$$

因此

$$
\frac{e^z-1-z}{z^3}
=
\frac{1}{2!}\frac{1}{z}
+
\frac{1}{3!}
+
\cdots
$$

所以 $\frac{1}{z}$ 项系数为

$$
\frac{1}{2}
$$

因此

$$
\boxed{
\int_C \frac{e^z-1-z}{z^3}\,dz
=
2\pi i\cdot \frac12
=
\pi i
}
$$

---

# 十、常见题型八：级数求特殊函数值

## 题 29

求

$$
\sum_{n=0}^{\infty}\frac{1}{n!}
$$

### 解

由

$$
e^z=\sum_{n=0}^{\infty}\frac{z^n}{n!}
$$

取

$$
z=1
$$

得到

$$
\boxed{
\sum_{n=0}^{\infty}\frac{1}{n!}=e
}
$$

---

## 题 30

求

$$
\sum_{n=0}^{\infty}(-1)^n\frac{1}{(2n)!}
$$

### 解

由

$$
\cos z
=
\sum_{n=0}^{\infty}(-1)^n\frac{z^{2n}}{(2n)!}
$$

取

$$
z=1
$$

得到

$$
\boxed{
\sum_{n=0}^{\infty}(-1)^n\frac{1}{(2n)!}
=
\cos 1
}
$$

---

## 题 31

求

$$
\sum_{n=0}^{\infty}(-1)^n\frac{1}{2n+1}
$$

### 解

由

$$
\arctan z
=
\sum_{n=0}^{\infty}(-1)^n\frac{z^{2n+1}}{2n+1},
\qquad |z|\le 1
$$

在 $z=1$ 处有

$$
\arctan 1=\frac{\pi}{4}
$$

所以

$$
\boxed{
\sum_{n=0}^{\infty}(-1)^n\frac{1}{2n+1}
=
\frac{\pi}{4}
}
$$

---

# 十一、常见题型九：证明函数解析

## 题 32

证明

$$
f(z)=\sum_{n=1}^{\infty}\frac{z^n}{n^2}
$$

在

$$
|z|<1
$$

内解析，并求 $f'(z)$。

### 解

这是幂级数。

收敛半径：

$$
R=1
$$

幂级数在收敛圆内解析，所以

$$
f(z)
$$

在

$$
|z|<1
$$

内解析。

并且可以逐项求导：

$$
f'(z)
=
\sum_{n=1}^{\infty}\frac{n z^{n-1}}{n^2}
=
\sum_{n=1}^{\infty}\frac{z^{n-1}}{n}
$$

答案：

$$
\boxed{
f'(z)=\sum_{n=1}^{\infty}\frac{z^{n-1}}{n},
\qquad |z|<1
}
$$

进一步地：

$$
f'(z)
=
\frac{1}{z}\sum_{n=1}^{\infty}\frac{z^n}{n}
=
-\frac{\log(1-z)}{z}
$$

所以

$$
\boxed{
f'(z)=-\frac{\log(1-z)}{z}
}
$$

其中 $z=0$ 处按极限定义补充，$f'(0)=1$。

---

# 十二、常见题型十：判断边界收敛

边界收敛最容易出错。

## 常见边界模板

### 模板 1

$$
\sum z^n
$$

收敛半径：

$$
R=1
$$

边界：

$$
|z|=1
$$

此时

$$
z^n
$$

一般不趋于 $0$，所以发散。

答案：

$$
\boxed{
\sum z^n \text{ 仅在 } |z|<1 \text{ 收敛}
}
$$

---

### 模板 2

$$
\sum \frac{z^n}{n}
$$

边界：

$$
|z|=1
$$

- $z=1$：发散；
- $|z|=1,z\neq 1$：条件收敛；
- 不绝对收敛。

答案：

$$
\boxed{
|z|<1 \text{ 绝对收敛； } |z|=1,z\neq1 \text{ 条件收敛}
}
$$

---

### 模板 3

$$
\sum \frac{z^n}{n^p}
$$

当 $p>1$ 时：

边界

$$
|z|=1
$$

有

$$
\left|\frac{z^n}{n^p}\right|=\frac{1}{n^p}
$$

所以绝对收敛。

答案：

$$
\boxed{
p>1 \Rightarrow |z|\le1 \text{ 绝对收敛}
}
$$

---

### 模板 4

$$
\sum n^p z^n
$$

边界

$$
|z|=1
$$

通项模长为

$$
|n^p z^n|=n^p
$$

不趋于 $0$，所以发散。

答案：

$$
\boxed{
\sum n^p z^n \text{ 收敛域为 } |z|<1
}
$$

---

# 十三、拓展性结论总结

## 结论 1：幂级数在收敛圆内局部一致收敛

若

$$
\sum a_n(z-z_0)^n
$$

收敛半径为 $R$，则对任意

$$
0<r<R
$$

都有

$$
\sum a_n(z-z_0)^n
$$

在

$$
|z-z_0|\le r
$$

上一致收敛。

即：

$$
\boxed{
幂级数在收敛圆内部紧集上一致收敛
}
$$

---

## 结论 2：幂级数在收敛圆内表示解析函数

$$
\boxed{
幂级数在其收敛圆内一定解析
}
$$

并且可以任意次求导。

---

## 结论 3：解析函数局部一定可以展开成 Taylor 级数

如果 $f$ 在 $z_0$ 的某个邻域内解析，则

$$
\boxed{
f(z)=\sum_{n=0}^{\infty}\frac{f^{(n)}(z_0)}{n!}(z-z_0)^n
}
$$

---

## 结论 4：Taylor 展开唯一

如果

$$
f(z)=\sum_{n=0}^{\infty}a_n(z-z_0)^n
=
\sum_{n=0}^{\infty}b_n(z-z_0)^n
$$

则

$$
\boxed{
a_n=b_n,\qquad n=0,1,2,\dots
}
$$

所以 Taylor 系数是唯一的。

---

## 结论 5：收敛半径等于最近奇点距离

如果 $f$ 在 $z_0$ 附近解析，则 Taylor 级数的收敛半径由最近奇点决定：

$$
\boxed{
R=\text{中心 }z_0\text{ 到最近奇点的距离}
}
$$

这是求收敛半径的高频技巧。

---

## 结论 6：求导、积分不改变收敛半径

若

$$
\sum a_n(z-z_0)^n
$$

收敛半径为 $R$，则

$$
\sum n a_n(z-z_0)^{n-1}
$$

和

$$
\sum \frac{a_n}{n+1}(z-z_0)^{n+1}
$$

收敛半径仍然是

$$
\boxed{R}
$$

---

## 结论 7：一致收敛可以交换极限和积分

如果

$$
\sum f_n(z)
$$

在曲线 $C$ 上一致收敛，则

$$
\boxed{
\int_C \sum_{n=1}^{\infty}f_n(z)\,dz
=
\sum_{n=1}^{\infty}\int_C f_n(z)\,dz
}
$$

---

## 结论 8：解析函数项级数局部一致收敛，则和函数解析

如果每个 $f_n(z)$ 在区域 $D$ 内解析，并且

$$
\sum f_n(z)
$$

在 $D$ 内局部一致收敛，则

$$
f(z)=\sum f_n(z)
$$

在 $D$ 内解析。

并且

$$
\boxed{
f'(z)=\sum f_n'(z)
}
$$

---

# 十四、期末常见“秒杀模板”

## 模板 1：求收敛半径

看到：

$$
\sum a_n(z-z_0)^n
$$

直接写：

$$
R=\frac{1}{\limsup |a_n|^{1/n}}
$$

若比值方便：

$$
R=\lim_{n\to\infty}\left|\frac{a_n}{a_{n+1}}\right|
$$

然后：

$$
|z-z_0|<R \text{ 收敛}
$$

$$
|z-z_0|>R \text{ 发散}
$$

$$
|z-z_0|=R \text{ 单独讨论}
$$

---

## 模板 2：判断一致收敛

如果能估计：

$$
|f_n(z)|\le M_n
$$

并且

$$
\sum M_n
$$

收敛，则直接写：

$$
\boxed{
由 Weierstrass 判别法，原级数一致收敛
}
$$

---

## 模板 3：Taylor 展开有理函数

优先变成：

$$
\frac{1}{1-w}
$$

或者

$$
\frac{1}{1+w}
$$

然后套：

$$
\frac{1}{1-w}=\sum w^n
$$

$$
\frac{1}{1+w}=\sum (-1)^n w^n
$$

如果是复杂分母，先部分分式分解。

---

## 模板 4：求和函数

从几何级数开始：

$$
\sum z^n=\frac{1}{1-z}
$$

然后通过求导、积分得到：

$$
\sum n z^n
$$

$$
\sum n^2 z^n
$$

$$
\sum \frac{z^n}{n}
$$

$$
\sum \frac{z^n}{n^2}
$$

---

## 模板 5：积分题找 $\frac1z$ 项

若要求

$$
\int_C F(z)\,dz
$$

并且 $F$ 可展开成 Laurent 形式：

$$
F(z)=\cdots + a_{-1}\frac1z+a_0+a_1z+\cdots
$$

则

$$
\boxed{
\int_C F(z)\,dz=2\pi i\,a_{-1}
}
$$

如果还没学留数，可以理解为：

$$
\boxed{
闭路积分只关心 \frac1z \text{ 项}
}
$$

---

# 十五、最后整理：高频题型清单

| 题型 | 常见问法 | 核心方法 |
|---|---|---|
| 求收敛半径 | 求 $\sum a_nz^n$ 的 $R$ | 根值法、比值法 |
| 求收敛域 | 判断边界 | 边界单独代入 |
| 一致收敛 | 证明某级数一致收敛 | Weierstrass 判别法 |
| 幂级数求和 | 求 $\sum nz^n$、$\sum z^n/n$ | 几何级数求导积分 |
| Taylor 展开 | 展开 $\frac1{z-a}$、$\frac1{1+z^2}$ | 化成几何级数 |
| 求 Taylor 系数 | 求 $a_n$ | 系数比较或 Taylor 公式 |
| 求积分 | $\int_C \frac{e^z}{z^k}dz$ | 展开后找 $\frac1z$ 项 |
| 求收敛半径 | 给一个函数 $f$，问 Taylor 半径 | 找最近奇点 |
| 证明解析 | 级数定义函数是否解析 | 局部一致收敛/幂级数性质 |

---

# 十六、最应该背下来的 10 个公式

$$
\boxed{
\frac{1}{1-z}=\sum_{n=0}^{\infty}z^n,\quad |z|<1
}
$$

$$
\boxed{
e^z=\sum_{n=0}^{\infty}\frac{z^n}{n!}
}
$$

$$
\boxed{
\sin z=\sum_{n=0}^{\infty}(-1)^n\frac{z^{2n+1}}{(2n+1)!}
}
$$

$$
\boxed{
\cos z=\sum_{n=0}^{\infty}(-1)^n\frac{z^{2n}}{(2n)!}
}
$$

$$
\boxed{
\log(1+z)=\sum_{n=1}^{\infty}(-1)^{n-1}\frac{z^n}{n},\quad |z|<1
}
$$

$$
\boxed{
-\log(1-z)=\sum_{n=1}^{\infty}\frac{z^n}{n},\quad |z|<1
}
$$

$$
\boxed{
R=\frac{1}{\limsup |a_n|^{1/n}}
}
$$

$$
\boxed{
R=\lim\left|\frac{a_n}{a_{n+1}}\right|
}
$$

$$
\boxed{
a_n=\frac{f^{(n)}(z_0)}{n!}
}
$$

$$
\boxed{
a_n=
\frac{1}{2\pi i}
\int_C
\frac{f(\zeta)}{(\zeta-z_0)^{n+1}}
\,d\zeta
}
$$

---

# 十七、考试时的判断顺序

遇到级数题，按这个流程：

$$
\boxed{
先看是不是幂级数
}
$$

如果是：

$$
\boxed{
先求收敛半径 R
}
$$

然后：

$$
\boxed{
圆内绝对收敛，圆外发散，边界单独讨论
}
$$

如果问一致收敛：

$$
\boxed{
优先用 Weierstrass 判别法
}
$$

如果问 Taylor 展开：

$$
\boxed{
优先化成几何级数或已知展开
}
$$

如果问积分：

$$
\boxed{
展开后找 \frac1z \text{ 项}
}
$$

如果问 Taylor 收敛半径：

$$
\boxed{
找最近奇点
}
$$

级数章的核心不是计算复杂，而是要形成这几个固定反射。



---
Powered by [ChatGPT Exporter](https://www.chatgptexporter.com)