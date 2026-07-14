# 微分几何：从一般向量场的协变导数到 Gauss 定理
## ——逻辑串讲、公式推导与期末复习

> **主要依据**：陈维桓《微分几何》第五章。  
> **学习目标**：不是孤立背公式，而是看清下面这条主线：
>
> $$
> \boxed{
> \text{度量 }g
> \Longrightarrow
> \text{Christoffel 记号 }\Gamma
> \Longrightarrow
> \text{协变导数 }D
> \Longrightarrow
> \text{曲率张量 }R
> \Longrightarrow
> K
> }
> $$
>
> 以及外在几何主线：
>
> $$
> \boxed{
> \text{第二基本形式 }b
> \Longrightarrow
> \text{Weingarten 映射 }S=g^{-1}b
> \Longrightarrow
> \kappa_1,\kappa_2,H,K
> }
> $$
>
> 两条主线最终由 **Gauss 方程**连接。

---

# 0. 全章逻辑地图

先看每个对象到底回答什么问题。

| 对象 | 回答的问题 | 最核心公式 |
|---|---|---|
| 第一基本形式 \(g\) | 切平面内怎样算长度、角度、面积 | \(\langle X,Y\rangle=[X]^Tg[Y]\) |
| Christoffel 记号 \(\Gamma_{ij}^k\) | 切基 \(\mathbf r_u,\mathbf r_v\) 在切平面内怎样变化 | \(D_{\mathbf r_i}\mathbf r_j=\Gamma_{ij}^k\mathbf r_k\) |
| 协变导数 \(D_XY\) | 沿 \(X\) 方向看切向量场 \(Y\) 在曲面内部怎样变化 | \((D_XY)^k=X^i(\partial_iY^k+\Gamma_{ij}^kY^j)\) |
| 第二基本形式 \(b\) | 切基向法线方向怎样变化 | \(b_{ij}=\langle\mathbf r_{ij},\mathbf n\rangle\) |
| Gauss 公式 | 切向量的空间总变化如何分成切向和法向 | \(\mathbf r_{ij}=\Gamma_{ij}^k\mathbf r_k+b_{ij}\mathbf n\) |
| Weingarten 公式 | 法向量怎样在切平面内变化 | \(\mathbf n_i=-g^{k\ell}b_{i\ell}\mathbf r_k\) |
| 形算子 \(S\) | 法向量沿每个切方向变化多快 | \(S=-d\mathbf n,\ [S]=g^{-1}b\) |
| 主曲率 | 哪些方向的法向变化最简单 | \(b\xi=\kappa g\xi\) |
| 自然标架运动公式 | \(\mathbf r_u,\mathbf r_v,\mathbf n\) 整体如何运动 | \(\mathcal F_i=\mathcal F\Omega_i\) |
| Gauss–Codazzi | 给定的 \(g,b\) 能否来自一张曲面 | 混合偏导相容条件 |
| Gauss 定理 | \(K\) 是否只由曲面内部度量决定 | \(K=R_{1212}/\det g\) |

整章最核心的统一式是

$$
\boxed{
\overline\nabla_XY
=
D_XY+\mathrm{II}(X,Y)\mathbf n.
}
$$

左边是三维空间里的**总变化**；右边分别是：

- \(D_XY\)：切平面内的变化；
- \(\mathrm{II}(X,Y)\mathbf n\)：法向变化。

---

# 1. 统一记号

设曲面参数表示为

$$
\mathbf r=\mathbf r(u,v).
$$

令

$$
u^1=u,\qquad u^2=v,
$$

并记

$$
\mathbf r_1=\mathbf r_u,\qquad
\mathbf r_2=\mathbf r_v.
$$

一般地，

$$
\mathbf r_i=\frac{\partial\mathbf r}{\partial u^i},
\qquad
\mathbf r_{ij}
=
\frac{\partial^2\mathbf r}
{\partial u^i\partial u^j}.
$$

单位法向量统一记为

$$
\boxed{
\mathbf n=
\frac{\mathbf r_u\times\mathbf r_v}
{\|\mathbf r_u\times\mathbf r_v\|}.
}
$$

采用 Einstein 求和约定：重复出现一次上标、一次下标时，对 \(1,2\) 求和。

例如

$$
X=X^i\mathbf r_i
$$

表示

$$
X=X^1\mathbf r_1+X^2\mathbf r_2.
$$

本文采用形算子约定

$$
\boxed{S=-d\mathbf n.}
$$

因此

$$
\boxed{
\mathrm{II}(X,Y)=\langle S(X),Y\rangle.
}
$$

---

# 2. 一般切向量场到底是什么

在每一点 \(p\)，切平面为

$$
T_pM=\operatorname{span}\{\mathbf r_u,\mathbf r_v\}.
$$

任意切向量场可以写成

$$
\boxed{
X=X^1(u,v)\mathbf r_u+X^2(u,v)\mathbf r_v,
}
$$

$$
\boxed{
Y=Y^1(u,v)\mathbf r_u+Y^2(u,v)\mathbf r_v.
}
$$

这里有两类东西都会随位置变化：

1. 坐标函数 \(Y^1,Y^2\) 会变；
2. 切基 \(\mathbf r_u,\mathbf r_v\) 也会变。

这是协变导数出现的根本原因。

> 即使 \(Y^1,Y^2\) 恒等于常数，向量 \(Y\) 仍可能变化，因为它所依赖的基向量在变化。

---

# 3. \(D_XY\) 中 \(X\) 和 \(Y\) 的角色

$$
D_XY
$$

读作：

> 沿 \(X\) 的方向，观察切向量场 \(Y\) 在曲面内部怎样变化。

因此：

- \(X\)：指定“沿哪个方向走”；
- \(Y\)：指定“观察哪个向量场”；
- \(D_XY\)：得到的切向变化。

例如

$$
D_{\mathbf r_u}\mathbf r_v
$$

表示：

> 沿 \(u\) 方向移动时，观察切基 \(\mathbf r_v\) 怎样变化，并只保留切平面内的变化。

---

# 4. 沿曲线推导一般向量场的协变导数

这是本章最需要真正理解的推导。

设曲面上一条曲线为

$$
\gamma(t)=\mathbf r(u(t),v(t)).
$$

曲线速度为

$$
\gamma'(t)
=
u'(t)\mathbf r_u+v'(t)\mathbf r_v.
$$

所以沿曲线方向可记为

$$
X=\gamma'
=
X^1\mathbf r_u+X^2\mathbf r_v,
$$

其中

$$
X^1=u',\qquad X^2=v'.
$$

沿曲线观察向量场

$$
Y=Y^1\mathbf r_u+Y^2\mathbf r_v.
$$

把 \(Y\) 对 \(t\) 做普通空间求导：

$$
\begin{aligned}
\frac{dY}{dt}
={}&
\frac{dY^1}{dt}\mathbf r_u
+
Y^1\frac{d\mathbf r_u}{dt}\\
&+
\frac{dY^2}{dt}\mathbf r_v
+
Y^2\frac{d\mathbf r_v}{dt}.
\end{aligned}
$$

其中

