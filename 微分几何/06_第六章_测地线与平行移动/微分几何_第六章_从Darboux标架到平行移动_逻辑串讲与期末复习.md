---
title: 微分几何第六章：从 Darboux 标架到平行移动
subtitle: 陈维桓《微分几何》§6.1—§6.5｜逻辑串讲、公式推导与期末复习
tags:
  - 微分几何
  - 第六章
  - Darboux标架
  - 测地曲率
  - 测地挠率
  - 测地线
  - 测地坐标
  - 常曲率曲面
  - 平行移动
---

# 微分几何第六章：从 Darboux 标架到平行移动
## ——承接“协变导数—Gauss 定理”的逻辑串讲与期末复习

> **主要依据**：陈维桓《微分几何》第六章 §6.1—§6.5。  
> **范围说明**：保留 Darboux 标架、测地曲率与测地挠率、测地线、测地坐标的计算、常曲率曲面和平行移动。  
> **明确排除**：指数映射、法坐标系（泛坐标相关内容）以及用变分法证明测地线性质。  
> **记号约定**：曲面单位法向量统一记为 \(\mathbf n\)，形算子取
>
> $$
> S=-d\mathbf n.
> $$

---

# 0. 从第五章到第六章：到底多了什么

上一章已经建立了曲面内部的微分工具：

$$
\boxed{
\overline\nabla_XY
=
D_XY+\mathrm{II}(X,Y)\mathbf n
}
$$

其中：

- \(\overline\nabla_XY\)：在三维空间中观察 \(Y\) 的总变化；
- \(D_XY\)：总变化的切向部分，即曲面内部看到的变化；
- \(\mathrm{II}(X,Y)\mathbf n\)：总变化的法向部分，即曲面嵌入空间造成的弯曲。

第六章只是把这个公式限制到曲面上的一条曲线：

$$
\gamma(s)=\mathbf r(u(s),v(s)).
$$

沿曲线的单位切向量记为

$$
\boxed{
\mathbf T=\gamma'(s).
}
$$

令 \(X=Y=\mathbf T\)，上一章的统一式立刻变成

$$
\boxed{
\gamma''(s)
=
\overline\nabla_{\mathbf T}\mathbf T
=
D_{\mathbf T}\mathbf T
+
\mathrm{II}(\mathbf T,\mathbf T)\mathbf n.
}
$$

这就是第六章全部内容的起点。

因为

$$
\mathrm{II}(\mathbf T,\mathbf T)=\kappa_n,
$$

而

$$
D_{\mathbf T}\mathbf T
$$

是曲率向量在切平面内的部分，所以它的有向大小就是测地曲率 \(\kappa_g\)。于是：

$$
\boxed{
\text{空间曲率向量}
=
\text{测地曲率部分}
+
\text{法曲率部分}.
}
$$

---

# 1. 第六章总逻辑地图

本章可以压缩成四条互相连接的主线。

## 主线一：曲面上的一条曲线

$$
\boxed{
\gamma
\longrightarrow
\mathbf T
\longrightarrow
\{\mathbf T,\mathbf n\times\mathbf T,\mathbf n\}
\longrightarrow
\kappa_g,\kappa_n,\tau_g
}
$$

它回答：

> 一条空间曲线被限制在曲面上以后，它的弯曲中有多少来自曲面，有多少来自曲线在曲面内部转弯？

## 主线二：测地线

$$
\boxed{
\kappa_g=0
\Longleftrightarrow
D_{\mathbf T}\mathbf T=0
\Longleftrightarrow
u^{k\prime\prime}+\Gamma^k_{ij}u^{i\prime}u^{j\prime}=0
}
$$

它回答：

> 曲面上什么曲线在曲面内部看来“没有转弯”？

## 主线三：测地坐标与曲率

$$
\boxed{
I=du^2+G\,dv^2
\Longrightarrow
K=-\frac{(\sqrt G)_{uu}}{\sqrt G}
}
$$

令

$$
h=\sqrt G,
$$

则

$$
\boxed{
h_{uu}+Kh=0.}
$$

它回答：

> 选取沿测地线的坐标后，Gauss 曲率如何直接控制相邻测地线之间的距离变化？

## 主线四：平行移动

$$
\boxed{
\frac{DX}{ds}=0
}
$$

它回答：

> 一个切向量怎样沿曲线移动，才算在曲面内部没有发生转动？

四条主线的统一核心仍然是协变导数：

$$
\boxed{
D_{\mathbf T}\mathbf T
\text{ 描述曲线自身的内蕴转弯},
\qquad
\frac{DX}{ds}
\text{ 描述一般切向量场的内蕴变化}.
}
$$

---

# 2. 沿曲线的协变导数

设曲面参数为

$$
\mathbf r=\mathbf r(u^1,u^2),
$$

曲线写成

$$
\gamma(s)=\mathbf r(u^1(s),u^2(s)).
$$

曲线切向量为

$$
\mathbf T
=
\frac{d\gamma}{ds}
=
\frac{du^i}{ds}\mathbf r_i.
$$

沿曲线给定切向量场

$$
X(s)=X^k(s)\mathbf r_k.
$$

普通空间导数为

$$
\frac{dX}{ds}
=
\frac{dX^k}{ds}\mathbf r_k
+
X^k\frac{d\mathbf r_k}{ds}.
$$

又有

$$
\frac{d\mathbf r_k}{ds}
=
\frac{du^i}{ds}\mathbf r_{ik}.
$$

利用 Gauss 公式

$$
\mathbf r_{ik}
=
\Gamma^j_{ik}\mathbf r_j+b_{ik}\mathbf n,
$$

得到

$$
\frac{dX}{ds}
=
\left(
\frac{dX^j}{ds}
+
\Gamma^j_{ik}X^k\frac{du^i}{ds}
\right)\mathbf r_j
+
b_{ik}X^k\frac{du^i}{ds}\mathbf n.
$$

因此切向部分为

$$
\boxed{
\frac{DX}{ds}
=
\left(
\frac{dX^j}{ds}
+
\Gamma^j_{ik}X^k\frac{du^i}{ds}
\right)\mathbf r_j.
}
$$

法向部分为

$$
\boxed{
\mathrm{II}(\mathbf T,X)\mathbf n.
}
$$

所以沿曲线的 Gauss 公式是

$$
\boxed{
\frac{dX}{ds}
=
\frac{DX}{ds}
+
\mathrm{II}(\mathbf T,X)\mathbf n.
}
$$

## 一句话理解

普通导数会离开切平面；协变导数只保留曲面内部的变化。

---

# 3. 把 \(X\) 取成曲线切向量会发生什么

取

$$
X=\mathbf T
=
u^{k\prime}\mathbf r_k.
$$

则

$$
\boxed{
\frac{D\mathbf T}{ds}
=
\left(
\frac{d^2u^k}{ds^2}
+
\Gamma^k_{ij}
\frac{du^i}{ds}
\frac{du^j}{ds}
\right)\mathbf r_k.
}
$$

另一方面，空间加速度为

$$
\boxed{
\gamma''(s)
=
\frac{D\mathbf T}{ds}
+
\mathrm{II}(\mathbf T,\mathbf T)\mathbf n.
}
$$

由于曲线是单位速度，

$$
\langle\mathbf T,\mathbf T\rangle=1,
$$

求导得

$$
\langle\gamma'',\mathbf T\rangle=0.
$$

所以 \(\gamma''\) 位于垂直于 \(\mathbf T\) 的二维平面中。这个平面恰好由下面两个方向张成：

1. 曲面法向 \(\mathbf n\)；
2. 切平面中垂直于 \(\mathbf T\) 的方向 \(\mathbf n\times\mathbf T\)。

这就自然产生 Darboux 标架。

---

# 4. Darboux 标架是什么

设 \(\gamma(s)\) 是有向曲面上的单位速度曲线，定义

