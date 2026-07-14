# 陈维桓《微分几何》第四章：知识总结与课后题详解

> 范围：§4.1、§4.2、§4.3、§4.4、§4.6。  
> 按考试范围删去 §4.5，并删去渐近方向、渐近曲线及直接依赖这些内容的习题。

# §4.1 第二基本形式

## 一、知识总结

### 1. 为什么需要第二基本形式

第一基本形式

$$
I=E(du)^2+2F\,du\,dv+G(dv)^2
$$

描述曲面内部的长度、角度和面积，但不能区分平面与圆柱面，因为二者局部可以保长对应。

第二基本形式用来描述曲面相对于三维空间的弯曲。设有向正则参数曲面

$$
\mathbf r=\mathbf r(u,v),
$$

选定单位法向量

$$
\mathbf n=\frac{\mathbf r_u\times\mathbf r_v}
{|\mathbf r_u\times\mathbf r_v|}.
$$

曲面在邻近点偏离切平面的二阶主部，由第二基本形式控制。

### 2. 第二类基本量

定义

$$
L=\mathbf r_{uu}\cdot\mathbf n,
\qquad
M=\mathbf r_{uv}\cdot\mathbf n,
\qquad
N=\mathbf r_{vv}\cdot\mathbf n.
$$

于是第二基本形式为

$$
\boxed{
II=L(du)^2+2M\,du\,dv+N(dv)^2.
}
$$

由于

$$
\mathbf r_u\cdot\mathbf n=0,
\qquad
\mathbf r_v\cdot\mathbf n=0,
$$

分别求导可得

$$
\boxed{
L=-\mathbf r_u\cdot\mathbf n_u,
\quad
M=-\mathbf r_u\cdot\mathbf n_v
=-\mathbf r_v\cdot\mathbf n_u,
\quad
N=-\mathbf r_v\cdot\mathbf n_v.
}
$$

因此也可写成

$$
\boxed{II=d^2\mathbf r\cdot\mathbf n=-d\mathbf r\cdot d\mathbf n.}
$$

这说明第二基本形式本质上记录法向量的变化。

### 3. 定向改变的影响

若把法向量改为 $-\mathbf n$，则

$$
L,M,N,II
$$

全部变号。因此：

- 第二基本形式依赖曲面定向；
- Gauss 曲率以后不会因定向改变；
- 平均曲率和主曲率会整体变号。

### 4. 参数变换下的不变性

在保持定向的容许参数变换下，第二基本形式作为二次型保持不变。虽然 $L,M,N$ 会改变，但

$$
L(du)^2+2M\,du\,dv+N(dv)^2
$$

表示同一个几何对象。

若参数变换翻转定向，则诱导单位法向量反向，第二基本形式整体变号。

### 5. 第二基本形式的几何意义

取点 $p=\mathbf r(u,v)$，邻近点为

$$
\mathbf r(u+\Delta u,v+\Delta v).
$$

该邻近点到 $p$ 点切平面的有向距离记为 $\delta$。Taylor 展开给出

$$
\delta
=
\frac12\left[
L(\Delta u)^2+2M\Delta u\Delta v+N(\Delta v)^2
\right]
+o\bigl((\Delta u)^2+(\Delta v)^2\bigr).
$$

所以

$$
\boxed{II\sim 2\delta.}
$$

曲面偏离切平面越快，第二基本形式绝对值越大。

### 6. Monge 型曲面的公式

设

$$
\mathbf r(x,y)=(x,y,f(x,y)),
$$

并记

$$
W=\sqrt{1+f_x^2+f_y^2}.
$$

取上法向

$$
\mathbf n=\frac{(-f_x,-f_y,1)}{W}.
$$

第一类基本量为

$$
E=1+f_x^2,
\qquad
F=f_xf_y,
\qquad
G=1+f_y^2.
$$

第二类基本量为

$$
\boxed{
L=\frac{f_{xx}}W,
\qquad
M=\frac{f_{xy}}W,
\qquad
N=\frac{f_{yy}}W.
}
$$

所以

$$
\boxed{
II=\frac{f_{xx}(dx)^2+2f_{xy}\,dx\,dy+f_{yy}(dy)^2}
{\sqrt{1+f_x^2+f_y^2}}.
}
$$

### 7. 两个重要判别

#### 平面判别

若一块连通曲面上

$$
II\equiv0,
$$

则 $d\mathbf n=0$，所以法向量为常向量，曲面是平面的一部分。

#### 球面判别

若

$$
II=cI,
\qquad c\neq0,
$$

并且 $c$ 为常数，则

$$
d\mathbf n=-c\,d\mathbf r.
$$

从而

$$
d(\mathbf n+c\mathbf r)=0.
$$

于是存在常向量 $\mathbf a$，使

$$
\mathbf n+c\mathbf r=\mathbf a.
$$

故

$$
\left|\mathbf r-\frac{\mathbf a}{c}\right|=\frac1{|c|},
$$

曲面是半径 $1/|c|$ 的球面的一部分。

### 8. 统一计算流程

给定参数曲面，求第二基本形式时严格按下列顺序：

1. 求 $\mathbf r_u,\mathbf r_v$；
2. 求 $\mathbf r_u\times\mathbf r_v$ 并单位化，得到 $\mathbf n$；
3. 求 $\mathbf r_{uu},\mathbf r_{uv},\mathbf r_{vv}$；
4. 计算 $L,M,N$；
5. 写出 $II=L(du)^2+2Mdu\,dv+N(dv)^2$；
6. 检查法向方向，若与答案相反，整个 $II$ 只差一个负号。

---

## 二、课后习题逐题详解

## 习题 1

### 题目

求下列曲面的第二基本形式：

1. 椭球面
   $$
   \mathbf r=(a\cos\varphi\cos\theta,
   a\cos\varphi\sin\theta,b\sin\varphi);
   $$
2. 旋转椭圆抛物面
   $$
   \mathbf r=(u,v,\tfrac12(u^2+v^2));
   $$
3. 双曲抛物面
   $$
   \mathbf r=(a(u+v),a(u-v),2uv);
   $$
4. 一般柱面
   $$
   \mathbf r=(f(u),g(u),v);
   $$
5. 劈锥曲面
   $$
   \mathbf r=(u\cos v,u\sin v,f(v));
   $$
6. Viviani 曲线的切线面；
7. 曲面
   $$
   \mathbf r=(v\cos u-k\sin u,
   v\sin u+k\cos u,v+ku).
   $$

### 解答

### （1）椭球面

记

$$
Q=\sqrt{a^2\sin^2\varphi+b^2\cos^2\varphi}.
$$

先求偏导：

$$
\mathbf r_\varphi=
(-a\sin\varphi\cos\theta,
-a\sin\varphi\sin\theta,
 b\cos\varphi),
$$

$$
\mathbf r_\theta=
(-a\cos\varphi\sin\theta,
 a\cos\varphi\cos\theta,0).
$$

取外法向

$$
\mathbf n=\frac{1}{Q}
(b\cos\varphi\cos\theta,
 b\cos\varphi\sin\theta,
 a\sin\varphi).
$$

二阶偏导为

$$
\mathbf r_{\varphi\varphi}
=(-a\cos\varphi\cos\theta,
-a\cos\varphi\sin\theta,
-b\sin\varphi),
$$

$$
\mathbf r_{\varphi\theta}
=(a\sin\varphi\sin\theta,
-a\sin\varphi\cos\theta,0),
$$

$$
\mathbf r_{\theta\theta}
=(-a\cos\varphi\cos\theta,
-a\cos\varphi\sin\theta,0).
$$

故

$$
L=-\frac{ab}{Q},
\qquad M=0,
\qquad N=-\frac{ab\cos^2\varphi}{Q}.
$$

因此

$$
\boxed{
II=-\frac{ab}{Q}
\left[(d\varphi)^2+
\cos^2\varphi(d\theta)^2\right].
}
$$

若取内法向，右端整体变号。

### （2）旋转椭圆抛物面

有

$$
\mathbf r_u=(1,0,u),
\qquad
\mathbf r_v=(0,1,v).
$$

所以

$$
\mathbf r_u\times\mathbf r_v=(-u,-v,1),
$$

取上法向

$$
\mathbf n=\frac{(-u,-v,1)}{\sqrt{1+u^2+v^2}}.
$$

二阶偏导为

$$
\mathbf r_{uu}=(0,0,1),
\quad
\mathbf r_{uv}=0,
\quad
\mathbf r_{vv}=(0,0,1).
$$

于是

$$
L=N=\frac1{\sqrt{1+u^2+v^2}},
\qquad M=0.
$$

故

$$
\boxed{
II=\frac{(du)^2+(dv)^2}
{\sqrt{1+u^2+v^2}}.
}
$$

### （3）双曲抛物面

有

$$
\mathbf r_u=(a,a,2v),
\qquad
\mathbf r_v=(a,-a,2u).
$$

叉积为

$$
\mathbf r_u\times\mathbf r_v
=2a(u+v,v-u,-a).
$$

令

$$
D=\sqrt{2u^2+2v^2+a^2},
$$

取

$$
\mathbf n=\frac{(u+v,v-u,-a)}D.
$$

而

$$
\mathbf r_{uu}=0,
\qquad
\mathbf r_{uv}=(0,0,2),
\qquad
\mathbf r_{vv}=0.
$$

所以

$$
L=N=0,
\qquad
M=-\frac{2a}{D}.
$$

第二基本形式中混合项为 $2Mdu\,dv$，故

$$
\boxed{
II=-\frac{4a}{D}\,du\,dv.
}
$$

### （4）一般柱面

有

$$
\mathbf r_u=(f',g',0),
\qquad
\mathbf r_v=(0,0,1).
$$

取

$$
\mathbf n=\frac{(g',-f',0)}{\sqrt{(f')^2+(g')^2}}.
$$

又

$$
\mathbf r_{uu}=(f'',g'',0),
\qquad
\mathbf r_{uv}=0,
\qquad
\mathbf r_{vv}=0.
$$

所以

$$
L=\frac{f''g'-g''f'}{\sqrt{(f')^2+(g')^2}},
\qquad M=N=0.
$$

因此

$$
\boxed{
II=\frac{f''g'-g''f'}{\sqrt{(f')^2+(g')^2}}
(du)^2.
}
$$

沿直母线方向 $dv$ 没有二阶弯曲项，这与柱面沿直母线方向是直线一致。

### （5）劈锥曲面

有

$$
\mathbf r_u=(\cos v,\sin v,0),
$$