$$
\frac{dY^1}{dt}
=
u'Y^1_u+v'Y^1_v,
$$

$$
\frac{dY^2}{dt}
=
u'Y^2_u+v'Y^2_v.
$$

基向量的导数是

$$
\frac{d\mathbf r_u}{dt}
=
u'\mathbf r_{uu}+v'\mathbf r_{uv},
$$

$$
\frac{d\mathbf r_v}{dt}
=
u'\mathbf r_{uv}+v'\mathbf r_{vv}.
$$

所以

$$
\begin{aligned}
\frac{dY}{dt}
={}&
(u'Y^1_u+v'Y^1_v)\mathbf r_u\\
&+
(u'Y^2_u+v'Y^2_v)\mathbf r_v\\
&+
Y^1(u'\mathbf r_{uu}+v'\mathbf r_{uv})\\
&+
Y^2(u'\mathbf r_{uv}+v'\mathbf r_{vv}).
\end{aligned}
$$

这个 \(\dfrac{dY}{dt}\) 是三维空间里的**总变化**，一般不完全位于切平面内。

因此必须继续使用 Gauss 公式分解二阶偏导。

---

# 5. Gauss 公式：二阶偏导的切向—法向分解

因为

$$
\mathbb R^3=T_pM\oplus N_pM,
$$

任意三维向量都能唯一分成切向部分和法向部分。

对二阶偏导：

$$
\mathbf r_{ij}
=
(\mathbf r_{ij})^\top
+
(\mathbf r_{ij})^\perp.
$$

定义

$$
D_{\mathbf r_i}\mathbf r_j
=
(\mathbf r_{ij})^\top.
$$

又因为法空间由单位法向量 \(\mathbf n\) 张成，

$$
(\mathbf r_{ij})^\perp
=
\langle\mathbf r_{ij},\mathbf n\rangle\mathbf n.
$$

定义第二基本形式系数

$$
\boxed{
b_{ij}=\langle\mathbf r_{ij},\mathbf n\rangle.
}
$$

于是

$$
\boxed{
\mathbf r_{ij}
=
D_{\mathbf r_i}\mathbf r_j+b_{ij}\mathbf n.
}
$$

而切向部分可以用切基展开：

$$
\boxed{
D_{\mathbf r_i}\mathbf r_j
=
\Gamma_{ij}^k\mathbf r_k.
}
$$

因此得到 Gauss 公式：

$$
\boxed{
\mathbf r_{ij}
=
\Gamma_{ij}^k\mathbf r_k+b_{ij}\mathbf n.
}
$$

展开为

$$
\boxed{
\mathbf r_{uu}
=
\Gamma_{11}^1\mathbf r_u
+
\Gamma_{11}^2\mathbf r_v
+
L\mathbf n,
}
$$

$$
\boxed{
\mathbf r_{uv}
=
\Gamma_{12}^1\mathbf r_u
+
\Gamma_{12}^2\mathbf r_v
+
M\mathbf n,
}
$$

$$
\boxed{
\mathbf r_{vv}
=
\Gamma_{22}^1\mathbf r_u
+
\Gamma_{22}^2\mathbf r_v
+
N\mathbf n.
}
$$

其中

$$
L=b_{11},\qquad M=b_{12},\qquad N=b_{22}.
$$

## 一句话理解

$$
\boxed{
\text{二阶偏导}
=
\text{切基在切平面内的变化}
+
\text{切基向法线的变化}.
}
$$

前者由 \(\Gamma\) 描述，后者由 \(b\) 描述。

---

# 6. 一般向量场的协变导数公式

将 Gauss 公式代入第 4 节的普通导数，取切向部分。

设

$$
X=X^1\mathbf r_u+X^2\mathbf r_v,
$$

$$
Y=Y^1\mathbf r_u+Y^2\mathbf r_v.
$$

则

$$
\boxed{
D_XY=(D_XY)^1\mathbf r_u+(D_XY)^2\mathbf r_v.
}
$$

其中

$$
\begin{aligned}
(D_XY)^1
={}&
X^1Y^1_u+X^2Y^1_v\\
&+
X^1Y^1\Gamma_{11}^1
+
X^1Y^2\Gamma_{12}^1\\
&+
X^2Y^1\Gamma_{12}^1
+
X^2Y^2\Gamma_{22}^1,
\end{aligned}
$$

$$
\begin{aligned}
(D_XY)^2
={}&
X^1Y^2_u+X^2Y^2_v\\
&+
X^1Y^1\Gamma_{11}^2
+
X^1Y^2\Gamma_{12}^2\\
&+
X^2Y^1\Gamma_{12}^2
+
X^2Y^2\Gamma_{22}^2.
\end{aligned}
$$

指标形式压缩为

$$
\boxed{
D_XY
=
X^i
\left(
\partial_iY^k+\Gamma_{ij}^kY^j
\right)\mathbf r_k.
}
$$

因此

$$
\boxed{
(D_XY)^k
=
X^i
\left(
\partial_iY^k+\Gamma_{ij}^kY^j
\right).
}
$$

这个公式必须拆成两部分理解：

$$
\boxed{
\partial_iY^k
}
$$

是 \(Y\) 的坐标系数变化；

$$
\boxed{
\Gamma_{ij}^kY^j
}
$$

是切基自身变化造成的修正。

---

# 7. 一般 Gauss 公式

普通空间导数不只包含切向部分。

完整公式是

$$
\boxed{
\overline\nabla_XY
=
D_XY+\mathrm{II}(X,Y)\mathbf n.
}
$$

而

$$
\boxed{
\mathrm{II}(X,Y)=b_{ij}X^iY^j.
}
$$

所以

$$
\boxed{
\overline\nabla_XY
=
X^i
\left(
\partial_iY^k+\Gamma_{ij}^kY^j
\right)\mathbf r_k
+
b_{ij}X^iY^j\mathbf n.
}
$$

这条公式可以拆成三层：

$$
\boxed{
\text{总变化}
=
\text{坐标系数变化}
+
\text{切基切向变化}
+
\text{切基法向变化}.
}
$$

对应为

$$
\partial_iY^k,\qquad
\Gamma_{ij}^k,\qquad
b_{ij}.
$$

---

# 8. 三个最重要的特殊情况

## 8.1 \(D_{\mathbf r_u}\mathbf r_u\)

因为

$$
\mathbf r_u=1\cdot\mathbf r_u+0\cdot\mathbf r_v,
$$

其坐标系数是常数，所以只有基变化项：

$$
\boxed{
D_{\mathbf r_u}\mathbf r_u
=
\Gamma_{11}^1\mathbf r_u+\Gamma_{11}^2\mathbf r_v.
}
$$

## 8.2 \(D_{\mathbf r_u}\mathbf r_v\)

$$
\boxed{
D_{\mathbf r_u}\mathbf r_v
=
\Gamma_{12}^1\mathbf r_u+\Gamma_{12}^2\mathbf r_v
=
(\mathbf r_{uv})^\top.
}
$$

## 8.3 \(D_{\mathbf r_v}\mathbf r_v\)