$$
\boxed{
\mathbf e_1=\mathbf T,
\qquad
\mathbf e_2=\mathbf n\times\mathbf T,
\qquad
\mathbf e_3=\mathbf n.
}
$$

则

$$
\boxed{
\{\mathbf e_1,\mathbf e_2,\mathbf e_3\}
}
$$

是沿曲线移动的单位正交标架，称为 **Darboux 标架**。

三个方向的几何意义：

| 向量 | 所在位置 | 几何意义 |
|---|---|---|
| \(\mathbf e_1=\mathbf T\) | 切平面内 | 曲线前进方向 |
| \(\mathbf e_2=\mathbf n\times\mathbf T\) | 切平面内 | 曲面内部垂直于曲线的方向 |
| \(\mathbf e_3=\mathbf n\) | 法方向 | 曲面单位法向 |

Darboux 标架不是只看曲线，也不是只看曲面，而是同时把二者放在一起：

$$
\boxed{
\text{Frenet 标架主要跟随曲线，}
\qquad
\text{Darboux 标架同时跟随曲线和曲面。}
}
$$

---

# 5. Darboux 标架运动公式

因为 \(\mathbf e_1\) 是单位向量，

$$
\mathbf e_1'\perp\mathbf e_1.
$$

所以只能写成

$$
\boxed{
\mathbf e_1'
=
\kappa_g\mathbf e_2
+
\kappa_n\mathbf e_3.
}
$$

其中：

- \(\kappa_g\)：测地曲率；
- \(\kappa_n\)：法曲率。

又因为

$$
\mathbf e_3=\mathbf n,
$$

由 Weingarten 公式

$$
\mathbf n'=-S(\mathbf T).
$$

把 \(S(\mathbf T)\) 在 \(\mathbf e_1,\mathbf e_2\) 下分解：

$$
S(\mathbf T)
=
\kappa_n\mathbf e_1
+
\tau_g\mathbf e_2.
$$

于是

$$
\boxed{
\mathbf e_3'
=
-\kappa_n\mathbf e_1
-\tau_g\mathbf e_2.
}
$$

最后利用正交关系或直接求导

$$
\mathbf e_2=\mathbf e_3\times\mathbf e_1,
$$

得到

$$
\boxed{
\mathbf e_2'
=
-\kappa_g\mathbf e_1
+
\tau_g\mathbf e_3.
}
$$

所以 Darboux 运动公式为

$$
\boxed{
\begin{aligned}
\mathbf e_1'
&=
\kappa_g\mathbf e_2+
\kappa_n\mathbf e_3,\\
\mathbf e_2'
&=
-\kappa_g\mathbf e_1+
\tau_g\mathbf e_3,\\
\mathbf e_3'
&=
-\kappa_n\mathbf e_1-
\tau_g\mathbf e_2.
\end{aligned}
}
$$

矩阵形式为

$$
\boxed{
\frac{d}{ds}
\begin{pmatrix}
\mathbf e_1&\mathbf e_2&\mathbf e_3
\end{pmatrix}
=
\begin{pmatrix}
\mathbf e_1&\mathbf e_2&\mathbf e_3
\end{pmatrix}
\begin{pmatrix}
0&-\kappa_g&-\kappa_n\\
\kappa_g&0&-\tau_g\\
\kappa_n&\tau_g&0
\end{pmatrix}.
}
$$

右侧系数矩阵是反对称矩阵，因为移动标架始终保持正交单位。

---

# 6. 三个曲率量分别表示什么

## 6.1 法曲率 \(\kappa_n\)

$$
\boxed{
\kappa_n
=
\langle\mathbf T',\mathbf n\rangle
=
\mathrm{II}(\mathbf T,\mathbf T)
=
\langle S(\mathbf T),\mathbf T\rangle.
}
$$

它表示：

> 曲线沿该切方向前进时，曲率向量朝曲面法向弯曲了多少。

它只依赖曲面和切方向，不依赖在该方向上具体选哪条曲线。

## 6.2 测地曲率 \(\kappa_g\)

$$
\boxed{
\kappa_g
=
\langle\mathbf T',\mathbf n\times\mathbf T\rangle.
}
$$

又因为

$$
\frac{D\mathbf T}{ds}
$$

