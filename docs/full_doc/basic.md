# 完整文档

！待整理

> 参考维基百科的 [数学公式教程](https://zh.wikipedia.org/wiki/Help:%E6%95%B0%E5%AD%A6%E5%85%AC%E5%BC%8F)；   
> 参考 [Cmd Markdown 公式指导手册](https://www.zybuluo.com/codeep/note/163962#%E4%B8%83%E4%BA%A4%E6%8D%A2%E5%9B%BE%E8%A1%A8%E4%BD%BF%E7%94%A8%E5%8F%82%E8%80%83)。

本文为 MathJax 在 Markdown 环境下的语法指引。

## 如何插入公式

$\LaTeX$ 的数学公式有两种：行中公式和独立公式（行间公式）。行中公式放在文中与其它文字混编，独立公式单独成行。

行中公式可以用如下方法表示：

`$ 数学公式 $`

独立公式可以用如下方法表示：

`$$ 数学公式 $$`

## 上标、下标及积分等

功能 | 语法 | 效果

`^` 表示上标，`_` 表示下标。如果上下标的内容多于一个字符，需要用 `{}` 将这些内容括成一个整体。上下标可以嵌套，也可以同时使用。

上标

`a^2`

${\displaystyle a^{2}}$

下标

`a_2`

${\displaystyle a_{2}}$

组合

`a^{2+2}`

${\displaystyle a^{2+2}}$

`a_{i,j}`

${\displaystyle a_{i,j}}$

结合上下标

`x_2^3`

${\displaystyle x_{2}^{3}}$

前置上下标

`{}_1^2\!X_3^4`

${\displaystyle {}_{1}^{2}\!X_{3}^{4}}$

导数（**HTML**）

`x'`

${\displaystyle x'}$

导数（**PNG**）

`x^\prime`

${\displaystyle x^{\prime}}$

导数（**错误**）

`x\prime`

${\displaystyle x\prime}$

导数点

`\dot{x}`

${\displaystyle {\dot {x}}}$

`\ddot{y}`

${\displaystyle {\ddot {y}}}$

向量

`\vec{c}`（只有一个字母）

${\displaystyle {\vec {c}}}$

`\overleftarrow{a b}`

${\displaystyle {\overleftarrow {ab}}}$

`\overrightarrow{c d}`

${\displaystyle {\overrightarrow {cd}}}$

`\overleftrightarrow{a b}`

${\displaystyle {\overleftrightarrow {ab}}}$

`\widehat{e f g}`

${\displaystyle {\widehat {efg}}}$

上弧

（注：正确应该用 \overarc，但在这里行不通。要用建议的语法作为解决办法。）（使用 \ overarc 时需要引入 {arcs} 包。）

`\overset{\frown} {AB}`

${\displaystyle {\overset {\frown}{AB}}}$

上划线

`\overline{h i j}`

${\displaystyle {\overline {hij}}}$

下划线

`\underline{k l m}`

${\displaystyle {\underline {klm}}}$

上括号

`\overbrace{1+2+\cdots+100}`

${\displaystyle \overbrace {1+2+\cdots +100} }$

`\begin{matrix} 5050 \\ \overbrace{ 1+2+\cdots+100 } \end{matrix}`

${\displaystyle {\begin{matrix}5050\\\overbrace {1+2+\cdots +100} \end{matrix}}}$

下括号

`\underbrace{a+b+\cdots+z}`

${\displaystyle \underbrace {a+b+\cdots +z} }$

`\begin{matrix} \underbrace{ a+b+\cdots+z } \\ 26 \end{matrix}`

${\displaystyle {\begin{matrix}\underbrace {a+b+\cdots +z} \\26\end{matrix}}}$

求和（累加）

`\sum_{k=1}^N k^2`

${\displaystyle \sum _{k=1}^{N}k^{2}}$

`\begin{matrix} \sum_{k=1}^N k^2 \end{matrix}`

${\displaystyle {\begin{matrix}\sum _{k=1}^{N}k^{2}\end{matrix}}}$

求积（累乘）

`\prod_{i=1}^N x_i`

${\displaystyle \prod _{i=1}^{N}x_{i}}$

`\begin{matrix} \prod_{i=1}^N x_i \end{matrix}`

${\displaystyle {\begin{matrix}\prod _{i=1}^{N}x_{i}\end{matrix}}}$

上积

`\coprod_{i=1}^N x_i`

${\displaystyle \coprod _{i=1}^{N}x_{i}}$

`\begin{matrix} \coprod_{i=1}^N x_i \end{matrix}`

${\displaystyle {\begin{matrix}\coprod _{i=1}^{N}x_{i}\end{matrix}}}$

极限

`\lim_{n \to \infty}x_n`

${\displaystyle \lim _{n\to \infty}x_{n}}$

`\begin{matrix} \lim_{n \to \infty}x_n \end{matrix}`

${\displaystyle {\begin{matrix}\lim _{n\to \infty }x_{n}\end{matrix}}}$

积分

`\int_{-N}^{N} e^x\, {\rm d}x`

${\displaystyle \int _{-N}^{N}e^{x}\,{\rm d} x}$

本例中 `\,` 和 `{\rm d}` 部分可省略，但建议加入，能使式子更美观。`{\rm d}`可以用`\mathrm{d}`等价替换。

`\begin{matrix} \int_{-N}^{N} e^x\, \mathrm{d}x \end{matrix}`（矩阵中积分符号变小）

${\displaystyle {\begin{matrix}\int _{-N}^{N}e^{x}\,\mathrm {d} x\end{matrix}}}$

双重积分

`\iint_{D}^{W} \, \mathrm{d}x\,\mathrm{d}y`

${\displaystyle \iint _{D}^{W}\,\mathrm {d} x\,\mathrm {d} y}$

三重积分

`\iiint_{E}^{V} \, \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z`

${\displaystyle \iiint _{E}^{V}\,\mathrm {d} x\,\mathrm {d} y\,\mathrm {d} z}$

闭合的曲线、曲面积分

`\oint_{C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y`

${\displaystyle \oint _{C}x^{3}\,\mathrm {d} x+4y^{2}\,\mathrm {d} y}$

交集

`\bigcap_1^{n} p`

${\displaystyle \bigcap _{1}^{n}p}$

并集

`\bigcup_1^{k} p`

${\displaystyle \bigcup _{1}^{k}p}$

## 分数

通常使用 `\frac {分子} {分母}` 命令产生一个分数，分数可嵌套。
便捷情况可直接输入 `\frac ab` 来快速生成一个 $\frac ab$ 。
如果分式很复杂，亦可使用 `分子 \over 分母` 命令，此时分数仅有一层。

功能 | 语法 | 效果

分数

`\frac{2}{4}=0.5`

${\displaystyle {\frac {2}{4}}=0.5}$

小型分数

`\tfrac{2}{4} = 0.5`

${\displaystyle {\tfrac {2}{4}}=0.5}$

连分式（大型嵌套分式）

`\cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} = a`

${\displaystyle {\cfrac {2}{c+{\cfrac {2}{d+{\cfrac {2}{4}}}}}}=a}$

大型不嵌套分式

`\dfrac{2}{4} = 0.5 \qquad \dfrac{2}{c + \dfrac{2}{d + \dfrac{2}{4}}} = a`

${\displaystyle {\dfrac {2}{4}}=0.5\qquad {\dfrac {2}{c+{\dfrac {2}{d+{\dfrac {2}{4}}}}}}=a}$

二项式系数

`\dbinom{n}{r}=\binom{n}{n-r}=\mathrm{C}_n^r=\mathrm{C}_n^{n-r}`

${\displaystyle {\dbinom {n}{r}}={\binom {n}{n-r}}=\mathrm {C} _{n}^{r}=\mathrm {C} _{n}^{n-r}}$

小型二项式系数

`\tbinom{n}{r}=\tbinom{n}{n-r}=\mathrm{C}_n^r=\mathrm{C}_n^{n-r}`

${\displaystyle {\tbinom {n}{r}}={\tbinom {n}{n-r}}=\mathrm {C} _{n}^{r}=\mathrm {C} _{n}^{n-r}}$

大型二项式系数

`\binom{n}{r}=\dbinom{n}{n-r}=\mathrm{C}_n^r=\mathrm{C}_n^{n-r}`

${\displaystyle {\binom {n}{r}}={\dbinom {n}{n-r}}=\mathrm {C} _{n}^{r}=\mathrm {C} _{n}^{n-r}}$

在以 e 为底的指数函数、极限和积分中尽量不要使用 `\frac` 符号：它会使整段函数看起来很怪，而且可能产生歧义。也正是因此它在专业数学排版中几乎从不出现。
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

## 括号

`()`、`[]` 和 `|` 表示符号本身，使用 `\{\}` 来表示 `{}` 。

功能 | 语法 | 显示

短括号

`\frac{1}{2}`

${\displaystyle ({\frac {1}{2}})}$

长括号

`\left(\frac{1}{2} \right`

${\displaystyle \left({\frac {1}{2}}\right)}$

使用 `\left` 和 `\right` 来创建自动匹配高度的 (圆括号)，[方括号] 和 {花括号} 。

功能 | 语法 | 显示

圆括号，小括号

`\left( \frac{a}{b} \right)`

${\displaystyle \left({\frac {a}{b}}\right)}$

方括号，中括号

`\left[ \frac{a}{b} \right]`

${\displaystyle \left[{\frac {a}{b}}\right]}$

花括号，大括号

`\left{ \frac{a}{b} \right}`

${\displaystyle \left\{{\frac {a}{b}}\right\}}$

角括号

`\left \langle \frac{a}{b} \right \rangle`

${\displaystyle \left\langle {\frac {a}{b}}\right\rangle }$

单竖线，绝对值

`\left| \frac{a}{b} \right|`

${\displaystyle \left| \frac{a}{b} \right|}$

双竖线，范

`\left \| \frac{a}{b} \right \|`

${\displaystyle \left\|{\frac {a}{b}}\right\|}$

取整函数

`\left \lfloor \frac{a}{b} \right \rfloor`

${\displaystyle \left\lfloor {\frac {a}{b}}\right\rfloor }$

取顶函数

`\left \lceil \frac{c}{d} \right \rceil`

${\displaystyle \left\lceil {\frac {c}{d}}\right\rceil }$

斜线与反斜线

`\left / \frac{a}{b} \right \backslash`

${\displaystyle \left/{\frac {a}{b}}\right\backslash }$

上下箭头

`\left \uparrow \frac{a}{b} \right \downarrow`

${\displaystyle \left\uparrow {\frac {a}{b}}\right\downarrow }$

`\left \Uparrow \frac{a}{b} \right \Downarrow`

${\displaystyle \left\Uparrow {\frac {a}{b}}\right\Downarrow }$

`\left \updownarrow \frac{a}{b} \right \Updownarrow`

${\displaystyle \left\updownarrow {\frac {a}{b}}\right\Updownarrow }$

混合括号

`\left[ 0,1 \right)`

${\displaystyle \left[0,1\right)}$ 

`\left \langle \psi \right |`

$\left \langle \psi \right |$

如果括号只有一边，要用 `\left.` 或 `\right.` 匹配另一边。

单左括号

`\left \{\frac{a}{b} \right.`

${\displaystyle \left\{{\frac {a}{b}}\right.}$

单右括号

`\left. \frac{a}{b} \right \}`

${\displaystyle \left.{\frac {a}{b}}\right\}}$

备注：

- 可以使用 `\big, \Big, \bigg, \Bigg` 控制括号的大小，比如代码

  `\Bigg ( \bigg [ \Big \{ \big \langle \left | \| \frac{a}{b} \| \right | \big \rangle \Big \} \bigg ] \Bigg )`

  显示︰

  $$\Bigg ( \bigg [ \Big \{ \big \langle \left | \| \frac{a}{b} \| \right | \big \rangle \Big \} \bigg ] \Bigg )$$ 

## 空格

注意 TeX 能够自动处理大多数的空格，但是您有时候需要自己来控制。

功能 | 语法 | 显示 | 宽度

### 2 个 quad 空格

`\alpha\qquad\beta`

${\displaystyle \alpha \qquad \beta}$

${\displaystyle mm}$

### quad 空格

`\alpha\quad\beta`

${\displaystyle \alpha \quad \beta}$

${\displaystyle m}$

### 大空格

`\alpha\ \beta`

${\displaystyle \alpha \ \beta}$

${\displaystyle {\frac{m}{3}}}$

### 中等空格

`\alpha\;\beta`

${\displaystyle \alpha \;\beta}$

${\displaystyle {\frac {2m}{7}}}$

### 小空格

`\alpha\,\beta`

${\displaystyle \alpha \,\beta}$

${\displaystyle {\frac {m}{6}}}$

### 没有空格

`\alpha\beta`

${\displaystyle \alpha \beta }$

${\displaystyle 0}$

### 紧贴

`\alpha\!\beta`

${\displaystyle \alpha \!\beta}$

${\displaystyle -{\frac {m}{6}}}$