$$
\mathbf r_v=(-u\sin v,u\cos v,f'(v)).
$$

叉积为

$$
\mathbf r_u\times\mathbf r_v
=(f'\sin v,-f'\cos v,u),
$$

故取

$$
\mathbf n=\frac{(f'\sin v,-f'\cos v,u)}
{\sqrt{u^2+(f')^2}}.
$$

二阶偏导为

$$
\mathbf r_{uu}=0,
$$

$$
\mathbf r_{uv}=(-\sin v,\cos v,0),
$$

$$
\mathbf r_{vv}=(-u\cos v,-u\sin v,f'').
$$

于是

$$
L=0,
$$

$$
M=-\frac{f'}{\sqrt{u^2+(f')^2}},
$$

$$
N=\frac{uf''}{\sqrt{u^2+(f')^2}}.
$$

所以

$$
\boxed{
II=
-\frac{2f'}{\sqrt{u^2+(f')^2}}\,du\,dv
+
\frac{uf''}{\sqrt{u^2+(f')^2}}(dv)^2.
}
$$

### （6）Viviani 曲线的切线面

Viviani 曲线为

$$
\mathbf c(u)=
\left(k(1+\cos u),k\sin u,2k\sin\frac u2\right),
\qquad k>0.
$$

它的切线面取为

$$
\mathbf R(u,v)=\mathbf c(u)+v\mathbf c'(u),
\qquad v\neq0.
$$

之所以要求 $v\neq0$，是因为 $v=0$ 时
$\mathbf R_u$ 与 $\mathbf R_v$ 平行，切线面在脊线上不是正则参数曲面。

先求曲线的前三阶导数：

$$
\mathbf c'(u)
=
\left(-k\sin u,k\cos u,k\cos\frac u2\right),
$$

$$
\mathbf c''(u)
=
\left(-k\cos u,-k\sin u,-\frac k2\sin\frac u2\right),
$$

$$
\mathbf c'''(u)
=
\left(k\sin u,-k\cos u,-\frac k4\cos\frac u2\right).
$$

记

$$
p=\mathbf c'(u),\qquad q=\mathbf c''(u),\qquad r=\mathbf c'''(u).
$$

则

$$
\mathbf R_u=p+vq,
\qquad
\mathbf R_v=p.
$$

因此

$$
\mathbf R_u\times\mathbf R_v
=(p+vq)\times p
=-v(p\times q).
$$

直接计算可得

$$
|p\times q|^2
=\frac{k^4}{4}
\left(5+3\cos^2\frac u2\right),
$$

从而

$$
|p\times q|
=\frac{k^2}{2}
\sqrt{5+3\cos^2\frac u2}.
$$

在 $v>0$ 的一侧，取由参数次序诱导的单位法向量

$$
\mathbf n
=-\frac{p\times q}{|p\times q|}.
$$

二阶偏导为

$$
\mathbf R_{uu}=q+vr,
\qquad
\mathbf R_{uv}=q,
\qquad
\mathbf R_{vv}=0.
$$

因为 $q\perp p\times q$，所以

$$
M=\mathbf R_{uv}\cdot\mathbf n=0,
\qquad N=0.
$$

又

$$
(p,q,r)
=(p\times q)\cdot r
=\frac{3k^3}{4}\cos\frac u2.
$$

故

$$
\begin{aligned}
L
&=(q+vr)\cdot\mathbf n\\
&=-v\frac{(p\times q)\cdot r}{|p\times q|}\\
&=-\frac{3kv\cos\frac u2}
{2\sqrt{5+3\cos^2\frac u2}}.
\end{aligned}
$$

于是，在 $v>0$ 且取上述法向时，

$$
\boxed{
II=
-\frac{3kv\cos\frac u2}
{2\sqrt{5+3\cos^2\frac u2}}
(du)^2.
}
$$

在 $v<0$ 一侧若仍取参数次序诱导的法向，应把 $v$ 换成 $|v|$；若反转法向，整个第二基本形式同时变号。

### （7）给定参数曲面

令

$$
\mathbf r(u,v)=
(v\cos u-k\sin u,
 v\sin u+k\cos u,v+ku).
$$

一阶偏导为

$$
\mathbf r_u=
(-v\sin u-k\cos u,
 v\cos u-k\sin u,k),
$$

$$
\mathbf r_v=(\cos u,\sin u,1).
$$

叉积为

$$
\mathbf r_u\times\mathbf r_v
=
(v\cos u-2k\sin u,
 v\sin u+2k\cos u,-v).
$$

其长度为

$$
|\mathbf r_u\times\mathbf r_v|
=\sqrt{2v^2+4k^2}.
$$

因此取单位法向量

$$
\mathbf n=
\frac{1}{\sqrt{2v^2+4k^2}}
(v\cos u-2k\sin u,
 v\sin u+2k\cos u,-v).
$$

再求二阶偏导：

$$
\mathbf r_{uu}
=(-v\cos u+k\sin u,
 -v\sin u-k\cos u,0),
$$

$$
\mathbf r_{uv}=(-\sin u,\cos u,0),
\qquad
\mathbf r_{vv}=0.
$$

于是

$$
\begin{aligned}
L
&=\mathbf r_{uu}\cdot\mathbf n\\
&=-\frac{v^2+2k^2}{\sqrt{2v^2+4k^2}},
\end{aligned}
$$

$$
M=\mathbf r_{uv}\cdot\mathbf n
=\frac{2k}{\sqrt{2v^2+4k^2}},
$$

$$
N=0.
$$

所以

$$
\boxed{
II=
-\frac{v^2+2k^2}{\sqrt{2v^2+4k^2}}(du)^2
+
\frac{4k}{\sqrt{2v^2+4k^2}}\,du\,dv.
}
$$

反转法向时，上式整体变号。

---

## 习题 2

### 题目

求下列隐式曲面的第二基本形式：

1. $z(x^2+y^2)=2xy$；
2. $x^2+y^2=(\tan^2\alpha)z^2$；
3. $xyz=k^3$，$k\neq0$。

### 解答

### （1）$z(x^2+y^2)=2xy$

使用极坐标

$$
x=u\cos v,
\qquad y=u\sin v.
$$

因为

$$
z=\frac{2xy}{x^2+y^2}=\sin2v,
$$

可取参数

$$
\mathbf r(u,v)=(u\cos v,u\sin v,\sin2v).
$$

偏导为

$$
\mathbf r_u=(\cos v,\sin v,0),
$$

$$
\mathbf r_v=(-u\sin v,u\cos v,2\cos2v).
$$

叉积为

$$
\mathbf r_u\times\mathbf r_v
=(2\sin v\cos2v,-2\cos v\cos2v,u).
$$

其长度为

$$
\sqrt{u^2+4\cos^22v}.
$$

再求

$$
\mathbf r_{uu}=0,
$$

$$
\mathbf r_{uv}=(-\sin v,\cos v,0),
$$

$$
\mathbf r_{vv}=(-u\cos v,-u\sin v,-4\sin2v).
$$

代入可得

$$
L=0,
\qquad
M=-\frac{2\cos2v}{\sqrt{u^2+4\cos^22v}},
$$

$$
N=\frac{4u\sin2v}{\sqrt{u^2+4\cos^22v}}.
$$

因此

$$
\boxed{
II=-\frac4{\sqrt{u^2+4\cos^22v}}
\left(\cos2v\,du\,dv-u\sin2v(dv)^2\right).
}
$$

### （2）圆锥面

可取

$$
x=u\cos v,
\qquad
y=u\sin v,
\qquad
z=u\cot\alpha.
$$

于是

$$
\mathbf r=(u\cos v,u\sin v,u\cot\alpha).
$$

计算得到 $L=M=0$，只有 $N$ 非零。选取适当法向后

$$
N=u\cos\alpha.
$$

所以

$$
\boxed{II=u\cos\alpha(dv)^2.}
$$

这说明圆锥面沿直母线方向 $du$ 的法曲率为零。

### （3）$xyz=k^3$

在 $xy\neq0$ 的区域写成 Monge 形式

$$
z=f(x,y)=\frac{k^3}{xy}.
$$

有

$$
f_x=-\frac{k^3}{x^2y},
\qquad
f_y=-\frac{k^3}{xy^2},
$$

$$
f_{xx}=\frac{2k^3}{x^3y},
\qquad
f_{xy}=\frac{k^3}{x^2y^2},
\qquad
f_{yy}=\frac{2k^3}{xy^3}.
$$

又

$$
W=
\sqrt{1+\frac{k^6}{x^4y^2}+\frac{k^6}{x^2y^4}}
=
\frac{\sqrt{x^4y^4+k^6(x^2+y^2)}}{|x^2y^2|}.
$$

在固定符号的连通区域内整理可得

$$
\boxed{
II=
\frac{2k^3}{\sqrt{k^6(x^2+y^2)+x^4y^4}}
\left[
\frac yx(dx)^2+dx\,dy+\frac xy(dy)^2
\right].
}
$$

若所取法向相反，整体变号。

---

## 习题 3

### 题目

设 $\mathbf c(s)$ 是以弧长 $s$ 为参数、曲率和挠率均不为零的空间曲线。求其切线面

$$
\mathbf R(s,t)=\mathbf c(s)+t\boldsymbol\alpha(s)
$$

的第二基本形式，其中 $\boldsymbol\alpha,\boldsymbol\beta,\boldsymbol\gamma$ 为 Frenet 标架。

### 解答

由 Frenet 公式

$$
\boldsymbol\alpha'=\kappa\boldsymbol\beta,
$$

$$
\boldsymbol\beta'=-\kappa\boldsymbol\alpha+\tau\boldsymbol\gamma,
$$

$$
\boldsymbol\gamma'=-\tau\boldsymbol\beta.
$$

先求一阶偏导：

$$
\mathbf R_s
=\mathbf c'(s)+t\boldsymbol\alpha'(s)
=\boldsymbol\alpha+t\kappa\boldsymbol\beta,
$$

$$
\mathbf R_t=\boldsymbol\alpha.
$$

因此

$$
\mathbf R_s\times\mathbf R_t
=t\kappa\boldsymbol\beta\times\boldsymbol\alpha
=-t\kappa\boldsymbol\gamma.
$$

在 $t\neq0$ 的区域，取

$$
\mathbf n=-\boldsymbol\gamma
$$

作为单位法向量。再求二阶偏导：

$$
\mathbf R_{ss}
=
\kappa\boldsymbol\beta
+t\left(
\kappa'\boldsymbol\beta
+\kappa\boldsymbol\beta'
\right),
$$

即

$$
\mathbf R_{ss}
=-t\kappa^2\boldsymbol\alpha
+(\kappa+t\kappa')\boldsymbol\beta
+t\kappa\tau\boldsymbol\gamma.
$$

此外

$$
\mathbf R_{st}=\kappa\boldsymbol\beta,
\qquad
\mathbf R_{tt}=0.
$$

故

$$
L=\mathbf R_{ss}\cdot(-\boldsymbol\gamma)
=-t\kappa\tau,
$$

$$
M=0,
\qquad N=0.
$$

所以

$$
\boxed{II=-t\kappa\tau(ds)^2.}
$$

若取相反法向，则右端变号。

补充检查：第一基本形式为

$$
I=(1+t^2\kappa^2)(ds)^2+2ds\,dt+(dt)^2.
$$

第二基本形式的行列式恒为零，体现切线面是可展曲面。

---

## 习题 4

### 题目

设曲面为 Monge 形式

$$
z=f(x,y).
$$

求其第一基本形式和第二基本形式。

### 解答

取参数

$$
\mathbf r(x,y)=(x,y,f(x,y)).
$$

则

$$
\mathbf r_x=(1,0,f_x),
\qquad
\mathbf r_y=(0,1,f_y).
$$

因此

$$
E=\mathbf r_x^2=1+f_x^2,
$$

$$
F=\mathbf r_x\cdot\mathbf r_y=f_xf_y,
$$

$$
G=\mathbf r_y^2=1+f_y^2.
$$

所以

$$
\boxed{
I=(1+f_x^2)(dx)^2+2f_xf_y\,dx\,dy+(1+f_y^2)(dy)^2.
}
$$

取上法向

$$
\mathbf n=\frac{(-f_x,-f_y,1)}W,
\qquad
W=\sqrt{1+f_x^2+f_y^2}.
$$

二阶偏导为

$$
\mathbf r_{xx}=(0,0,f_{xx}),
$$

$$
\mathbf r_{xy}=(0,0,f_{xy}),
$$

$$
\mathbf r_{yy}=(0,0,f_{yy}).
$$

故

$$
L=\frac{f_{xx}}W,
\qquad
M=\frac{f_{xy}}W,
\qquad
N=\frac{f_{yy}}W.
$$

最终

$$
\boxed{
II=\frac{f_{xx}(dx)^2+2f_{xy}\,dx\,dy+f_{yy}(dy)^2}{W}.
}
$$

---

## 习题 5

### 题目

证明欧氏空间中的刚体运动保持曲面的第一基本形式和第二基本形式不变。

### 解答

设刚体运动为

$$
\widetilde{\mathbf r}=A\mathbf r+\mathbf b,
$$

其中 $A$ 为正交矩阵，$A^TA=I$，$\mathbf b$ 为常向量。

因为

$$
\widetilde{\mathbf r}_u=A\mathbf r_u,
\qquad
\widetilde{\mathbf r}_v=A\mathbf r_v,
$$

且正交变换保持内积，所以

$$
\widetilde E
=(A\mathbf r_u)\cdot(A\mathbf r_u)=E,
$$

$$
\widetilde F=F,
\qquad
\widetilde G=G.
$$

故第一基本形式不变。

若 $\det A=1$，则

$$
(A\mathbf r_u)\times(A\mathbf r_v)
=A(\mathbf r_u\times\mathbf r_v),
$$

所以可取

$$
\widetilde{\mathbf n}=A\mathbf n.
$$

又

$$
\widetilde{\mathbf r}_{uu}=A\mathbf r_{uu},
$$

因此

$$
\widetilde L
=(A\mathbf r_{uu})\cdot(A\mathbf n)=L.
$$

同理

$$
\widetilde M=M,
\qquad
\widetilde N=N.
$$

所以第二基本形式不变。

若 $\det A=-1$，空间定向被翻转。若仍要求使用由参数叉积诱导的法向，则法向会多一个负号，$II$ 相应变号；若把有向曲面的法向一同按 $A$ 搬运，则几何上的第二基本形式仍被保持。

---

## 习题 6

### 题目

证明：若一张可展曲面上存在两族彼此不同的连续直线族，则该曲面必为平面的一部分。

### 解答

可展曲面的基本特征是：沿每一条直母线，切平面保持不变。因此，若第一族直线的切方向为 $\mathbf X$，则

$$
d\mathbf n(\mathbf X)=0.
$$

若还存在另一族与第一族不同的直线，其切方向为 $\mathbf Y$，则同理

$$
d\mathbf n(\mathbf Y)=0.
$$

在两族直线横截的位置，$\mathbf X,\mathbf Y$ 线性无关，构成切平面的基底。因此对任意切向量

$$
\mathbf Z=a\mathbf X+b\mathbf Y
$$

都有

$$
d\mathbf n(\mathbf Z)=0.
$$

这说明

$$
d\mathbf n=0.
$$

所以曲面的单位法向量在该邻域内为常向量。于是切平面处处平行，并且

$$
d(\mathbf r\cdot\mathbf n)
=d\mathbf r\cdot\mathbf n+\mathbf r\cdot d\mathbf n=0.
$$

因此

$$
\mathbf r\cdot\mathbf n=c
$$

为常数，曲面落在同一个平面内。

故

$$
\boxed{\text{该曲面是平面的一部分。}}
$$

# §4.2 法曲率

## 一、知识总结

### 1. 曲面上曲线的法曲率

设曲面上曲线以弧长 $s$ 为参数：

$$
\mathbf c(s)=\mathbf r(u(s),v(s)).
$$

其单位切向量为

$$
\mathbf T=\frac{d\mathbf c}{ds}.
$$

空间曲线的曲率向量为

$$
\frac{d^2\mathbf c}{ds^2}=\kappa\boldsymbol\beta.
$$

把曲率向量投影到曲面法向量 $\mathbf n$ 上，定义法曲率

$$
\boxed{
k_n=\frac{d^2\mathbf c}{ds^2}\cdot\mathbf n.
}
$$

若 $\vartheta$ 是曲线主法向量 $\boldsymbol\beta$ 与曲面法向量 $\mathbf n$ 的夹角，则

$$
\boxed{k_n=\kappa\cos\vartheta.}
$$

### 2. 法曲率只依赖切方向

由链式法则

$$
\frac{d\mathbf c}{ds}
=\mathbf r_u\frac{du}{ds}
+\mathbf r_v\frac{dv}{ds}.
$$

再次求导并与 $\mathbf n$ 点乘，所有只含 $\mathbf r_u,\mathbf r_v$ 的项消失，得到

$$
k_n=L\left(\frac{du}{ds}\right)^2
+2M\frac{du}{ds}\frac{dv}{ds}
+N\left(\frac{dv}{ds}\right)^2.
$$

因为 $s$ 是弧长参数，

$$
1=E\left(\frac{du}{ds}\right)^2
+2F\frac{du}{ds}\frac{dv}{ds}
+G\left(\frac{dv}{ds}\right)^2.
$$

因此对任意非零方向 $(du,dv)$，

$$
\boxed{
k_n=\frac{II}{I}
=\frac{L(du)^2+2Mdu\,dv+N(dv)^2}
{E(du)^2+2Fdu\,dv+G(dv)^2}.
}
$$

分子分母都是二次齐次式，所以只与方向比 $du:dv$ 有关。

### 3. 法截面与法截线

在曲面上一点，给定一个切方向。由该切方向与曲面法向量张成的平面，称为该方向的法截面。

法截面与曲面相交所得的平面曲线，称为法截线。

法截线本身就在法截面内，其相对曲率恰好等于曲面沿该方向的法曲率：

$$
\boxed{k_n=\kappa_r.}
$$

这给法曲率以最直接的几何解释：它就是用垂直于切平面的“刀”沿该方向切曲面所得剖面线的有向曲率。

### 4. 法曲率的符号

法曲率的符号依赖所选曲面法向：

- 曲线朝法向一侧弯曲，$k_n>0$；
- 曲线朝反法向一侧弯曲，$k_n<0$；
- 反转法向后，所有法曲率变号。

### 5. 常见曲面的法曲率

#### 平面

$$
II=0\quad\Longrightarrow\quad k_n=0.
$$

#### 半径为 $a$ 的球面

取外法向时

$$
\boxed{k_n=-\frac1a}
$$

对任意点、任意方向都成立；取内法向则为 $1/a$。

#### 半径为 $a$ 的圆柱面

若 $\theta$ 是切方向与纬圆方向的夹角，取外法向时

$$
\boxed{k_n=-\frac1a\cos^2\theta.}
$$

沿直母线方向为 $0$，沿纬圆方向绝对值最大。

### 6. 统一做题流程

求某条曲线在曲面上的法曲率：

1. 写出曲线在参数平面中的关系；
2. 求该曲线的方向比 $du:dv$；
3. 求曲面的 $E,F,G,L,M,N$；
4. 代入 $k_n=II/I$；
5. 最后再代入曲线上的参数关系。

---

## 二、课后习题逐题详解

## 习题 1

### 题目

悬链面的参数方程为

$$
\mathbf r(u,v)=
\left(
\sqrt{u^2+a^2}\cos v,
\sqrt{u^2+a^2}\sin v,
 a\log\left(u+\sqrt{u^2+a^2}\right)
\right).
$$

求第一、第二基本形式，并求在 $(u,v)=(0,0)$ 处沿

$$
d\mathbf r=2\mathbf r_u+\mathbf r_v
$$

方向的法曲率。

### 解答

记

$$
\rho=\sqrt{u^2+a^2}.
$$

有

$$
\rho_u=\frac u\rho,
\qquad
\frac d{du}\left[a\log(u+\rho)\right]=\frac a\rho.
$$

所以

$$
\mathbf r_u=
\left(
\frac u\rho\cos v,
\frac u\rho\sin v,
\frac a\rho
\right),
$$

$$
\mathbf r_v=(-\rho\sin v,\rho\cos v,0).
$$

于是

$$
E=\mathbf r_u^2
=\frac{u^2+a^2}{\rho^2}=1,
$$

$$
F=0,
\qquad
G=\rho^2=u^2+a^2.
$$

因此

$$
\boxed{I=(du)^2+(u^2+a^2)(dv)^2.}
$$

叉积为

$$
\mathbf r_u\times\mathbf r_v
=(-a\cos v,-a\sin v,u),
$$

其长度为 $\rho$。取

$$
\mathbf n=\frac{(-a\cos v,-a\sin v,u)}\rho.
$$

二阶偏导为

$$
\mathbf r_{uu}
=
\left(
\frac{a^2}{\rho^3}\cos v,
\frac{a^2}{\rho^3}\sin v,
-\frac{au}{\rho^3}
\right),
$$

$$
\mathbf r_{uv}
=
\left(
-\frac u\rho\sin v,
\frac u\rho\cos v,0
\right),
$$

$$
\mathbf r_{vv}=(-\rho\cos v,-\rho\sin v,0).
$$

所以

$$
L=-\frac a{u^2+a^2},
\qquad M=0,
\qquad N=a.
$$

故

$$
\boxed{
II=-\frac a{u^2+a^2}(du)^2+a(dv)^2.
}
$$

在 $(0,0)$ 处，方向

$$
2\mathbf r_u+\mathbf r_v
$$

对应参数方向

$$
du:dv=2:1.
$$

此时

$$
E=1,
\quad F=0,
\quad G=a^2,
$$

$$
L=-\frac1a,
\quad M=0,
\quad N=a.
$$

所以

$$
k_n
=
\frac{L\cdot2^2+2M\cdot2\cdot1+N\cdot1^2}
{E\cdot2^2+2F\cdot2\cdot1+G\cdot1^2}.
$$

即

$$
\boxed{
k_n=\frac{-4/a+a}{4+a^2}
=\frac{a^2-4}{a(a^2+4)}.
}
$$

---

## 习题 2

### 题目

曲面

$$
z=\frac{x^2}{\alpha^2}+\frac{y^2}{\beta^2}
$$

被平面

$$
z=ky
$$

截得一条曲线。求该截线在原点处的法曲率。

### 解答

取曲面参数

$$
\mathbf r(x,y)=
\left(x,y,\frac{x^2}{\alpha^2}+\frac{y^2}{\beta^2}\right).
$$

在原点有

$$
f_x=f_y=0,
$$

所以

$$
E=G=1,
\qquad F=0.
$$

取上法向，有

$$
L=f_{xx}=\frac2{\alpha^2},
\qquad
M=0,
\qquad
N=f_{yy}=\frac2{\beta^2}.
$$

现在求截线在原点的切方向。截线满足

$$
\frac{x^2}{\alpha^2}+\frac{y^2}{\beta^2}=ky.
$$

对一条过原点的参数曲线 $x=x(t),y=y(t)$ 求导：

$$
\frac{2x}{\alpha^2}x'
+\frac{2y}{\beta^2}y'
=ky'.
$$

在原点代入 $x=y=0$ 得

$$
ky'(0)=0.
$$

若 $k\neq0$，则

$$
y'(0)=0,
$$

所以切方向沿 $x$ 轴，即

$$
dx:dy=1:0.
$$

因此

$$
\boxed{
k_n=\frac{L}{E}=\frac2{\alpha^2}.}
$$

注意：$\beta$ 和 $k$ 决定截线离开原点后的形状，但不改变原点处的切方向，所以不出现在最终答案中。

---

## 习题 3

### 题目

证明：曲面上一条曲线在一点的法曲率，等于该曲线向对应法截面作正投影后所得平面曲线在该点的相对曲率。

### 解答

设原曲线以弧长 $s$ 为参数，点 $p$ 处单位切向量为 $\mathbf T$。由 $\mathbf T$ 和曲面法向量 $\mathbf n$ 张成法截面 $\Pi$。

把曲线正投影到 $\Pi$ 上，投影曲线记为 $\widetilde{\mathbf c}$。

在 $p$ 点，因为 $\mathbf T\in\Pi$，投影不改变一阶切向量，所以

$$
\widetilde{\mathbf c}'(0)=\mathbf c'(0)=\mathbf T.
$$

特别地，投影曲线在该点的速度仍为 $1$，因此用同一个参数计算二阶导数不会引入速度修正项。

原曲线曲率向量为

$$
\mathbf c''(0).
$$

投影曲线的曲率向量，就是把 $\mathbf c''(0)$ 正投影到 $\Pi$：

$$
\widetilde{\mathbf c}''(0)
=\operatorname{proj}_{\Pi}\mathbf c''(0).
$$

法截面中的正法向取为 $\mathbf n$。因为 $\mathbf n\in\Pi$，正投影不改变向量在 $\mathbf n$ 方向的分量，所以

$$
\widetilde{\mathbf c}''(0)\cdot\mathbf n
=\mathbf c''(0)\cdot\mathbf n.
$$

左边是投影平面曲线的相对曲率，右边是原曲线的法曲率。因此

$$
\boxed{\widetilde\kappa_r=k_n.}
$$

---

## 习题 4

### 题目

两曲面 $S_1,S_2$ 相交成曲线 $C$。在交点 $p$，两曲面的单位法向量夹角为 $\theta$，交线沿公共切方向在两曲面上的法曲率分别为 $k_{n1},k_{n2}$。求交线在 $p$ 点的空间曲率 $\kappa$。

### 解答

设交线以弧长为参数，曲率向量为

$$
\mathbf q=\frac{d^2\mathbf c}{ds^2}.
$$

因为 $\mathbf q$ 垂直于交线切向量，而 $\mathbf n_1,\mathbf n_2$ 也都垂直于交线切向量，所以

$$
\mathbf q\in\operatorname{span}\{\mathbf n_1,\mathbf n_2\}.
$$

写成

$$
\mathbf q=a\mathbf n_1+b\mathbf n_2.
$$

由法曲率定义，

$$
\mathbf q\cdot\mathbf n_1=k_{n1},
\qquad
\mathbf q\cdot\mathbf n_2=k_{n2}.
$$

又

$$
\mathbf n_1\cdot\mathbf n_2=\cos\theta,
$$

所以

$$
\begin{cases}
a+b\cos\theta=k_{n1},\\
a\cos\theta+b=k_{n2}.
\end{cases}
$$

解得

$$
a=\frac{k_{n1}-k_{n2}\cos\theta}{\sin^2\theta},
$$

$$
b=\frac{k_{n2}-k_{n1}\cos\theta}{\sin^2\theta}.
$$

交线曲率为

$$
\kappa=|\mathbf q|.
$$

计算

$$
|\mathbf q|^2=a^2+b^2+2ab\cos\theta,
$$

整理后得到

$$
\boxed{
\kappa^2=
\frac{k_{n1}^2+k_{n2}^2-2k_{n1}k_{n2}\cos\theta}
{\sin^2\theta}.
}
$$

所以

$$
\boxed{
\kappa=
\frac{
\sqrt{k_{n1}^2+k_{n2}^2-2k_{n1}k_{n2}\cos\theta}}
{|\sin\theta|}.
}
$$

---

## 习题 5

### 题目

求下列曲面上已知曲线的法曲率：

1. 半径为 $a$ 的球面上的曲线 $u+v=\pi/2$；
2. Viviani 曲线的切线面
   $$
   \mathbf R(u,v)=\mathbf c(u)+v\mathbf c'(u)
   $$
   上的曲线 $u+v=c$；
3. 曲面
   $$
   \mathbf r(u,v)=(u,v,kuv)
   $$
   上的曲线 $u=v^2$。

### 解答

### （1）球面

球面参数为

$$
\mathbf r=(a\cos u\cos v,a\cos u\sin v,a\sin u).
$$

取外法向

$$
\mathbf n=\frac{\mathbf r}{a}.
$$

对半径为 $a$ 的球面，Weingarten 映射为 $-(1/a)I$，所以每个方向的法曲率都相同：

$$
\boxed{k_n=-\frac1a.}
$$

若教材选取内法向，则答案为 $1/a$。曲线方程 $u+v=\pi/2$ 不影响结果。

### （2）曲线切线面上的曲线 $u+v=c$

设空间曲线为

$$
\mathbf c=\mathbf c(u),
$$

且

$$
\mathbf c'(u)\times\mathbf c''(u)\ne\mathbf0.
$$

它的切线面为

$$
\mathbf R(u,v)=\mathbf c(u)+v\mathbf c'(u).
$$

为简化记号，令

$$
\mathbf p=\mathbf c'(u),
\qquad
\mathbf q=\mathbf c''(u),
\qquad
\mathbf h=\mathbf c'''(u).
$$

先求曲面的偏导：

$$
\mathbf R_u=\mathbf p+v\mathbf q,
\qquad
\mathbf R_v=\mathbf p.
$$

因此第一类基本量为

$$
E=|\mathbf p+v\mathbf q|^2,
$$

$$
F=(\mathbf p+v\mathbf q)\cdot\mathbf p,
$$

$$
G=|\mathbf p|^2.
$$

在 $v\ne0$ 的正则部分，取单位法向量

$$
\mathbf n
=\frac{\mathbf p\times\mathbf q}
{|\mathbf p\times\mathbf q|}.
$$

二阶偏导为

$$
\mathbf R_{uu}=\mathbf q+v\mathbf h,
$$

$$
\mathbf R_{uv}=\mathbf q,
\qquad
\mathbf R_{vv}=\mathbf0.
$$

由于 $\mathbf n$ 同时垂直于 $\mathbf p$ 和 $\mathbf q$，故

$$
M=\mathbf R_{uv}\cdot\mathbf n=0,
\qquad
N=\mathbf R_{vv}\cdot\mathbf n=0.
$$

而

$$
\begin{aligned}
L
&=(\mathbf q+v\mathbf h)\cdot\mathbf n\\
&=v\,\mathbf h\cdot
\frac{\mathbf p\times\mathbf q}
{|\mathbf p\times\mathbf q|}\\
&=v\frac{(\mathbf p,\mathbf q,\mathbf h)}
{|\mathbf p\times\mathbf q|}.
\end{aligned}
$$

这里

$$
(\mathbf a,\mathbf b,\mathbf c)
=(\mathbf a\times\mathbf b)\cdot\mathbf c
$$

表示混合积。

曲线 $u+v=c$ 满足

$$
v=c-u,
\qquad dv=-du.
$$

沿该方向，第一基本形式为

$$
\begin{aligned}
I
&=E(du)^2+2Fdu\,dv+G(dv)^2\\
&=(E-2F+G)(du)^2.
\end{aligned}
$$

注意

$$
\begin{aligned}
E-2F+G
&=|\mathbf p+v\mathbf q|^2
-2(\mathbf p+v\mathbf q)\cdot\mathbf p
+|\mathbf p|^2\\
&=|v\mathbf q|^2\\
&=v^2|\mathbf q|^2.
\end{aligned}
$$

所以

$$
I=v^2|\mathbf q|^2(du)^2.
$$

第二基本形式为

$$
II=L(du)^2
=v\frac{(\mathbf p,\mathbf q,\mathbf h)}
{|\mathbf p\times\mathbf q|}(du)^2.
$$

因此法曲率为

$$
\boxed{
k_n
=
\frac{(\mathbf c',\mathbf c'',\mathbf c''')}
{(c-u)\,|\mathbf c'\times\mathbf c''|\,|\mathbf c''|^2}.
}
$$

这个表达式对应于上面选取的法向量

$$
\mathbf n=\frac{\mathbf c'\times\mathbf c''}
{|\mathbf c'\times\mathbf c''|}.
$$

若改用由参数次序直接诱导的法向量

$$
\frac{\mathbf R_u\times\mathbf R_v}
{|\mathbf R_u\times\mathbf R_v|}
=-\operatorname{sgn}(v)
\frac{\mathbf c'\times\mathbf c''}
{|\mathbf c'\times\mathbf c''|},
$$

则答案相应变为

$$
\boxed{
k_n
=-\frac{(\mathbf c',\mathbf c'',\mathbf c''')}
{|c-u|\,|\mathbf c'\times\mathbf c''|\,|\mathbf c''|^2}.
}
$$

两种写法只反映法向量选择不同。

### （3）曲面 $z=kuv$ 上的曲线 $u=v^2$

曲面是 Monge 形式

$$
f(u,v)=kuv.
$$

有

$$
f_u=kv,
\qquad
f_v=ku,
$$

$$
f_{uu}=0,
\qquad
f_{uv}=k,
\qquad
f_{vv}=0.
$$

令

$$
W=\sqrt{1+k^2u^2+k^2v^2}.
$$

则

$$
E=1+k^2v^2,
\qquad
F=k^2uv,
\qquad
G=1+k^2u^2,
$$

$$
L=0,
\qquad
M=\frac kW,
\qquad
N=0.
$$

曲线 $u=v^2$ 以 $v$ 为参数，有

$$
du=2v\,dv.
$$

所以

$$
II=2Mdu\,dv
=\frac{4kv}{W}(dv)^2.
$$

而

$$
I=E(2v)^2+2F(2v)+G.
$$

直接利用空间曲线计算最稳妥。令

$$
\mathbf c(v)=(v^2,v,kv^3),
$$

其速度平方为

$$
|\mathbf c'(v)|^2=4v^2+1+9k^2v^4.
$$

同时

$$
W=\sqrt{1+k^2v^2+k^2v^4}.
$$

故

$$
\boxed{
k_n=
\frac{4kv}
{(1+4v^2+9k^2v^4)
\sqrt{1+k^2v^2+k^2v^4}}.
}
$$

这里符号取决于曲面定向；若法向量反向，结果整体变号。

---

## 习题 8

### 题目

研究圆柱面上曲线与法截线的高阶切触，并说明同一切方向的曲线为什么具有相同的法曲率。

### 解答

取半径为 $a$ 的圆柱面

$$
\mathbf r(u,v)=(a\cos u,a\sin u,v).
$$

其第一、第二基本形式取外法向时为

$$
I=a^2(du)^2+(dv)^2,
$$

$$
II=-a(du)^2.
$$

给定方向 $(du,dv)$，任意通过该点并具有这一切方向的曲线，其法曲率均为

$$
\boxed{
k_n=-\frac{a(du)^2}{a^2(du)^2+(dv)^2}.
}
$$

现在取由该方向和法向量决定的法截面。法截线与任意同方向曲线在该点具有：

1. 相同的位置；
2. 相同的切向量；
3. 相同的曲率向量在曲面法向上的分量。

因此它们至少有相同的二阶法向展开。若把切平面作为 $xy$ 平面、法向作为 $z$ 轴，并令公共切方向为 $x$ 轴，则两条曲线都可写成

$$
z=\frac12k_nx^2+o(x^2).
$$

所以二阶主部完全一致，法曲率相同。

若要求更高阶切触，则还需比较三阶及以上展开；这时结果会依赖曲线在切平面内的偏转，不能只由法曲率决定。故法曲率精确刻画的是曲面沿给定方向的二阶弯曲，而不是整条曲线的全部高阶形状。


---

# §4.3 Weingarten 映射和主曲率

## 一、本节知识总结

## 1. Gauss 映射

设定向正则曲面为

$$
S:\mathbf r=\mathbf r(u,v),
$$

单位法向量为

$$
\mathbf n=\mathbf n(u,v).
$$

把曲面上的点映到该点单位法向量在单位球面上的终点，得到 **Gauss 映射**

$$
\boxed{
G:S\longrightarrow \mathbb S^2,
\qquad
G(\mathbf r(u,v))=\mathbf n(u,v).
}
$$

若

$$
\mathbf X=a\mathbf r_u+b\mathbf r_v\in T_pS,
$$

则 Gauss 映射的切映射为

$$
G_{*p}(\mathbf X)
=a\mathbf n_u+b\mathbf n_v.
$$

由于

$$
\mathbf n_u\cdot\mathbf n=0,
\qquad
\mathbf n_v\cdot\mathbf n=0,
$$

所以 $G_{*p}(\mathbf X)$ 仍位于与 $\mathbf n$ 垂直的平面内。这个平面既可看作 $T_pS$，也可看作单位球面在 $\mathbf n(p)$ 处的切平面。

---

## 2. Weingarten 映射

教材采用

$$
\boxed{W=-G_*}
$$

定义 Weingarten 映射。因此

$$
\boxed{
W(\mathbf X)=-D_{\mathbf X}\mathbf n.
}
$$

特别地，

$$
W(\mathbf r_u)=-\mathbf n_u,
\qquad
W(\mathbf r_v)=-\mathbf n_v.
$$

它描述的是：沿曲面某个切方向移动时，单位法向量改变得多快。

---

## 3. Weingarten 映射与第二基本形式

对任意切向量 $\mathbf X,\mathbf Y$，有

$$
\boxed{
II(\mathbf X,\mathbf Y)
=\langle W(\mathbf X),\mathbf Y\rangle.
}
$$

证明只需利用

$$
\langle \mathbf n,\mathbf Y\rangle=0.
$$

沿 $\mathbf X$ 求导：

$$
\langle D_{\mathbf X}\mathbf n,\mathbf Y\rangle
+
\langle \mathbf n,D_{\mathbf X}\mathbf Y\rangle=0.
$$

于是

$$
\langle W(\mathbf X),\mathbf Y\rangle
=-\langle D_{\mathbf X}\mathbf n,\mathbf Y\rangle
=
\langle \mathbf n,D_{\mathbf X}\mathbf Y\rangle
=II(\mathbf X,\mathbf Y).
$$

由于第二基本形式对称，

$$
II(\mathbf X,\mathbf Y)=II(\mathbf Y,\mathbf X),
$$

故

$$
\boxed{
\langle W(\mathbf X),\mathbf Y\rangle
=
\langle \mathbf X,W(\mathbf Y)\rangle.
}
$$

所以 $W$ 是关于第一基本形式的自共轭线性映射。

---

## 4. 主曲率和主方向

若非零切向量 $\mathbf X$ 满足

$$
W(\mathbf X)=\kappa\mathbf X,
$$

则：

- $\mathbf X$ 的方向称为**主方向**；
- 特征值 $\kappa$ 称为相应的**主曲率**。

曲面一点处的两个主曲率记为

$$
\kappa_1,\qquad \kappa_2.
$$

因为 $W$ 自共轭，所以：

1. $\kappa_1,\kappa_2$ 都是实数；
2. 当 $\kappa_1\ne\kappa_2$ 时，对应主方向互相垂直；
3. 当 $\kappa_1=\kappa_2$ 时，任意切方向都是主方向。

若

$$
\kappa_1=\kappa_2,
$$

该点称为**脐点**。此时

$$
W=\kappa I,
$$

并且

$$
II=\kappa I.
$$

---

## 5. 法曲率的线性代数表达

给定非零切向量 $\mathbf X$，其方向上的法曲率为

$$
\boxed{
\kappa_n(\mathbf X)
=
\frac{II(\mathbf X,\mathbf X)}{I(\mathbf X,\mathbf X)}
=
\frac{\langle W\mathbf X,\mathbf X\rangle}
{\langle \mathbf X,\mathbf X\rangle}.
}
$$

若 $\mathbf X$ 是单位向量，则

$$
\kappa_n(\mathbf X)=\langle W\mathbf X,\mathbf X\rangle.
$$

这就是自共轭线性变换的 Rayleigh 商。它的最大值、最小值正是两个主曲率。

---

## 6. Euler 公式

在一点取两个互相垂直的单位主方向 $\mathbf e_1,\mathbf e_2$。任意单位切向量可写成

$$
\mathbf e
=
\cos\theta\,\mathbf e_1
+
\sin\theta\,\mathbf e_2.
$$

于是

$$
W\mathbf e
=
\kappa_1\cos\theta\,\mathbf e_1
+
\kappa_2\sin\theta\,\mathbf e_2.
$$

所以

$$
\begin{aligned}
\kappa_n(\theta)
&=\langle W\mathbf e,\mathbf e\rangle\\
&=\kappa_1\cos^2\theta
+\kappa_2\sin^2\theta.
\end{aligned}
$$

即

$$
\boxed{
\kappa_n(\theta)
=
\kappa_1\cos^2\theta
+
\kappa_2\sin^2\theta.
}
$$

也可写成

$$
\boxed{
\kappa_n(\theta)
=H+\frac{\kappa_1-\kappa_2}{2}\cos2\theta,
}
$$

其中

$$
H=\frac{\kappa_1+\kappa_2}{2}.
$$

---

## 7. Gauss 曲率与平均曲率

定义

$$
\boxed{
K=\kappa_1\kappa_2
}
$$

为 Gauss 曲率，定义

$$
\boxed{
H=\frac{\kappa_1+\kappa_2}{2}
}
$$

为平均曲率。

从线性代数看，

$$
\boxed{
K=\det W,
\qquad
2H=\operatorname{tr}W.
}
$$

因此主曲率满足特征方程

$$
\boxed{
\kappa^2-2H\kappa+K=0.
}
$$

于是

$$
\boxed{
\kappa_{1,2}
=H\pm\sqrt{H^2-K}.
}
$$

---

## 8. 曲率线与 Rodrigues 判别

曲面上一条正则曲线

$$
\mathbf c(t)=\mathbf r(u(t),v(t))
$$

若其每一点的切方向都是主方向，则称为**曲率线**。

曲率线的核心判别是：

$$
W(\mathbf c')=\kappa\mathbf c'.
$$

由于

$$
W(\mathbf c')=-\frac{d\mathbf n}{dt},
$$

所以等价于

$$
\boxed{
\frac{d\mathbf n}{dt}
=-\kappa\frac{d\mathbf c}{dt}.
}
$$

也就是

$$
\boxed{
\frac{d\mathbf n}{dt}
\parallel
\frac{d\mathbf c}{dt}.
}
$$

这就是 Rodrigues 判别。

---

## 9. 曲率线与法线直纹面

沿曲线 $\mathbf c(t)$ 的法线构成直纹面

$$
\mathbf R(t,s)
=
\mathbf c(t)+s\mathbf n(t).
$$

该直纹面可展的充分必要条件为

$$
(\mathbf c',\mathbf n,\mathbf n')=0.
$$

由于 $\mathbf c',\mathbf n'$ 都垂直于 $\mathbf n$，上式等价于

$$
\mathbf c'\parallel\mathbf n'.
$$

因此

$$
\boxed{
\text{曲线是曲率线}
\iff
\text{沿曲线的法线构成可展曲面}.
}
$$

典型结论：

- 旋转面的经线和纬线都是曲率线；
- 可展曲面的直母线是曲率线。

---

## 二、课后习题逐题详解

## 习题 1

### 题目

求抛物面

$$
z=\frac{x^2}{a^2}+\frac{y^2}{b^2}
$$

在原点处的法曲率和主曲率。

### 解答

取 Monge 参数

$$
\mathbf r(x,y)
=
\left(x,y,\frac{x^2}{a^2}+\frac{y^2}{b^2}\right).
$$

记

$$
f(x,y)=\frac{x^2}{a^2}+\frac{y^2}{b^2}.
$$

则

$$
f_x=\frac{2x}{a^2},
\qquad
f_y=\frac{2y}{b^2}.
$$

在原点处，

$$
f_x(0,0)=f_y(0,0)=0.
$$

因此

$$
E=1,
\qquad
F=0,
\qquad
G=1.
$$

取向上的单位法向量。在原点处，

$$
f_{xx}=\frac{2}{a^2},
\qquad
f_{xy}=0,
\qquad
f_{yy}=\frac{2}{b^2}.
$$

故第二基本形式为

$$
II
=
\frac{2}{a^2}(dx)^2
+
\frac{2}{b^2}(dy)^2.
$$

若单位切方向与 $x$ 轴夹角为 $\theta$，则

$$
dx=\cos\theta,
\qquad
dy=\sin\theta.
$$

所以

$$
\boxed{
\kappa_n(\theta)
=
\frac{2}{a^2}\cos^2\theta
+
\frac{2}{b^2}\sin^2\theta.
}
$$

这已经是 Euler 公式。因此两个坐标方向就是主方向，主曲率为

$$
\boxed{
\kappa_1=\frac{2}{a^2},
\qquad
\kappa_2=\frac{2}{b^2}.
}
$$

若改变法向量方向，两个主曲率和全部法曲率同时变号。

---

## 习题 2

### 题目

证明：曲面在任意固定一点处，沿任意两个彼此正交的切方向的法曲率之和是常数。

### 解答

在该点取两个互相垂直的单位主方向 $\mathbf e_1,\mathbf e_2$，相应主曲率为 $\kappa_1,\kappa_2$。

设第一个单位方向与 $\mathbf e_1$ 的夹角为 $\theta$，则

$$
\mathbf e
=
\cos\theta\,\mathbf e_1
+
\sin\theta\,\mathbf e_2.
$$

与它垂直的单位方向可取为

$$
\mathbf e^\perp
=
-\sin\theta\,\mathbf e_1
+
\cos\theta\,\mathbf e_2.
$$

由 Euler 公式，

$$
\kappa_n(\mathbf e)
=
\kappa_1\cos^2\theta
+
\kappa_2\sin^2\theta,
$$

$$
\kappa_n(\mathbf e^\perp)
=
\kappa_1\sin^2\theta
+
\kappa_2\cos^2\theta.
$$

相加得

$$
\begin{aligned}
\kappa_n(\mathbf e)+\kappa_n(\mathbf e^\perp)
&=\kappa_1(\cos^2\theta+\sin^2\theta)\\
&\quad+\kappa_2(\sin^2\theta+\cos^2\theta)\\
&=\kappa_1+\kappa_2.
\end{aligned}
$$

因此

$$
\boxed{
\kappa_n(\mathbf e)+\kappa_n(\mathbf e^\perp)
=\kappa_1+\kappa_2=2H,
}
$$

与 $\theta$ 无关，故为常数。

---

## 习题 4

### 题目

证明：曲面上任意一点 $p$ 的某个邻域内，都存在正交参数系 $(u,v)$，使两族参数曲线在点 $p$ 处的切方向分别是该点的两个互相垂直的主方向。

### 解答

设曲面在 $p$ 点的两个单位主方向为

$$
\mathbf e_1,
\qquad
\mathbf e_2,
$$

且

$$
\mathbf e_1\perp\mathbf e_2.
$$

先过 $p$ 作一条曲面曲线 $C$，使其在 $p$ 点的切向量为 $\mathbf e_1$。这是常微分方程局部存在性或曲面上切向量场积分曲线定理的直接结果。

沿 $C$ 的每一点，在曲面切平面内取与 $C$ 的切方向垂直的方向。由正交轨线的局部存在定理，可以从 $C$ 上各点出发作一族与 $C$ 正交的曲线。

把 $C$ 作为一条 $v=$ 常数的参数曲线，把这些正交轨线作为 $u=$ 常数的参数曲线，就得到局部参数系 $(u,v)$。

按构造，两族参数曲线处处正交，因此

$$
F=\mathbf r_u\cdot\mathbf r_v=0.
$$

在点 $p$，一族参数曲线沿 $\mathbf e_1$，另一族沿与它垂直的方向。由于二维切平面中与 $\mathbf e_1$ 垂直的单位方向只有 $\pm\mathbf e_2$，故在 $p$ 点有

$$
\mathbf r_u\parallel\mathbf e_1,
\qquad
\mathbf r_v\parallel\mathbf e_2
$$

或二者次序交换。

所以所需正交参数系局部存在。

---

## 习题 5

### 题目

设固定点处某切方向与第一主方向的夹角为 $\theta$，相应法曲率记为 $\kappa_n(\theta)$。证明

$$
\frac1\pi\int_0^\pi\kappa_n(\theta)\,d\theta=H.
$$

### 解答

由 Euler 公式，

$$
\kappa_n(\theta)
=
\kappa_1\cos^2\theta
+
\kappa_2\sin^2\theta.
$$

于是

$$
\begin{aligned}
\int_0^\pi\kappa_n(\theta)\,d\theta
&=
\kappa_1\int_0^\pi\cos^2\theta\,d\theta
+
\kappa_2\int_0^\pi\sin^2\theta\,d\theta.
\end{aligned}
$$

利用

$$
\int_0^\pi\cos^2\theta\,d\theta
=
\int_0^\pi\sin^2\theta\,d\theta
=\frac\pi2,
$$

得到

$$
\int_0^\pi\kappa_n(\theta)\,d\theta
=
\frac\pi2(\kappa_1+\kappa_2).
$$

两边除以 $\pi$：

$$
\boxed{
\frac1\pi\int_0^\pi\kappa_n(\theta)\,d\theta
=
\frac{\kappa_1+\kappa_2}{2}=H.
}
$$

因此平均曲率确实等于一点处所有无向切方向法曲率的平均值。

---

## 习题 6

### 题目

在曲面一个非脐点 $p$，任取两个夹角恒为 $\theta_0$ 的切方向。若这两个方向的法曲率之和与第一个方向的选择无关，证明

$$
\theta_0=\frac\pi2
\pmod\pi.
$$

### 解答

因为 $p$ 是非脐点，

$$
\kappa_1\ne\kappa_2.
$$

令第一个方向与第一主方向的夹角为 $\theta$，则第二个方向与第一主方向的夹角为 $\theta+\theta_0$。

由 Euler 公式，

$$
\kappa_n(\theta)
=H+A\cos2\theta,
$$

其中

$$
A=\frac{\kappa_1-\kappa_2}{2}\ne0.
$$

于是两法曲率之和为

$$
\begin{aligned}
S(\theta)
&=\kappa_n(\theta)+\kappa_n(\theta+\theta_0)\\
&=2H+A\bigl[\cos2\theta+\cos(2\theta+2\theta_0)\bigr].
\end{aligned}
$$

利用和差化积，

$$
\cos2\theta+\cos(2\theta+2\theta_0)
=
2\cos\theta_0\cos(2\theta+\theta_0).
$$

故

$$
S(\theta)
=2H+2A\cos\theta_0\cos(2\theta+\theta_0).
$$

题设要求 $S(\theta)$ 与 $\theta$ 无关。由于 $A\ne0$，只能有

$$
\cos\theta_0=0.
$$

因此

$$
\boxed{
\theta_0=\frac\pi2+k\pi,
\qquad k\in\mathbb Z.
}
$$

若只考虑两条无向直线的夹角，则结论就是

$$
\boxed{\theta_0=\frac\pi2.}
$$

---

# §4.4 主方向和主曲率的计算

## 一、本节知识总结

## 1. 两个基本形式的矩阵

设

$$
I=E(du)^2+2Fdu\,dv+G(dv)^2,
$$

$$
II=L(du)^2+2Mdu\,dv+N(dv)^2.
$$

记

$$
\mathsf g=
\begin{pmatrix}
E&F\\
F&G
\end{pmatrix},
\qquad
\mathsf b=
\begin{pmatrix}
L&M\\
M&N
\end{pmatrix}.
$$

正则性保证

$$
\Delta=EG-F^2>0.
$$

在基底 $(\mathbf r_u,\mathbf r_v)$ 下，Weingarten 映射的矩阵为

$$
\boxed{
[W]=\mathsf g^{-1}\mathsf b.
}
$$

因为本文把切向量的坐标写成列向量，所以这是最直接的写法。具体地，

$$
\boxed{
[W]
=
\frac1{EG-F^2}
\begin{pmatrix}
GL-FM&GM-FN\\
EM-FL&EN-FM
\end{pmatrix}.
}
$$

---

## 2. 主曲率的特征方程

主曲率 $\kappa$ 满足

$$
\det(\mathsf b-\kappa\mathsf g)=0.
$$

即

$$
\boxed{
\begin{vmatrix}
L-\kappa E&M-\kappa F\\
M-\kappa F&N-\kappa G
\end{vmatrix}=0.
}
$$

展开得

$$
(EG-F^2)\kappa^2
-(EN+GL-2FM)\kappa
+(LN-M^2)=0.
$$

除以 $EG-F^2$，得到

$$
\boxed{
\kappa^2-2H\kappa+K=0.
}
$$

---

## 3. Gauss 曲率和平均曲率的计算公式

由特征方程的常数项与一次项，

$$
\boxed{
K=\frac{LN-M^2}{EG-F^2},
}
$$

$$
\boxed{
H=\frac{EN+GL-2FM}{2(EG-F^2)}.
}
$$

主曲率为

$$
\boxed{
\kappa_{1,2}=H\pm\sqrt{H^2-K}.
}
$$

注意：

- 法向量反向时，$L,M,N,H,\kappa_1,\kappa_2$ 同时变号；
- $K$ 不变。

---

## 4. 主方向的计算

求出主曲率 $\kappa$ 后，主方向 $(du,dv)$ 满足

$$
\boxed{
\begin{cases}
(L-\kappa E)du+(M-\kappa F)dv=0,\\
(M-\kappa F)du+(N-\kappa G)dv=0.
\end{cases}
}
$$

两式线性相关，任选一个非零方程即可求方向比。

例如，当 $L-\kappa E$ 与 $M-\kappa F$ 不同时为零时，可取

$$
\boxed{
du:dv=-(M-\kappa F):(L-\kappa E).
}
$$

主方向最后必须理解为空间切向量

$$
\mathbf X=du\,\mathbf r_u+dv\,\mathbf r_v.
$$

---

## 5. 曲率线微分方程

曲线是曲率线，等价于其切方向 $(du,dv)$ 是主方向。消去特征值 $\kappa$，可得

$$
\boxed{
\begin{vmatrix}
(dv)^2&-du\,dv&(du)^2\\
E&F&G\\
L&M&N
\end{vmatrix}=0.
}
$$

展开为

$$
\boxed{
(FN-GM)(dv)^2
+(EN-GL)du\,dv
+(EM-FL)(du)^2=0.
}
$$

若参数曲线本身就是曲率线，则

$$
F=0,
\qquad
M=0.
$$

此时

$$
I=E(du)^2+G(dv)^2,
$$

$$
II=L(du)^2+N(dv)^2,
$$

并且

$$
\boxed{
\kappa_1=\frac LE,
\qquad
\kappa_2=\frac NG.
}
$$

---

## 6. Monge 曲面的 $K,H$ 公式

对图形曲面

$$
z=f(x,y),
$$

记

$$
p=f_x,
\quad q=f_y,
\quad r=f_{xx},
\quad s=f_{xy},
\quad t=f_{yy}.
$$

取向上法向量，则

$$
\boxed{
K=\frac{rt-s^2}{(1+p^2+q^2)^2}.
}
$$

平均曲率为

$$
\boxed{
H=
\frac{(1+q^2)r-2pqs+(1+p^2)t}
{2(1+p^2+q^2)^{3/2}}.
}
$$

这是计算图形曲面时最常用的两个公式。

---

## 7. 脐点判定

一点是脐点，当且仅当存在实数 $\kappa$，使

$$
\boxed{
L=\kappa E,
\qquad
M=\kappa F,
\qquad
N=\kappa G.
}
$$

也就是

$$
\boxed{II=\kappa I.}
$$

对 Monge 曲面，脐点条件可以化成关于 $f$ 的一阶、二阶偏导数的代数方程，见习题 7。

---

## 8. 第三基本形式

定义第三基本形式

$$
\boxed{
III=d\mathbf n\cdot d\mathbf n.
}
$$

若写成

$$
III=e(du)^2+2fdu\,dv+g(dv)^2,
$$

则其矩阵为

$$
\boxed{
\begin{pmatrix}
e&f\\
f&g
\end{pmatrix}
=
\mathsf b\mathsf g^{-1}\mathsf b.
}
$$

三个基本形式满足

$$
\boxed{
III-2HII+KI=0.
}
$$

证明只需把 Cayley--Hamilton 公式

$$
W^2-2HW+KI=0
$$

作用在切向量上，再与另一个切向量作内积。

---

## 9. 平行曲面

设

$$
\bar{\mathbf r}(u,v)
=
\mathbf r(u,v)+\lambda\mathbf n(u,v).
$$

在主方向 $\mathbf e_i$ 上，

$$
d\bar{\mathbf r}(\mathbf e_i)
=(1-\lambda\kappa_i)d\mathbf r(\mathbf e_i).
$$

所以，只要

$$
1-\lambda\kappa_i\ne0,
$$

平行曲面仍正则，而且主方向不变，主曲率变为

$$
\boxed{
\bar\kappa_i
=
\frac{\kappa_i}{1-\lambda\kappa_i}.
}
$$

令

$$
D_\lambda
=(1-\lambda\kappa_1)(1-\lambda\kappa_2)
=1-2\lambda H+\lambda^2K,
$$

则

$$
\boxed{
\bar K
=
\frac{K}{1-2\lambda H+\lambda^2K},
}
$$

$$
\boxed{
\bar H
=
\frac{H-\lambda K}{1-2\lambda H+\lambda^2K}.
}
$$

---

## 二、课后习题逐题详解

## 习题 1

### 题目

求螺旋面

$$
\mathbf r(u,v)
=(u\cos v,u\sin v,u+v)
$$

的 Gauss 曲率和平均曲率。

### 解答

先求一阶偏导：

$$
\mathbf r_u=(\cos v,\sin v,1),
$$

$$
\mathbf r_v=(-u\sin v,u\cos v,1).
$$

所以

$$
E=\mathbf r_u^2=2,
$$

$$
F=\mathbf r_u\cdot\mathbf r_v=1,
$$

$$
G=\mathbf r_v^2=u^2+1.
$$

因此

$$
EG-F^2=2(u^2+1)-1=2u^2+1.
$$

记

$$
w=\sqrt{2u^2+1}.
$$

计算叉积：

$$
\mathbf r_u\times\mathbf r_v
=
(\sin v-u\cos v,-\cos v-u\sin v,u).
$$

故取单位法向量

$$
\mathbf n
=
\frac1w
(\sin v-u\cos v,-\cos v-u\sin v,u).
$$

二阶偏导为

$$
\mathbf r_{uu}=\mathbf 0,
$$

$$
\mathbf r_{uv}=(-\sin v,\cos v,0),
$$

$$
\mathbf r_{vv}=(-u\cos v,-u\sin v,0).
$$

于是

$$
L=0,
$$

$$
M=\mathbf r_{uv}\cdot\mathbf n=-\frac1w,
$$

$$
N=\mathbf r_{vv}\cdot\mathbf n=\frac{u^2}{w}.
$$

Gauss 曲率为

$$
\begin{aligned}
K
&=\frac{LN-M^2}{EG-F^2}\\
&=\frac{-1/w^2}{w^2}\\
&=-\frac1{w^4}.
\end{aligned}
$$

即

$$
\boxed{
K=-\frac1{(2u^2+1)^2}.
}
$$

平均曲率为

$$
\begin{aligned}
H
&=\frac{EN+GL-2FM}{2(EG-F^2)}\\
&=\frac{2\cdot u^2/w-2\cdot1\cdot(-1/w)}{2w^2}\\
&=\frac{2(u^2+1)/w}{2w^2}.
\end{aligned}
$$

故

$$
\boxed{
H=\frac{u^2+1}{(2u^2+1)^{3/2}}.
}
$$

若法向量反向，$H$ 变号，而 $K$ 不变。

---

## 习题 2

### 题目

平面曲线

$$
\mathbf c(s)=(g(s),0,f(s))
$$

绕 $z$ 轴旋转一周得到旋转面，其中 $s$ 是曲线的弧长参数。求曲面的 Gauss 曲率。

### 解答

旋转面的参数方程为

$$
\mathbf r(s,v)
=(g(s)\cos v,g(s)\sin v,f(s)).
$$

因为 $s$ 是弧长参数，

$$
(g')^2+(f')^2=1.
$$

一阶偏导：

$$
\mathbf r_s
=(g'\cos v,g'\sin v,f'),
$$

$$
\mathbf r_v
=(-g\sin v,g\cos v,0).
$$

所以

$$
E=1,
\qquad
F=0,
\qquad
G=g^2.
$$

可取单位法向量

$$
\mathbf n=(-f'\cos v,-f'\sin v,g').
$$

二阶偏导：

$$
\mathbf r_{ss}
=(g''\cos v,g''\sin v,f''),
$$

$$
\mathbf r_{sv}
=(-g'\sin v,g'\cos v,0),
$$

$$
\mathbf r_{vv}
=(-g\cos v,-g\sin v,0).
$$

故

$$
L=g'f''-f'g'',
\qquad
M=0,
\qquad
N=gf'.
$$

因此

$$
K
=
\frac{LN}{EG}
=
\frac{f'(g'f''-f'g'')}{g}.
$$

利用弧长条件求导：

$$
g'g''+f'f''=0.
$$

若写

$$
g'=\cos\varphi,
\qquad
f'=\sin\varphi,
$$

则

$$
g''=-\varphi'\sin\varphi,
\qquad
f''=\varphi'\cos\varphi,
$$

从而

$$
g'f''-f'g''=\varphi',
$$

以及

$$
g''=-\varphi'f'.
$$

所以

$$
\boxed{
K=-\frac{g''(s)}{g(s)}.
}
$$

这一定要记住：当母线用弧长参数表示时，旋转面的 Gauss 曲率可直接由旋转半径函数 $g(s)$ 得到。

---

## 习题 3

### 题目

求下列曲面的 Gauss 曲率 $K$ 和平均曲率 $H$。

1. $\mathbf r=(u\cos v,u\sin v,ku^2)$；
2. 平面曲线 $z=k\sqrt{x},y=0$ 绕 $z$ 轴旋转所得曲面；
3. 曳物线
   $$
   \mathbf c(t)=\left(k\sin t,0,k\left(\log\tan\frac t2+\cos t\right)\right)
   $$
   绕 $z$ 轴旋转所得伪球面；
4. Scherk 曲面
   $$
   z=\frac1k\bigl(\log\cos kx-\log\cos ky\bigr).
   $$

### 解答

### （1）旋转抛物面

曲面为

$$
\mathbf r(u,v)
=(u\cos v,u\sin v,ku^2),
\qquad u>0.
$$

它是旋转图形面 $z=f(u)$，其中

$$
f(u)=ku^2,
\quad
f'=2ku,
\quad
f''=2k.
$$

旋转图形面的公式为

$$
K=\frac{f'f''}{u(1+f'^2)^2},
$$

$$
H=\frac12
\left[
\frac{f''}{(1+f'^2)^{3/2}}
+
\frac{f'}{u\sqrt{1+f'^2}}
\right].
$$

代入得

$$
\boxed{
K=\frac{4k^2}{(1+4k^2u^2)^2}.
}
$$

再算平均曲率：

$$
\begin{aligned}
H
&=\frac12\left[
\frac{2k}{(1+4k^2u^2)^{3/2}}
+
\frac{2k}{\sqrt{1+4k^2u^2}}
\right]\\
&=\frac{k(2+4k^2u^2)}{(1+4k^2u^2)^{3/2}}.
\end{aligned}
$$

即

$$
\boxed{
H=\frac{2k(1+2k^2u^2)}{(1+4k^2u^2)^{3/2}}.
}
$$

---

### （2）$z=k\sqrt{x}$ 绕 $z$ 轴旋转

旋转后可取参数

$$
\mathbf r(u,v)
=(u\cos v,u\sin v,k\sqrt u),
\qquad u>0.
$$

这里

$$
f(u)=k\sqrt u,
$$

$$
f'(u)=\frac{k}{2\sqrt u},
\qquad
f''(u)=-\frac{k}{4u^{3/2}}.
$$

代入旋转图形面公式：

$$
\begin{aligned}
K
&=\frac{f'f''}{u(1+f'^2)^2}\\
&=
\frac{-k^2/(8u^2)}
{u\left(1+k^2/(4u)\right)^2}.
\end{aligned}
$$

化简得

$$
\boxed{
K=-\frac{2k^2}{u(4u+k^2)^2}.
}
$$

平均曲率为

$$
\begin{aligned}
H
&=\frac12\left[
\frac{-k/(4u^{3/2})}
{\left(1+k^2/(4u)\right)^{3/2}}
+
\frac{k/(2\sqrt u)}
{u\sqrt{1+k^2/(4u)}}
\right]\\
&=
\frac{k(2u+k^2)}{2u(4u+k^2)^{3/2}}.
\end{aligned}
$$

所以

$$
\boxed{
H=\frac{k(2u+k^2)}{2u(4u+k^2)^{3/2}}.
}
$$

---

### （3）伪球面

旋转参数写成

$$
\mathbf r(t,v)
=
\left(
 k\sin t\cos v,
 k\sin t\sin v,
 k\left(\log\tan\frac t2+\cos t\right)
\right).
$$

令

$$
\rho(t)=k\sin t,
$$

$$
z(t)=k\left(\log\tan\frac t2+\cos t\right).
$$

则

$$
\rho'=k\cos t,
$$

$$
z'=k\left(\frac1{\sin t}-\sin t\right)
=\frac{k\cos^2t}{\sin t}.
$$

所以母线速度为

$$
q=\sqrt{(\rho')^2+(z')^2}
=k\frac{\cos t}{\sin t}
$$

（在 $0<t<\pi/2$ 内）。

取相应法向量后，两条参数曲线是主曲率线。计算得到

$$
\kappa_1=-\frac{\tan t}{k},
\qquad
\kappa_2=\frac{\cot t}{k}.
$$

因此

$$
\boxed{
K=\kappa_1\kappa_2=-\frac1{k^2}.
}
$$

平均曲率为

$$
\boxed{
H=\frac1{2k}(\cot t-\tan t).
}
$$

伪球面的关键特征是

$$
\boxed{K\equiv-1/k^2,}
$$

即 Gauss 曲率为负常数。

---

### （4）Scherk 曲面

设

$$
f(x,y)
=
\frac1k\bigl(\log\cos kx-\log\cos ky\bigr).
$$

则

$$
f_x=-\tan kx,
\qquad
f_y=\tan ky,
$$

$$
f_{xx}=-k\sec^2kx,
\qquad
f_{xy}=0,
\qquad
f_{yy}=k\sec^2ky.
$$

Gauss 曲率为

$$
K=\frac{f_{xx}f_{yy}-f_{xy}^2}
{(1+f_x^2+f_y^2)^2}.
$$

故

$$
\boxed{
K=
-\frac{k^2\sec^2kx\sec^2ky}
{\left(1+\tan^2kx+\tan^2ky\right)^2}.
}
$$

平均曲率分子为

$$
(1+f_y^2)f_{xx}
-2f_xf_yf_{xy}
+(1+f_x^2)f_{yy}.
$$

因为 $f_{xy}=0$，且

$$
1+f_y^2=\sec^2ky,
\qquad
1+f_x^2=\sec^2kx,
$$

所以分子为

$$
-k\sec^2ky\sec^2kx
+k\sec^2kx\sec^2ky=0.
$$

因此

$$
\boxed{H=0.}
$$

---

## 习题 4

### 题目

求双曲抛物面

$$
\mathbf r(u,v)
=
(a(u+v),b(u-v),2uv)
$$

的 Gauss 曲率、平均曲率、两个主曲率及相应主方向。

### 解答

一阶偏导为

$$
\mathbf r_u=(a,b,2v),
$$

$$
\mathbf r_v=(a,-b,2u).
$$

故

$$
E=a^2+b^2+4v^2,
$$

$$
F=a^2-b^2+4uv,
$$

$$
G=a^2+b^2+4u^2.
$$

记

$$
A=a^2+b^2,
\qquad
B=a^2-b^2.
$$

则

$$
E=A+4v^2,
\quad
F=B+4uv,
\quad
G=A+4u^2.
$$

叉积为

$$
\mathbf r_u\times\mathbf r_v
=
(2b(u+v),2a(v-u),-2ab).
$$

记

$$
D=
\sqrt{b^2(u+v)^2+a^2(u-v)^2+a^2b^2}.
$$

则

$$
|\mathbf r_u\times\mathbf r_v|=2D.
$$

取

$$
\mathbf n
=
\frac1D
\bigl(b(u+v),a(v-u),-ab\bigr).
$$

二阶偏导为

$$
\mathbf r_{uu}=0,
\qquad
\mathbf r_{uv}=(0,0,2),
\qquad
\mathbf r_{vv}=0.
$$

所以

$$
L=0,
\qquad
M=-\frac{2ab}{D},
\qquad
N=0.
$$

另外

$$
EG-F^2=4D^2.
$$

于是

$$
\begin{aligned}
K
&=\frac{-M^2}{EG-F^2}\\
&=\frac{-4a^2b^2/D^2}{4D^2}.
\end{aligned}
$$

故

$$
\boxed{
K=-\frac{a^2b^2}{D^4}.
}
$$

平均曲率为

$$
\begin{aligned}
H
&=\frac{-2FM}{2(EG-F^2)}\\
&=-\frac{FM}{EG-F^2}\\
&=\frac{abF}{2D^3}.
\end{aligned}
$$

即

$$
\boxed{
H=\frac{ab(a^2-b^2+4uv)}{2D^3}.
}
$$

主曲率为

$$
\kappa_{1,2}=H\pm\sqrt{H^2-K}.
$$

注意

$$
H^2-K
=
\frac{a^2b^2F^2}{4D^6}
+
\frac{a^2b^2}{D^4}
=
\frac{a^2b^2(F^2+4D^2)}{4D^6}.
$$

而

$$
F^2+4D^2=EG.
$$

因此

$$
\boxed{
\kappa_{1,2}
=
\frac{ab}{2D^3}
\left(F\pm\sqrt{EG}\right).
}
$$

对每个主曲率 $\kappa_i$，主方向 $(du,dv)$ 满足

$$
-\kappa_iE\,du
+
(M-\kappa_iF)dv=0.
$$

可取方向比

$$
\boxed{
(du:dv)_i
=
(M-\kappa_iF):\kappa_iE.
}
$$

对应的空间主方向为

$$
\boxed{
\mathbf X_i
=(M-\kappa_iF)\mathbf r_u
+
\kappa_iE\mathbf r_v.
}
$$

由于 $K<0$，两个主曲率异号，这也与双曲抛物面的马鞍形状一致。

---

## 习题 5

### 题目

设单位速空间曲线为 $\mathbf c(s)$，其 Frenet 标架为

$$
\mathbf T(s),\mathbf \beta(s),\mathbf \gamma(s),
$$

曲率、挠率分别为 $\kappa(s),\tau(s)$。半径为 $\lambda$ 的管状曲面为

$$
\mathbf r(s,\theta)
=
\mathbf c(s)
+
\lambda\bigl(
\cos\theta\,\mathbf\beta(s)
+
\sin\theta\,\mathbf\gamma(s)
\bigr).
$$

求其 Gauss 曲率、平均曲率和主曲率。

### 解答

记

$$
\mathbf e_r
=
\cos\theta\,\mathbf\beta
+
\sin\theta\,\mathbf\gamma,
$$

$$
\mathbf e_\theta
=
-\sin\theta\,\mathbf\beta
+
\cos\theta\,\mathbf\gamma.
$$

则

$$
\mathbf r=\mathbf c+\lambda\mathbf e_r.
$$

利用 Frenet 公式

$$
\mathbf T'=\kappa\mathbf\beta,
$$

$$
\mathbf\beta'=-\kappa\mathbf T+\tau\mathbf\gamma,
$$

$$
\mathbf\gamma'=-\tau\mathbf\beta,
$$

得到

$$
(\mathbf e_r)_s
=-\kappa\cos\theta\,\mathbf T
+\tau\mathbf e_\theta.
$$

因此

$$
\mathbf r_s
=
(1-\lambda\kappa\cos\theta)\mathbf T
+
\lambda\tau\mathbf e_\theta.
$$

记

$$
A=1-\lambda\kappa\cos\theta.
$$

则

$$
\mathbf r_s=A\mathbf T+\lambda\tau\mathbf e_\theta,
$$

$$
\mathbf r_\theta=\lambda\mathbf e_\theta.
$$

取管面外向单位法向量

$$
\mathbf n=\mathbf e_r.
$$

圆周方向 $\partial_\theta$ 上，

$$
\mathbf n_\theta=\mathbf e_\theta,
$$

而

$$
\mathbf r_\theta=\lambda\mathbf e_\theta.
$$

所以

$$
W(\mathbf r_\theta)
=-\mathbf n_\theta
=-\frac1\lambda\mathbf r_\theta.
$$

故一个主曲率为

$$
\boxed{
\kappa_2=-\frac1\lambda.
}
$$

再考虑参数方向组合

$$
X=\partial_s-\tau\partial_\theta.
$$

则

$$
d\mathbf r(X)
=
\mathbf r_s-\tau\mathbf r_\theta
=A\mathbf T.
$$

同时

$$
d\mathbf n(X)
=
\mathbf n_s-\tau\mathbf n_\theta
=-\kappa\cos\theta\,\mathbf T.
$$

所以

$$
W(d\mathbf r(X))
=-d\mathbf n(X)
=
\kappa\cos\theta\,\mathbf T
=
\frac{\kappa\cos\theta}{A}d\mathbf r(X).
$$

故另一个主曲率为

$$
\boxed{
\kappa_1
=
\frac{\kappa(s)\cos\theta}
{1-\lambda\kappa(s)\cos\theta}.
}
$$

因此

$$
\boxed{
K
=
-\frac{\kappa(s)\cos\theta}
{\lambda\left(1-\lambda\kappa(s)\cos\theta\right)}.
}
$$

平均曲率为

$$
\begin{aligned}
H
&=\frac12\left[
\frac{\kappa\cos\theta}{A}
-
\frac1\lambda
\right]\\
&=
\frac{2\lambda\kappa\cos\theta-1}
{2\lambda A}.
\end{aligned}
$$

即

$$
\boxed{
H=
\frac{2\lambda\kappa(s)\cos\theta-1}
{2\lambda\left(1-\lambda\kappa(s)\cos\theta\right)}.
}
$$

曲面正则要求

$$
1-\lambda\kappa(s)\cos\theta\ne0.
$$

---

## 习题 6

### 题目

设曲面

$$
S:\mathbf r=\mathbf r(u,v)
$$

的平行曲面为

$$
\bar S:\bar{\mathbf r}(u,v)
=
\mathbf r(u,v)+\lambda\mathbf n(u,v).
$$

证明：

1. 两曲面在对应点的切平面互相平行；
2. 对应把 $S$ 上的曲率线映为 $\bar S$ 上的曲率线；
3. 两曲面的 $K,H$ 满足
   $$
   \bar K=\frac{K}{1-2\lambda H+\lambda^2K},
   \qquad
   \bar H=\frac{H-\lambda K}{1-2\lambda H+\lambda^2K}.
   $$

### 解答

### （1）切平面平行

对任意切向量 $\mathbf X$，

$$
d\bar{\mathbf r}(\mathbf X)
=
d\mathbf r(\mathbf X)+\lambda d\mathbf n(\mathbf X).
$$

因为

$$
d\mathbf n(\mathbf X)=-W(d\mathbf r(\mathbf X))
$$

仍是原曲面的切向量，所以 $d\bar{\mathbf r}(\mathbf X)$ 也位于原曲面的切平面。

若平行曲面正则，$d\bar{\mathbf r}$ 的像是二维的，因此

$$
T_{\bar p}\bar S=T_pS.
$$

故两切平面互相平行，且可以选取相同的单位法向量 $\mathbf n$。

---

### （2）曲率线保持

设 $\mathbf e_i$ 是原曲面的主方向，

$$
W(\mathbf e_i)=\kappa_i\mathbf e_i.
$$

则

$$
d\bar{\mathbf r}(\mathbf e_i)
=
\mathbf e_i+
\lambda d\mathbf n(\mathbf e_i)
=
(1-\lambda\kappa_i)\mathbf e_i.
$$

因此对应后的切方向仍与 $\mathbf e_i$ 平行。

又因为两曲面采用同一个法向量场，

$$
\bar W\bigl(d\bar{\mathbf r}(\mathbf e_i)\bigr)
=-d\mathbf n(\mathbf e_i)
=\kappa_i\mathbf e_i.
$$

而

$$
\mathbf e_i
=
\frac1{1-\lambda\kappa_i}
 d\bar{\mathbf r}(\mathbf e_i).
$$

所以

$$
\bar W\bigl(d\bar{\mathbf r}(\mathbf e_i)\bigr)
=
\frac{\kappa_i}{1-\lambda\kappa_i}
 d\bar{\mathbf r}(\mathbf e_i).
$$

故对应方向仍是主方向。曲率线被映为曲率线。

---

### （3）曲率公式

由上面的计算，平行曲面的主曲率为

$$
\boxed{
\bar\kappa_i
=
\frac{\kappa_i}{1-\lambda\kappa_i}.
}
$$

因此

$$
\begin{aligned}
\bar K
&=\bar\kappa_1\bar\kappa_2\\
&=
\frac{\kappa_1\kappa_2}
{(1-\lambda\kappa_1)(1-\lambda\kappa_2)}.
\end{aligned}
$$

分母为

$$
1-\lambda(\kappa_1+\kappa_2)
+\lambda^2\kappa_1\kappa_2
=1-2\lambda H+\lambda^2K.
$$

故

$$
\boxed{
\bar K
=
\frac{K}{1-2\lambda H+\lambda^2K}.
}
$$

平均曲率为

$$
\begin{aligned}
\bar H
&=\frac12
\left[
\frac{\kappa_1}{1-\lambda\kappa_1}
+
\frac{\kappa_2}{1-\lambda\kappa_2}
\right]\\
&=
\frac{\kappa_1+\kappa_2-2\lambda\kappa_1\kappa_2}
{2(1-\lambda\kappa_1)(1-\lambda\kappa_2)}.
\end{aligned}
$$

于是

$$
\boxed{
\bar H
=
\frac{H-\lambda K}
{1-2\lambda H+\lambda^2K}.
}
$$

---

## 习题 7

### 题目

求 Monge 曲面

$$
z=f(x,y)
$$

上的脐点所满足的充分必要条件。

### 解答

记

$$
p=f_x,
\quad q=f_y,
\quad r=f_{xx},
\quad s=f_{xy},
\quad t=f_{yy},
$$

并令

$$
w=\sqrt{1+p^2+q^2}.
$$

第一基本量为

$$
E=1+p^2,
\qquad
F=pq,
\qquad
G=1+q^2.
$$

取向上法向量时，第二基本量为

$$
L=\frac r w,
\qquad
M=\frac s w,
\qquad
N=\frac t w.
$$

脐点条件是存在 $\kappa$，使

$$
L=\kappa E,
\qquad
M=\kappa F,
\qquad
N=\kappa G.
$$

消去 $\kappa$，可以写成三个行列式条件：

$$
LG-NE=0,
$$

$$
ME-LF=0,
$$

$$
MG-NF=0.
$$

代入 $E,F,G,L,M,N$，得到

$$
\boxed{
(1+q^2)r-(1+p^2)t=0,
}
$$

$$
\boxed{
(1+p^2)s-pqr=0,
}
$$

$$
\boxed{
(1+q^2)s-pqt=0.
}
$$

所以一点是脐点的充分必要条件为

$$
\boxed{
\begin{cases}
(1+f_y^2)f_{xx}-(1+f_x^2)f_{yy}=0,\\
(1+f_x^2)f_{xy}-f_xf_yf_{xx}=0,\\
(1+f_y^2)f_{xy}-f_xf_yf_{yy}=0.
\end{cases}
}
$$

这三个式子中通常只有两个独立，但同时写出最安全。

---

## 习题 8

### 题目

求下列曲面上的脐点。

1. 椭圆抛物面
   $$
   2z=\frac{x^2}{a^2}+\frac{y^2}{b^2},
   \qquad a>b>0;
   $$
2. 三轴椭球面
   $$
   \frac{x^2}{a^2}+
   \frac{y^2}{b^2}+
   \frac{z^2}{c^2}=1,
   \qquad a>b>c>0.
   $$

### 解答

### （1）椭圆抛物面

写成

$$
f(x,y)=\frac{x^2}{2a^2}+\frac{y^2}{2b^2}.
$$

于是

$$
p=\frac{x}{a^2},
\qquad
q=\frac{y}{b^2},
$$

$$
r=\frac1{a^2},
\qquad
s=0,
\qquad
t=\frac1{b^2}.
$$

脐点条件中的后两式给出

$$
pq=0,
$$

即

$$
xy=0.
$$

第一式给出

$$
\frac{1+y^2/b^4}{a^2}
=
\frac{1+x^2/a^4}{b^2}.
$$

若 $y=0$，则

$$
\frac1{a^2}
=
\frac{1+x^2/a^4}{b^2},
$$

右边大于 $1/b^2>1/a^2$，不可能。

故必须 $x=0$。此时

$$
\frac{1+y^2/b^4}{a^2}
=
\frac1{b^2}.
$$

所以

$$
y^2=b^2(a^2-b^2).
$$

又

$$
z=\frac{y^2}{2b^2}
=\frac{a^2-b^2}{2}.
$$

因此两个脐点为

$$
\boxed{
\left(
0,
\pm b\sqrt{a^2-b^2},
\frac{a^2-b^2}{2}
\right).
}
$$

---

### （2）三轴椭球面

三轴椭球面的脐点均位于中间半轴对应的对称平面 $y=0$ 内。

在 $y=0$ 的椭圆

$$
\frac{x^2}{a^2}+\frac{z^2}{c^2}=1
$$

上，脐点条件化为

$$
\frac{x^2}{a^4}
:
\frac{z^2}{c^4}
=
\frac{a^2-b^2}{b^2-c^2}.
$$

与椭球方程联立，得到

$$
x^2
=
\frac{a^2(a^2-b^2)}{a^2-c^2},
$$

$$
z^2
=
\frac{c^2(b^2-c^2)}{a^2-c^2}.
$$

因此共有四个脐点：

$$
\boxed{
\left(
\pm a\sqrt{\frac{a^2-b^2}{a^2-c^2}},
0,
\pm c\sqrt{\frac{b^2-c^2}{a^2-c^2}}
\right),
}
$$

其中两个正负号可以独立选择，所以共有四个点。

---

## 习题 9

### 题目

设

$$
\mathsf g=
\begin{pmatrix}E&F\\F&G\end{pmatrix},
\qquad
\mathsf b=
\begin{pmatrix}L&M\\M&N\end{pmatrix}.
$$

证明：

1. $\mathsf b\mathsf g^{-1}$ 可用 $\mathbf r_u,\mathbf r_v,\mathbf n_u,\mathbf n_v$ 的叉积形式表示；
2. 若第三基本形式矩阵为
   $$
   \mathsf c=
   \begin{pmatrix}e&f\\f&g\end{pmatrix},
   $$
   则
   $$
   \mathsf c=\mathsf b\mathsf g^{-1}\mathsf b.
   $$

### 解答

记

$$
\Delta=EG-F^2.
$$

### （1）第一恒等式

先直接计算

$$
\mathsf g^{-1}
=
\frac1\Delta
\begin{pmatrix}
G&-F\\
-F&E
\end{pmatrix}.
$$

于是

$$
\mathsf b\mathsf g^{-1}
=
\frac1\Delta
\begin{pmatrix}
LG-MF&ME-LF\\
MG-NF&NE-MF
\end{pmatrix}.
$$

另一方面，

$$
\mathbf n
=
\frac{\mathbf r_u\times\mathbf r_v}{\sqrt\Delta}.
$$

利用向量三重积公式，

$$
\mathbf r_v\times\mathbf n
=
\frac{G\mathbf r_u-F\mathbf r_v}{\sqrt\Delta},
$$

$$
\mathbf r_u\times\mathbf n
=
\frac{F\mathbf r_u-E\mathbf r_v}{\sqrt\Delta}.
$$

又有

$$
\mathbf n_u\cdot\mathbf r_u=-L,
\qquad
\mathbf n_u\cdot\mathbf r_v=-M,
$$

$$
\mathbf n_v\cdot\mathbf r_u=-M,
\qquad
\mathbf n_v\cdot\mathbf r_v=-N.
$$

所以

$$
-\mathbf n_u\cdot(\mathbf r_v\times\mathbf n)
=
\frac{LG-MF}{\sqrt\Delta},
$$

$$
\mathbf n_u\cdot(\mathbf r_u\times\mathbf n)
=
\frac{ME-LF}{\sqrt\Delta},
$$

$$
-\mathbf n_v\cdot(\mathbf r_v\times\mathbf n)
=
\frac{MG-NF}{\sqrt\Delta},
$$

$$
\mathbf n_v\cdot(\mathbf r_u\times\mathbf n)
=
\frac{NE-MF}{\sqrt\Delta}.
$$

因此

$$
\boxed{
\mathsf b\mathsf g^{-1}
=
\frac1{\sqrt\Delta}
\begin{pmatrix}
-\mathbf n_u\cdot(\mathbf r_v\times\mathbf n)&
\mathbf n_u\cdot(\mathbf r_u\times\mathbf n)\\
-\mathbf n_v\cdot(\mathbf r_v\times\mathbf n)&
\mathbf n_v\cdot(\mathbf r_u\times\mathbf n)
\end{pmatrix}.
}
$$

---

### （2）第三基本形式矩阵

第三基本形式为

$$
III=d\mathbf n\cdot d\mathbf n.
$$

其系数矩阵是

$$
\mathsf c
=
\begin{pmatrix}
\mathbf n_u\cdot\mathbf n_u&
\mathbf n_u\cdot\mathbf n_v\\
\mathbf n_v\cdot\mathbf n_u&
\mathbf n_v\cdot\mathbf n_v
\end{pmatrix}.
$$

在坐标基底下，

$$
W=\mathsf g^{-1}\mathsf b.
$$

而

$$
d\mathbf n=-W\,d\mathbf r.
$$

因此

$$
III(\mathbf X,\mathbf Y)
=I(W\mathbf X,W\mathbf Y).
$$

矩阵形式为

$$
\mathsf c
=W^T\mathsf gW.
$$

代入 $W=\mathsf g^{-1}\mathsf b$，并利用 $\mathsf g,\mathsf b$ 对称：

$$
\begin{aligned}
\mathsf c
&=(\mathsf g^{-1}\mathsf b)^T
\mathsf g
(\mathsf g^{-1}\mathsf b)\\
&=\mathsf b\mathsf g^{-1}\mathsf g\mathsf g^{-1}\mathsf b\\
&=\mathsf b\mathsf g^{-1}\mathsf b.
\end{aligned}
$$

故

$$
\boxed{
\begin{pmatrix}e&f\\f&g\end{pmatrix}
=
\begin{pmatrix}L&M\\M&N\end{pmatrix}
\begin{pmatrix}E&F\\F&G\end{pmatrix}^{-1}
\begin{pmatrix}L&M\\M&N\end{pmatrix}.
}
$$

---

# §4.6 某些特殊曲面

## 一、本节知识总结

## 1. 本节研究什么

本节集中讨论两类具有特殊曲率性质的曲面：

1. **Gauss 曲率为常数的曲面**；
2. **平均曲率为零的曲面，即极小曲面**。

其中考试中更常见的是极小曲面。判断一个给定曲面是否为极小曲面，核心就是计算平均曲率 $H$，或者把曲面写成图形 $z=f(x,y)$ 后代入极小曲面方程。

---

## 2. 旋转曲面的曲率公式

考虑旋转曲面

$$
\mathbf r(u,v)
=
\bigl(u\cos v,u\sin v,f(u)\bigr),
\qquad u>0.
$$

先求偏导：

$$
\mathbf r_u=(\cos v,\sin v,f'(u)),
$$

$$
\mathbf r_v=(-u\sin v,u\cos v,0).
$$

因此第一类基本量为

$$
E=1+f'^2,
\qquad F=0,
\qquad G=u^2.
$$

取单位法向量

$$
\mathbf n
=
\frac{1}{\sqrt{1+f'^2}}
\bigl(-f'\cos v,-f'\sin v,1\bigr).
$$

二阶偏导为

$$
\mathbf r_{uu}=(0,0,f''),
$$

$$
\mathbf r_{uv}=(-\sin v,\cos v,0),
$$

$$
\mathbf r_{vv}=(-u\cos v,-u\sin v,0).
$$

所以第二类基本量为

$$
L=\frac{f''}{\sqrt{1+f'^2}},
\qquad M=0,
\qquad N=\frac{uf'}{\sqrt{1+f'^2}}.
$$

由于 $F=M=0$，经线和纬线方向就是主方向。两个主曲率分别为

$$
\boxed{
\kappa_1=
\frac{f''}{(1+f'^2)^{3/2}}
}
$$

和

$$
\boxed{
\kappa_2=
\frac{f'}{u\sqrt{1+f'^2}}
}.
$$

于是

$$
\boxed{
K=\frac{f'f''}{u(1+f'^2)^2}
}
$$

以及

$$
\boxed{
H=\frac{u f''+f'(1+f'^2)}
{2u(1+f'^2)^{3/2}}
}.
$$

法向量反向时，两个主曲率和 $H$ 同时变号，但 $K$ 不变。

---

## 3. 常 Gauss 曲率旋转面

若上述旋转面的 Gauss 曲率恒为常数 $K_0$，则

$$
\frac{f'f''}{u(1+f'^2)^2}=K_0.
$$

令

$$
q(u)=\frac{f'(u)}{\sqrt{1+f'(u)^2}}.
$$

则

$$
q'(u)=\frac{f''(u)}{(1+f'^2)^{3/2}},
$$

从而

$$
q q'
=
\frac{f'f''}{(1+f'^2)^2}.
$$

因此常曲率方程变为

$$
q q'=K_0u.
$$

积分得到

$$
\frac12q^2=\frac12K_0u^2+C,
$$

即

$$
\boxed{
\frac{f'^2}{1+f'^2}=K_0u^2+C_1.
}
$$

这给出了常 Gauss 曲率旋转面的基本积分关系。

典型例子：

- $K=0$：平面、圆柱面、圆锥面等局部可展曲面；
- $K>0$：球面是最典型例子；
- $K<0$：伪球面是最典型例子。

---

## 4. 极小曲面的定义

若曲面的平均曲率恒为零，即

$$
\boxed{H=0,}
$$

则称该曲面为**极小曲面**。

“极小”并不是说曲面整体面积一定最小，而是说曲面在固定边界的小变分下，面积的一阶变化为零。因此极小曲面是面积泛函的临界曲面。

由于

$$
H=\frac{\kappa_1+\kappa_2}{2},
$$

极小曲面满足

$$
\boxed{\kappa_1+\kappa_2=0.}
$$

因此在非平点处，两个主曲率大小相等、符号相反：

$$
\kappa_2=-\kappa_1.
$$

于是

$$
K=\kappa_1\kappa_2=-\kappa_1^2\le 0.
$$

所以极小曲面的 Gauss 曲率不会为正。

---

## 5. 图形曲面的极小曲面方程

设曲面写成图形

$$
z=f(x,y),
$$

参数方程为

$$
\mathbf r(x,y)=(x,y,f(x,y)).
$$

第一类基本量为

$$
E=1+f_x^2,
\qquad F=f_xf_y,
\qquad G=1+f_y^2.
$$

取向上的单位法向量

$$
\mathbf n
=
\frac{(-f_x,-f_y,1)}
{\sqrt{1+f_x^2+f_y^2}}.
$$

于是

$$
L=\frac{f_{xx}}{\sqrt{1+f_x^2+f_y^2}},
$$

$$
M=\frac{f_{xy}}{\sqrt{1+f_x^2+f_y^2}},
$$

$$
N=\frac{f_{yy}}{\sqrt{1+f_x^2+f_y^2}}.
$$

代入平均曲率公式

$$
H=\frac{LG-2MF+NE}{2(EG-F^2)},
$$

得到

$$
H=
\frac{
(1+f_y^2)f_{xx}
-2f_xf_yf_{xy}
+(1+f_x^2)f_{yy}
}
{2(1+f_x^2+f_y^2)^{3/2}}.
$$

所以图形曲面是极小曲面的充分必要条件为

$$
\boxed{
(1+f_y^2)f_{xx}
-2f_xf_yf_{xy}
+(1+f_x^2)f_{yy}=0.
}
$$

这是本节最重要的公式。

---

## 6. 极小旋转面与悬链面

对旋转曲面

$$
\mathbf r(u,v)
=
(u\cos v,u\sin v,f(u)),
$$

极小条件 $H=0$ 为

$$
u f''+f'(1+f'^2)=0.
$$

注意到

$$
\frac{d}{du}
\left(
\frac{u f'}{\sqrt{1+f'^2}}
\right)
=
\frac{f'(1+f'^2)+u f''}{(1+f'^2)^{3/2}},
$$

所以方程可积分为

$$
\frac{u f'}{\sqrt{1+f'^2}}=a,
$$

其中 $a$ 为常数。

若 $a=0$，则 $f'=0$，得到平面。

若 $a\ne0$，则

$$
f'^2=\frac{a^2}{u^2-a^2}.
$$

因此

$$
f'(u)=\pm\frac{a}{\sqrt{u^2-a^2}},
$$

积分得

$$
f(u)=\pm a\operatorname{arcosh}\frac{u}{|a|}+b.
$$

等价地写成

$$
\boxed{
u=|a|\cosh\frac{z-b}{a}.}
$$

这就是悬链线绕轴旋转形成的**悬链面**。

结论：非平面的极小旋转面局部上必为悬链面。

---

## 7. 常见极小曲面

### 7.1 平面

平面的两个主曲率都为零，故 $H=0$。

### 7.2 悬链面

悬链线绕其对称轴旋转所得，是唯一的非平面极小旋转面。

### 7.3 正螺旋面

$$
\mathbf r(u,v)
=
(u\cos v,u\sin v,bv).
$$

它满足 $H=0$。

### 7.4 Scherk 曲面

$$
\boxed{
z=\frac1a
\log\frac{\cos ay}{\cos ax},
\qquad a\ne0.
}
$$

它满足极小曲面方程。

### 7.5 Enneper 曲面

一种常见参数形式为

$$
\boxed{
\mathbf r(u,v)=
\bigl(
3u(1+v^2)-u^3,
3v(1+u^2)-v^3,
3(u^2-v^2)
\bigr).
}
$$

它也是极小曲面。

---

## 8. Gauss 映射保角与极小曲面

设曲面在一点的两个主方向组成单位正交基。在该基下，第一基本形式和第三基本形式分别为

$$
I=(d\xi)^2+(d\eta)^2,
$$

$$
III=\kappa_1^2(d\xi)^2+\kappa_2^2(d\eta)^2.
$$

Gauss 映射保角意味着存在正函数 $\lambda$，使

$$
III=\lambda I.
$$

于是

$$
\kappa_1^2=\kappa_2^2.
$$

因此只有两种可能：

$$
\kappa_1=-\kappa_2,
$$

此时 $H=0$，曲面是极小曲面；或者

$$
\kappa_1=\kappa_2,
$$

此时曲面处处全脐。连通的全脐曲面只能是平面或球面。平面本身也是极小曲面，所以最终结论是：

$$
\boxed{
\text{Gauss 映射保角的曲面，或者是球面，或者是极小曲面。}
}
$$

---

## 二、课后习题逐题详解

## 习题 1

### 题目

证明

$$
z=c\arctan\frac{y}{x}
$$

是极小曲面，并求它的主曲率。

### 解答

这个曲面直接在直角坐标下计算会比较繁琐。注意到

$$
\arctan\frac{y}{x}
$$

正是平面极坐标中的角变量，因此令

$$
x=\rho\cos\theta,
\qquad y=\rho\sin\theta.
$$

曲面可写成

$$
\mathbf r(\rho,\theta)
=
(\rho\cos\theta,\rho\sin\theta,c\theta),
\qquad \rho>0.
$$

这正是正螺旋面的参数形式。

求偏导：

$$
\mathbf r_\rho
=(\cos\theta,\sin\theta,0),
$$

$$
\mathbf r_\theta
=(-\rho\sin\theta,\rho\cos\theta,c).
$$

所以

$$
E=\mathbf r_\rho\cdot\mathbf r_\rho=1,
$$

$$
F=\mathbf r_\rho\cdot\mathbf r_\theta=0,
$$

$$
G=\mathbf r_\theta\cdot\mathbf r_\theta
=\rho^2+c^2.
$$

计算叉积：

$$
\mathbf r_\rho\times\mathbf r_\theta
=
(c\sin\theta,-c\cos\theta,\rho).
$$

其长度为

$$
\sqrt{\rho^2+c^2}.
$$

记

$$
w=\sqrt{\rho^2+c^2},
$$

取单位法向量

$$
\mathbf n
=
\frac1w
(c\sin\theta,-c\cos\theta,\rho).
$$

二阶偏导为

$$
\mathbf r_{\rho\rho}=(0,0,0),
$$

$$
\mathbf r_{\rho\theta}
=(-\sin\theta,\cos\theta,0),
$$

$$
\mathbf r_{\theta\theta}
=(-\rho\cos\theta,-\rho\sin\theta,0).
$$

所以

$$
L=\mathbf r_{\rho\rho}\cdot\mathbf n=0,
$$

$$
M=\mathbf r_{\rho\theta}\cdot\mathbf n
=-\frac{c}{w},
$$

$$
N=\mathbf r_{\theta\theta}\cdot\mathbf n=0.
$$

平均曲率为

$$
H=\frac{LG-2MF+NE}{2(EG-F^2)}.
$$

由于

$$
L=N=F=0,
$$

故

$$
\boxed{H=0.}
$$

所以该曲面是极小曲面。

Gauss 曲率为

$$
K=\frac{LN-M^2}{EG-F^2}
=
-\frac{c^2/w^2}{w^2}.
$$

因此

$$
\boxed{
K=-\frac{c^2}{(\rho^2+c^2)^2}.
}
$$

由于 $H=0$，主曲率满足

$$
\kappa_1+\kappa_2=0,
$$

$$
\kappa_1\kappa_2=K.
$$

所以

$$
\kappa_1^2=-K
=
\frac{c^2}{(\rho^2+c^2)^2}.
$$

按照当前法向量方向，可以取

$$
\boxed{
\kappa_1=\frac{c}{\rho^2+c^2},
\qquad
\kappa_2=-\frac{c}{\rho^2+c^2}.
}
$$

若只写与法向选择无关的形式，则

$$
\boxed{
\{\kappa_1,\kappa_2\}
=
\left\{
\frac{|c|}{\rho^2+c^2},
-\frac{|c|}{\rho^2+c^2}
\right\}.
}
$$

又因为

$$
\rho^2=x^2+y^2,
$$

故也可写成

$$
\boxed{
\kappa_{1,2}
=
\pm\frac{|c|}{x^2+y^2+c^2}.
}
$$

---

## 习题 2

### 题目

1. 证明

$$
z=\frac1a\log\frac{\cos ay}{\cos ax},
\qquad a\ne0,
$$

是极小曲面。该曲面称为 Scherk 曲面。

2. 证明形如

$$
z=f(x)+g(y)
$$

的极小曲面必为 Scherk 曲面或平面。

### 解答

### （1）验证 Scherk 曲面是极小曲面

令

$$
F(x,y)
=
\frac1a
\bigl(\log\cos ay-\log\cos ax\bigr).
$$

求一阶偏导：

$$
F_x
=
\frac1a\cdot a\tan ax
=
\tan ax,
$$

$$
F_y
=
\frac1a\cdot(-a\tan ay)
=
-\tan ay.
$$

再求二阶偏导：

$$
F_{xx}=a\sec^2 ax,
$$

$$
F_{yy}=-a\sec^2 ay,
$$

$$
F_{xy}=0.
$$

极小曲面方程为

$$
(1+F_y^2)F_{xx}
-2F_xF_yF_{xy}
+(1+F_x^2)F_{yy}=0.
$$

代入：

$$
1+F_y^2
=1+\tan^2 ay
=\sec^2 ay,
$$

$$
1+F_x^2
=1+\tan^2 ax
=\sec^2 ax.
$$

因此左端等于

$$
\sec^2 ay\cdot a\sec^2 ax
+
\sec^2 ax\cdot(-a\sec^2 ay).
$$

两项正好抵消，故

$$
0=0.
$$

所以

$$
\boxed{
H=0,
}
$$

Scherk 曲面是极小曲面。

---

### （2）分类形如 $z=f(x)+g(y)$ 的极小曲面

设

$$
z=f(x)+g(y).
$$

则

$$
z_x=f'(x),
\qquad z_y=g'(y),
$$

$$
z_{xx}=f''(x),
\qquad z_{yy}=g''(y),
\qquad z_{xy}=0.
$$

代入极小曲面方程：

$$
\bigl(1+g'^2(y)\bigr)f''(x)
+
\bigl(1+f'^2(x)\bigr)g''(y)=0.
$$

两边除以

$$
\bigl(1+f'^2(x)\bigr)
\bigl(1+g'^2(y)\bigr),
$$

得到

$$
\frac{f''(x)}{1+f'^2(x)}
+
\frac{g''(y)}{1+g'^2(y)}=0.
$$

第一项只依赖 $x$，第二项只依赖 $y$。它们的和对所有 $x,y$ 恒为零，因此两项都必须是常数。设

$$
\frac{f''(x)}{1+f'^2(x)}=a,
$$

$$
\frac{g''(y)}{1+g'^2(y)}=-a.
$$

注意到

$$
\frac{d}{dx}\arctan f'(x)
=
\frac{f''(x)}{1+f'^2(x)},
$$

所以

$$
\arctan f'(x)=ax+b.
$$

从而

$$
f'(x)=\tan(ax+b).
$$

若 $a\ne0$，积分得

$$
f(x)
=-\frac1a\log|\cos(ax+b)|+C_1.
$$

同理，

$$
\frac{d}{dy}\arctan g'(y)=-a,
$$

故

$$
\arctan g'(y)=-ay+d,
$$

$$
g'(y)=\tan(d-ay).
$$

积分得

$$
g(y)
=
\frac1a\log|\cos(d-ay)|+C_2.
$$

因此

$$
z
=
\frac1a
\log
\frac{|\cos(d-ay)|}{|\cos(ax+b)|}
+C.
$$

通过平移 $x,y,z$，可把常数 $b,d,C$ 消去，于是局部上化为

$$
\boxed{
z=\frac1a\log\frac{\cos ay}{\cos ax}.
}
$$

这就是 Scherk 曲面。

若 $a=0$，则

$$
f''=0,
\qquad g''=0.
$$

所以

$$
f(x)=\alpha x+\beta,
$$

$$
g(y)=\gamma y+\delta.
$$

于是

$$
z=\alpha x+\gamma y+C,
$$

它是平面。

故结论为

$$
\boxed{
形如\ z=f(x)+g(y)\ 的极小曲面，
局部上必为 Scherk 曲面或平面。
}
$$

---

## 习题 3

### 题目

1. 证明

$$
\mathbf r(u,v)=
\bigl(
3u(1+v^2)-u^3,
3v(1+u^2)-v^3,
3(u^2-v^2)
\bigr)
$$

是极小曲面。该曲面称为 Enneper 曲面。

2. 证明 Enneper 曲面的曲率线是平面曲线，并求出这些曲线所在的平面。

### 解答

为简化记号，令

$$
q=u^2+v^2.
$$

曲面参数方程为

$$
\mathbf r(u,v)
=
\bigl(
3u+3uv^2-u^3,
3v+3u^2v-v^3,
3u^2-3v^2
\bigr).
$$

### （1）证明它是极小曲面

先求一阶偏导：

$$
\mathbf r_u
=
3(1+v^2-u^2,\,2uv,\,2u),
$$

$$
\mathbf r_v
=
3(2uv,\,1+u^2-v^2,\,-2v).
$$

计算第一类基本量。

首先

$$
\begin{aligned}
E
&=\mathbf r_u\cdot\mathbf r_u\\
&=9\left[
(1+v^2-u^2)^2+4u^2v^2+4u^2
\right].
\end{aligned}
$$

展开并整理：

$$
(1+v^2-u^2)^2+4u^2v^2+4u^2
=(1+u^2+v^2)^2.
$$

所以

$$
E=9(1+q)^2.
$$

类似地，

$$
G=9(1+q)^2.
$$

再算

$$
\begin{aligned}
F
&=\mathbf r_u\cdot\mathbf r_v\\
&=9\bigl[
2uv(1+v^2-u^2)
+2uv(1+u^2-v^2)
-4uv
\bigr]\\
&=0.
\end{aligned}
$$

因此

$$
\boxed{
E=G=9(1+u^2+v^2)^2,
\qquad F=0.
}
$$

计算叉积可得

$$
\mathbf r_u\times\mathbf r_v
=
9(1+q)
(-2u,2v,1-u^2-v^2).
$$

而

$$
4u^2+4v^2+(1-u^2-v^2)^2
=(1+q)^2.
$$

所以单位法向量可取为

$$
\boxed{
\mathbf n
=
\frac{(-2u,2v,1-u^2-v^2)}{1+u^2+v^2}.
}
$$

求二阶偏导：

$$
\mathbf r_{uu}=(-6u,6v,6),
$$

$$
\mathbf r_{uv}=(6v,6u,0),
$$

$$
\mathbf r_{vv}=(6u,-6v,-6).
$$

计算第二类基本量：

$$
\begin{aligned}
L
&=\mathbf r_{uu}\cdot\mathbf n\\
&=\frac{12u^2+12v^2+6(1-u^2-v^2)}{1+q}\\
&=6,
\end{aligned}
$$

$$
\begin{aligned}
M
&=\mathbf r_{uv}\cdot\mathbf n\\
&=\frac{-12uv+12uv}{1+q}\\
&=0,
\end{aligned}
$$

$$
N=\mathbf r_{vv}\cdot\mathbf n=-6.
$$

所以

$$
\boxed{L=6,\qquad M=0,\qquad N=-6.}
$$

平均曲率为

$$
H=\frac{LG-2MF+NE}{2(EG-F^2)}.
$$

由于 $E=G$、$F=M=0$，故

$$
LG+NE=6G-6E=0.
$$

所以

$$
\boxed{H=0.}
$$

因此 Enneper 曲面是极小曲面。

---

### （2）求曲率线所在的平面

由上面的计算，

$$
F=0,
\qquad M=0.
$$

因此参数曲线网既正交，又由主方向组成。也就是说：

- $v=v_0$ 的 $u$-曲线是曲率线；
- $u=u_0$ 的 $v$-曲线是曲率线。

下面分别证明它们是平面曲线。

#### 第一族：$v=v_0$

固定 $v=v_0$，曲线方程为

$$
x=3u(1+v_0^2)-u^3,
$$

$$
y=3v_0(1+u^2)-v_0^3,
$$

$$
z=3(u^2-v_0^2).
$$

计算

$$
\begin{aligned}
y-v_0z
&=3v_0(1+u^2)-v_0^3
-v_0\cdot3(u^2-v_0^2)\\
&=3v_0+3v_0u^2-v_0^3
-3v_0u^2+3v_0^3\\
&=3v_0+2v_0^3.
\end{aligned}
$$

因此整条曲线位于平面

$$
\boxed{
y-v_0z=v_0(3+2v_0^2)
}
$$

内。

#### 第二族：$u=u_0$

固定 $u=u_0$，曲线方程为

$$
x=3u_0(1+v^2)-u_0^3,
$$

$$
y=3v(1+u_0^2)-v^3,
$$

$$
z=3(u_0^2-v^2).
$$

计算

$$
\begin{aligned}
x+u_0z
&=3u_0(1+v^2)-u_0^3
+u_0\cdot3(u_0^2-v^2)\\
&=3u_0+3u_0v^2-u_0^3
+3u_0^3-3u_0v^2\\
&=3u_0+2u_0^3.
\end{aligned}
$$

因此整条曲线位于平面

$$
\boxed{
x+u_0z=u_0(3+2u_0^2)
}
$$

内。

综上，Enneper 曲面的两族曲率线都是平面曲线，其所在平面分别为

$$
\boxed{
y-v_0z=v_0(3+2v_0^2)}
$$

和

$$
\boxed{
x+u_0z=u_0(3+2u_0^2).}
$$

---

## 习题 4

### 题目

1. 证明正螺旋面

$$
\mathbf r(u,v)
=
(u\cos v,u\sin v,bv)
$$

是极小曲面。

2. 证明形如

$$
z=f\left(\frac yx\right)
$$

的极小曲面必为正螺旋面或平面。

### 解答

### （1）证明正螺旋面是极小曲面

设

$$
\mathbf r(u,v)
=(u\cos v,u\sin v,bv).
$$

求偏导：

$$
\mathbf r_u=(\cos v,\sin v,0),
$$

$$
\mathbf r_v=(-u\sin v,u\cos v,b).
$$

所以

$$
E=1,
\qquad F=0,
\qquad G=u^2+b^2.
$$

叉积为

$$
\mathbf r_u\times\mathbf r_v
=(b\sin v,-b\cos v,u).
$$

记

$$
w=\sqrt{u^2+b^2},
$$

取单位法向量

$$
\mathbf n
=
\frac1w(b\sin v,-b\cos v,u).
$$

二阶偏导为

$$
\mathbf r_{uu}=(0,0,0),
$$

$$
\mathbf r_{uv}=(-\sin v,\cos v,0),
$$

$$
\mathbf r_{vv}=(-u\cos v,-u\sin v,0).
$$

于是

$$
L=0,
$$

$$
M=-\frac b w,
$$

$$
N=0.
$$

平均曲率为

$$
H=\frac{LG-2MF+NE}{2(EG-F^2)}=0.
$$

故

$$
\boxed{H=0,}
$$

正螺旋面是极小曲面。

同时

$$
K=\frac{LN-M^2}{EG-F^2}
=-\frac{b^2}{(u^2+b^2)^2}.
$$

---

### （2）分类形如 $z=f(y/x)$ 的极小曲面

令

$$
x=\rho\cos\theta,
\qquad y=\rho\sin\theta.
$$

则

$$
\frac yx=\tan\theta.
$$

设

$$
h(\theta)=f(\tan\theta).
$$

曲面可参数化为

$$
\mathbf r(\rho,\theta)
=
(\rho\cos\theta,\rho\sin\theta,h(\theta)).
$$

求偏导：

$$
\mathbf r_\rho
=(\cos\theta,\sin\theta,0),
$$

$$
\mathbf r_\theta
=(-\rho\sin\theta,\rho\cos\theta,h').
$$

因此

$$
E=1,
\qquad F=0,
\qquad G=\rho^2+h'^2.
$$

叉积为

$$
\mathbf r_\rho\times\mathbf r_\theta
=(h'\sin\theta,-h'\cos\theta,\rho).
$$

记

$$
w=\sqrt{\rho^2+h'^2},
$$

取单位法向量

$$
\mathbf n
=
\frac1w
(h'\sin\theta,-h'\cos\theta,\rho).
$$

二阶偏导：

$$
\mathbf r_{\rho\rho}=(0,0,0),
$$

$$
\mathbf r_{\rho\theta}=(-\sin\theta,\cos\theta,0),
$$

$$
\mathbf r_{\theta\theta}
=(-\rho\cos\theta,-\rho\sin\theta,h'').
$$

所以

$$
L=0,
$$

$$
M=-\frac{h'}w,
$$

$$
N=\frac{\rho h''}{w}.
$$

平均曲率为

$$
H
=
\frac{LG-2MF+NE}{2(EG-F^2)}.
$$

由于 $L=F=0$、$E=1$，得到

$$
H
=
\frac{N}{2G}
=
\frac{\rho h''}
{2(\rho^2+h'^2)^{3/2}}.
$$

极小条件 $H=0$ 对所有 $\rho>0$ 成立，因此

$$
h''(\theta)=0.
$$

从而

$$
h(\theta)=a\theta+b.
$$

于是

$$
z=a\theta+b
=a\arctan\frac yx+b.
$$

当 $a\ne0$ 时，这是正螺旋面的一片；当 $a=0$ 时，这是水平平面。

所以

$$
\boxed{
形如\ z=f(y/x)\ 的极小曲面，
局部上必为正螺旋面或平面。
}
$$

---

## 习题 5

### 题目

证明：如果从曲面到单位球面的 Gauss 映射是保角对应，则该曲面或者是球面，或者是极小曲面。

### 解答

设曲面为 $S$，Gauss 映射为

$$
G:S\longrightarrow S^2.
$$

在曲面上某一点 $p$，取两个彼此正交的单位主方向

$$
\mathbf e_1,\mathbf e_2,
$$

对应主曲率为

$$
\kappa_1,\kappa_2.
$$

在此主方向正交基下，第一基本形式为

$$
I=(d\xi)^2+(d\eta)^2.
$$

Gauss 映射的切映射满足

$$
G_*(\mathbf e_i)
=-\kappa_i\mathbf e_i.
$$

所以 Gauss 映射诱导的度量，也就是第三基本形式，为

$$
III
=
\kappa_1^2(d\xi)^2
+
\kappa_2^2(d\eta)^2.
$$

Gauss 映射保角，意味着存在正函数 $\lambda$，使得

$$
III=\lambda I.
$$

比较两个方向的系数：

$$
\kappa_1^2=\lambda,
$$

$$
\kappa_2^2=\lambda.
$$

因此

$$
\kappa_1^2=\kappa_2^2.
$$

所以有两种可能。

### 情形一

$$
\kappa_1=-\kappa_2.
$$

则

$$
H=\frac{\kappa_1+\kappa_2}{2}=0.
$$

所以曲面是极小曲面。

### 情形二

$$
\kappa_1=\kappa_2.
$$

这说明每一点都是脐点，即 Weingarten 映射为数量映射：

$$
W=\kappa I.
$$

连通的全脐曲面只能是平面或球面。

若 $\kappa=0$，则曲面是平面，而平面本身满足 $H=0$，已经属于极小曲面。

若 $\kappa\ne0$，则曲面是球面的一部分。

因此最终得到

$$
\boxed{
Gauss 映射保角的曲面，
或者是球面，或者是极小曲面。
}
$$

---

## 习题 6

### 题目

推导极小曲面

$$
z=f(x,y)
$$

所满足的微分方程

$$
(1+f_y^2)f_{xx}
-2f_xf_yf_{xy}
+(1+f_x^2)f_{yy}=0.
$$

### 解答

把曲面写成参数形式

$$
\mathbf r(x,y)
=(x,y,f(x,y)).
$$

求一阶偏导：

$$
\mathbf r_x=(1,0,f_x),
$$

$$
\mathbf r_y=(0,1,f_y).
$$

因此第一类基本量为

$$
E=\mathbf r_x\cdot\mathbf r_x
=1+f_x^2,
$$

$$
F=\mathbf r_x\cdot\mathbf r_y
=f_xf_y,
$$

$$
G=\mathbf r_y\cdot\mathbf r_y
=1+f_y^2.
$$

叉积为

$$
\mathbf r_x\times\mathbf r_y
=(-f_x,-f_y,1).
$$

记

$$
W=\sqrt{1+f_x^2+f_y^2},
$$

取向上的单位法向量

$$
\mathbf n
=
\frac{(-f_x,-f_y,1)}W.
$$

二阶偏导为

$$
\mathbf r_{xx}=(0,0,f_{xx}),
$$

$$
\mathbf r_{xy}=(0,0,f_{xy}),
$$

$$
\mathbf r_{yy}=(0,0,f_{yy}).
$$

于是第二类基本量为

$$
L=\frac{f_{xx}}W,
$$

$$
M=\frac{f_{xy}}W,
$$

$$
N=\frac{f_{yy}}W.
$$

先计算

$$
EG-F^2
=(1+f_x^2)(1+f_y^2)-f_x^2f_y^2.
$$

所以

$$
EG-F^2
=1+f_x^2+f_y^2
=W^2.
$$

平均曲率公式为

$$
H
=
\frac{LG-2MF+NE}
{2(EG-F^2)}.
$$

代入：

$$
\begin{aligned}
LG-2MF+NE
&=
\frac1W
\left[
(1+f_y^2)f_{xx}
-2f_xf_yf_{xy}
+(1+f_x^2)f_{yy}
\right].
\end{aligned}
$$

因此

$$
H
=
\frac{
(1+f_y^2)f_{xx}
-2f_xf_yf_{xy}
+(1+f_x^2)f_{yy}
}
{2W^3}.
$$

又因为

$$
W^3=(1+f_x^2+f_y^2)^{3/2}>0,
$$

所以极小条件 $H=0$ 等价于分子为零，即

$$
\boxed{
(1+f_y^2)f_{xx}
-2f_xf_yf_{xy}
+(1+f_x^2)f_{yy}=0.
}
$$

---

## 习题 7

### 题目

将一个旋转曲面 $S$ 沿它的旋转轴平移，得到一个单参数曲面族。

1. 求一个共轴旋转曲面 $S^*$，使得它与上述曲面族中的每一个曲面都垂直相交；
2. 设 $S$ 与 $S^*$ 的 Gauss 曲率分别为 $K$ 与 $K^*$，证明

$$
K=-K^*.
$$

### 解答

不妨设旋转轴为 $z$ 轴，并把原旋转曲面写成

$$
S:
\quad
\mathbf r(u,v)
=
\bigl(f(u)\cos v,f(u)\sin v,u\bigr),
\qquad f(u)>0.
$$

沿 $z$ 轴平移 $t$ 后得到

$$
S_t:
\quad
\mathbf r_t(u,v)
=
\bigl(f(u)\cos v,f(u)\sin v,u+t\bigr).
$$

在经过旋转轴的半平面内，每个 $S_t$ 的母线为

$$
\gamma_t(u)=(f(u),u+t).
$$

其切向量为

$$
\gamma_t'(u)=(f'(u),1).
$$

---

### （1）构造正交相交的共轴旋转面

设所求旋转面 $S^*$ 的母线为

$$
\gamma^*(u)=(f(u),\lambda(u)),
$$

即

$$
S^*:
\quad
\mathbf r^*(u,v)
=
\bigl(f(u)\cos v,f(u)\sin v,\lambda(u)\bigr).
$$

对固定的 $u$，选择

$$
t=\lambda(u)-u,
$$

则 $S^*$ 上的点

$$
\bigl(f(u)\cos v,f(u)\sin v,\lambda(u)\bigr)
$$

恰好也在 $S_t$ 上，因此两曲面沿一个平行圆相交。

$S^*$ 的母线切向量为

$$
( f'(u),\lambda'(u)).
$$

两旋转面沿公共平行圆相交时，它们的夹角等于两条母线在子午平面内的夹角。因此要求垂直相交，只需令

$$
(f'(u),1)\cdot(f'(u),\lambda'(u))=0.
$$

于是

$$
f'(u)^2+\lambda'(u)=0.
$$

即

$$
\lambda'(u)=-f'(u)^2.
$$

积分得到

$$
\boxed{
\lambda(u)
=-\int f'(u)^2\,du+C.
}
$$

因此所求共轴旋转面为

$$
\boxed{
\mathbf r^*(u,v)
=
\left(
 f(u)\cos v,
 f(u)\sin v,
 -\int f'(u)^2\,du+C
\right).
}
$$

---

### （2）证明 $K=-K^*$

先推导一般旋转面的 Gauss 曲率公式。

设

$$
\mathbf R(u,v)
=
\bigl(\rho(u)\cos v,\rho(u)\sin v,z(u)\bigr),
\qquad \rho(u)>0.
$$

求偏导：

$$
\mathbf R_u
=(\rho'\cos v,\rho'\sin v,z'),
$$

$$
\mathbf R_v
=(-\rho\sin v,\rho\cos v,0).
$$

所以

$$
E=\rho'^2+z'^2,
\qquad F=0,
\qquad G=\rho^2.
$$

记

$$
w=\sqrt{\rho'^2+z'^2}.
$$

可取单位法向量

$$
\mathbf n
=\frac1w
(-z'\cos v,-z'\sin v,\rho').
$$

二阶偏导为

$$
\mathbf R_{uu}
=(\rho''\cos v,\rho''\sin v,z''),
$$

$$
\mathbf R_{uv}
=(-\rho'\sin v,\rho'\cos v,0),
$$

$$
\mathbf R_{vv}
=(-\rho\cos v,-\rho\sin v,0).
$$

因此

$$
L=\frac{\rho'z''-z'\rho''}{w},
\qquad M=0,
\qquad N=\frac{\rho z'}w.
$$

代入

$$
K=\frac{LN-M^2}{EG-F^2},
$$

得到

$$
\boxed{
K
=
\frac{z'(\rho'z''-z'\rho'')}
{\rho(\rho'^2+z'^2)^2}.
}
$$

对于原曲面 $S$，有

$$
\rho(u)=f(u),
\qquad z(u)=u.
$$

所以

$$
\rho'=f',
\quad \rho''=f'',
\quad z'=1,
\quad z''=0.
$$

因此

$$
K
=
\frac{1\cdot(f'\cdot0-1\cdot f'')}
{f(1+f'^2)^2}.
$$

即

$$
\boxed{
K=-\frac{f''}{f(1+f'^2)^2}.
}
$$

对于 $S^*$，有

$$
\rho(u)=f(u),
\qquad z(u)=\lambda(u),
$$

并且

$$
\lambda'=-f'^2,
$$

$$
\lambda''=-2f'f''.
$$

代入一般公式：

$$
K^*
=
\frac{
\lambda'\bigl(f'\lambda''-\lambda'f''\bigr)
}
{f(f'^2+\lambda'^2)^2}.
$$

先化简分子中的括号：

$$
\begin{aligned}
f'\lambda''-\lambda'f''
&=f'(-2f'f'')-(-f'^2)f''\\
&=-2f'^2f''+f'^2f''\\
&=-f'^2f''.
\end{aligned}
$$

所以分子为

$$
\lambda'(-f'^2f'')
=(-f'^2)(-f'^2f'')
=f'^4f''.
$$

分母为

$$
\begin{aligned}
f(f'^2+\lambda'^2)^2
&=f(f'^2+f'^4)^2\\
&=f\bigl(f'^2(1+f'^2)\bigr)^2\\
&=ff'^4(1+f'^2)^2.
\end{aligned}
$$

因此在 $f'\ne0$ 的点，

$$
K^*
=
\frac{f'^4f''}
{ff'^4(1+f'^2)^2}
=
\frac{f''}{f(1+f'^2)^2}.
$$

故

$$
\boxed{
K^*=-K.
}
$$

上述构造和曲率计算在 $f'\neq0$ 的正则区间内成立；若曲面可用其他正则参数延拓到端点，则曲率恒等式再由连续性延拓。原参数在 $f'=0$ 处退化时，不能直接用该参数式计算 $K^*$。

因此所构造的两个共轴旋转面在对应交点处满足

$$
\boxed{K=-K^*.}
$$