$$
\boxed{
D_{\mathbf r_v}\mathbf r_v
=
\Gamma_{22}^1\mathbf r_u+\Gamma_{22}^2\mathbf r_v.
}
$$

这三式就是 Christoffel 记号最直接的几何定义。

---

# 9. 度量矩阵 \(g\)

第一基本形式系数为

$$
\boxed{
g_{ij}=\langle\mathbf r_i,\mathbf r_j\rangle.
}
$$

矩阵形式：

$$
\boxed{
g=(g_{ij})
=
\begin{pmatrix}
E&F\\
F&G
\end{pmatrix}.
}
$$

其中

$$
E=\langle\mathbf r_u,\mathbf r_u\rangle,\qquad
F=\langle\mathbf r_u,\mathbf r_v\rangle,\qquad
G=\langle\mathbf r_v,\mathbf r_v\rangle.
$$

若

$$
X=X^i\mathbf r_i,\qquad
Y=Y^j\mathbf r_j,
$$

则

$$
\boxed{
\langle X,Y\rangle=g_{ij}X^iY^j.
}
$$

矩阵形式：

$$
\boxed{
\langle X,Y\rangle=[X]^Tg[Y].
}
$$

逆度量矩阵记为

$$
g^{-1}=(g^{ij}),
$$

满足

$$
\boxed{
g^{ik}g_{kj}=\delta^i_j.
}
$$

二维中

$$
\boxed{
g^{-1}
=
\frac1{EG-F^2}
\begin{pmatrix}
G&-F\\
-F&E
\end{pmatrix}.
}
$$

> 注意：\(g^{ij}\) 是逆矩阵的元素，不是 \(g_{ij}\) 的逐项倒数。

---

# 10. 第一类和第二类 Christoffel 记号

第二类 Christoffel 记号定义为切向坐标：

$$
\boxed{
D_{\mathbf r_i}\mathbf r_j
=
\Gamma_{ij}^k\mathbf r_k.
}
$$

第一类 Christoffel 记号定义为

$$
\boxed{
\Gamma_{ij,\ell}
=
\langle\mathbf r_{ij},\mathbf r_\ell\rangle.
}
$$

由 Gauss 公式：

$$
\mathbf r_{ij}
=
\Gamma_{ij}^k\mathbf r_k+b_{ij}\mathbf n.
$$

与 \(\mathbf r_\ell\) 做内积：

$$
\Gamma_{ij,\ell}
=
\Gamma_{ij}^k
\langle\mathbf r_k,\mathbf r_\ell\rangle.
$$

因此

$$
\boxed{
\Gamma_{ij,\ell}
=
g_{k\ell}\Gamma_{ij}^k.
}
$$

乘逆度量：

$$
\boxed{
\Gamma_{ij}^k
=
g^{k\ell}\Gamma_{ij,\ell}.
}
$$

## 矩阵本质

固定 \(i,j\)，有

$$
\begin{pmatrix}
\Gamma_{ij,1}\\
\Gamma_{ij,2}
\end{pmatrix}
=
g
\begin{pmatrix}
\Gamma_{ij}^1\\
\Gamma_{ij}^2
\end{pmatrix}.
$$

所以

$$
\boxed{
\begin{pmatrix}
\Gamma_{ij}^1\\
\Gamma_{ij}^2
\end{pmatrix}
=
g^{-1}
\begin{pmatrix}
\Gamma_{ij,1}\\
\Gamma_{ij,2}
\end{pmatrix}.
}
$$

这只是线性代数中的

$$
b=gx
\quad\Longrightarrow\quad
x=g^{-1}b.
$$

---

# 11. Christoffel 记号为什么能由 \(g\) 计算

从

$$
g_{j\ell}
=
\langle\mathbf r_j,\mathbf r_\ell\rangle
$$

对 \(u^i\) 求导：

$$
\partial_i g_{j\ell}
=
\langle\mathbf r_{ij},\mathbf r_\ell\rangle
+
\langle\mathbf r_j,\mathbf r_{i\ell}\rangle.
$$

即

$$
\partial_i g_{j\ell}
=
\Gamma_{ij,\ell}
+
\Gamma_{i\ell,j}.
$$

将三组同类等式作“前两式相加减第三式”，得到

$$
\boxed{
\Gamma_{ij,\ell}
=
\frac12
\left(
\partial_i g_{j\ell}
+
\partial_j g_{i\ell}
-
\partial_\ell g_{ij}
\right).
}
$$

再升指标：

$$
\boxed{
\Gamma_{ij}^k
=
\frac12g^{k\ell}
\left(
\partial_i g_{j\ell}
+
\partial_j g_{i\ell}
-
\partial_\ell g_{ij}
\right).
}
$$

因此

$$
\boxed{
g及其一阶导数
\Longrightarrow
\Gamma.
}
$$

这说明协变导数 \(D\) 完全由第一基本形式决定。

---

# 12. \(E,F,G\) 下常用第一类 Christoffel 记号

$$
\Gamma_{11,1}=\frac12E_u,
$$

$$
\Gamma_{11,2}=F_u-\frac12E_v,
$$

$$
\Gamma_{12,1}=\frac12E_v,
$$

$$
\Gamma_{12,2}=\frac12G_u,
$$

$$
\Gamma_{22,1}=F_v-\frac12G_u,
$$

$$
\Gamma_{22,2}=\frac12G_v.
$$

然后统一用

$$
\boxed{
\begin{pmatrix}
\Gamma_{ij}^1\\
\Gamma_{ij}^2
\end{pmatrix}
=
\frac1{EG-F^2}
\begin{pmatrix}
G&-F\\
-F&E
\end{pmatrix}
\begin{pmatrix}
\Gamma_{ij,1}\\
\Gamma_{ij,2}
\end{pmatrix}.
}
$$

期末计算题中，这通常比逐个套三指标公式更稳。

---

# 13. 为什么 Christoffel 记号不是曲率

考虑平面极坐标：

$$
\mathbf r(\rho,\theta)
=
(\rho\cos\theta,\rho\sin\theta,0).
$$

有

$$
\mathbf r_\rho
=
(\cos\theta,\sin\theta,0),
$$

$$
\mathbf r_\theta
=
(-\rho\sin\theta,\rho\cos\theta,0).
$$

虽然曲面是平面，但

$$
\mathbf r_{\rho\theta}
=
\frac1\rho\mathbf r_\theta,
$$

$$
\mathbf r_{\theta\theta}
=
-\rho\mathbf r_\rho.
$$

所以

$$
\Gamma_{12}^2=\frac1\rho,
\qquad
\Gamma_{22}^1=-\rho.
$$

因此

$$
\boxed{
\Gamma\neq0
\not\Rightarrow
K\neq0.
}
$$

Christoffel 记号记录“所选坐标基如何变化”，其中包含坐标效应；真正曲率要看 \(\Gamma\) 的导数和二次组合。

---

# 14. 协变导数的基本性质

## 14.1 对第一个变量函数线性

$$
\boxed{
D_{fX+gZ}Y
=
fD_XY+gD_ZY.
}
$$

第一个变量只指定求导方向，因此不会对 \(f,g\) 求导。

## 14.2 对第二个变量满足 Leibniz 法则

