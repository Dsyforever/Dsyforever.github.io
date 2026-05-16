---
layout: default
title: "RMNP 和 Muon 下降方向的等价性"
date: 2026-05-17
permalink: /blog/dsyblog-zh/
hide_from_blog_index: true
---

# Muon 与 RMNP 下降方向差异的证明

## 1. 背景设置

这里只是给一个最简单的例子（神经网络的结论非常复杂，需要更深的分析）考虑最简单的线性回归损失：
$$L(W) = \tfrac{1}{2}\|W\|_F^2$$
其梯度为 $\nabla L = W$。Muon 和 RMNP 两种优化器在这个损失下的下降方向分别为:

- **Muon**:$(WW^T)^{-1/2}\,W$
- **RMNP**:$\mathrm{diag}(WW^T)^{-1/2}\,W$

我们关心的核心问题是:在初始化的情形下,这两个方向的差异有多大?即估计
$$\Delta := (WW^T)^{-1/2}W - \mathrm{diag}(WW^T)^{-1/2}W$$
的各种范数。

**记号约定**:
- $A := WW^T$
- $D := \mathrm{diag}(WW^T)$,$D_{ii} = \|W_{i*}\|^2$
- $E := A - D$,$E_{i\ell} = \langle W_{i*}, W_{\ell*}\rangle$ 当 $i\neq\ell$

---

## 2. 主定理

**主定理**. 设 $W \in \mathbb{R}^{m \times n}$,$W_{ij} \stackrel{\text{iid}}{\sim} \mathcal{N}(0, 1)$,$m$ 固定。存在仅依赖于 $m$ 的正常数 $c_1, c_2, C$,使得当 $n \geq C$ 时:

**(A) 算子范数高概率界**
$$\mathbb{P}\bigl[\|\Delta\|_{\mathrm{op}} \leq c_1/\sqrt n\bigr] \geq 1 - n^{-2}$$

**(B) Frobenius 范数高概率界**
$$\mathbb{P}\bigl[\|\Delta\|_F \leq c_2/\sqrt n\bigr] \geq 1 - n^{-2}$$

---

## 3. 引理

### 3.1 Balakrishnan 积分表示

对正定 $X \succ 0$:
$$X^{-1/2} = \frac{1}{\pi}\int_0^\infty t^{-1/2}(X+tI)^{-1}\,dt$$

**证明**. 谱分解后归约为标量 $\lambda^{-1/2} = \frac{1}{\pi}\int_0^\infty\frac{dt}{\sqrt t(\lambda+t)}$;代换 $t=\lambda u$ 化为 $\frac{1}{\sqrt\lambda}\cdot\frac{1}{\pi}\int_0^\infty\frac{du}{\sqrt u(1+u)} = \frac{1}{\sqrt\lambda}$,后者用 $B(1/2,1/2) = \pi$。$\square$

参考材料:Higham, *Functions of Matrices* (2008)。

### 3.2 标量积分

对 $a, b > 0$:
$$\int_0^\infty \frac{dt}{\sqrt t\,(a+t)(b+t)} = \frac{\pi}{\sqrt{ab}(\sqrt a+\sqrt b)}$$

**证明**. 代换 $t=s^2$,$dt=2s\,ds$:
$$2\int_0^\infty\frac{ds}{(a+s^2)(b+s^2)} = \frac{2}{b-a}\int_0^\infty\!\!\left[\frac{1}{a+s^2}-\frac{1}{b+s^2}\right]ds = \frac{\pi}{\sqrt{ab}(\sqrt a+\sqrt b)}$$
$\square$

### 3.3 Davidson-Szarek 不等式

设 $W \in \mathbb{R}^{m\times n}$,$m \leq n$,$W_{ij}\stackrel{\text{iid}}{\sim}\mathcal{N}(0,1)$。对所有 $t > 0$:

$$\mathbb{P}\bigl[\sigma_{\max}(W) \geq \sqrt n + \sqrt m + t\bigr] \leq e^{-t^2/2}$$

$$\mathbb{P}\bigl[\sigma_{\min}(W) \leq \sqrt n - \sqrt m - t\bigr] \leq e^{-t^2/2}$$

