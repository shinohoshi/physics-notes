+++
date = '2026-07-04T01:20:47+08:00'
draft = false
title = '拉格朗日力学与最小作用量原理'
tags = ['分析力学', '拉格朗日', '变分法']
categories = ['理论物理']
summary = '从最小作用量原理出发，推导拉格朗日方程，并用几个经典例子说明其应用。'
ShowToc = true
+++

## 最小作用量原理

经典力学最基本的表述不是牛顿第二定律 ${\mathbf{F}} = m{\mathbf{a}}$，而是**最小作用量原理**（Principle of Least Action）。

考虑一个力学系统，其位形由广义坐标 $q_i(t)$ 描述。定义**作用量**（action）：

$$
S[q] = \int_{t_1}^{t_2} L(q, \dot{q}, t) \, \dd t
$$

其中 $L = T - V$ 是系统的拉格朗日量（Lagrangian），即动能减势能。

## 变分法推导

对 $q_i(t)$ 做微小变分 $\delta q_i(t)$，要求 $\delta q_i(t_1) = \delta q_i(t_2) = 0$：

$$
\begin{aligned}
\delta S &= \int_{t_1}^{t_2} \sum_i \left( \frac{\partial L}{\partial q_i} \delta q_i + \frac{\partial L}{\partial \dot{q}_i} \delta \dot{q}_i \right) \dd t \\
&= \int_{t_1}^{t_2} \sum_i \left[ \frac{\partial L}{\partial q_i} - \frac{\dd}{\dd t}\left( \frac{\partial L}{\partial \dot{q}_i} \right) \right] \delta q_i \, \dd t = 0
\end{aligned}
$$

由于 $\delta q_i$ 是任意的，得到**欧拉-拉格朗日方程**：

$$
\boxed{\frac{\dd}{\dd t}\left( \frac{\partial L}{\partial \dot{q}_i} \right) - \frac{\partial L}{\partial q_i} = 0}
$$

## 对称性与守恒律

诺特定理（Noether's Theorem）指出：每个连续对称性对应一个守恒量。

- 时间平移不变性 $\leftrightarrow$ 能量守恒
- 空间平移不变性 $\leftrightarrow$ 动量守恒
- 旋转不变性 $\leftrightarrow$ 角动量守恒