$$
\boxed{
D_X(fY)
=
X(f)Y+fD_XY.
}
$$

## 14.3 度量相容性

$$
\boxed{
X\langle Y,Z\rangle
=
\langle D_XY,Z\rangle
+
\langle Y,D_XZ\rangle.
}
$$

指标形式为

$$
\boxed{
\nabla_k g_{ij}=0.
}
$$

展开：

$$
\boxed{
\partial_k g_{ij}
=
\Gamma_{ki}^\ell g_{\ell j}
+
\Gamma_{kj}^\ell g_{i\ell}.
}
$$

## 14.4 无挠性

$$
\boxed{
D_XY-D_YX=[X,Y].
}
$$

坐标向量场满足

$$
[\mathbf r_u,\mathbf r_v]=0,
$$

所以

$$
D_{\mathbf r_u}\mathbf r_v
=
D_{\mathbf r_v}\mathbf r_u.
$$

因此

$$
\boxed{
\Gamma_{ij}^k=\Gamma_{ji}^k.
}
$$

---

# 15. 第二基本形式 \(b\)

第二基本形式矩阵为

$$
\boxed{
b=(b_{ij})
=
\begin{pmatrix}
L&M\\
M&N
\end{pmatrix}.
}
$$

对切向量

$$
X=X^i\mathbf r_i,\qquad
Y=Y^j\mathbf r_j,
$$

有

$$
\boxed{
\mathrm{II}(X,Y)=b_{ij}X^iY^j.
}
$$

矩阵形式：

$$
\boxed{
\mathrm{II}(X,Y)=[X]^Tb[Y].
}
$$

第一基本形式与第二基本形式的对照：

| 第一基本形式 | 第二基本形式 |
|---|---|
| \(g_{ij}=\langle\mathbf r_i,\mathbf r_j\rangle\) | \(b_{ij}=\langle\mathbf r_{ij},\mathbf n\rangle\) |
| 测量长度、夹角、面积 | 测量向法线方向的弯曲 |
| 内蕴度量 | 与嵌入和法向选择有关 |
| 矩阵 \(g\) | 矩阵 \(b\) |

---

# 16. Weingarten 公式

Gauss 公式研究切向量怎样变化；Weingarten 公式研究法向量怎样变化。

因为

$$
\langle\mathbf n,\mathbf n\rangle=1,
$$

对 \(u^i\) 求导：

$$
\langle\mathbf n_i,\mathbf n\rangle=0.
$$

所以

$$
\mathbf n_i\in T_pM.
$$

设

$$
\mathbf n_i=c_i^k\mathbf r_k.
$$

另一方面，由

$$
\langle\mathbf n,\mathbf r_j\rangle=0
$$

求导：

$$
\langle\mathbf n_i,\mathbf r_j\rangle
+
\langle\mathbf n,\mathbf r_{ij}\rangle
=0.
$$

所以

$$
\boxed{
\langle\mathbf n_i,\mathbf r_j\rangle=-b_{ij}.
}
$$

代入

$$
\mathbf n_i=c_i^k\mathbf r_k
$$

得到

$$
c_i^kg_{kj}=-b_{ij}.
$$

乘逆度量矩阵：

$$
c_i^k=-g^{k\ell}b_{i\ell}.
$$

因此

$$
\boxed{
\mathbf n_i
=
-g^{k\ell}b_{i\ell}\mathbf r_k.
}
$$

令

$$
b_i{}^k=g^{k\ell}b_{i\ell},
$$

则

$$
\boxed{
\mathbf n_i=-b_i{}^k\mathbf r_k.
}
$$

这就是 Weingarten 公式。

---

# 17. 形算子 \(S\) 及其矩阵

定义

$$
\boxed{
S=-d\mathbf n.
}
$$

所以

$$
S(\mathbf r_i)=-\mathbf n_i.
$$

由 Weingarten 公式：

$$
\boxed{
S(\mathbf r_i)=b_i{}^k\mathbf r_k.
}
$$

因此在切基 \(\{\mathbf r_u,\mathbf r_v\}\) 下，

$$
\boxed{
[S]=A=g^{-1}b.
}
$$

这是本章最重要的矩阵公式之一。

## 为什么不是直接 \(b\)

因为 \(b_{ij}\) 是通过内积得到的“下指标量”：

$$
b_{ij}
=
\langle S(\mathbf r_i),\mathbf r_j\rangle.
$$

而矩阵 \(A\) 需要的是 \(S(\mathbf r_i)\) 的坐标。

非正交基下：

$$
\text{内积数据}
=
g\times\text{坐标数据}.
$$

所以必须乘 \(g^{-1}\)：

$$
\boxed{
A=g^{-1}b.
}
$$

---

# 18. 形算子的自伴性

由于第二基本形式对称：

$$
b_{ij}=b_{ji}.
$$

又有

$$
b=gA.
$$

因此

$$
(gA)^T=gA.
$$

即

$$
\boxed{
A^Tg=gA.
}
$$

这不是说 \(A\) 在普通意义下一定对称，而是说它关于度量 \(g\) 自伴：

$$
\boxed{
\langle S(X),Y\rangle
=
\langle X,S(Y)\rangle.
}
$$

因此 \(S\) 的特征值为实数，不同特征值对应的主方向正交。

---

# 19. 法曲率、主方向和主曲率

对非零切向量 \(X\)，法曲率定义为

$$
\boxed{
k_n(X)
=
\frac{\mathrm{II}(X,X)}
{\mathrm I(X,X)}.
}
$$

矩阵形式：

$$
\boxed{
k_n(\xi)
=
\frac{\xi^Tb\xi}{\xi^Tg\xi}.
}
$$

之所以要除以 \(\mathrm I(X,X)\)，是为了消除向量长度变化，只保留方向信息。

若 \(X\) 是单位切向量，

$$
k_n(X)=\mathrm{II}(X,X)=\langle S(X),X\rangle.
$$

若

$$
\boxed{
S(X)=\kappa X,
}
$$

则 \(X\) 是主方向，\(\kappa\) 是主曲率。

在坐标中：

$$
A\xi=\kappa\xi.
$$

由于

$$
A=g^{-1}b,
$$

等价于

$$
\boxed{
b\xi=\kappa g\xi.
}
$$

因此主曲率满足

$$
\boxed{
\det(b-\kappa g)=0.
}
$$

---

# 20. Euler 公式

设单位正交主方向为

$$
\mathbf e_1,\mathbf e_2,
$$

对应主曲率为

$$
\kappa_1,\kappa_2.
$$

任意单位方向写成

$$
X=\cos\theta\,\mathbf e_1+\sin\theta\,\mathbf e_2.
$$

则

$$
\boxed{
k_n(\theta)
=
\kappa_1\cos^2\theta
+
\kappa_2\sin^2\theta.
}
$$

结论：

1. 法曲率的最大值和最小值是主曲率；
2. 法曲率极值方向就是主方向；
3. 脐点处 \(\kappa_1=\kappa_2\)，所有方向都是主方向。

---

# 21. Gauss 曲率和平均曲率

因为主曲率是形算子 \(A\) 的两个特征值，

