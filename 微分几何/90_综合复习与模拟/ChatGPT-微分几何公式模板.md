# 微分几何公式模板

**User:** Anonymous  
**Created:** 7/3/2026 14:42:35  
**Updated:** 7/3/2026 14:45:16  
**Exported:** 7/3/2026 17:12:13  
**Link:** [https://chatgpt.com/c/6a4759c0-e9dc-83ee-b0ff-046aad9bd549](https://chatgpt.com/c/6a4759c0-e9dc-83ee-b0ff-046aad9bd549)  

## Response:
2026/7/3 14:42:35

我按期末做题口径整理：从正则曲面、第一基本形式开始，到第二基本形式、曲率、测地线、曲面方程。重点放在“题目里能直接套”的公式。

> **提供微分几何曲面论公式模板**
>
> 用户请求“微分几何曲面论开始所有做题公式默写模板，附上答案”，应该希望得到一个配有答案的公式填空模板。可能需要涵盖从曲面论开始的内容，包括正则曲面、第一基本形式、曲面上的曲线等。我打算创建一个结构化的模板，并在每个公式旁留有空白，以便补充答案。
>
> **草拟微分几何公式模板**
>
> 我打算创建一个简洁但全面的微分几何公式模板，使用Markdown格式。包括必要的定义，如r_u, r_v，正则条件r_u × r_v != 0，以及切平面方程和单位法向量等。模板还将涵盖第一基本形式，曲线长度公式和角度公式等内容。在草拟时会确保公式正确且易于理解。
>
> **推导曲面上的法向曲率和主曲率**
>
> 在推导法向曲率时，设定 \( n_u = a r_u + b r_v \)，通过与 \( r_u \) 和 \( r_v \) 点乘得到系数。然后得出曲率相关公式，主曲率和平均曲率的计算方法，以及二次形式与高斯曲率的公式。最后，探索主方向方程，整理相关公式和矩阵。
>
> 已思考 1m 14s

下面这份可以直接当“公式默写模板”。复习时先遮住答案列，只看“默写模板”填空。

# 微分几何曲面论做题公式默写模板

## 0. 基本记号

| 默写模板 | 答案 |
|---|---|
| 参数曲面记为：$\mathbf r=\underline{\qquad}$ | $\mathbf r=\mathbf r(u,v)$ |
| 两个切向量：$\mathbf r_1=\underline{\qquad},\ \mathbf r_2=\underline{\qquad}$ | $\mathbf r_u,\ \mathbf r_v$ |
| 正则曲面的判定条件：$\underline{\qquad}$ | $\mathbf r_u\times \mathbf r_v\ne 0$ |
| 单位法向量：$\mathbf n=\underline{\qquad}$ | $\displaystyle \mathbf n=\frac{\mathbf r_u\times \mathbf r_v}{|\mathbf r_u\times \mathbf r_v|}$ |
| 切平面方程：$\underline{\qquad}$ | $(\mathbf X-\mathbf r(u_0,v_0))\cdot \mathbf n=0$ |
| 切平面的一般参数式：$\mathbf X=\underline{\qquad}$ | $\mathbf X=\mathbf r(u_0,v_0)+a\mathbf r_u+b\mathbf r_v$ |

---

# 一、第一基本形式

## 1. 第一基本量

| 默写模板 | 答案 |
|---|---|
| $E=\underline{\qquad}$ | $E=\mathbf r_u\cdot \mathbf r_u$ |
| $F=\underline{\qquad}$ | $F=\mathbf r_u\cdot \mathbf r_v$ |
| $G=\underline{\qquad}$ | $G=\mathbf r_v\cdot \mathbf r_v$ |
| 第一基本形式：$I=\underline{\qquad}$ | $I=E\,du^2+2F\,du\,dv+G\,dv^2$ |
| 第一基本形式矩阵：$(g_{ij})=\underline{\qquad}$ | $\displaystyle (g_{ij})=\begin{pmatrix}E&F\\F&G\end{pmatrix}$ |
| 面积元：$dA=\underline{\qquad}$ | $\displaystyle dA=\sqrt{EG-F^2}\,du\,dv$ |
| $|\mathbf r_u\times \mathbf r_v|^2=\underline{\qquad}$ | $|\mathbf r_u\times \mathbf r_v|^2=EG-F^2$ |

---

## 2. 曲面上曲线的弧长

设曲线  
$$
\gamma(t)=\mathbf r(u(t),v(t)).
$$

| 默写模板 | 答案 |
|---|---|
| $\gamma'(t)=\underline{\qquad}$ | $\gamma'=\mathbf r_u u'+\mathbf r_v v'$ |
| 曲线速度：$\left|\gamma'(t)\right|=\underline{\qquad}$ | $\displaystyle \sqrt{E(u')^2+2Fu'v'+G(v')^2}$ |
| 弧长公式：$s=\underline{\qquad}$ | $\displaystyle s=\int_a^b\sqrt{E(u')^2+2Fu'v'+G(v')^2}\,dt$ |
| 若用 $v=v(u)$，则 $ds=\underline{\qquad}$ | $\displaystyle ds=\sqrt{E+2Fv'+G(v')^2}\,du$ |
| 若用 $u=u(v)$，则 $ds=\underline{\qquad}$ | $\displaystyle ds=\sqrt{E(u')^2+2Fu'+G}\,dv$ |

---

## 3. 角度公式

设两个方向分别为  
$$
du:dv,\qquad \delta u:\delta v.
$$

| 默写模板 | 答案 |
|---|---|
| 两方向夹角满足：$\cos\theta=\underline{\qquad}$ | $\displaystyle \cos\theta=\frac{E\,du\,\delta u+F(du\,\delta v+dv\,\delta u)+G\,dv\,\delta v}{\sqrt{E\,du^2+2Fdu\,dv+Gdv^2}\sqrt{E\,\delta u^2+2F\delta u\,\delta v+G\delta v^2}}$ |
| 两方向正交条件：$\underline{\qquad}=0$ | $E\,du\,\delta u+F(du\,\delta v+dv\,\delta u)+G\,dv\,\delta v=0$ |
| 坐标曲线 $u=\text{常数}$ 与 $v=\text{常数}$ 正交条件：$\underline{\qquad}$ | $F=0$ |

---

## 4. 面积公式

| 默写模板 | 答案 |
|---|---|
| 曲面面积公式：$A=\underline{\qquad}$ | $\displaystyle A=\iint_D \sqrt{EG-F^2}\,du\,dv$ |
| 若 $F=0$，面积元 $dA=\underline{\qquad}$ | $\displaystyle dA=\sqrt{EG}\,du\,dv$ |

---

## 5. 保长、保角、等距

| 默写模板 | 答案 |
|---|---|
| 两曲面等距的判定：$\underline{\qquad}$ | 第一基本形式相同，即 $E=\bar E,\ F=\bar F,\ G=\bar G$ |
| 保角映射判定：$\underline{\qquad}$ | 第一基本形式只差一个正函数因子：$\bar I=\lambda^2 I$ |
| 等温坐标条件：$\underline{\qquad}$ | $F=0,\ E=G$ |
| 正交坐标条件：$\underline{\qquad}$ | $F=0$ |

---

# 二、第二基本形式

## 1. 第二基本量

| 默写模板 | 答案 |
|---|---|
| $L=\underline{\qquad}$ | $L=\mathbf r_{uu}\cdot \mathbf n$ |
| $M=\underline{\qquad}$ | $M=\mathbf r_{uv}\cdot \mathbf n$ |
| $N=\underline{\qquad}$ | $N=\mathbf r_{vv}\cdot \mathbf n$ |
| 第二基本形式：$II=\underline{\qquad}$ | $II=L\,du^2+2M\,du\,dv+N\,dv^2$ |
| 第二基本形式矩阵：$(b_{ij})=\underline{\qquad}$ | $\displaystyle (b_{ij})=\begin{pmatrix}L&M\\M&N\end{pmatrix}$ |
| 另一组公式：$L=-\underline{\qquad}$ | $L=-\mathbf r_u\cdot \mathbf n_u$ |
| $M=-\underline{\qquad}=-\underline{\qquad}$ | $M=-\mathbf r_u\cdot \mathbf n_v=-\mathbf r_v\cdot \mathbf n_u$ |
| $N=-\underline{\qquad}$ | $N=-\mathbf r_v\cdot \mathbf n_v$ |

---

## 2. 法曲率

设方向为  
$$
du:dv.
$$

| 默写模板 | 答案 |
|---|---|
| 法曲率公式：$k_n=\underline{\qquad}$ | $\displaystyle k_n=\frac{II}{I}=\frac{Ldu^2+2Mdu\,dv+Ndv^2}{Edu^2+2Fdu\,dv+Gdv^2}$ |
| 若方向写成 $dv/du=p$，则 $k_n=\underline{\qquad}$ | $\displaystyle k_n=\frac{L+2Mp+Np^2}{E+2Fp+Gp^2}$ |
| 若曲线为单位速曲线 $\gamma(s)$，则 $k_n=\underline{\qquad}$ | $\displaystyle k_n=\gamma''(s)\cdot \mathbf n$ |

---

# 三、曲率公式

## 1. 高斯曲率与平均曲率

| 默写模板 | 答案 |
|---|---|
| 高斯曲率：$K=\underline{\qquad}$ | $\displaystyle K=\frac{LN-M^2}{EG-F^2}$ |
| 平均曲率：$H=\underline{\qquad}$ | $\displaystyle H=\frac{EN-2FM+GL}{2(EG-F^2)}$ |
| 主曲率满足方程：$\underline{\qquad}$ | $k^2-2Hk+K=0$ |
| 主曲率：$k_{1,2}=\underline{\qquad}$ | $\displaystyle k_{1,2}=H\pm\sqrt{H^2-K}$ |
| $K$ 与主曲率关系：$\underline{\qquad}$ | $K=k_1k_2$ |
| $H$ 与主曲率关系：$\underline{\qquad}$ | $\displaystyle H=\frac{k_1+k_2}{2}$ |

---

## 2. 主方向与曲率线

| 默写模板                                                     | 答案                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| 主方向满足：$\underline{\qquad}$                             | $II-kI=0$，即 $(L-kE)du^2+2(M-kF)du\,dv+(N-kG)dv^2=0$        |
| 主曲率方程的行列式形式：$\underline{\qquad}=0$               | $\displaystyle \begin{vmatrix}L-kE&M-kF\\M-kF&N-kG\end{vmatrix}=0$ |
| 曲率线微分方程：$\underline{\qquad}=0$                       | $$(EM-FL)du^2+(EN-GL)du\,dv+(FN-GM)dv^2=0$$                  |
| 若坐标网正交，即 $F=0$，坐标曲线为曲率线的条件：$\underline{\qquad}$ | $M=0$                                                        |
| 欧拉公式：$k_n=\underline{\qquad}$                           | $k_n=k_1\cos^2\theta+k_2\sin^2\theta$                        |

---

## 3. 渐近方向与渐近线

| 默写模板 | 答案 |
|---|---|
| 渐近方向定义：$\underline{\qquad}$ | 法曲率 $k_n=0$ 的方向 |
| 渐近方向方程：$\underline{\qquad}=0$ | $Ldu^2+2Mdu\,dv+Ndv^2=0$ |
| 用 $p=dv/du$ 表示：$\underline{\qquad}=0$ | $L+2Mp+Np^2=0$ |
| 存在两个实渐近方向的条件：$\underline{\qquad}$ | $K<0$ |
| 抛物点处渐近方向情况：$\underline{\qquad}$ | $K=0$，一般只有一个渐近方向 |
| 椭圆点处渐近方向情况：$\underline{\qquad}$ | $K>0$，没有实渐近方向 |

---

## 4. 共轭方向

设两个方向为  
$$
du:dv,\qquad \delta u:\delta v.
$$

| 默写模板 | 答案 |
|---|---|
| 共轭方向条件：$\underline{\qquad}=0$ | $Ldu\,\delta u+M(du\,\delta v+dv\,\delta u)+Ndv\,\delta v=0$ |
| 若两个坐标方向共轭，则条件为：$\underline{\qquad}$ | $M=0$ |
| 主方向与共轭方向关系：$\underline{\qquad}$ | 主方向是一对互相正交的共轭方向 |

---

# 四、Weingarten 变换与基本方程

## 1. Weingarten 变换

| 默写模板 | 答案 |
|---|---|
| Weingarten 变换定义：$S=\underline{\qquad}$ | $S=-d\mathbf n$ |
| 第二基本形式与 $S$ 的关系：$\underline{\qquad}$ | $II(X,Y)=I(SX,Y)$ |
| $S$ 的矩阵：$\underline{\qquad}$ | $\displaystyle S=(g_{ij})^{-1}(b_{ij})$ |
| 展开为矩阵：$S=\underline{\qquad}$ | $\displaystyle S=\frac1{EG-F^2}\begin{pmatrix}G&-F\\-F&E\end{pmatrix}\begin{pmatrix}L&M\\M&N\end{pmatrix}$ |
| 主曲率是 $S$ 的：$\underline{\qquad}$ | 特征值 |
| 主方向是 $S$ 的：$\underline{\qquad}$ | 特征向量 |

---

## 2. Gauss 公式

| 默写模板 | 答案 |
|---|---|
| $\mathbf r_{uu}=\underline{\qquad}$ | $\mathbf r_{uu}=\Gamma^1_{11}\mathbf r_u+\Gamma^2_{11}\mathbf r_v+L\mathbf n$ |
| $\mathbf r_{uv}=\underline{\qquad}$ | $\mathbf r_{uv}=\Gamma^1_{12}\mathbf r_u+\Gamma^2_{12}\mathbf r_v+M\mathbf n$ |
| $\mathbf r_{vv}=\underline{\qquad}$ | $\mathbf r_{vv}=\Gamma^1_{22}\mathbf r_u+\Gamma^2_{22}\mathbf r_v+N\mathbf n$ |

---

## 3. Christoffel 符号

| 默写模板 | 答案 |
|---|---|
| Christoffel 符号通式：$\Gamma^k_{ij}=\underline{\qquad}$ | $\displaystyle \Gamma^k_{ij}=\frac12 g^{kl}\left(\frac{\partial g_{jl}}{\partial u^i}+\frac{\partial g_{il}}{\partial u^j}-\frac{\partial g_{ij}}{\partial u^l}\right)$ |
| 其中 $(g^{ij})=\underline{\qquad}$ | $(g^{ij})=(g_{ij})^{-1}$ |
| $g_{ij}$ 矩阵为：$\underline{\qquad}$ | $\displaystyle \begin{pmatrix}E&F\\F&G\end{pmatrix}$ |

---

# 五、测地线

## 1. 测地线定义

| 默写模板 | 答案 |
|---|---|
| 曲面曲线的曲率分解：$\underline{\qquad}$ | $k^2=k_n^2+k_g^2$ |
| 测地线定义：$\underline{\qquad}$ | 测地曲率 $k_g=0$ 的曲线 |
| 单位速曲线是测地线等价于：$\underline{\qquad}$ | $\gamma''(s)$ 平行于曲面法向量 $\mathbf n$ |
| 测地线直观含义：$\underline{\qquad}$ | 曲面上的“最直曲线”或局部最短线的候选 |

---

## 2. 测地线方程

设曲线  
$$
\gamma(s)=\mathbf r(u(s),v(s))
$$
以弧长 $s$ 为参数。

| 默写模板 | 答案 |
|---|---|
| 第一条测地线方程：$\underline{\qquad}$ | $\displaystyle u''+\Gamma^1_{11}(u')^2+2\Gamma^1_{12}u'v'+\Gamma^1_{22}(v')^2=0$ |
| 第二条测地线方程：$\underline{\qquad}$ | $\displaystyle v''+\Gamma^2_{11}(u')^2+2\Gamma^2_{12}u'v'+\Gamma^2_{22}(v')^2=0$ |

---

## 3. 测地曲率公式

| 默写模板 | 答案 |
|---|---|
| 单位速曲线测地曲率：$k_g=\underline{\qquad}$ | $\displaystyle k_g=\gamma''(s)\cdot(\mathbf n\times \gamma'(s))$ |
| 曲线是测地线的判定：$\underline{\qquad}$ | $k_g=0$ |
| 平面曲线作为曲面曲线时，若曲率向量总沿曲面法向，则：$\underline{\qquad}$ | 它是测地线 |

---

# 六、常见特殊曲面公式

## 1. 图形曲面 $z=f(x,y)$

设  
$$
\mathbf r(x,y)=(x,y,f(x,y)).
$$

| 默写模板 | 答案 |
|---|---|
| $\mathbf r_x=\underline{\qquad}$ | $(1,0,f_x)$ |
| $\mathbf r_y=\underline{\qquad}$ | $(0,1,f_y)$ |
| $E=\underline{\qquad}$ | $1+f_x^2$ |
| $F=\underline{\qquad}$ | $f_xf_y$ |
| $G=\underline{\qquad}$ | $1+f_y^2$ |
| 单位法向量：$\mathbf n=\underline{\qquad}$ | $\displaystyle \frac{(-f_x,-f_y,1)}{\sqrt{1+f_x^2+f_y^2}}$ |
| $L=\underline{\qquad}$ | $\displaystyle \frac{f_{xx}}{\sqrt{1+f_x^2+f_y^2}}$ |
| $M=\underline{\qquad}$ | $\displaystyle \frac{f_{xy}}{\sqrt{1+f_x^2+f_y^2}}$ |
| $N=\underline{\qquad}$ | $\displaystyle \frac{f_{yy}}{\sqrt{1+f_x^2+f_y^2}}$ |
| 高斯曲率：$K=\underline{\qquad}$ | $\displaystyle K=\frac{f_{xx}f_{yy}-f_{xy}^2}{(1+f_x^2+f_y^2)^2}$ |
| 平均曲率：$H=\underline{\qquad}$ | $\displaystyle H=\frac{(1+f_y^2)f_{xx}-2f_xf_yf_{xy}+(1+f_x^2)f_{yy}}{2(1+f_x^2+f_y^2)^{3/2}}$ |

---

## 2. 旋转曲面

设  
$$
\mathbf r(u,v)=(f(u)\cos v,\ f(u)\sin v,\ g(u)).
$$

| 默写模板 | 答案 |
|---|---|
| $E=\underline{\qquad}$ | $f'^2+g'^2$ |
| $F=\underline{\qquad}$ | $0$ |
| $G=\underline{\qquad}$ | $f^2$ |
| 单位法向量：$\mathbf n=\underline{\qquad}$ | $\displaystyle \frac{(-g'\cos v,-g'\sin v,f')}{\sqrt{f'^2+g'^2}}$ |
| $L=\underline{\qquad}$ | $\displaystyle \frac{f'g''-f''g'}{\sqrt{f'^2+g'^2}}$ |
| $M=\underline{\qquad}$ | $0$ |
| $N=\underline{\qquad}$ | $\displaystyle \frac{fg'}{\sqrt{f'^2+g'^2}}$ |
| 若母线弧长参数，即 $f'^2+g'^2=1$，则主曲率为：$\underline{\qquad}$ | $\displaystyle k_1=f'g''-f''g',\quad k_2=\frac{g'}{f}$ |
| 若 $F=M=0$，则主曲率：$\underline{\qquad}$ | $\displaystyle k_1=\frac LE,\quad k_2=\frac NG$ |

符号可能随法向量选择改变，但 $K=k_1k_2$ 不变，$H$ 会随法向反向而变号。

---

## 3. 正交参数曲面

若  
$$
F=0.
$$

| 默写模板 | 答案 |
|---|---|
| 第一基本形式：$I=\underline{\qquad}$ | $I=E\,du^2+G\,dv^2$ |
| 面积元：$dA=\underline{\qquad}$ | $\sqrt{EG}\,du\,dv$ |
| 若 $M=0$，则主曲率：$\underline{\qquad}$ | $\displaystyle k_1=\frac LE,\quad k_2=\frac NG$ |
| 高斯曲率：$K=\underline{\qquad}$ | $\displaystyle K=\frac{LN-M^2}{EG}$ |
| 若 $F=M=0$，则 $K=\underline{\qquad}$ | $\displaystyle K=\frac LE\cdot \frac NG$ |

---

## 4. 等温参数曲面

若  
$$
E=G=\lambda^2,\qquad F=0.
$$

| 默写模板 | 答案 |
|---|---|
| 第一基本形式：$I=\underline{\qquad}$ | $I=\lambda^2(du^2+dv^2)$ |
| 面积元：$dA=\underline{\qquad}$ | $\lambda^2\,du\,dv$ |
| 高斯曲率：$K=\underline{\qquad}$ | $\displaystyle K=-\frac{1}{\lambda^2}\Delta \ln \lambda$ |
| 其中 $\Delta=\underline{\qquad}$ | $\displaystyle \Delta=\frac{\partial^2}{\partial u^2}+\frac{\partial^2}{\partial v^2}$ |

---

## 5. 特殊正交形式

若  
$$
ds^2=du^2+f(u)^2dv^2.
$$

| 默写模板 | 答案 |
|---|---|
| 高斯曲率：$K=\underline{\qquad}$ | $\displaystyle K=-\frac{f''(u)}{f(u)}$ |

若  
$$
ds^2=E(u,v)du^2+G(u,v)dv^2.
$$

| 默写模板 | 答案 |
|---|---|
| 正交坐标高斯曲率：$K=\underline{\qquad}$ | $\displaystyle K=-\frac{1}{2\sqrt{EG}}\left[\frac{\partial}{\partial u}\left(\frac{G_u}{\sqrt{EG}}\right)+\frac{\partial}{\partial v}\left(\frac{E_v}{\sqrt{EG}}\right)\right]$ |

---

# 七、极小曲面、可展曲面、脐点

## 1. 极小曲面

| 默写模板 | 答案 |
|---|---|
| 极小曲面的判定：$\underline{\qquad}$ | $H=0$ |
| 图形曲面 $z=f(x,y)$ 是极小曲面的方程：$\underline{\qquad}=0$ | $(1+f_y^2)f_{xx}-2f_xf_yf_{xy}+(1+f_x^2)f_{yy}=0$ |

---

## 2. 可展曲面

| 默写模板 | 答案 |
|---|---|
| 可展曲面的核心判定：$\underline{\qquad}$ | $K=0$ |
| 即：$\underline{\qquad}=0$ | $LN-M^2=0$ |
| 圆柱面、圆锥面、切线曲面通常属于：$\underline{\qquad}$ | 可展曲面 |

---

## 3. 脐点

| 默写模板 | 答案 |
|---|---|
| 脐点定义：$\underline{\qquad}$ | 两个主曲率相等，即 $k_1=k_2$ |
| 脐点等价条件：$\underline{\qquad}$ | 所有方向法曲率相同 |
| 球面上每一点都是：$\underline{\qquad}$ | 脐点 |
| 平面上每一点也是：$\underline{\qquad}$ | 脐点，且 $k_1=k_2=0$ |

---

# 八、曲面点的分类

| 默写模板 | 答案 |
|---|---|
| 椭圆点条件：$\underline{\qquad}$ | $K>0$ |
| 双曲点条件：$\underline{\qquad}$ | $K<0$ |
| 抛物点条件：$\underline{\qquad}$ | $K=0$，且第二基本形式不全为零 |
| 平点条件：$\underline{\qquad}$ | $L=M=N=0$ |
| 椭圆点渐近方向数量：$\underline{\qquad}$ | 无实渐近方向 |
| 双曲点渐近方向数量：$\underline{\qquad}$ | 两个实渐近方向 |
| 抛物点渐近方向数量：$\underline{\qquad}$ | 一般一个实渐近方向 |

---

# 九、常见题型公式路线

## 题型 1：给参数曲面，求 $E,F,G,L,M,N,K,H$

默写流程：

$$
\boxed{
\mathbf r_u,\mathbf r_v
\Rightarrow 
\mathbf n
\Rightarrow 
E,F,G
\Rightarrow 
\mathbf r_{uu},\mathbf r_{uv},\mathbf r_{vv}
\Rightarrow 
L,M,N
\Rightarrow 
K,H
}
$$

答案公式：

$$
E=\mathbf r_u^2,\quad F=\mathbf r_u\cdot \mathbf r_v,\quad G=\mathbf r_v^2.
$$

$$
\mathbf n=\frac{\mathbf r_u\times \mathbf r_v}{|\mathbf r_u\times \mathbf r_v|}.
$$

$$
L=\mathbf r_{uu}\cdot\mathbf n,\quad M=\mathbf r_{uv}\cdot\mathbf n,\quad N=\mathbf r_{vv}\cdot\mathbf n.
$$

$$
K=\frac{LN-M^2}{EG-F^2}.
$$

$$
H=\frac{EN-2FM+GL}{2(EG-F^2)}.
$$

---

## 题型 2：求曲面上曲线弧长

模板：

$$
\gamma(t)=\mathbf r(u(t),v(t)).
$$

$$
s=\int \underline{\qquad}\,dt.
$$

答案：

$$
s=\int \sqrt{E(u')^2+2Fu'v'+G(v')^2}\,dt.
$$

---

## 题型 3：求面积

模板：

$$
A=\iint_D \underline{\qquad}\,du\,dv.
$$

答案：

$$
A=\iint_D\sqrt{EG-F^2}\,du\,dv.
$$

---

## 题型 4：判断保长、保角

模板：

$$
I=E\,du^2+2Fdu\,dv+G\,dv^2.
$$

两曲面等距：

$$
\underline{\qquad}
$$

两曲面保角：

$$
\underline{\qquad}
$$

答案：

$$
\text{等距：} I=\bar I.
$$

$$
\text{保角：} \bar I=\lambda^2 I.
$$

---

## 题型 5：求法曲率

模板：

方向 $du:dv$ 的法曲率为：

$$
k_n=\underline{\qquad}
$$

答案：

$$
k_n=\frac{Ldu^2+2Mdu\,dv+Ndv^2}{Edu^2+2Fdu\,dv+Gdv^2}.
$$

---

## 题型 6：求主曲率

模板：

$$
K=\underline{\qquad},\qquad H=\underline{\qquad}.
$$

$$
k_{1,2}=\underline{\qquad}.
$$

答案：

$$
K=\frac{LN-M^2}{EG-F^2},
$$

$$
H=\frac{EN-2FM+GL}{2(EG-F^2)},
$$

$$
k_{1,2}=H\pm\sqrt{H^2-K}.
$$

---

## 题型 7：求渐近线

模板：

渐近方向满足：

$$
\underline{\qquad}=0.
$$

答案：

$$
Ldu^2+2Mdu\,dv+Ndv^2=0.
$$

若设 $p=dv/du$，则：

$$
L+2Mp+Np^2=0.
$$

---

## 题型 8：求曲率线

模板：

曲率线微分方程：

$$
\underline{\qquad}=0.
$$

答案：

$$
(EM-FL)du^2+(EN-GL)du\,dv+(FN-GM)dv^2=0.
$$

若 $F=0$，常用简化：

$$
M=0 \Longrightarrow \text{坐标曲线是曲率线}.
$$

---

## 题型 9：求测地线

模板：

测地线方程为：

$$
u''+\underline{\qquad}=0,
$$

$$
v''+\underline{\qquad}=0.
$$

答案：

$$
u''+\Gamma^1_{11}(u')^2+2\Gamma^1_{12}u'v'+\Gamma^1_{22}(v')^2=0,
$$

$$
v''+\Gamma^2_{11}(u')^2+2\Gamma^2_{12}u'v'+\Gamma^2_{22}(v')^2=0.
$$

---

# 十、最核心必背清单

考试前优先默写这些：

$$
\boxed{
E=\mathbf r_u^2,\quad F=\mathbf r_u\cdot\mathbf r_v,\quad G=\mathbf r_v^2
}
$$

$$
\boxed{
I=Edu^2+2Fdu\,dv+Gdv^2
}
$$

$$
\boxed{
dA=\sqrt{EG-F^2}\,du\,dv
}
$$

$$
\boxed{
\mathbf n=\frac{\mathbf r_u\times\mathbf r_v}{|\mathbf r_u\times\mathbf r_v|}
}
$$

$$
\boxed{
L=\mathbf r_{uu}\cdot\mathbf n,\quad M=\mathbf r_{uv}\cdot\mathbf n,\quad N=\mathbf r_{vv}\cdot\mathbf n
}
$$

$$
\boxed{
II=Ldu^2+2Mdu\,dv+Ndv^2
}
$$

$$
\boxed{
k_n=\frac{II}{I}
}
$$

$$
\boxed{
K=\frac{LN-M^2}{EG-F^2}
}
$$

$$
\boxed{
H=\frac{EN-2FM+GL}{2(EG-F^2)}
}
$$

$$
\boxed{
k_{1,2}=H\pm\sqrt{H^2-K}
}
$$

$$
\boxed{
\text{渐近线： }Ldu^2+2Mdu\,dv+Ndv^2=0
}
$$

$$
\boxed{
\text{曲率线： }(EM-FL)du^2+(EN-GL)du\,dv+(FN-GM)dv^2=0
}
$$

$$
\boxed{
\text{测地线： }
u''+\Gamma^1_{11}(u')^2+2\Gamma^1_{12}u'v'+\Gamma^1_{22}(v')^2=0
}
$$

$$
\boxed{
v''+\Gamma^2_{11}(u')^2+2\Gamma^2_{12}u'v'+\Gamma^2_{22}(v')^2=0
}
$$

---

# 十一、做题时的固定顺序

遇到任何曲面论计算题，按这个顺序写：

$$
\boxed{
1.\ \mathbf r_u,\mathbf r_v
}
$$

$$
\boxed{
2.\ E,F,G
}
$$

$$
\boxed{
3.\ \mathbf n
}
$$

$$
\boxed{
4.\ \mathbf r_{uu},\mathbf r_{uv},\mathbf r_{vv}
}
$$

$$
\boxed{
5.\ L,M,N
}
$$

$$
\boxed{
6.\ K,H,k_1,k_2
}
$$

$$
\boxed{
7.\ 按题目要求求面积、弧长、渐近线、曲率线、测地线
}
$$

这套顺序基本覆盖曲面论大部分计算题。



---
Powered by [ChatGPT Exporter](https://www.chatgptexporter.com)