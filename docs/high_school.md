# 高中

**注意：这里不含小学、初中已经学过的符号。**

## 分数/分式

通常使用 `\frac {分子} {分母}` 表示分数，分数可嵌套。  
如果分子和分母都只有一个字符，可直接输入 `\frac ab` 来快速生成 $\frac ab$。  
如果分式很复杂，亦可使用 `分子 \over 分母` 命令，此时分数仅有一层。

例子：

分数 `\frac{2}{4}=0.5`，普通的 `\frac` 命令在行内公式中默认使用小尺寸，在行间公式中默认使用大尺寸。

行内公式显示效果： ${\frac {2}{4}}=0.5$  
行间公式显示效果：
$${\frac {2}{4}}=0.5$$

小型分数 ${\tfrac {2}{4}}=0.5$ `\tfrac{2}{4} = 0.5`

连分式（大型嵌套分式）${\cfrac {2}{c+{\cfrac {2}{d+{\cfrac {2}{4}}}}}}=a$ `\cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} = a`

大型不嵌套分式 $\dfrac {2}{4}=0.5$ `\dfrac{2}{4} = 0.5`，${\dfrac {2}{c+{\dfrac {2}{d+{\dfrac {2}{4}}}}}}=a$ `\dfrac{2}{c + \dfrac{2}{d + \dfrac{2}{4}}} = a`

在指数、极限和积分中尽量**不要**使用 `\frac` 符号：它会使整段函数看起来很怪，而且可能产生歧义。也正是因此它在专业数学排版中几乎从不出现。
横着写这些分式，中间使用斜线间隔 `/`（用斜线代替分数线）。

- 例子：

```latex
\begin{array}{cc}
\mathrm{Bad} & \mathrm{Better} \\
\hline \\
e^{i\frac{\pi}2} \quad e^{\frac{i\pi}2}& e^{i\pi/2} \\
\int_{-\frac\pi2}^\frac\pi2 \sin x\,dx & \int_{-\pi/2}^{\pi/2}\sin x\,dx \\
\end{array}
```

- 显示：

$$
\begin{array}{cc}
\mathrm{Bad} & \mathrm{Better} \\
\hline \\
e^{i\frac{\pi}2} \quad e^{\frac{i\pi}2}& e^{i\pi/2} \\
\int_{-\frac\pi2}^\frac\pi2 \sin x\,dx & \int_{-\pi/2}^{\pi/2}\sin x\,dx \\
\end{array}
$$


## 集合

- 特殊的集合

空集 $\varnothing$ `\varnothing`  
正整数集 $\mathbb{N^+},\mathbb{N^*},\mathbb{Z^+},\mathbb{Z^*}$ `\mathbb{N^+},\mathbb{N^*},\mathbb{Z^+},\mathbb{Z^*}`  
自然数集 $\mathbb{N}$ `\mathbb{N}`  
整数集 $\mathbb{Z}$ `\mathbb{Z}`  
有理数集 $\mathbb{Q}$ `\mathbb{Q}`  
实数集 $\mathbb{R}$ `\mathbb{R}`  
复数集 $\mathbb{C}$ `\mathbb{C}`  

- 元素与集合的关系

属于与不属于 $\in ,\notin ,\not \in ,\ni ,\not \ni$ `\in, \notin, \not\in, \ni, \not\ni`

- 集合与集合的关系

包含于，子集 $\subseteq$ `\subseteq`  
真包含于，真子集 $\subsetneqq$ `\subsetneqq`  
不包含于，不是子集 $\nsubseteq$ `\nsubseteq`

立体几何中常把 $\subsetneqq$ 简写作 $\subset$。

- 集合运算

交集，并集 $\cap,\cup$ `\cap,\cup`

> 以上为国内教科书写法，完整符号表看 [这里](full_doc/symbols.md#集合)。

## 基本初等函数

- 对数函数 $\log x,\ln x,\lg x$ `\log x,\ln x,\lg x`
- 三角函数

## 立体几何

- 点、线、面的位置关系

## 向量

- 向量符号

## 逻辑

- 或、与、非
- 全称量词 (对于所有)
- 存在量词
- 充分条件/可推出
- 必要条件
- 充分必要条件/充要条件/等价于

## 统计与概率

- 最小二乘法/线性回归方程

## 微积分基础

- 无穷大/无限
- 极限
- 导数/导函数
- 积分

## 复数

## 计数原理

- 排列
- 组合

## 物理

- 正比于

## 希腊字母

正弦型函数 $y=A\sin(\omega x+\varphi)$ `y=A\sin(\omega x+\varphi)`：$\omega$ 圆频率或角频率，$\varphi$ 称为初相位或初相角，周期为 $T=\frac{2\pi}{\omega}$。

辅助角公式常用字母 $\varphi$ `\varphi`

摩擦因数/动摩擦因数 $\mu$ `\mu`  
平行板电容器的电容 $C=\frac{\varepsilon S}{4\pi k d}$：介电常数 $\varepsilon$ `\varepsilon`

更多希腊字母参见 [这里](full_doc/fonts.md#希腊字母)。

<!--
## 正则表达式笔记

### 公式后自动补源码

    \$([0-9a-zA-Z\(\)\[\]\{\} \\\^\+\-_]+?)\$ (?!`)

替换为

    $$$1$$ `$1` 

### 旧文档格式转新格式

    (.*?)\n\n(`.*?`)\n\n(\$.*?\$)

替换为

    $1 $3 $

或

    (?<=\n)(`.*?`)\n\n(\$.*?\$)

替换为

    $2 $1

### 去除 displaystyle

    \$\{\\displaystyle (.*?)\}\$

    $$$1$$