$$
K=\kappa_1\kappa_2,
$$

$$
H=\frac{\kappa_1+\kappa_2}{2}.
$$

所以

$$
\boxed{
K=\det A
=
\frac{\det b}{\det g}.
}
$$

即

$$
\boxed{
K=
\frac{LN-M^2}{EG-F^2}.
}
$$

平均曲率为

$$
\boxed{
H=\frac12\operatorname{tr}A.
}
$$

指标形式：

$$
\boxed{
2H=g^{ij}b_{ij}.
}
$$

经典形式：

$$
\boxed{
H=
\frac{EN-2FM+GL}
{2(EG-F^2)}.
}
$$

主曲率满足

$$
\boxed{
\kappa^2-2H\kappa+K=0.
}
$$

因此

$$
\boxed{
\kappa_{1,2}
=
H\pm\sqrt{H^2-K}.
}
$$

形算子满足 Cayley–Hamilton 恒等式：

$$
\boxed{
S^2-2HS+KI=0.
}
$$

---

# 22. 改变法向量方向会发生什么

若

$$
\mathbf n\mapsto-\mathbf n,
$$

则

$$
b\mapsto-b,
$$

$$
S\mapsto-S,
$$

$$
\kappa_i\mapsto-\kappa_i,
$$

$$
H\mapsto-H.
$$

但

$$
\boxed{
K=\kappa_1\kappa_2
}
$$

不变。

这是期末判断题常见考点。

---

# 23. 自然标架运动公式

自然标架为

$$
\boxed{
\{\mathbf r_u,\mathbf r_v,\mathbf n\}.
}
$$

它一般不是正交单位标架，但在正则点线性无关。

把三个向量按列排成矩阵：

$$
\mathcal F=
\begin{pmatrix}
|&|&|\\
\mathbf r_u&\mathbf r_v&\mathbf n\\
|&|&|
\end{pmatrix}.
$$

## 沿 \(u\) 方向

$$
\boxed{
\mathcal F_u=\mathcal F\Omega_u,
}
$$

其中

$$
\boxed{
\Omega_u=
\begin{pmatrix}
\Gamma_{11}^1&\Gamma_{12}^1&-b_1{}^1\\
\Gamma_{11}^2&\Gamma_{12}^2&-b_1{}^2\\
L&M&0
\end{pmatrix}.
}
$$

## 沿 \(v\) 方向

$$
\boxed{
\mathcal F_v=\mathcal F\Omega_v,
}
$$

其中

$$
\boxed{
\Omega_v=
\begin{pmatrix}
\Gamma_{12}^1&\Gamma_{22}^1&-b_2{}^1\\
\Gamma_{12}^2&\Gamma_{22}^2&-b_2{}^2\\
M&N&0
\end{pmatrix}.
}
$$

## 如何阅读矩阵

以 \(\Omega_u\) 第一列为例：

$$
\begin{pmatrix}
\Gamma_{11}^1\\
\Gamma_{11}^2\\
L
\end{pmatrix}
$$

表示

$$
\mathbf r_{u,u}
=
\Gamma_{11}^1\mathbf r_u
+
\Gamma_{11}^2\mathbf r_v
+
L\mathbf n.
$$

第三列表示

$$
\mathbf n_u
=
-b_1{}^1\mathbf r_u-b_1{}^2\mathbf r_v.
$$

所以自然标架运动公式只是把 Gauss 公式和 Weingarten 公式装进矩阵。

---

# 24. 为什么会出现 Gauss–Codazzi 方程

若这些标架真的来自一张光滑曲面，则混合偏导必须可交换：

$$
\mathcal F_{uv}=\mathcal F_{vu}.
$$

由

$$
\mathcal F_u=\mathcal F\Omega_u,
\qquad
\mathcal F_v=\mathcal F\Omega_v,
$$

计算得到

$$
\boxed{
(\Omega_u)_v-(\Omega_v)_u
+
\Omega_v\Omega_u-\Omega_u\Omega_v
=0.
}
$$

等价地，根据矩阵放置约定也可写成

$$
\Omega_{u,v}-\Omega_{v,u}+[\Omega_v,\Omega_u]=0.
$$

这个矩阵相容条件展开后分成：

- Gauss 方程；
- Codazzi 方程。

核心理解是：

$$
\boxed{
\text{标架先沿 }u\text{ 再沿 }v
=
\text{先沿 }v\text{ 再沿 }u.
}
$$

---

# 25. 曲率张量的指标表示

本文采用陈维桓教材常用指标约定：

$$
\boxed{
R^\delta{}_{\alpha\beta\gamma}
=
\frac{\partial\Gamma^\delta_{\alpha\gamma}}
{\partial u^\beta}
-
\frac{\partial\Gamma^\delta_{\alpha\beta}}
{\partial u^\gamma}
+
\Gamma^\mu_{\alpha\gamma}
\Gamma^\delta_{\mu\beta}
-
\Gamma^\mu_{\alpha\beta}
\Gamma^\delta_{\mu\gamma}.
}
$$

降指标：

$$
\boxed{
R_{\lambda\alpha\beta\gamma}
=
g_{\lambda\delta}
R^\delta{}_{\alpha\beta\gamma}.
}
$$

这说明曲率张量由

$$
\boxed{
\partial\Gamma+\Gamma\Gamma
}
$$

构成。

因此即使能在某一点选坐标使

$$
\Gamma_{ij}^k(p)=0,
$$

也不能推出

$$
K(p)=0,
$$

因为 \(\partial\Gamma(p)\) 可能不为零。

---

# 26. Gauss 方程

由自然标架混合偏导相容，得到

$$
\boxed{
R^\delta{}_{\alpha\beta\gamma}
=
b_{\alpha\beta}b_\gamma{}^\delta
-
b_{\alpha\gamma}b_\beta{}^\delta.
}
$$

降指标：

$$
\boxed{
R_{\lambda\alpha\beta\gamma}
=
b_{\alpha\beta}b_{\lambda\gamma}
-
b_{\alpha\gamma}b_{\lambda\beta}.
}
$$

二维中最重要的分量是

$$
\boxed{
R_{1212}
=
b_{11}b_{22}-b_{12}^2
=
LN-M^2.
}
$$

因此

$$
\boxed{
R_{1212}
=
K(EG-F^2).
}
$$

即

$$
\boxed{
K=\frac{R_{1212}}{EG-F^2}.
}
$$

---

# 27. Codazzi 方程

Codazzi 方程可写为

$$
\boxed{
\frac{\partial b_{\alpha\beta}}{\partial u^\gamma}
-
\frac{\partial b_{\alpha\gamma}}{\partial u^\beta}
=
\Gamma^\mu_{\alpha\gamma}b_{\mu\beta}
-
\Gamma^\mu_{\alpha\beta}b_{\mu\gamma}.
}
$$

定义第二基本形式的协变导数

$$
\boxed{
b_{\alpha\beta;\gamma}
=
\partial_\gamma b_{\alpha\beta}
-
\Gamma^\mu_{\alpha\gamma}b_{\mu\beta}
-
\Gamma^\mu_{\beta\gamma}b_{\alpha\mu}.
}
$$