是 \(\mathbf T'\) 的切向部分，所以

$$
\boxed{
\frac{D\mathbf T}{ds}
=
\kappa_g(\mathbf n\times\mathbf T).
}
$$

它表示：

> 曲线在曲面内部看来，向左或向右转弯了多少。

## 6.3 测地挠率 \(\tau_g\)

由定义

$$
\boxed{
\tau_g
=
\langle S(\mathbf T),\mathbf n\times\mathbf T\rangle
=
-\langle\mathbf n',\mathbf n\times\mathbf T\rangle.
}
$$

它表示：

> 沿曲线前进时，曲面法向量是否向曲线横向发生旋转。

因此：

- \(\kappa_n\) 看 \(S(\mathbf T)\) 沿 \(\mathbf T\) 的分量；
- \(\tau_g\) 看 \(S(\mathbf T)\) 沿 \(\mathbf n\times\mathbf T\) 的分量。

统一写成

$$
\boxed{
S(\mathbf T)
=
\kappa_n\mathbf T
+
\tau_g(\mathbf n\times\mathbf T).
}
$$

---

# 7. 空间曲率的正交分解

对单位速度曲线，空间曲率向量为

$$
\mathbf T'=\kappa\mathbf N.
$$

Darboux 公式给出

$$
\mathbf T'
=
\kappa_g\mathbf e_2+
\kappa_n\mathbf n.
$$

由于 \(\mathbf e_2\perp\mathbf n\)，两边取模平方：

$$
\boxed{
\kappa^2
=
\kappa_g^2+
\kappa_n^2.
}
$$

这不是三个标量直接相加，而是两个互相垂直的曲率分量做勾股分解。

因此：

$$
\boxed{
|\kappa_g|
=
\sqrt{\kappa^2-\kappa_n^2}.
}
$$

但这个公式只能直接给绝对值。若要求有向测地曲率，必须使用

$$
\boxed{
\kappa_g
=
\left\langle
\frac{d\mathbf T}{ds},
\mathbf n\times\mathbf T
\right\rangle.
}
$$

---

# 8. 非弧长参数下怎样计算测地曲率

若曲线用一般参数 \(t\) 表示：

$$
\gamma=\gamma(t),
$$

速度为

$$
q=\left\|\frac{d\gamma}{dt}\right\|,
\qquad
\frac{ds}{dt}=q.
$$

单位切向量

$$
\mathbf T
=
\frac{\gamma_t}{q}.
$$

于是

$$
\frac{d\mathbf T}{ds}
=
\frac1q\frac{d\mathbf T}{dt}.
$$

所以

$$
\boxed{
\kappa_g
=
\frac1q
\frac{d\mathbf T}{dt}
\cdot
(\mathbf n\times\mathbf T).
}
$$

还可以化成三重积形式：

$$
\boxed{
\kappa_g
=
\frac{
\det(\mathbf n,\gamma_t,\gamma_{tt})
}{\|\gamma_t\|^3}.
}
$$

此公式的符号依赖曲面定向和曲线定向。

## 最容易犯的错误

不是弧长参数时，不能直接写

$$
\kappa_g
=
\gamma_{tt}\cdot(\mathbf n\times\gamma_t).
$$

因为 \(\gamma_t\) 未必是单位向量。

---

# 9. 测地挠率与主方向

设一点处单位主方向为

$$
\mathbf p_1,\mathbf p_2,
$$

对应主曲率为

$$
\kappa_1,\kappa_2.
$$

若曲线切方向与第一主方向夹角为 \(\theta\)，则

$$
\mathbf T
=
\cos\theta\,\mathbf p_1
+
\sin\theta\,\mathbf p_2.
$$

与 \(\mathbf T\) 垂直的切向单位向量为

$$
\mathbf e_2
=
-\sin\theta\,\mathbf p_1
+
\cos\theta\,\mathbf p_2.
$$

由于

$$
S(\mathbf T)
=
\kappa_1\cos\theta\,\mathbf p_1
+
\kappa_2\sin\theta\,\mathbf p_2,
$$

所以

$$
\boxed{
\kappa_n
=
\kappa_1\cos^2\theta
+
\kappa_2\sin^2\theta.
}
$$

同时

$$
\boxed{
\tau_g
=
(\kappa_2-\kappa_1)
\sin\theta\cos\theta
=
\frac{\kappa_2-\kappa_1}{2}\sin2\theta.
}
$$

在非脐点 \(\kappa_1\ne\kappa_2\) 处，

$$
\boxed{
\tau_g=0
\iff
\theta=0\text{ 或 }\frac\pi2
\iff
\mathbf T\text{ 是主方向}.
}
$$

因此：

$$
\boxed{
\text{曲线是曲率线}
\iff
\tau_g\equiv0
}
$$

在非脐点区域成立。

若一点为脐点，\(S=\kappa I\)，所有方向都是主方向，所有方向的测地挠率都为零。

---

# 10. 测地挠率与法曲率变化率

Euler 公式为

$$
\kappa_n(\theta)
=
\kappa_1\cos^2\theta
+
\kappa_2\sin^2\theta.
$$

对 \(\theta\) 求导：

$$
\frac{d\kappa_n}{d\theta}
=
2(\kappa_2-\kappa_1)
\sin\theta\cos\theta.
$$

所以

$$
\boxed{
\tau_g
=
\frac12\frac{d\kappa_n}{d\theta}.
}
$$

这条公式说明：

> 测地挠率测量的是法曲率随方向变化的速度。

主方向恰好是法曲率取得极值的方向，所以在主方向上

$$
\tau_g=0.
$$

---

# 11. Frenet 标架与 Darboux 标架的区别

对空间曲线，Frenet 标架为

$$
\{\mathbf T,\mathbf N,\mathbf B\}.
$$

对曲面上的曲线，Darboux 标架为

$$
\{\mathbf T,\mathbf n\times\mathbf T,\mathbf n\}.
$$

两者共同使用 \(\mathbf T\)，但另外两个方向不同：

- \(\mathbf N\) 由曲线在空间中的弯曲决定；
- \(\mathbf n\) 由曲面决定；
- \(\mathbf n\times\mathbf T\) 是切平面内横向方向。

曲率向量分解

$$
\kappa\mathbf N
=
\kappa_g(\mathbf n\times\mathbf T)
+
\kappa_n\mathbf n
$$

就是两个标架之间最核心的联系。

## 特殊情况

### 曲线是测地线

$$
\kappa_g=0,
$$

所以

$$
\mathbf N\parallel\mathbf n.
$$

即曲线主法向与曲面法向平行。

### 曲线是渐近线

$$
\kappa_n=0,
$$

所以曲率向量完全位于切平面内：

$$
\mathbf N\parallel\mathbf n\times\mathbf T.
$$

### 曲线是曲率线

$$
\tau_g=0.
$$

此时曲面法向的变化只沿曲线切向方向。

三类曲线分别由三个量为零刻画：

$$
\boxed{
\begin{array}{c|c}
\text{曲线类型}&\text{判据}\\
\hline
\text{测地线}&\kappa_g=0\\
\text{渐近线}&\kappa_n=0\\
\text{曲率线}&\tau_g=0
\end{array}
}
$$

---

# 12. Liouville 公式：正交参数下怎样求测地曲率

设曲面采用正交参数：

$$
\boxed{
I=E\,du^2+G\,dv^2,
\qquad F=0.
}
$$

取正交单位切标架

$$
\mathbf a_1
=
\frac{\mathbf r_u}{\sqrt E},
\qquad
\mathbf a_2
=
\frac{\mathbf r_v}{\sqrt G}.
$$

设单位速度曲线切向量与正向 \(u\)-曲线的夹角为 \(\theta\)：

$$
\boxed{
\mathbf T
=
\cos\theta\,\mathbf a_1
+
\sin\theta\,\mathbf a_2.
}
$$

则 Liouville 公式为

$$
\boxed{
\kappa_g
=
\frac{d\theta}{ds}
-
\frac1{2\sqrt G}
\frac{\partial\log E}{\partial v}
\cos\theta
+
\frac1{2\sqrt E}
\frac{\partial\log G}{\partial u}
\sin\theta.
}
$$

这条公式由两部分组成：

$$
\boxed{
\kappa_g
=
\text{曲线相对参数标架的转角速度}
+
\text{参数标架自身的转动修正}.
}
$$

其中

$$
\frac{d\theta}{ds}
$$

描述曲线相对于局部正交标架的转动；其余两项来自曲面上的正交标架本身随位置发生转动。

---

# 13. Liouville 公式的两个最高频特例

## 13.1 \(u\)-参数曲线

\(v\) 为常数，切向沿 \(\mathbf a_1\)，所以

$$
\theta=0,
\qquad
\frac{d\theta}{ds}=0.
$$

因此

$$
\boxed{
\kappa_g^{(u)}
=
-\frac1{2\sqrt G}
\frac{\partial\log E}{\partial v}.
}
$$

所以

$$
\boxed{
\text{全部 }u\text{-曲线为测地线}
\iff
E_v=0.
}
$$

## 13.2 \(v\)-参数曲线

\(u\) 为常数，切向沿 \(\mathbf a_2\)，所以

$$
\theta=\frac\pi2.
$$

因此

$$
\boxed{
\kappa_g^{(v)}
=
\frac1{2\sqrt E}
\frac{\partial\log G}{\partial u}.
}
$$

所以

$$
\boxed{
\text{全部 }v\text{-曲线为测地线}
\iff
G_u=0.
}
$$

## 记忆方式

- \(u\)-曲线的长度系数是 \(E\)，检查它沿横向 \(v\) 是否变化；
- \(v\)-曲线的长度系数是 \(G\)，检查它沿横向 \(u\) 是否变化。

---

# 14. 什么是测地线

曲面上的单位速度曲线称为测地线，如果

$$
\boxed{
\kappa_g=0.
}
$$

因为

$$
\frac{D\mathbf T}{ds}
=
\kappa_g(\mathbf n\times\mathbf T),
$$

所以等价于

$$
\boxed{
\frac{D\mathbf T}{ds}=0.
}
$$

又由曲率向量分解

$$
\mathbf T'
=
\kappa_g(\mathbf n\times\mathbf T)
+
\kappa_n\mathbf n,
$$

可知测地线还等价于

$$
\boxed{
\mathbf T'
\parallel
\mathbf n.
}
$$

因此测地线有三种完全等价的理解：

$$
\boxed{
\begin{aligned}
\kappa_g&=0,\\
D_{\mathbf T}\mathbf T&=0,\\
\gamma''(s)&\perp T_pM.
\end{aligned}
}
$$

## 几何意义

测地线不是空间直线，而是：

> 在曲面内部看来不向左右转弯的曲线。

它在三维空间中可以弯曲，只是曲率向量完全来自曲面法向弯曲。

---

# 15. 弧长参数下的测地线方程

设

$$
\gamma(s)=\mathbf r(u^1(s),u^2(s)).
$$

切向量为

$$
\mathbf T
=
\frac{du^i}{ds}\mathbf r_i.
$$

沿曲线协变求导：

$$
\frac{D\mathbf T}{ds}
=
\left(
\frac{d^2u^k}{ds^2}
+
\Gamma^k_{ij}
\frac{du^i}{ds}
\frac{du^j}{ds}
\right)\mathbf r_k.
$$

测地线条件为

$$
\frac{D\mathbf T}{ds}=0.
$$

因为 \(\mathbf r_1,\mathbf r_2\) 线性无关，得到

$$
\boxed{
\frac{d^2u^k}{ds^2}
+
\Gamma^k_{ij}
\frac{du^i}{ds}
\frac{du^j}{ds}
=0,
\qquad k=1,2.
}
$$

二维展开为

$$
\boxed{
\begin{aligned}
u''
+
\Gamma^1_{11}u'^2
+2\Gamma^1_{12}u'v'
+
\Gamma^1_{22}v'^2
&=0,\\
v''
+
\Gamma^2_{11}u'^2
+2\Gamma^2_{12}u'v'
+
\Gamma^2_{22}v'^2
&=0.
\end{aligned}
}
$$

这说明：

$$
\boxed{
I
\longrightarrow
\Gamma
\longrightarrow
\text{测地线方程}.
}
$$

测地线完全由第一基本形式决定，是内蕴对象。

---

# 16. 一般参数下为什么右边会多一项

若曲线不是用弧长或仿射参数，而用一般参数 \(t\)，同一条测地线的坐标通常不满足右端为零的方程。

设

$$
\gamma(t)=\gamma(s(t)).
$$

则

$$
\frac{d\gamma}{dt}
=
\frac{ds}{dt}\mathbf T.
$$

沿曲线协变求导：

$$
\frac{D}{dt}rac{d\gamma}{dt}
=
\frac{d^2s}{dt^2}\mathbf T
+
\left(\frac{ds}{dt}\right)^2
\frac{D\mathbf T}{ds}.
$$

若曲线像是测地线，\(D\mathbf T/ds=0\)，则

$$
\frac{D\dot\gamma}{dt}
=
\frac{s''(t)}{s'(t)}\dot\gamma.
$$

所以一般参数下的曲线像为测地线，当且仅当存在函数 \(\lambda(t)\)，使

$$
\boxed{
\frac{D\dot\gamma}{dt}
=
\lambda(t)\dot\gamma.
}
$$

坐标形式为

$$
\boxed{
\frac{d^2u^k}{dt^2}
+
\Gamma^k_{ij}
\frac{du^i}{dt}
\frac{du^j}{dt}
=
\lambda(t)\frac{du^k}{dt}.
}
$$

## 为什么是“平行于切向量”而不是等于零

一般参数会改变速度大小，即产生切向加速度；但它不会改变曲线在曲面内部是否向左右转弯。

当参数是弧长或更一般的仿射参数时，\(\lambda=0\)。

---

# 17. 测地线的三个常用判定入口

## 入口一：直接算测地曲率

$$
\boxed{
\kappa_g=0.
}
$$

适合：已给出具体空间曲线和曲面法向量。

## 入口二：看曲率向量方向

$$
\boxed{
\gamma''(s)\parallel\mathbf n.
}
$$

适合：曲线已用弧长参数，空间加速度容易计算。

## 入口三：代入测地线方程

$$
\boxed{
u^{k\prime\prime}+\Gamma^k_{ij}u^{i\prime}u^{j\prime}=0.
}
$$

适合：题目只给第一基本形式或参数表达式。

## 做题原则

选择最短入口，不要每道题都从同一个定义硬算。

---

# 18. 典型曲面上的测地线

## 18.1 平面

直角坐标下

$$
I=du^2+dv^2,
$$

所有 Christoffel 记号为零，测地线方程为

$$
u''=0,
\qquad
v''=0.
$$

所以测地线是直线。

## 18.2 球面

单位球面上，测地线是大圆。

原因之一：大圆是球面与过球心平面的交线，其曲率向量始终指向球心，也就是球面法向方向，所以

$$
\kappa_g=0.
$$

小圆一般不是测地线。

## 18.3 圆柱面

把圆柱面沿母线展开成平面，测地线对应平面直线，所以圆柱面上的测地线包括：

- 母线；
- 水平圆周；
- 一般螺线。

它们统一对应展开平面中不同斜率的直线。

这也说明：

> 测地线由第一基本形式决定，局部等距映射会把测地线送到测地线。

---

# 19. 旋转面与 Clairaut 关系

若旋转面取子午线弧长参数 \(u\)，旋转角为 \(v\)，第一基本形式为

$$
\boxed{
I=du^2+\rho(u)^2dv^2,
}
$$

其中 \(\rho(u)\) 是点到旋转轴的距离。

设单位速度测地线与子午线方向的夹角为 \(\theta\)。则

$$
\mathbf T
=
\cos\theta\,\mathbf a_1
+
\sin\theta\,\mathbf a_2.
$$

由于

$$
\mathbf a_2
=
\frac1\rho\mathbf r_v,
$$

有

$$
\sin\theta
=
\rho v'.
$$

测地线方程的第二式可写成

$$
\frac{d}{ds}(\rho^2v')=0.
$$

所以

$$
\rho^2v'=C.
$$

利用 \(\sin\theta=\rho v'\)，得到 Clairaut 关系：

$$
\boxed{
\rho\sin\theta=C.
}
$$

## 几何解释

测地线靠近旋转轴时 \(\rho\) 变小，因此 \(|\sin\theta|\) 必须变大，曲线会更加接近纬线方向。

若 \(|C|>\rho(u)\)，则该区域无法到达，因为 \(|\sin\theta|\le1\)。

## 角度约定提醒

这里 \(\theta\) 是测地线与子午线方向的夹角。若题目把角度定义为与纬线方向的夹角，正弦会变成余弦。

---

# 20. 测地线的局部存在唯一性

测地线方程是二阶常微分方程组：

$$
\frac{d^2u^k}{ds^2}
=
-
\Gamma^k_{ij}(u)
\frac{du^i}{ds}
\frac{du^j}{ds}.
$$

若 Christoffel 记号足够光滑，则给定初始条件

$$
\boxed{
\gamma(0)=p,
\qquad
\gamma'(0)=V\in T_pM,
}
$$

局部存在唯一测地线。

这意味着：

> 给定一点和一个初始切方向，局部只有一条沿该方向出发的测地线。

本范围内只需要把它理解为常微分方程的局部存在唯一性，不使用指数映射重新表述。

---

# 21. 测地坐标的基本形式

本范围保留测地坐标的计算，不讨论通过指数映射或法坐标构造它。

若参数曲线 \(v=\text{常数}\) 是单位速度测地线，并且与另一族参数线正交，则第一基本形式具有形式

$$
\boxed{
I=du^2+G(u,v)\,dv^2.
}
$$

令

$$
\boxed{
h(u,v)=\sqrt{G(u,v)}.}
$$

则

$$
\boxed{
I=du^2+h(u,v)^2dv^2.
}
$$

这里：

- \(u\) 沿每条测地线测量弧长；
- \(h\,dv\) 描述相邻测地线之间的横向距离。

所以 \(h\) 的变化反映测地线束是会聚还是发散。

---

# 22. 测地坐标下的 Christoffel 记号

对

$$
I=du^2+h^2dv^2,
$$

有

$$
E=1,
\qquad
F=0,
\qquad
G=h^2.
$$

逆度量为

$$
(g^{ij})
=
\begin{pmatrix}
1&0\\
0&h^{-2}
\end{pmatrix}.
$$

非零 Christoffel 记号为

$$
\boxed{
\Gamma^1_{22}
=-hh_u,
}
$$

$$
\boxed{
\Gamma^2_{12}
=
\Gamma^2_{21}
=
\frac{h_u}{h},
}
$$

$$
\boxed{
\Gamma^2_{22}
=
\frac{h_v}{h}.
}
$$

其余为零：

$$
\Gamma^1_{11}
=
\Gamma^1_{12}
=
\Gamma^2_{11}
=0.
$$

特别地，\(v=\) 常数时

$$
v'=0,
\qquad
u'=1,
$$

测地线方程自动成立，所以 \(u\)-曲线确实是单位速度测地线。

---

# 23. 测地坐标下直接求 Gauss 曲率

对

$$
I=du^2+h(u,v)^2dv^2,
$$

代入曲率张量或正交参数曲率公式，可以得到

$$
\boxed{
K
=
-\frac{h_{uu}}{h}.
}
$$

因为

$$
h=\sqrt G,
$$

也可写成

$$
\boxed{
K
=
-\frac{(\sqrt G)_{uu}}{\sqrt G}.
}
$$

这是第六章最重要的内蕴计算公式之一。

## 为什么公式里没有 \(v\) 的二阶导数

\(u\) 已被选成沿测地线的弧长参数，度量在这个方向上被标准化为 \(1\)。Gauss 曲率控制的是横向尺度 \(h\) 沿测地线方向的二阶变化。

因此：

$$
\boxed{
K>0
\Rightarrow
h_{uu}<0,
}
$$

相邻测地线倾向于会聚；

$$
\boxed{
K<0
\Rightarrow
h_{uu}>0,
}
$$

相邻测地线倾向于更快发散。

---

# 24. 曲率方程 \(h_{uu}+Kh=0\)

由

$$
K=-\frac{h_{uu}}h,
$$

直接得到

$$
\boxed{
h_{uu}+Kh=0.}
$$

这条方程把几何问题转化为一维二阶微分方程：

$$
\boxed{
\text{Gauss 曲率}
\longleftrightarrow
\text{相邻测地线横向间距的二阶变化}.
}
$$

如果 \(K\) 是常数，则对每个固定 \(v\)，\(h\) 关于 \(u\) 满足常系数方程。

---

# 25. 常正曲率、零曲率、常负曲率的三种解

设常数曲率为 \(K\)。

## 25.1 \(K=c^2>0\)

$$
h_{uu}+c^2h=0.
$$

一般解：

$$
\boxed{
h(u,v)
=
A(v)\cos(cu)
+
B(v)\sin(cu).
}
$$

表现为振荡型，相邻测地线可能重新会聚。

## 25.2 \(K=0\)

$$
h_{uu}=0.
$$

一般解：

$$
\boxed{
h(u,v)=A(v)+B(v)u.}
$$

表现为线性变化。

## 25.3 \(K=-c^2<0\)

$$
h_{uu}-c^2h=0.
$$

一般解：

$$
\boxed{
h(u,v)
=
A(v)\cosh(cu)
+
B(v)\sinh(cu).
}
$$

表现为双曲型，相邻测地线通常迅速发散。

---

# 26. 两类常见初始条件必须区分

## 26.1 极型初始条件

若许多测地线从同一点出发，常见条件是

$$
\boxed{
h(0,v)=0,
\qquad
h_u(0,v)=1.}
$$

则

$$
\boxed{
 h(u)=
 \begin{cases}
 \dfrac{\sin(cu)}{c},&K=c^2>0,\\[2mm]
 u,&K=0,\\[1mm]
 \dfrac{\sinh(cu)}{c},&K=-c^2<0.
 \end{cases}
}
$$

## 26.2 平行型初始条件

若初始横向尺度归一化，并且初始时横向尺度变化率为零，常见条件是

$$
\boxed{
h(0,v)=1,
\qquad
h_u(0,v)=0.}
$$

则

$$
\boxed{
 h(u)=
 \begin{cases}
 \cos(cu),&K=c^2>0,\\
 1,&K=0,\\
 \cosh(cu),&K=-c^2<0.
 \end{cases}
}
$$

这两组不能混用：

- 极型是 \(\sin,u,\sinh\)；
- 平行型是 \(\cos,1,\cosh\)。

---

# 27. 三种标准常曲率度量

使用极型初始条件，可以得到三种标准形式。

## 正曲率 \(K=c^2\)

$$
\boxed{
I
=
du^2+
\frac{\sin^2(cu)}{c^2}dv^2.
}
$$

对应半径 \(1/c\) 的球面局部度量。

## 零曲率 \(K=0\)

$$
\boxed{
I=du^2+u^2dv^2.
}
$$

对应平面的极坐标度量。

## 负曲率 \(K=-c^2\)

$$
\boxed{
I
=
du^2+
\frac{\sinh^2(cu)}{c^2}dv^2.
}
$$

对应双曲平面的极型度量。

这三个公式统一为

$$
I=du^2+S_K(u)^2dv^2,
$$

其中 \(S_K\) 分别是正弦型、线性型和双曲正弦型函数。

---

# 28. 测地坐标公式怎样做题

看到

$$
I=du^2+G(u,v)dv^2
$$

时，形成以下条件反射：

## 第一步

设

$$
\boxed{h=\sqrt G.}
$$

## 第二步

直接写

$$
\boxed{K=-\dfrac{h_{uu}}h.}
$$

## 第三步

若 \(K\) 已知，改写为

$$
\boxed{h_{uu}+Kh=0.}
$$

## 第四步

根据初始条件决定使用：

- \(\sin/u/\sinh\) 型；
- \(\cos/1/\cosh\) 型；
- 或一般的 \(A(v),B(v)\) 形式。

## 例

若

$$
I=du^2+\cosh^2u\,dv^2,
$$

则

$$
h=\cosh u,
\qquad
h_{uu}=\cosh u.
$$

所以

$$
\boxed{K=-1.}
$$

---

# 29. 沿曲线的平行移动

设 \(\gamma(s)\) 是曲面上的曲线，\(X(s)\) 是沿曲线的切向量场。

若

$$
\boxed{
\frac{DX}{ds}=0,
}
$$

则称 \(X\) 沿 \(\gamma\) 平行移动。

这不是说 \(X\) 在三维空间中不变，而是说：

> 从曲面内部的 Levi-Civita 联络来看，\(X\) 没有发生变化。

普通导数仍可能有法向分量：

$$
\frac{dX}{ds}
=
\mathrm{II}(\mathbf T,X)\mathbf n.
$$

所以平行移动的向量可以在空间中转动，只是它的转动完全由曲面嵌入造成，没有切平面内的额外旋转。

---

# 30. 平行移动方程

设

$$
X=X^k\mathbf r_k,
$$

曲线坐标为

$$
u^i=u^i(s).
$$

沿曲线协变导数为

$$
\frac{DX}{ds}
=
\left(
\frac{dX^k}{ds}
+
\Gamma^k_{ij}X^j\frac{du^i}{ds}
\right)\mathbf r_k.
$$

因此平行移动满足一阶线性方程组

$$
\boxed{
\frac{dX^k}{ds}
+
\Gamma^k_{ij}X^j\frac{du^i}{ds}
=0,
\qquad k=1,2.
}
$$

二维展开为

$$
\boxed{
\begin{aligned}
(X^1)'
&+
\Gamma^1_{11}X^1u'
+
\Gamma^1_{12}X^2u'
+
\Gamma^1_{21}X^1v'
+
\Gamma^1_{22}X^2v'
=0,\\
(X^2)'
&+
\Gamma^2_{11}X^1u'
+
\Gamma^2_{12}X^2u'
+
\Gamma^2_{21}X^1v'
+
\Gamma^2_{22}X^2v'
=0.
\end{aligned}
}
$$

更紧凑地写为

$$
\boxed{
X^{k\prime}
+
\Gamma^k_{ij}u^{i\prime}X^j
=0.
}
$$

---

# 31. 为什么平行移动不等于“分量不变”

错误理解：

$$
X^1,X^2\text{ 为常数}
\quad\Longrightarrow\quad
X\text{ 平行}.
$$

这一般不成立，因为切基

$$
\mathbf r_1,
\mathbf r_2
$$

本身会随位置变化。

真正的平行条件是：

$$
\boxed{
X^{k\prime}
+
\Gamma^k_{ij}u^{i\prime}X^j
=0.
}
$$

其中：

- \(X^{k\prime}\) 是坐标分量变化；
- \(\Gamma^k_{ij}u^{i\prime}X^j\) 是移动基底带来的修正。

只有在特殊坐标或特殊曲线上，平行移动才可能表现为坐标分量恒定。

---

# 32. 平行移动保持长度和夹角

若 \(X,Y\) 都沿 \(\gamma\) 平行，则

$$
\frac{DX}{ds}=0,
\qquad
\frac{DY}{ds}=0.
$$

利用度量相容性：

$$
\frac{d}{ds}\langle X,Y\rangle
=
\left\langle\frac{DX}{ds},Y\right\rangle
+
\left\langle X,\frac{DY}{ds}\right\rangle.
$$

所以

$$
\boxed{
\frac{d}{ds}\langle X,Y\rangle=0.
}
$$

特别地，取 \(Y=X\)：

$$
\boxed{
\frac{d}{ds}\|X\|^2=0.
}
$$

因此平行移动保持：

- 向量长度；
- 两向量夹角；
- 正交性；
- 单位性。

这也是 Levi-Civita 联络“与度量相容”的直接几何表现。

---

# 33. 测地线与平行移动是同一个框架

测地线的单位切向量 \(\mathbf T\) 满足

$$
\boxed{
\frac{D\mathbf T}{ds}=0.
}
$$

所以：

$$
\boxed{
\gamma\text{ 是测地线}
\iff
\mathbf T\text{ 沿 }\gamma\text{ 平行移动}.
}
$$

这说明测地线不是一个孤立定义，而是平行移动的特殊情形：

> 一条曲线是测地线，当且仅当它自己的切向量沿自己平行。

坐标上，把

$$
X^k=u^{k\prime}
$$

代入平行移动方程，就得到测地线方程：

$$
\boxed{
u^{k\prime\prime}+\Gamma^k_{ij}u^{i\prime}u^{j\prime}=0.}
$$

---

# 34. 用正交单位标架理解平行移动

设曲面上选定局部正交单位标架

$$
\mathbf a_1,
\mathbf a_2.
$$

任意单位切向量可写成

$$
X
=
\cos\varphi\,\mathbf a_1
+
\sin\varphi\,\mathbf a_2.
$$

即使 \(\varphi\) 不变，\(X\) 也可能变化，因为标架 \(\mathbf a_1,\mathbf a_2\) 本身在转动。

设标架沿曲线的内蕴转动速度为 \(\omega(\mathbf T)\)，则

$$
\boxed{
\frac{DX}{ds}=0
\iff
\varphi'+\omega(\mathbf T)=0.
}
$$

即：

> 向量相对标架的转角速度，必须恰好抵消标架自身的转动速度。

同理，若曲线切向量

$$
\mathbf T
=
\cos\theta\,\mathbf a_1
+
\sin\theta\,\mathbf a_2,
$$

则

$$
\boxed{
\kappa_g
=
\theta'+\omega(\mathbf T).
}
$$

所以

$$
\kappa_g=0
$$

正是切向量相对转动抵消标架转动，也就是 \(\mathbf T\) 平行。

Liouville 公式就是把 \(\omega(\mathbf T)\) 用 \(E,G\) 写出来。

---

# 35. 第六章的统一矩阵视角

沿曲线取 Darboux 标架

$$
\mathcal E
=
\begin{pmatrix}
|&|&|\\
\mathbf e_1&\mathbf e_2&\mathbf e_3\\
|&|&|
\end{pmatrix}.
$$

运动公式可写成

$$
\boxed{
\mathcal E'
=
\mathcal E\Omega,
}
$$

其中

$$
\Omega
=
\begin{pmatrix}
0&-\kappa_g&-\kappa_n\\
\kappa_g&0&-\tau_g\\
\kappa_n&\tau_g&0
\end{pmatrix}.
$$

三个系数分别控制三个二维平面内的旋转：

| 系数 | 控制的旋转平面 | 几何内容 |
|---|---|---|
| \(\kappa_g\) | \(\mathbf e_1\mathbf e_2\) 平面 | 曲线在曲面内转弯 |
| \(\kappa_n\) | \(\mathbf e_1\mathbf e_3\) 平面 | 曲线沿曲面法向弯曲 |
| \(\tau_g\) | \(\mathbf e_2\mathbf e_3\) 平面 | 曲面法向横向扭转 |

这与上一章自然标架运动公式完全同构：

- 上一章沿 \(u,v\) 两个方向研究曲面标架变化；
- 本章沿一条曲线方向研究 Darboux 标架变化。

本质都是：

$$
\boxed{
\text{移动标架的导数}
=
\text{标架本身}
\times
\text{连接系数矩阵}.
}
$$

---

# 36. 四个量的层级关系

本章容易混淆 \(\kappa,\kappa_n,\kappa_g,\tau_g\)。可以按下面层级区分。

## 空间曲线层

$$
\kappa
$$

表示曲线作为 \(\mathbb R^3\) 中空间曲线的总弯曲。

## 曲面与方向层

$$
\kappa_n
$$

表示曲面在切方向 \(\mathbf T\) 上的法向弯曲，只依赖曲面和方向。

## 曲线在曲面内部层

$$
\kappa_g
$$

表示该具体曲线在曲面内部的转弯。

## 曲面法向沿曲线变化层

$$
\tau_g
$$

表示曲面法向沿曲线横向旋转的程度，反映该方向是否为主方向。

关系为

$$
\boxed{
\kappa^2=\kappa_n^2+\kappa_g^2,
}
$$

而 \(\tau_g\) 不参与这个勾股分解，因为它描述的是法向标架的扭转，而不是曲率向量的分量。

---

# 37. 综合题标准流程一：给曲面和具体曲线

题目给：

- 参数曲面或隐式曲面；
- 曲面上的曲线；
- 求 \(\kappa_n,\kappa_g,\tau_g\) 或判断曲线类型。

## 第一步：求曲线单位切向量

若不是弧长参数：

$$
\boxed{
\mathbf T
=
\frac{\gamma_t}{\|\gamma_t\|}.
}
$$

## 第二步：求曲面单位法向量

$$
\boxed{
\mathbf n
=
\frac{\mathbf r_u\times\mathbf r_v}
{\|\mathbf r_u\times\mathbf r_v\|}
}
$$

或隐式曲面使用

$$
\mathbf n
=
\frac{\nabla F}{\|\nabla F\|}.
$$

## 第三步：构造横向切向量

$$
\boxed{
\mathbf e_2
=
\mathbf n\times\mathbf T.
}
$$

## 第四步：求曲率向量

$$
\frac{d\mathbf T}{ds}.
$$

## 第五步：投影

$$
\boxed{
\kappa_g
=
\frac{d\mathbf T}{ds}\cdot\mathbf e_2,
}
$$

$$
\boxed{
\kappa_n
=
\frac{d\mathbf T}{ds}\cdot\mathbf n.
}
$$

## 第六步：测地挠率

可用

$$
\boxed{
\tau_g
=
-\mathbf n'\cdot\mathbf e_2
}
$$

或通过形算子

$$
\boxed{
\tau_g
=
\langle S(\mathbf T),\mathbf e_2\rangle.
}
$$

## 第七步：判断

$$
\kappa_g=0
\Rightarrow
\text{测地线},
$$

$$
\kappa_n=0
\Rightarrow
\text{渐近线},
$$

$$
\tau_g=0
\Rightarrow
\text{曲率线}.
$$

---

# 38. 综合题标准流程二：只给第一基本形式

题目给

$$
I=E\,du^2+2F\,du\,dv+G\,dv^2
$$

并要求测地线或平行移动。

## 第一步：写度量矩阵

$$
\boxed{
g=
\begin{pmatrix}
E&F\\
F&G
\end{pmatrix}.
}
$$

## 第二步：求逆矩阵

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

## 第三步：求 Christoffel 记号

$$
\boxed{
\Gamma^k_{ij}
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

## 第四步：根据题目写方程

### 测地线

$$
\boxed{
u^{k\prime\prime}+\Gamma^k_{ij}u^{i\prime}u^{j\prime}=0.}
$$

### 平行移动

$$
\boxed{X^{k\prime}+\Gamma^k_{ij}u^{i\prime}X^j=0.}
$$

## 第五步：寻找结构

检查：

- 是否正交参数；
- 是否存在循环坐标；
- 是否是旋转面；
- 是否能形成全导数；
- 是否可直接使用 Clairaut 第一积分。

---

# 39. 综合题标准流程三：看到测地坐标

看到

$$
I=du^2+G(u,v)dv^2
$$

直接执行：

$$
\boxed{
G
\longrightarrow
h=\sqrt G
\longrightarrow
K=-\frac{h_{uu}}h.
}
$$

若 \(K\) 为常数：

$$
\boxed{
h_{uu}+Kh=0.}
$$

若还要求参数线：

- \(u\)-曲线自动是单位速度测地线；
- \(v\)-曲线为测地线当且仅当
  $$
  h_u=0
  $$
  或等价地
  $$
  G_u=0.
  $$

若是旋转面形式

$$
I=du^2+\rho(u)^2dv^2,
$$

还可立即写：

$$
\boxed{K=-\frac{\rho''}{\rho}}
$$

以及 Clairaut 关系

$$
\boxed{\rho\sin\theta=C.}
$$

---

# 40. 期末证明题的常用起点

## 40.1 证明曲率分解

从

$$
\mathbf T'
=
\kappa_g\mathbf e_2+
\kappa_n\mathbf n
$$

出发，利用两方向正交。

## 40.2 证明测地线等价条件

从

$$
\frac{D\mathbf T}{ds}
=
\kappa_g(\mathbf n\times\mathbf T)
$$

出发。

## 40.3 证明曲率线与测地挠率

从

$$
S(\mathbf T)
=
\kappa_n\mathbf T+
\tau_g(\mathbf n\times\mathbf T)
$$

出发。

若 \(\tau_g=0\)，则 \(S(\mathbf T)\parallel\mathbf T\)，所以 \(\mathbf T\) 是特征方向。

## 40.4 证明平行移动保持内积

从度量相容性

$$
\frac{d}{ds}\langle X,Y\rangle
=
\left\langle\frac{DX}{ds},Y\right\rangle
+
\left\langle X,\frac{DY}{ds}\right\rangle
$$

出发。

## 40.5 由测地坐标求曲率

先求少数非零 Christoffel 记号，再代入

$$
K=\frac{R_{1212}}{\det g},
$$

最终化为

$$
K=-\frac{h_{uu}}h.
$$

---

# 41. 高频例题一：单位球面纬线

单位球面上固定余纬 \(\varphi\) 的纬线为

$$
\gamma(t)
=
(\sin\varphi\cos t,
\sin\varphi\sin t,
\cos\varphi).
$$

它是半径 \(\sin\varphi\) 的空间圆，所以空间曲率

$$
\kappa
=
\frac1{\sin\varphi}.
$$

单位球面的法曲率绝对值为 \(1\)，故

$$
|\kappa_n|=1.
$$

因此

$$
|\kappa_g|
=
\sqrt{
\frac1{\sin^2\varphi}-1
}
=
|\cot\varphi|.
$$

所以

$$
\boxed{|\kappa_g|=|\cot\varphi|.}
$$

当

$$
\varphi=\frac\pi2
$$

时是大圆，\(\kappa_g=0\)，因此大圆是测地线。

---

# 42. 高频例题二：正交参数曲线判定

设

$$
I=du^2+e^{2u}dv^2.
$$

有

$$
E=1,
\qquad
G=e^{2u}.
$$

## \(u\)-曲线

因为

$$
E_v=0,
$$

所以全部 \(u\)-曲线都是测地线。

## \(v\)-曲线

测地曲率为

$$
\kappa_g^{(v)}
=
\frac1{2\sqrt E}
\frac{\partial\log G}{\partial u}
=
\frac12\cdot2
=1.
$$

所以 \(v\)-曲线不是测地线。

同时令

$$
h=e^u,
$$

则

$$
K=-\frac{h_{uu}}h=-1.
$$

一题中连续得到：

$$
\boxed{
\text{参数线判定}
\longrightarrow
\text{测地曲率}
\longrightarrow
\text{Gauss 曲率}.
}
$$

---

# 43. 高频例题三：圆柱面上的测地线

圆柱面参数为

$$
\mathbf r(u,v)
=
(R\cos v,R\sin v,u).
$$

第一基本形式为

$$
I=du^2+R^2dv^2.
$$

系数均为常数，所以所有 Christoffel 记号为零。

测地线方程：

$$
u''=0,
\qquad
v''=0.
$$

故

$$
u=as+b,
\qquad
v=cs+d.
$$

代回空间参数：

$$
\gamma(s)
=
(R\cos(cs+d),
R\sin(cs+d),
as+b).
$$

因此测地线是一般螺线，特殊情形包括：

- \(c=0\)：母线；
- \(a=0\)：水平圆；
- \(ac\ne0\)：普通螺线。

---

# 44. 高频例题四：常曲率反求度量

设

$$
I=du^2+G(u)dv^2
$$

且

$$
K=4.
$$

令

$$
h=\sqrt G.
$$

则

$$
h''+4h=0.
$$

所以

$$
h=A\cos2u+B\sin2u.
$$

因此在 \(h>0\) 的局部区域内

$$
\boxed{
G(u)
=
\bigl(A\cos2u+B\sin2u\bigr)^2.
}
$$

若再给极型初始条件

$$
h(0)=0,
\qquad
h'(0)=1,
$$

则

$$
h=\frac12\sin2u,
$$

从而

$$
\boxed{
I=du^2+rac14\sin^2(2u)dv^2.
}
$$

---

# 45. 高频例题五：平面极坐标中的平行移动

平面极坐标度量为

$$
I=d\rho^2+\rho^2d\theta^2.
$$

非零 Christoffel 记号为

$$
\Gamma^\rho_{\theta\theta}=-\rho,
\qquad
\Gamma^\theta_{\rho\theta}
=
\Gamma^\theta_{\theta\rho}
=
\frac1\rho.
$$

沿圆周

$$
\rho=R,
\qquad
\theta=t,
$$

设

$$
X=X^\rho\mathbf r_\rho+X^\theta\mathbf r_\theta.
$$

平行移动方程为

$$
\boxed{
\begin{aligned}
\frac{dX^\rho}{dt}-R X^\theta&=0,\\
\frac{dX^\theta}{dt}+\frac1R X^\rho&=0.
\end{aligned}
}
$$

坐标分量并非常数，但对应的几何向量在平面中保持固定方向。

这个例子清楚说明：

$$
\boxed{
\Gamma\ne0
\text{ 可能只是坐标基变化，}
\qquad
K=0
\text{ 仍然可以成立。}
}
$$

---

# 46. 最容易失分的十个错误

## 错误 1：把测地线理解成空间直线

正确条件是

$$
\kappa_g=0,
$$

不是

$$
\kappa=0.
$$

## 错误 2：把曲率分解写成普通加法

错误：

$$
\kappa=\kappa_g+\kappa_n.
$$

正确：

$$
\kappa^2=\kappa_g^2+\kappa_n^2.
$$

## 错误 3：非弧长参数直接用单位速度公式

必须先求

$$
\mathbf T=\frac{\gamma_t}{\|\gamma_t\|}.
$$

## 错误 4：混淆三种特殊曲线

$$
\kappa_g=0\Rightarrow\text{测地线},
$$

$$
\kappa_n=0\Rightarrow\text{渐近线},
$$

$$
\tau_g=0\Rightarrow\text{曲率线}.
$$

## 错误 5：把 \(\tau_g=0\) 无条件写成唯一主方向

在脐点所有方向都满足 \(\tau_g=0\)。

## 错误 6：把正交参数曲线条件记反

$$
u\text{-曲线检查 }E_v,
\qquad
v\text{-曲线检查 }G_u.
$$

## 错误 7：测地线方程漏掉交叉项系数 \(2\)

$$
2\Gamma^k_{12}u'v'.
$$

## 错误 8：一般参数仍强行令方程右端为零

曲线像为测地线时，一般参数满足

$$
u^{k\prime\prime}+\Gamma^k_{ij}u^{i\prime}u^{j\prime}
=\lambda u^{k\prime}.
$$

## 错误 9：平行移动要求坐标分量恒定

正确条件是

$$
X^{k\prime}+\Gamma^k_{ij}u^{i\prime}X^j=0.
$$

## 错误 10：常曲率初始条件混淆

- 极型：\(\sin,u,\sinh\)；
- 平行型：\(\cos,1,\cosh\)。

---

# 47. 第六章核心公式表

## 沿曲线协变导数

$$
\boxed{
\frac{DX}{ds}
=
\left(
\frac{dX^k}{ds}
+
\Gamma^k_{ij}X^j\frac{du^i}{ds}
\right)\mathbf r_k.
}
$$

## 沿曲线 Gauss 公式

$$
\boxed{
\frac{dX}{ds}
=
\frac{DX}{ds}
+
\mathrm{II}(\mathbf T,X)\mathbf n.
}
$$

## Darboux 运动公式

$$
\boxed{
\begin{aligned}
\mathbf T'
&=
\kappa_g(\mathbf n\times\mathbf T)+\kappa_n\mathbf n,\\
(\mathbf n\times\mathbf T)'
&=
-\kappa_g\mathbf T+\tau_g\mathbf n,\\
\mathbf n'
&=
-\kappa_n\mathbf T-\tau_g(\mathbf n\times\mathbf T).
\end{aligned}
}
$$

## 法曲率

$$
\boxed{
\kappa_n
=
\mathrm{II}(\mathbf T,\mathbf T)
=
\langle S(\mathbf T),\mathbf T\rangle.
}
$$

## 测地曲率

$$
\boxed{
\kappa_g
=
\left\langle
\frac{d\mathbf T}{ds},
\mathbf n\times\mathbf T
\right\rangle.
}
$$

## 测地挠率

$$
\boxed{
\tau_g
=
\langle S(\mathbf T),\mathbf n\times\mathbf T\rangle.
}
$$

## 曲率分解

$$
\boxed{
\kappa^2=\kappa_g^2+\kappa_n^2.
}
$$

## 主方向判定

$$
\boxed{
\tau_g=0
\iff
\mathbf T\text{ 为主方向}
}
$$

在非脐点处成立。

## Liouville 公式

$$
\boxed{
\kappa_g
=
\frac{d\theta}{ds}
-
\frac1{2\sqrt G}
\frac{\partial\log E}{\partial v}\cos\theta
+
\frac1{2\sqrt E}
\frac{\partial\log G}{\partial u}\sin\theta.
}
$$

## 测地线方程

$$
\boxed{
\frac{d^2u^k}{ds^2}
+
\Gamma^k_{ij}
\frac{du^i}{ds}
\frac{du^j}{ds}
=0.
}
$$

## Clairaut 关系

$$
\boxed{
\rho\sin\theta=C.
}
$$

## 测地坐标曲率公式

$$
\boxed{
I=du^2+h^2dv^2
\Longrightarrow
K=-\frac{h_{uu}}h.
}
$$

## 常曲率方程

$$
\boxed{
h_{uu}+Kh=0.}
$$

## 平行移动方程

$$
\boxed{
X^{k\prime}
+
\Gamma^k_{ij}u^{i\prime}X^j
=0.
}
$$

---

# 48. 必须形成的五条条件反射

## 看到“曲面上的具体曲线，求测地曲率”

$$
\boxed{
\gamma
\to
\mathbf T
\to
\frac{d\mathbf T}{ds}
\to
\mathbf n\times\mathbf T
\to
\kappa_g.
}
$$

## 看到“判断是否为测地线”

优先选最短方法：

$$
\boxed{
\kappa_g=0
\quad\text{或}\quad
\frac{D\mathbf T}{ds}=0
\quad\text{或}\quad
\text{代入测地线方程}.
}
$$

## 看到“只给第一基本形式”

$$
\boxed{
I
\to
\Gamma
\to
\text{测地线方程或平行移动方程}.
}
$$

## 看到

$$
I=du^2+Gdv^2
$$

立刻：

$$
\boxed{
h=\sqrt G,
\qquad
K=-\frac{h_{uu}}h.}
$$

## 看到“常曲率”

立刻：

$$
\boxed{h_{uu}+Kh=0.}
$$

---

# 49. 从第五章到第六章的最终统一

第五章建立：

$$
\boxed{
\overline\nabla_XY
=
D_XY+
\mathrm{II}(X,Y)\mathbf n.
}
$$

第六章令

$$
X=Y=\mathbf T,
$$

得到

$$
\boxed{
\mathbf T'
=
D_{\mathbf T}\mathbf T
+
\mathrm{II}(\mathbf T,\mathbf T)\mathbf n.
}
$$

然后分别命名：

$$
\boxed{
D_{\mathbf T}\mathbf T
=
\kappa_g(\mathbf n\times\mathbf T),
}
$$

$$
\boxed{
\mathrm{II}(\mathbf T,\mathbf T)
=
\kappa_n.
}
$$

于是

$$
\boxed{
\mathbf T'
=
\kappa_g(\mathbf n\times\mathbf T)
+
\kappa_n\mathbf n.
}
$$

当切向部分消失：

$$
\boxed{
D_{\mathbf T}\mathbf T=0,
}
$$

就得到测地线。

把它写成坐标分量：

$$
\boxed{
u^{k\prime\prime}+\Gamma^k_{ij}u^{i\prime}u^{j\prime}=0.}
$$

选择沿测地线的坐标：

$$
\boxed{I=du^2+h^2dv^2,}
$$

Gauss 曲率化成

$$
\boxed{K=-\frac{h_{uu}}h.}
$$

最后把一般切向量 \(X\) 的切向变化设为零：

$$
\boxed{
\frac{DX}{ds}=0,
}
$$

就得到平行移动。

所以第六章并没有引入互不相关的新公式，而是在同一个协变导数框架下依次研究：

$$
\boxed{
\begin{array}{c}
\text{曲线切向量怎样变化}\\
\Downarrow\\
\text{测地曲率与测地线}\\
\Downarrow\\
\text{测地坐标中曲率怎样控制测地线束}\\
\Downarrow\\
\text{一般切向量怎样沿曲线保持平行}
\end{array}
}
$$

---

# 50. 最终总理解

把第五章和第六章压缩成一句话：

> 第一基本形式 \(g\) 决定 Christoffel 记号和协变导数；协变导数告诉我们如何只在曲面内部比较不同点的切向量。对曲线切向量 \(\mathbf T\) 做协变导数，就得到测地曲率；当它为零时，曲线是测地线。沿测地线建立坐标后，Gauss 曲率控制相邻测地线之间的横向距离函数 \(h\)，满足 \(h_{uu}+Kh=0\)。对一般切向量场令协变导数为零，就得到平行移动。

最终逻辑图：

$$
\boxed{
\begin{array}{ccccccccc}
g
&\Longrightarrow&
\Gamma
&\Longrightarrow&
D
&\Longrightarrow&
\dfrac{DX}{ds}
&\Longrightarrow&
\text{平行移动}
\\[2mm]
&&&&\Downarrow&&&&\\[-1mm]
&&&&
D_{\mathbf T}\mathbf T
&\Longrightarrow&
\kappa_g
&\Longrightarrow&
\text{测地线}
\end{array}
}
$$

以及

$$
\boxed{
S
\Longrightarrow
\kappa_n,\tau_g
\Longrightarrow
\text{法向弯曲与主方向}
}
$$

再由测地坐标：

$$
\boxed{
I=du^2+h^2dv^2
\Longrightarrow
K=-\frac{h_{uu}}h
\Longrightarrow
h_{uu}+Kh=0.
}
$$

这三条路线共同构成第六章 §6.1—§6.5 的完整逻辑。