参考材料:Vershynin, *High-Dimensional Probability* (2018)。

### 3.4 Laurent-Massart $\chi^2$ 集中

设 $Z \sim \chi^2_n$。对所有 $x > 0$:

$$\mathbb{P}\bigl[Z \geq n + 2\sqrt{nx} + 2x\bigr] \leq e^{-x},\qquad \mathbb{P}\bigl[Z \leq n - 2\sqrt{nx}\bigr] \leq e^{-x}$$

参考材料:B. Laurent & P. Massart (2000), *Ann. Stat.* 28(5), 1302-1338。

### 3.5 高概率事件

定义
$$\Omega_n := \{\sigma_{\min}(W)\geq\sqrt n/2\}\cap\{\sigma_{\max}(W)\leq 2\sqrt n\}\cap\{\min_i D_{ii}\geq n/2\}\cap\{\|E\|_{\mathrm{op}}\leq c_0\sqrt n\}$$
其中 $c_0$ 仅依赖于 $m$。则当 $n$ 充分大时,$\mathbb{P}(\Omega_n^c) \leq n^{-2}$。

**证明**.

**(a) 奇异值的界**:对 Davidson-Szarek 不等式(3.3)取 $t = \sqrt n/4$,当 $n \geq 16m$:
$$\mathbb{P}\bigl[\sigma_{\max}(W) \leq 2\sqrt n\bigr] \geq 1 - e^{-n/32},\qquad \mathbb{P}\bigl[\sigma_{\min}(W) \geq \tfrac{\sqrt n}{2}\bigr] \geq 1 - e^{-n/32}$$

**(b) 行范数的界**:$D_{ii} = \|W_{i*}\|^2\sim\chi^2_n$。对 Laurent-Massart 不等式(3.4)取 $x = n/16$:
$$\mathbb{P}[D_{ii} \leq n/2] \leq e^{-n/16}$$
Union bound 对 $i = 1,\ldots,m$:
$$\mathbb{P}\bigl[\min_i D_{ii} \geq n/2\bigr] \geq 1 - m e^{-n/16}$$

**(c) $\|E\|_{\mathrm{op}}$ 的界**:每个 $E_{i\ell} = \sum_{k=1}^n W_{ik}W_{\ell k}$($i\neq\ell$)是 $n$ 个独立均值 0、亚指数随机变量之和。由 Bernstein 不等式:
$$\mathbb{P}[|E_{i\ell}|\geq u] \leq 2\exp\!\bigl(-c\min(u^2/n, u)\bigr)$$
取 $u = c_0'\sqrt n$($c_0'$ 充分大),概率至少 $1 - e^{-c'n}$。Union bound 对 $\binom{m}{2}$ 对,概率仍至少 $1 - m^2 e^{-c'n}$。