则 Codazzi 方程简写为

$$
\boxed{
b_{\alpha\beta;\gamma}
=
b_{\alpha\gamma;\beta}.
}
$$

为什么 \(\partial_\gamma b_{\alpha\beta}\) 后面有两个修正项？

因为 \(b_{\alpha\beta}\) 有两个下指标，每个指标都对应一个随位置变化的切基，所以每个下指标都要减去一个 Christoffel 修正。

---

# 28. 正交曲率参数下的高频 Codazzi 公式

若参数线是正交曲率线：

$$
F=0,\qquad M=0,
$$

于是

$$
I=E\,du^2+G\,dv^2,
$$

$$
II=L\,du^2+N\,dv^2.
$$

主曲率为

$$
\kappa_1=\frac LE,
\qquad
\kappa_2=\frac NG.
$$

Codazzi 方程化为

$$
\boxed{
\frac{\partial\kappa_1}{\partial v}
=
\frac{E_v}{2E}
(\kappa_2-\kappa_1),
}
$$

$$
\boxed{
\frac{\partial\kappa_2}{\partial u}
=
\frac{G_u}{2G}
(\kappa_1-\kappa_2).
}
$$

这是证明以下结论的常用工具：

- 常主曲率曲面分类；
- 常平均曲率曲面的局部形式；
- 已知 \(I,II\) 求未知函数；
- 曲面刚性问题。

---

# 29. 曲面唯一性定理

若两张有向曲面在同一参数区域内具有相同的第一、第二基本形式：

$$
g_{ij}^{(1)}=g_{ij}^{(2)},
$$

$$
b_{ij}^{(1)}=b_{ij}^{(2)},
$$

则它们至多相差一个保持定向的刚体运动。

即存在刚体运动 \(T\)，使

$$
\boxed{
\mathbf r^{(2)}=T\circ\mathbf r^{(1)}.
}
$$

## 证明逻辑

### 第一步：在一点对齐

用刚体运动使两曲面在某一点：

- 位置相同；
- \(\mathbf r_u,\mathbf r_v,\mathbf n\) 相同。

### 第二步：比较运动方程

因为 \(g,b\) 相同，所以：

- \(\Gamma\) 相同；
- \(b_i{}^j\) 相同；
- 两组自然标架满足同一个一阶线性方程组。

同初值下解唯一，因此自然标架处处相同。

### 第三步：恢复位置向量

若

$$
\mathbf r_u^{(1)}=\mathbf r_u^{(2)},
\qquad
\mathbf r_v^{(1)}=\mathbf r_v^{(2)},
$$

则

$$
d(\mathbf r^{(1)}-\mathbf r^{(2)})=0.
$$

连通区域上两者只差常向量；初始点已对齐，所以常向量为零。

## 期末记忆

$$
\boxed{
I+II
\Longrightarrow
\text{曲面在刚体运动意义下唯一}.
}
$$

只给 \(I\) 不唯一：平面和圆柱面局部等距。

---

# 30. 曲面存在性定理

反过来，给定两个二次形式：

$$
I=g_{ij}\,du^i du^j,
$$

$$
II=b_{ij}\,du^i du^j,
$$

什么时候能找到曲面实现它们？

局部存在所需条件：

1. \(g=(g_{ij})\) 正定；
2. \(g_{ij},b_{ij}\) 足够光滑；
3. \(b_{ij}=b_{ji}\)；
4. Gauss–Codazzi 方程成立；
5. 参数区域通常要求单连通，以保证积分与路径无关。

## 构造逻辑

### 第一步：由 \(g,b\) 求运动方程系数

由 \(g\) 求 \(\Gamma\)，由 \(g^{-1}b\) 求 Weingarten 系数。

### 第二步：解自然标架方程

求形式标架

$$
\mathbf x_1,\mathbf x_2,\mathbf x_3
$$

满足与自然标架相同的运动方程。

Gauss–Codazzi 正是该方程组的可积条件。

### 第三步：积分位置向量

若能证明

$$
\partial_2\mathbf x_1=\partial_1\mathbf x_2,
$$

则一形式

$$
\mathbf x_1\,du+\mathbf x_2\,dv
$$

为闭形式。

在单连通区域上存在 \(\mathbf r\)，使

$$
\mathbf r_u=\mathbf x_1,
\qquad
\mathbf r_v=\mathbf x_2.
$$

于是得到所需曲面。

---

# 31. 曲面论基本定理

把存在性和唯一性合在一起：

> 给定正定第一基本形式 \(I\) 和对称第二基本形式 \(II\)，若它们满足 Gauss–Codazzi 方程，则局部存在曲面以 \(I,II\) 为两个基本形式；该曲面在保持定向的刚体运动意义下唯一。

逻辑关系：

$$
\boxed{
\begin{array}{c}
I,II\text{ 满足 Gauss–Codazzi}\\
\Downarrow\\
\text{存在曲面}\\
\Downarrow\\
\text{并且至多相差刚体运动}
\end{array}
}
$$

---

# 32. Gauss 绝妙定理

从外在公式看：

$$
K=\frac{LN-M^2}{EG-F^2},
$$

似乎 \(K\) 依赖第二基本形式。

但 Gauss 方程给出

$$
R_{1212}=LN-M^2.
$$

而 \(R_{1212}\) 完全由 \(g\) 及其一、二阶偏导决定。

所以

$$
\boxed{
K=\frac{R_{1212}}{\det g}
}
$$

完全由第一基本形式决定。

这就是 Gauss 绝妙定理：

$$
\boxed{
K\text{ 是内蕴量}.
}
$$

## 直接推论

保长对应保持第一基本形式，因此保持 Gauss 曲率：

$$
\boxed{
\text{局部等距}
\Longrightarrow
K\text{ 保持}.
}
$$

因此：

- 球面 \(K>0\)；
- 圆柱面 \(K=0\)；
- 双曲抛物面 \(K<0\)；

任意两者之间都不可能局部等距。

但要注意：

$$
\boxed{
K\text{ 相同只是局部等距的必要条件，不是充分条件}.
}
$$

---

# 33. 常用内蕴曲率公式

## 33.1 等温参数

若

$$
I=\lambda^2(du^2+dv^2),
$$

则

$$
\boxed{
K
=
-\frac1{\lambda^2}
\left[
(\log\lambda)_{uu}
+
(\log\lambda)_{vv}
\right].
}
$$

## 33.2 特殊度量

若

$$
I=du^2+f(u)^2dv^2,
$$

则

$$
\boxed{
K=-\frac{f''(u)}{f(u)}.
}
$$

若写成

$$
I=du^2+G(u)dv^2,
$$

则取

$$
f(u)=\sqrt{G(u)},
$$

得到

$$
\boxed{
K
=
-\frac1{\sqrt G}
\frac{d^2\sqrt G}{du^2}.
}
$$

展开为

