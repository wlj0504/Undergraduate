# 分式线性函数讲解

**User:** Anonymous  
**Created:** 7/5/2026 1:46:11  
**Updated:** 7/5/2026 1:47:20  
**Exported:** 7/5/2026 1:49:07  
**Link:** [https://chatgpt.com/c/6a4946d1-01b8-83ee-802c-ccdaa807b601](https://chatgpt.com/c/6a4946d1-01b8-83ee-802c-ccdaa807b601)  

## Response:
2026/7/5 01:46:11

我按“期末做题能用”的方式讲：先把分式线性变换拆成基本变换，再给区域映射题的固定流程，最后列常见模板和例题。

> **解释分式线性变换**
>
> 用户希望了解分式线性变换映射，尤其在考试中应用。这里不需要互联网资源，因为数学是稳定的。可以通过简洁有结构的方式解释，但包括练习可能更好。虽然没有工具，但我可以直接提供详细的答案，例如Mobius变换的公式和应用。
>
> 已思考 21s

## 1. 分式线性函数到底是什么

分式线性变换，也叫 Möbius 变换：

$$
w=f(z)=\frac{az+b}{cz+d},\qquad ad-bc\neq 0
$$

其中 $a,b,c,d\in \mathbb C$。

它作用在扩充复平面上：

$$
\widehat{\mathbb C}=\mathbb C\cup\{\infty\}
$$

特殊点要记住：

$$
z=-\frac dc \quad \Longmapsto \quad w=\infty
$$

$$
z=\infty \quad \Longmapsto \quad w=\frac ac
$$

如果 $c=0$，就是普通的一次函数：

$$
w=\frac ad z+\frac bd
$$

---

## 2. 最核心结论：广义圆映成广义圆

广义圆指：

$$
\text{圆或直线}
$$

分式线性变换一定把：

$$
\boxed{\text{圆或直线} \longmapsto \text{圆或直线}}
$$

更具体：

| 原来的图形 | 是否经过极点 $z=-\frac dc$ | 像 |
|---|---|---|
| 圆/直线 | 不经过极点 | 圆 |
| 圆/直线 | 经过极点 | 直线 |

因为极点会被映到 $\infty$，而经过 $\infty$ 的广义圆就是直线。

---

## 3. 不要死背图形，记住四种基本变换

一般的分式线性变换可以分解成：

$$
z\mapsto z+\beta
$$

$$
z\mapsto \alpha z
$$

$$
z\mapsto \frac1z
$$

这几类。

### 1）平移

$$
w=z+b
$$

效果：整体平移。

例如：

$$
w=z+1
$$

就是所有点向右平移 1。

---

### 2）旋转与伸缩

$$
w=az
$$

若

$$
a=re^{i\theta}
$$

则

$$
w=re^{i\theta}z
$$

表示：

- 放大 $r$ 倍；
- 旋转 $\theta$ 角。

例如：

$$
w=2iz
$$

表示放大 2 倍，再逆时针旋转 $\frac\pi2$。

---

### 3）倒数变换

$$
w=\frac1z
$$

这是最重要、最容易考的。

设

$$
z=re^{i\theta}
$$

则

$$
w=\frac1z=\frac1r e^{-i\theta}
$$

所以它的作用是：

$$
\boxed{\text{模长取倒数，辐角取相反数}}
$$

也就是：

- 离原点远的点变近；
- 离原点近的点变远；
- 角度关于实轴反射；
- $0\leftrightarrow \infty$。

---

## 4. 倒数变换下直线和圆的典型变化

### 情况一：过原点的直线

例如：

$$
\operatorname{Im}z=0
$$

也就是实轴。

令

$$
w=\frac1z
$$

如果 $z$ 在实轴上，那么 $w$ 仍在实轴上。

所以：

$$
\boxed{\text{过原点的直线映成过原点的直线}}
$$

---

### 情况二：不过原点的直线

例如：

$$
\operatorname{Re}z=\frac12
$$

令

$$
w=u+iv,\qquad z=\frac1w=\frac{u-iv}{u^2+v^2}
$$

所以

$$
\operatorname{Re}z=\frac{u}{u^2+v^2}
$$

代入：

$$
\frac{u}{u^2+v^2}=\frac12
$$

得到：

$$
u^2+v^2=2u
$$

即：

$$
(u-1)^2+v^2=1
$$

所以：

$$
\boxed{\operatorname{Re}z=\frac12
\quad \xrightarrow{w=1/z}\quad
|w-1|=1}
$$

也就是说：

$$
\boxed{\text{不过原点的直线映成过原点的圆}}
$$

---

### 情况三：过原点的圆

例如：

$$
|z-1|=1
$$

这个圆过 $0$。

令

$$
z=\frac1w
$$

代入：

$$
\left|\frac1w-1\right|=1
$$

$$
\left|\frac{1-w}{w}\right|=1
$$

$$
|1-w|=|w|
$$

平方：

$$
(1-u)^2+v^2=u^2+v^2
$$

得到：

$$
u=\frac12
$$

所以：

$$
\boxed{|z-1|=1
\quad \xrightarrow{w=1/z}\quad
\operatorname{Re}w=\frac12}
$$

即：

$$
\boxed{\text{过原点的圆映成不过原点的直线}}
$$

---

### 情况四：不过原点的圆

不过原点的圆会映成不过原点的圆。

总结：

| 原图形 | 是否过 $0$ | 在 $w=1/z$ 下的像 |
|---|---|---|
| 直线 | 过 $0$ | 直线 |
| 直线 | 不过 $0$ | 过 $0$ 的圆 |
| 圆 | 过 $0$ | 直线 |
| 圆 | 不过 $0$ | 圆 |

---

## 5. 区域映射题的固定做法

期末最常考的是：

> 求某个区域在分式线性变换下的像。

不要直接想象。按下面三步做。

---

### 第一步：找边界

区域的边界通常是：

- 直线；
- 圆；
- 实轴；
- 虚轴；
- 单位圆；
- 半平面边界。

---

### 第二步：求边界的像

方法有两种。

#### 方法 A：取三个点

因为分式线性变换把广义圆映成广义圆。

所以一条直线或一个圆，只要找三个点的像，就能确定像。

例如边界是实轴，可以取：

$$
0,\quad 1,\quad \infty
$$

然后算它们的像。

---

#### 方法 B：用逆变换代入

如果

$$
w=\frac{az+b}{cz+d}
$$

则反解：

$$
z=\frac{b-dw}{cw-a}
$$

然后把 $z$ 代入原来的边界方程。

比如原区域是：

$$
\operatorname{Re}z>0
$$

就把

$$
z=\frac{b-dw}{cw-a}
$$

代进去，化成关于 $w=u+iv$ 的不等式。

---

### 第三步：取测试点判断哪一侧

边界映成圆或直线之后，还要判断区域在圆内还是圆外、在线左边还是右边。

取一个区域内部点 $z_0$，算：

$$
w_0=f(z_0)
$$

看 $w_0$ 落在哪一侧。

---

## 6. 例题 1：右半平面映到哪里

求

$$
w=\frac{z-1}{z+1}
$$

把区域

$$
\operatorname{Re}z>0
$$

映成什么？

---

### 第一步：边界

$$
\operatorname{Re}z=0
$$

也就是虚轴。

---

### 第二步：求边界的像

取边界上的点：

$$
z=0,\quad z=i,\quad z=\infty
$$

分别代入：

$$
z=0:\quad w=\frac{-1}{1}=-1
$$

$$
z=\infty:\quad w=1
$$

$$
z=i:\quad w=\frac{i-1}{i+1}
$$

计算模长：

$$
\left|\frac{i-1}{i+1}\right|
=
\frac{|i-1|}{|i+1|}
=
\frac{\sqrt2}{\sqrt2}=1
$$

所以边界虚轴映成单位圆：

$$
|w|=1
$$

---

### 第三步：取测试点

取右半平面内的点：

$$
z=1
$$

则

$$
w=\frac{1-1}{1+1}=0
$$

因为

$$
0
$$

在单位圆内部，所以：

$$
\boxed{\operatorname{Re}z>0
\quad \xrightarrow{w=\frac{z-1}{z+1}}\quad
|w|<1}
$$

---

## 7. 例题 2：上半平面映到单位圆

经典公式：

$$
\boxed{
w=\frac{z-i}{z+i}
}
$$

它把上半平面

$$
\operatorname{Im}z>0
$$

映成单位圆内部：

$$
|w|<1
$$

为什么？

---

边界是实轴：

$$
z=x,\quad x\in\mathbb R
$$

代入：

$$
w=\frac{x-i}{x+i}
$$

于是：

$$
|w|
=
\frac{|x-i|}{|x+i|}
=
1
$$

所以实轴映成单位圆：

$$
|w|=1
$$

再取上半平面内一点：

$$
z=i
$$

代入：

$$
w=\frac{i-i}{i+i}=0
$$

所以内部映成：

$$
\boxed{|w|<1}
$$

---

## 8. 常见标准映射模板

这些期末很常用。

### 1）上半平面到单位圆

$$
\boxed{
w=\frac{z-i}{z+i}
}
$$

对应：

$$
\operatorname{Im}z>0
\quad\longmapsto\quad
|w|<1
$$

更一般地，如果 $z_0$ 在上半平面，则

$$
\boxed{
w=e^{i\theta}\frac{z-z_0}{z-\overline{z_0}}
}
$$

把上半平面映成单位圆。

---

### 2）单位圆到上半平面

$$
\boxed{
w=i\frac{1+z}{1-z}
}
$$

对应：

$$
|z|<1
\quad\longmapsto\quad
\operatorname{Im}w>0
$$

---

### 3）单位圆到右半平面

$$
\boxed{
w=\frac{1+z}{1-z}
}
$$

对应：

$$
|z|<1
\quad\longmapsto\quad
\operatorname{Re}w>0
$$

验证一下：

取 $z=0$，则

$$
w=1
$$

确实在右半平面。

---

### 4）右半平面到单位圆

$$
\boxed{
w=\frac{z-1}{z+1}
}
$$

对应：

$$
\operatorname{Re}z>0
\quad\longmapsto\quad
|w|<1
$$

---

### 5）单位圆自映射

如果 $|a|<1$，则

$$
\boxed{
w=e^{i\theta}\frac{z-a}{1-\overline a z}
}
$$

把单位圆内部映到单位圆内部。

其中：

$$
z=a \quad\longmapsto\quad w=0
$$

这是单位圆自同构的标准形式。

---

## 9. 由三个点确定一个分式线性变换

分式线性变换由三个点唯一确定。

如果要求：

$$
z_1\mapsto w_1,\qquad z_2\mapsto w_2,\qquad z_3\mapsto w_3
$$

可以用交比公式：

$$
\boxed{
\frac{(w-w_1)(w_2-w_3)}
{(w-w_3)(w_2-w_1)}
=
\frac{(z-z_1)(z_2-z_3)}
{(z-z_3)(z_2-z_1)}
}
$$

这个公式非常适合考试构造映射。

---

## 10. 例题 3：构造一个映射

求一个分式线性变换，把上半平面映成单位圆，并且

$$
i\mapsto 0
$$

因为上半平面的边界是实轴，单位圆的边界是 $|w|=1$。

标准模板直接是：

$$
\boxed{
w=\frac{z-i}{z+i}
}
$$

检查：

$$
z=i \Rightarrow w=0
$$

如果 $z=x\in\mathbb R$，则：

$$
|w|=\left|\frac{x-i}{x+i}\right|=1
$$

所以实轴映成单位圆，取测试点 $z=i$ 映成 $0$，因此上半平面映成单位圆内部。

---

## 11. 例题 4：求单位圆到右半平面的映射

求一个变换，把

$$
|z|<1
$$

映成

$$
\operatorname{Re}w>0
$$

可以直接用标准公式：

$$
\boxed{
w=\frac{1+z}{1-z}
}
$$

验证边界：

若

$$
|z|=1
$$

令

$$
z=e^{it}
$$

则

$$
w=\frac{1+e^{it}}{1-e^{it}}
$$

化简可知它是纯虚数，所以单位圆边界映成虚轴。

测试点：

$$
z=0\Rightarrow w=1
$$

而

$$
\operatorname{Re}1>0
$$

所以单位圆内部映成右半平面。

---

## 12. 期末做题模板

遇到题目：

$$
w=\frac{az+b}{cz+d}
$$

求某区域的像。

直接写：

### 第一步：确定边界

例如：

$$
D=\{z:\operatorname{Im}z>0\}
$$

边界是：

$$
\operatorname{Im}z=0
$$

即实轴。

---

### 第二步：求边界像

用三点法。

例如实轴取：

$$
0,\quad 1,\quad \infty
$$

然后算：

$$
f(0),\quad f(1),\quad f(\infty)
$$

由这三个点确定像圆或像直线。

---

### 第三步：判断区域一侧

取一个内部点。

例如上半平面取：

$$
z=i
$$

右半平面取：

$$
z=1
$$

单位圆取：

$$
z=0
$$

算它的像，看落在边界的哪边。

---

## 13. 你最应该背的内容

### 第一组：基本性质

$$
\boxed{
w=\frac{az+b}{cz+d},\quad ad-bc\neq 0
}
$$

$$
\boxed{
z=-\frac dc \mapsto \infty,\qquad \infty\mapsto \frac ac
}
$$

$$
\boxed{
\text{分式线性变换把广义圆映成广义圆}
}
$$

---

### 第二组：区域映射流程

$$
\boxed{
\text{边界} \to \text{边界像} \to \text{测试点判断区域}
}
$$

---

### 第三组：常见标准公式

$$
\boxed{
\operatorname{Im}z>0
\longmapsto
|w|<1:
\quad
w=\frac{z-i}{z+i}
}
$$

$$
\boxed{
|z|<1
\longmapsto
\operatorname{Im}w>0:
\quad
w=i\frac{1+z}{1-z}
}
$$

$$
\boxed{
|z|<1
\longmapsto
\operatorname{Re}w>0:
\quad
w=\frac{1+z}{1-z}
}
$$

$$
\boxed{
\operatorname{Re}z>0
\longmapsto
|w|<1:
\quad
w=\frac{z-1}{z+1}
}
$$

$$
\boxed{
|z|<1 \text{ 的自映射}:
\quad
w=e^{i\theta}\frac{z-a}{1-\overline a z},\quad |a|<1
}
$$

---

## 14. 最容易混的点

### 混点一：为什么直线有时变成圆？

因为在扩充复平面里，直线可以看成经过 $\infty$ 的圆。

分式线性变换会把 $\infty$ 移到有限点，所以直线可能变成圆。

---

### 混点二：为什么要取测试点？

因为边界只告诉你边界像。

比如边界映成：

$$
|w|=1
$$

但区域可能是：

$$
|w|<1
$$

也可能是：

$$
|w|>1
$$

必须取一个内部点判断。

---

### 混点三：为什么三个点能确定像？

因为圆或直线由三个点确定。

分式线性变换又把广义圆映成广义圆，所以只需要算三个点的像。

---

## 15. 最简考试口诀

$$
\boxed{
\text{分式线性看边界，边界三点定圆线，内部一点判内外。}
}
$$

再加一句：

$$
\boxed{
\text{上半平面用 } \frac{z-i}{z+i},\quad
\text{单位圆到右半平面用 } \frac{1+z}{1-z}.
}
$$

这部分期末核心不是画得多精确，而是会把区域边界送过去，然后用测试点判断像域。



---
Powered by [ChatGPT Exporter](https://www.chatgptexporter.com)