由粗界 $\|E\|_{\mathrm{op}}\leq m\cdot\max_{i,\ell}|E_{i\ell}|\leq c_0\sqrt n$(取 $c_0 = m c_0'$)。

合并 (a)(b)(c) 三个"坏"事件:每个概率指数小,当 $n$ 充分大时总和 $\leq n^{-2}$。$\square$

### 3.6 精确微扰恒等式

在 $A, D\succ 0$ 上:
$$A^{-1/2}-D^{-1/2} = -\frac{1}{\pi}\int_0^\infty t^{-1/2}(A+tI)^{-1}E(D+tI)^{-1}\,dt$$

**证明**. 由 Balakrishnan 积分表示(3.1)应用于 $A$ 和 $D$ 后相减,再用代数恒等式 $X^{-1}-Y^{-1} = -X^{-1}(X-Y)Y^{-1}$(取 $X=A+tI,Y=D+tI$,$X-Y = E$)。$\square$

### 3.7 确定性算子范数界

对所有 $A, D\succ 0$:
$$\|A^{-1/2}-D^{-1/2}\|_{\mathrm{op}} \leq \frac{\|E\|_{\mathrm{op}}}{\sqrt{\lambda_{\min}(A)\,\lambda_{\min}(D)}\bigl(\sqrt{\lambda_{\min}(A)}+\sqrt{\lambda_{\min}(D)}\bigr)}$$

**证明**. 对精确微扰恒等式(3.6)取算子范数,用 $\|XYZ\|_{\mathrm{op}}\leq\|X\|_{\mathrm{op}}\|Y\|_{\mathrm{op}}\|Z\|_{\mathrm{op}}$ 和标量积分(3.2)。$\square$

---

## 4. 主定理证明

### 4.1 证明 (A):算子范数高概率界

在 $\Omega_n$ 上(由 3.5):
- $\lambda_{\min}(A) = \sigma_{\min}(W)^2 \geq n/4$
- $\lambda_{\min}(D) \geq n/2$
- $\|E\|_{\mathrm{op}}\leq c_0\sqrt n$
- $\|W\|_{\mathrm{op}}\leq 2\sqrt n$

代入确定性算子范数界(3.7):分母 $\geq \sqrt{(n/4)(n/2)}\cdot(\sqrt{n/4}+\sqrt{n/2}) \geq c_4 n^{3/2}$,所以
$$\|A^{-1/2}-D^{-1/2}\|_{\mathrm{op}}\leq \frac{c_0\sqrt n}{c_4 n^{3/2}} = \frac{c_5}{n}$$

由 $\Delta = (A^{-1/2}-D^{-1/2})W$:
$$\|\Delta\|_{\mathrm{op}}\leq \frac{c_5}{n}\cdot 2\sqrt n = \frac{c_1}{\sqrt n}$$

由高概率事件(3.5),$\Omega_n$ 概率至少 $1 - n^{-2}$,得结论 (A)。$\square$

### 4.2 证明 (B):Frobenius 范数高概率界

$\Delta$ 是 $m\times n$ 矩阵,$m$ 固定。由 $\|\Delta\|_F\leq\sqrt m\cdot\|\Delta\|_{\mathrm{op}}$,在 $\Omega_n$ 上:
$$\|\Delta\|_F\leq \sqrt m\cdot\frac{c_1}{\sqrt n} = \frac{c_2}{\sqrt n}$$

概率同样至少 $1-n^{-2}$,得结论 (B)。$\square$

---

## 5. 结论与讨论

### 5.1 总结

| 量 | 估计 | 概率 |
|---|---|---|
| $\|\Delta\|_{\mathrm{op}}$ | $\leq c_1/\sqrt n$ | $\geq 1 - n^{-2}$ |
| $\|\Delta\|_F$ | $\leq c_2/\sqrt n$ | $\geq 1 - n^{-2}$ |

所有 $c_i$ 仅依赖于 $m$(固定),不依赖于 $n$。

### 5.2 直觉

回到我们考虑的最简单线性回归 $L(W) = \tfrac{1}{2}\|W\|_F^2$:当 $n\to\infty$、$m$ 固定时,Muon 下降方向 $(WW^T)^{-1/2}W$ 与 RMNP 下降方向 $\mathrm{diag}(WW^T)^{-1/2}W$ 在依概率意义下渐近相等,差异速率为 $\Theta(1/\sqrt n)$。

差异的本质来源是 $WW^T$ 的非对角部分 $E$:$E_{i\ell} = \langle W_{i*}, W_{\ell*}\rangle$ 反映"第 $i$ 行和第 $\ell$ 行的相关性"。在高维($n\gg m$)下,独立随机向量近似正交,所以这些非对角元相对量级是 $O(1/\sqrt n)$。

直观上看:RMNP 把每一行单独单位化,得到 $m$ 个独立的单位向量;Muon 在此基础上再做一次小修正,把它们调整成精确正交。当行向量之间的内积已经 $O(1/\sqrt n)$ 时,这个修正自然也是 $O(1/\sqrt n)$ 量级。

---

## 6. 数值模拟实验

### 6.1 实验设置

- $m \in \{3, 5, 10, 20\}$,每个 $m$ 单独做一组实验
- 对每个 $m$,$n$ 取值 $\{50, 100, 200, 500, 1000, 2000, 5000, 10000, 20000\}$
- 每个 $(m, n)$ 做 500 次蒙特卡洛采样
- $W_{ij}$ 独立采自 $\mathcal{N}(0,1)$
- $(WW^T)^{-1/2}$ 通过对称矩阵特征分解 $WW^T = U\Lambda U^T$ 后,取 $U\Lambda^{-1/2}U^T$ 计算

### 6.2 实验结果

<figure style="margin: 1.4rem auto 1.6rem auto; text-align: center; max-width: 920px;">
	<img src="/images/blog/norm_decay_two_panels.png" alt="不同 m 取值下，Muon 与 RMNP 下降方向差异范数随 n 增大而衰减的数值模拟结果。" style="width: 100%; height: auto; display: block; margin: 0 auto; border-radius: 6px;" />
	<figcaption style="margin-top: 0.55rem; font-size: 0.92em; line-height: 1.45; color: #5c6675;">图 1. 在多个固定的 $m$ 取值下，两种范数都按约 $n^{-1/2}$ 的速率衰减。</figcaption>
</figure>

**$m = 3$**:

| $n$ | $\mathbb{E}\|\Delta\|_{\mathrm{op}}$ | $\mathbb{E}\|\Delta\|_F$ |
|---|---|---|
| 50 | 0.122 | 0.157 |
| 100 | 0.087 | 0.113 |
| 200 | 0.060 | 0.079 |
| 500 | 0.040 | 0.052 |
| 1000 | 0.026 | 0.034 |
| 2000 | 0.019 | 0.025 |
| 5000 | 0.012 | 0.016 |
| 10000 | 0.009 | 0.011 |
| 20000 | 0.006 | 0.008 |

**$m = 5$**:

| $n$ | $\mathbb{E}\|\Delta\|_{\mathrm{op}}$ | $\mathbb{E}\|\Delta\|_F$ |
|---|---|---|
| 50 | 0.221 | 0.312 |
| 100 | 0.154 | 0.220 |
| 200 | 0.109 | 0.156 |
| 500 | 0.068 | 0.098 |
| 1000 | 0.047 | 0.068 |
| 2000 | 0.033 | 0.048 |
| 5000 | 0.021 | 0.031 |
| 10000 | 0.015 | 0.022 |
| 20000 | 0.011 | 0.015 |

**$m = 10$**:

| $n$ | $\mathbb{E}\|\Delta\|_{\mathrm{op}}$ | $\mathbb{E}\|\Delta\|_F$ |
|---|---|---|
| 50 | 0.378 | 0.680 |
| 100 | 0.266 | 0.480 |
| 200 | 0.185 | 0.334 |
| 500 | 0.116 | 0.211 |
| 1000 | 0.083 | 0.149 |
| 2000 | 0.058 | 0.105 |
| 5000 | 0.037 | 0.067 |
| 10000 | 0.026 | 0.047 |
| 20000 | 0.018 | 0.033 |

**$m = 20$**:

| $n$ | $\mathbb{E}\|\Delta\|_{\mathrm{op}}$ | $\mathbb{E}\|\Delta\|_F$ |
|---|---|---|
| 50 | 0.589 | 1.426 |
| 100 | 0.412 | 0.994 |
| 200 | 0.288 | 0.694 |
| 500 | 0.181 | 0.436 |
| 1000 | 0.128 | 0.308 |
| 2000 | 0.090 | 0.218 |
| 5000 | 0.057 | 0.138 |
| 10000 | 0.040 | 0.097 |
| 20000 | 0.029 | 0.069 |

### 6.3 结论

对每一个固定的 $m$,两种范数在 log-log 坐标下都与 $1/\sqrt n$ 参考线平行,验证
$$\mathbb{E}\|\Delta\|_{\mathrm{op}} = \Theta(1/\sqrt n),\qquad \mathbb{E}\|\Delta\|_F = \Theta(1/\sqrt n)$$

不同 $m$ 的曲线相互平行(同样的斜率 $-1/2$),只在常数因子上有差异,这进一步验证了"$m$ 固定、$n\to\infty$"这一渐近模式与 $m$ 的具体取值无关。

实验结果与理论预测完全一致。