$$
\boxed{
K
=
-\frac{G''}{2G}
+
\frac{(G')^2}{4G^2}.
}
$$

## 33.3 一般参数

一般情况下：

1. 由 \(E,F,G\) 求 \(\Gamma\)；
2. 由 \(\Gamma\) 求 \(R_{1212}\)；
3. 使用

$$
\boxed{
K=\frac{R_{1212}}{EG-F^2}.
}
$$

---

# 34. 与第六章的直接连接

这一章的 \(D_XY\) 会直接进入测地线、平行移动和测地曲率。

## 34.1 沿曲线的协变导数

曲线

$$
\gamma(t)=\mathbf r(u(t),v(t))
$$

的切向量为

$$
\dot\gamma=\dot u^i\mathbf r_i.
$$

沿曲线的切向量场

$$
Y=Y^k(t)\mathbf r_k
$$

满足

$$
\boxed{
\frac{DY}{dt}
=
\left(
\frac{dY^k}{dt}
+
\Gamma_{ij}^k\dot u^iY^j
\right)\mathbf r_k.
}
$$

## 34.2 平行移动

若

$$
\boxed{
\frac{DY}{dt}=0,
}
$$

则称 \(Y\) 沿曲线平行。

坐标方程：

$$
\boxed{
\frac{dY^k}{dt}
+
\Gamma_{ij}^k\dot u^iY^j
=0.
}
$$

## 34.3 测地线

若曲线以弧长 \(s\) 为参数，其切向量为

$$
T=\frac{d\gamma}{ds}.
$$

测地线条件为

$$
\boxed{
D_TT=0.
}
$$

坐标形式：

$$
\boxed{
\frac{d^2u^k}{ds^2}
+
\Gamma_{ij}^k
\frac{du^i}{ds}
\frac{du^j}{ds}
=0.
}
$$

所以 Christoffel 记号在第六章中的角色是：

> 修正曲线坐标的普通二阶导数，使“切向加速度为零”成为坐标无关的几何条件。

---

# 35. 期末计算题标准流程

给定参数曲面

$$
\mathbf r(u,v),
$$

按以下顺序做。

## 第一步：正则性、切向量和法向量

$$
\mathbf r_u,\qquad
\mathbf r_v,
$$

检查

$$
\mathbf r_u\times\mathbf r_v\neq0.
$$

再求

$$
\mathbf n=
\frac{\mathbf r_u\times\mathbf r_v}
{\|\mathbf r_u\times\mathbf r_v\|}.
$$

## 第二步：第一基本形式

$$
E=\langle\mathbf r_u,\mathbf r_u\rangle,
$$

$$
F=\langle\mathbf r_u,\mathbf r_v\rangle,
$$

$$
G=\langle\mathbf r_v,\mathbf r_v\rangle.
$$

组成

$$
g=
\begin{pmatrix}
E&F\\
F&G
\end{pmatrix}.
$$

## 第三步：二阶偏导和第二基本形式

$$
\mathbf r_{uu},\qquad
\mathbf r_{uv},\qquad
\mathbf r_{vv}.
$$

$$
L=\langle\mathbf r_{uu},\mathbf n\rangle,
$$

$$
M=\langle\mathbf r_{uv},\mathbf n\rangle,
$$

$$
N=\langle\mathbf r_{vv},\mathbf n\rangle.
$$

组成

$$
b=
\begin{pmatrix}
L&M\\
M&N
\end{pmatrix}.
$$

## 第四步：Christoffel 记号

稳妥方法：

$$
\Gamma_{ij,\ell}
=
\langle\mathbf r_{ij},\mathbf r_\ell\rangle,
$$

然后

$$
\Gamma_{ij}^k
=
g^{k\ell}\Gamma_{ij,\ell}.
$$

或直接由 \(E,F,G\) 的导数计算。

## 第五步：写 Gauss 公式

$$
\mathbf r_{ij}
=
\Gamma_{ij}^k\mathbf r_k+b_{ij}\mathbf n.
$$

## 第六步：Weingarten 映射

$$
A=g^{-1}b.
$$

再由

$$
S(\mathbf r_i)=A_i{}^k\mathbf r_k
$$

写出 \(\mathbf n_u,\mathbf n_v\)。

## 第七步：曲率

$$
K=\det A,
$$

$$
H=\frac12\operatorname{tr}A.
$$

主曲率解

$$
\det(b-\kappa g)=0.
$$

主方向解

$$
(b-\kappa g)\xi=0.
$$

---

# 36. 期末证明题的三个万能出发点

不知道从哪里开始时，优先对下面三式求导：

## 36.1 度量关系

$$
\boxed{
\langle\mathbf r_i,\mathbf r_j\rangle=g_{ij}.
}
$$

产生 Christoffel 公式、度量相容性。

## 36.2 切法正交

$$
\boxed{
\langle\mathbf n,\mathbf r_i\rangle=0.
}
$$

产生

$$
b_{ij}
=
-\langle\mathbf n_i,\mathbf r_j\rangle
$$

以及 Weingarten 公式。

## 36.3 法向量单位化

$$
\boxed{
\langle\mathbf n,\mathbf n\rangle=1.
}
$$

产生

$$
\mathbf n_i\perp\mathbf n,
$$

从而说明 \(\mathbf n_i\) 是切向量。

---

# 37. 高频恒等式汇总

## 度量与逆度量

$$
\boxed{
g_{ij}=g_{ji}
}
$$

$$
\boxed{
g^{ik}g_{kj}=\delta^i_j
}
$$

$$
\boxed{
\partial_\ell g^{ij}
=
-g^{ia}(\partial_\ell g_{ab})g^{bj}
}
$$

$$
\boxed{
\det g=EG-F^2
}
$$

$$
\boxed{
dA=\sqrt{EG-F^2}\,du\,dv
}
$$

## Christoffel

$$
\boxed{
\Gamma_{ij}^k=\Gamma_{ji}^k
}
$$

$$
\boxed{
\Gamma_{ij,\ell}
=
\frac12
\left(
\partial_i g_{j\ell}
+
\partial_j g_{i\ell}
-
\partial_\ell g_{ij}
\right)
}
$$

$$
\boxed{
\Gamma_{ij}^k
=
g^{k\ell}\Gamma_{ij,\ell}
}
$$

$$
\boxed{
\nabla_k g_{ij}=0
}
$$

$$
\boxed{
\Gamma_{ik}^k
=
\partial_i\log\sqrt{\det g}
}
$$

## Gauss–Weingarten

$$
\boxed{
\mathbf r_{ij}
=
\Gamma_{ij}^k\mathbf r_k+b_{ij}\mathbf n
}
$$

$$
\boxed{
\mathbf n_i
=
-g^{k\ell}b_{i\ell}\mathbf r_k
}
$$

## 第二基本形式和形算子

$$
\boxed{
b_{ij}=b_{ji}
}
$$

$$
\boxed{
b_{ij}
=
\langle\mathbf r_{ij},\mathbf n\rangle
=
-\langle\mathbf n_i,\mathbf r_j\rangle
}
$$

$$
\boxed{
A=g^{-1}b
}
$$

$$
\boxed{
A^Tg=gA
}
$$

## 曲率

$$
\boxed{
K=\det A=\frac{LN-M^2}{EG-F^2}
}
$$

$$
\boxed{
2H=\operatorname{tr}A=g^{ij}b_{ij}
}
$$

$$
\boxed{
A^2-2HA+KI=0
}
$$

$$
\boxed{
R_{1212}=LN-M^2=K(EG-F^2)
}
$$

---

# 38. 最容易失分的错误

## 38.1 把 \(D_XY\) 当作普通导数

错误：

$$
D_XY=X(Y^1)\mathbf r_u+X(Y^2)\mathbf r_v.
$$

漏掉切基变化。

正确：

$$
D_XY
=
X^i(\partial_iY^k+\Gamma_{ij}^kY^j)\mathbf r_k.
$$

## 38.2 把 \(b\) 当作形算子矩阵

错误：

$$
[S]=b.
$$

正确：

$$
\boxed{
[S]=g^{-1}b.
}
$$

只有 \(g=I\) 时二者才相同。

## 38.3 把坐标分量当成内积

若

$$
V=V^i\mathbf r_i,
$$

一般没有

$$
V^i=\langle V,\mathbf r_i\rangle.
$$

正确关系：

$$
\boxed{
\langle V,\mathbf r_i\rangle=g_{ij}V^j.
}
$$

## 38.4 把 \(g^{ij}\) 看成逐项倒数

$$
(g^{ij})=(g_{ij})^{-1},
$$

不能逐项取倒数。

## 38.5 认为 \(\Gamma\neq0\) 就有曲率

平面极坐标反例说明：

$$
\Gamma\neq0,\qquad K=0.
$$

## 38.6 忘记法向量方向影响符号

翻转 \(\mathbf n\) 后：

- \(L,M,N\) 变号；
- 主曲率、\(H\) 变号；
- \(K\) 不变。

## 38.7 曲率张量符号约定混用

不同教材对 \(R\) 的指标顺序和符号可能不同。考试必须使用教师或教材约定，并保证：

$$
R_{1212}=LN-M^2
$$

与所用定义一致。

---

# 39. 典型题型与答题模板

## 题型一：求 \(D_XY\)

已知

$$
X=X^1\mathbf r_u+X^2\mathbf r_v,
$$

$$
Y=Y^1\mathbf r_u+Y^2\mathbf r_v.
$$

步骤：

1. 求 \(Y^1_u,Y^1_v,Y^2_u,Y^2_v\)；
2. 求所需 \(\Gamma_{ij}^k\)；
3. 代入

$$
(D_XY)^k
=
X^i(\partial_iY^k+\Gamma_{ij}^kY^j);
$$

4. 写回

$$
D_XY=(D_XY)^1\mathbf r_u+(D_XY)^2\mathbf r_v.
$$

## 题型二：求二阶偏导分解

直接写

$$
\mathbf r_{ij}
=
\Gamma_{ij}^1\mathbf r_u
+
\Gamma_{ij}^2\mathbf r_v
+
b_{ij}\mathbf n.
$$

切向系数由 \(g^{-1}\) 解出，法向系数与 \(\mathbf n\) 做内积。

## 题型三：求 \(\mathbf n_u,\mathbf n_v\)

先算

$$
A=g^{-1}b.
$$

若

$$
A=
\begin{pmatrix}
a&c\\
b&d
\end{pmatrix},
$$

则

$$
S(\mathbf r_u)=a\mathbf r_u+b\mathbf r_v,
$$

$$
S(\mathbf r_v)=c\mathbf r_u+d\mathbf r_v.
$$

所以

$$
\mathbf n_u=-S(\mathbf r_u),
$$

$$
\mathbf n_v=-S(\mathbf r_v).
$$

## 题型四：求主曲率和主方向

解

$$
\det(b-\kappa g)=0.
$$

得到 \(\kappa\) 后解

$$
(b-\kappa g)\xi=0.
$$

最后将坐标向量 \(\xi=(a,b)^T\) 写回切向量

$$
a\mathbf r_u+b\mathbf r_v.
$$

## 题型五：验证 \(I,II\) 能否来自曲面

检查：

1. \(g\) 正定；
2. \(b\) 对称；
3. 由 \(g\) 求 \(\Gamma\)；
4. 检查 Gauss 方程；
5. 检查两条 Codazzi 方程。

## 题型六：由第一基本形式求 \(K\)

优先识别特殊形式：

- 等温：\(\lambda^2(du^2+dv^2)\)；
- \(du^2+f(u)^2dv^2\)；
- 一般形式再走 \(\Gamma\to R_{1212}\to K\)。

---

# 40. 必须背下来的核心链

## 第一条：协变导数

$$
\boxed{
D_XY
=
X^i
\left(
\partial_iY^k+\Gamma_{ij}^kY^j
\right)\mathbf r_k.
}
$$

## 第二条：Gauss 公式

$$
\boxed{
\mathbf r_{ij}
=
\Gamma_{ij}^k\mathbf r_k+b_{ij}\mathbf n.
}
$$

## 第三条：Christoffel 由度量决定

$$
\boxed{
\Gamma_{ij}^k
=
\frac12g^{k\ell}
\left(
\partial_i g_{j\ell}
+
\partial_j g_{i\ell}
-
\partial_\ell g_{ij}
\right).
}
$$

## 第四条：Weingarten 公式

$$
\boxed{
\mathbf n_i
=
-g^{k\ell}b_{i\ell}\mathbf r_k.
}
$$

## 第五条：形算子

$$
\boxed{
[S]=g^{-1}b.
}
$$

## 第六条：曲率

$$
\boxed{
K=\det(g^{-1}b)
=
\frac{LN-M^2}{EG-F^2},
}
$$

$$
\boxed{
2H=\operatorname{tr}(g^{-1}b).
}
$$

## 第七条：Gauss 方程

$$
\boxed{
R_{1212}=LN-M^2.
}
$$

## 第八条：Gauss 定理

$$
\boxed{
K=\frac{R_{1212}}{\det g},
}
$$

所以 \(K\) 完全由第一基本形式决定。

---

# 41. 最终总理解

把整章压缩成一句话：

> 曲面上的切基 \(\mathbf r_u,\mathbf r_v\) 会随着位置变化。它们在切平面内部的变化由 Christoffel 记号描述，向法线方向的变化由第二基本形式描述；法向量的变化由 Weingarten 映射描述。把这些变化装进自然标架运动公式，再要求混合偏导相容，就得到 Gauss–Codazzi 方程。形算子的特征值给出主曲率，而 Gauss 方程进一步证明 \(K\) 虽然可以从外在弯曲计算，却完全由内在度量决定。

最终逻辑图：

$$
\boxed{
\begin{array}{ccccc}
g
&\Longrightarrow&
\Gamma
&\Longrightarrow&
D\\[2mm]
&&\Downarrow&&\Downarrow\\[-1mm]
&&R&\Longrightarrow&K
\end{array}
}
$$

以及

$$
\boxed{
b
\Longrightarrow
S=g^{-1}b
\Longrightarrow
\kappa_1,\kappa_2
\Longrightarrow
H,K.
}
$$

两条路线通过

$$
\boxed{
R_{1212}=LN-M^2
}
$$

汇合，这正是本章最重要的结构。
