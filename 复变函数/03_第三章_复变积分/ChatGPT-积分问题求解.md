# 积分问题求解

**User:** Anonymous  
**Created:** 7/6/2026 19:04:43  
**Updated:** 7/6/2026 19:25:08  
**Exported:** 7/6/2026 19:31:39  
**Link:** [https://chatgpt.com/c/6a4b8bbc-1a48-83ee-9e7b-ca20f5ce5d5a](https://chatgpt.com/c/6a4b8bbc-1a48-83ee-9e7b-ca20f5ce5d5a)  

## Response:
2026/7/6 19:24:41

这里的“衰减为 0”不是说

$$
e^{iz}
$$

在整个上半圆弧上每一点都均匀趋于 $0$。严格说，是说**大圆弧积分趋于 0**：

$$
\int_{C_R}\frac{z e^{iz}}{z^2+1}\,dz\to 0
\qquad R\to+\infty
$$

其中 $C_R$ 是上半圆弧：

$$
z=Re^{i\theta},\qquad 0\le \theta\le \pi
$$

---

## 1. 先看 $e^{iz}$ 为什么会变小

设

$$
z=x+iy
$$

则

$$
e^{iz}=e^{i(x+iy)}=e^{ix-y}
$$

所以

$$
|e^{iz}|=|e^{ix-y}|=e^{-y}
$$

在上半平面：

$$
y>0
$$

因此

$$
e^{-y}<1
$$

而且 $y$ 越大，$e^{-y}$ 越接近 $0$。

这就是所谓的“指数衰减”。

---

## 2. 在上半圆弧上具体是什么样？

上半圆弧：

$$
z=Re^{i\theta}=R\cos\theta+iR\sin\theta
$$

所以

$$
y=R\sin\theta
$$

于是

$$
|e^{iz}|=e^{-R\sin\theta}
$$

当 $0<\theta<\pi$ 时，

$$
\sin\theta>0
$$

所以

$$
e^{-R\sin\theta}\to 0
\qquad R\to+\infty
$$

因此在上半圆大部分地方，$e^{iz}$ 都会快速变小。

---

## 3. 但是端点附近好像不衰减，怎么办？

注意：

$$
\theta=0,\pi
$$

时，

$$
\sin\theta=0
$$

所以端点附近

$$
e^{-R\sin\theta}
$$

确实不明显衰减。

但问题不是看点值，而是看整个弧积分：

$$
\int_{C_R}\frac{z e^{iz}}{z^2+1}\,dz
$$

在大圆弧上：

$$
\left|\frac{z}{z^2+1}\right|
\sim \frac{R}{R^2}
=
\frac1R
$$

也就是说有一个 $\frac1R$ 的因子。

同时

$$
|dz|=R\,d\theta
$$

所以估计为：

$$
\left|
\int_{C_R}\frac{z e^{iz}}{z^2+1}\,dz
\right|
\le
\int_0^\pi
\left|\frac{z}{z^2+1}\right|
|e^{iz}||dz|
$$

当 $R$ 足够大时，

$$
\left|\frac{z}{z^2+1}\right|\le \frac{2}{R}
$$

所以

$$
\le
\int_0^\pi
\frac{2}{R}e^{-R\sin\theta}R\,d\theta
$$

即

$$
\le
2\int_0^\pi e^{-R\sin\theta}\,d\theta
$$

而这个积分满足：

$$
\int_0^\pi e^{-R\sin\theta}\,d\theta\to 0
$$

所以大圆弧积分趋于 $0$。

---

## 4. 为什么 $\int_0^\pi e^{-R\sin\theta}d\theta\to0$？

利用对称性：

$$
\int_0^\pi e^{-R\sin\theta}\,d\theta
=
2\int_0^{\pi/2}e^{-R\sin\theta}\,d\theta
$$

在区间 $[0,\pi/2]$ 上有估计：

$$
\sin\theta\ge \frac{2}{\pi}\theta
$$

所以

$$
e^{-R\sin\theta}
\le
e^{-\frac{2R}{\pi}\theta}
$$

于是

$$
\int_0^\pi e^{-R\sin\theta}\,d\theta
\le
2\int_0^{\pi/2}e^{-\frac{2R}{\pi}\theta}\,d\theta
$$

计算得：

$$
2\int_0^{\pi/2}e^{-\frac{2R}{\pi}\theta}\,d\theta
=
\frac{\pi}{R}(1-e^{-R})
$$

所以

$$
\int_0^\pi e^{-R\sin\theta}\,d\theta
\le
\frac{\pi}{R}(1-e^{-R})
\to 0
$$

因此

$$
\boxed{
\int_{C_R}\frac{z e^{iz}}{z^2+1}\,dz\to 0
}
$$

---

## 5. 一句话理解

在上半平面：

$$
|e^{iz}|=e^{-\operatorname{Im}z}
$$

而上半圆弧大部分地方有

$$
\operatorname{Im}z=R\sin\theta
$$

随着 $R\to\infty$，指数项快速变小；端点附近虽然不明显衰减，但区域很窄，再加上有理函数部分约为 $\frac1R$，所以整个大圆弧积分趋于 $0$。

所以这里的“衰减为 0”准确说是：

$$
\boxed{
e^{iz}\text{ 在上半平面具有指数衰减性，从而大圆弧积分趋于 }0
}
$$



---
Powered by [ChatGPT Exporter](https://www.chatgptexporter.com)