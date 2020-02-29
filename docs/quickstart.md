# 快速入门

本文参考 [Cmd Markdown 公式指导手册](https://www.zybuluo.com/codeep/note/163962)

## 输入公式

行内公式用`$数学公式$`，行间公式用

```plain
$$
数学公式
$$
```

行内公式放在文中与其它文字混编，行间公式单独成行。例子：

行内公式 $x=1$ 与文字混排

行间公式
$$
x=1
$$
独立成行

```markdown
行内公式 $x=1$ 与文字混排

行间公式
$$
x=1
$$
独立成行
```

> 若需要给公式编号，参见 [大括号和行标的使用](#大括号和行标的使用) 。

## 上下标

`^` 表示上标，`_` 表示下标。如果上下标的内容多于一个字符，需要用 `{}` 将这些内容括成一个整体。上下标可以嵌套，也可以同时使用，上下标的先后次序并不重要，二者互不影响。

例子：$x^{y^z}=(1+{\rm e}^x)^{-2xy^w}$

有时需要在符号的左上，左下角加上角标，此时可以在要加角标字符前面使用空的分组，给空分组加角标：${}_m^n H$ `{}_m^n H`

### 撇号

数学公式中的 $'$ 号（一个英文单引号`'`）就是一种特殊的上标，撇号可以与下标混用，也可以连续使用（普通的上标不能连续使用），但不能与上标直接混用。例子：

$a = a'$ `a = a'`

$b_0' = b_0''$ `b_0' = b_0''`

${c'}^2 = (c')^2$ `{c'}^2 = (c')^2`

${\color{Red}{\rm Bad:}}$ $c'^2$ `c'^2`

### 角度

Latex没有直接表示角度的符号，可以用符号 $\circ$（`\circ`）的上标表示。例子：$\angle A = 90^\circ$ `\angle A = 90^\circ`

----------

以下未整理

----------


### 数学算子中上下标的位置

在显示公式中，多数数学算子的上下标，位置是在正上或正下方

$\max_n f(n) = \sum_{i=0}^n A_i$ `\max_n f(n) = \sum_{i=0}^n A_i`

但对于积分号等个别算子，显示公式的上下标也在右上左下角：

$\int_0^1 f(t) \ dt = \iint_D g(x,y) \ dx dy$ \int_0^1 f(t) \ dt = \iint_D g(x,y) \ dx dy

其实也可以手动改变上下标的位置. 在上下标前用\limits命令会使上下标在正上正下方，而使用\nolimits则使上下标在角上

$\iiint\limits_D \ df = \max\nolimits_D g$ `\iiint\limits_D \ df = \max\nolimits_D g`

$\sum\nolimits_{i=0}^n A_i = \sum_{i=0}^n A_i$ `\sum\nolimits_{i=0}^n A_i = \sum_{i=0}^n A_i`

### overser/underset

如果我们想要给任意符号的上下方添加标记，那么我们可以使用 `overset` 和 `underset` 命令

$\overset{*}{X}$ `\overset{*}{X}`

$\underset{*}{X}$ `\underset{*}{X}`

$\overset{*}{\underset{@}{X}}$ `\overset{*}{\underset{@}{X}}`

14. 上下画线与花括号，\overline 与\overunder命令可以用来在公式的上方和下方划横线

$\overline{a+b} = \overline a + \overline b$ \overline{a+b} = \overline a + \overline b

$\underline a = (a_0，a_1，a_2，\dots)$ \underline a = (a_0，a_1，a_2，\dots)

这种结构可以任意嵌套或与其他数学结构组合 

$\overline{\underline{\underline a} + \overline{b}^2} - c^{\underline n}$ `\overline{\underline{\underline a} + \overline{b}^2} - c^{\underline n}`

15. 与上一条类似，如果你想要在公式上加箭头\overleftarrow，\overrightarrow，overleftrightarrow，underleftarrow，underrightarrow，underleftrightarrow，此外，还可以使用overbrace 和underbrace带上花括号，并可以使用上下角标在花括号上作标注

$\overleftrightarrow{a+b}$ `\overleftrightarrow{a+b}`

$( \overbrace{a_0，a_1，\dots，a_n} ^{\text{共 n + 1 项}} ) = ( \underbrace{0，0，\dots，0}_{n}，1 )$ `( \overbrace{a_0，a_1，\dots，a_n} ^ {\text{共 n + 1 项}} ) = ( \underbrace{0，0，\dots，0}_{n}，1 )`

16. 分式. 在Latex中，分式用frac<分子><分母>得到

$\frac 12 + \frac 1a = \frac{2+a}{2a}$ `\frac 12 + \frac 1a = \frac{2+a}{2a}`

有时需要指定较大或者较小的分式，可以使用\dfrac和\tfrac

$\tfrac 12 f(x) = \frac{1}{\dfrac 1a + \dfrac 1b + c}$ `\tfrac 12 f(x) = \frac{1}{\dfrac 1a + \dfrac 1b + c}`

连分式是一种特殊的分式，cfrac专用于输入连分式。

$\cfrac{1}{1 + \cfrac{2}{1 + \cfrac{3}{1+x}}} = \cfrac[r]{1}{1 + \cfrac{2}{1 + \cfrac[l]{3}{1+x}}}$

`\cfrac{1}{1 + \cfrac{2}{1 + \cfrac{3}{1+x}}} = \cfrac[r]{1}{1 + \cfrac{2}{1 + \cfrac[l]{3}{1+x}}}`

17. 二项式系数. \binom 用于输入二项式系数，其用法与\frac类似

$(a + b) ^ 2 = \binom 20 a ^ 2 + \binom 21 ab + \binom 22 b ^ 2$ `(a + b) ^ 2 = \binom 20 a ^ 2 + \binom 21 ab + \binom 22 b ^ 2`

18. 根式. 在Latex中用 \sqrt得到，同时可以带一个参数，表示开方的次数

$\sqrt 4 = \sqrt[3]{8} = 2$ `\sqrt 4 = \sqrt[3]{8} = 2`

19. 矩阵. 在Latex中，矩阵是用 `\matrix` 和 `\pmatrix` 排版的，在矩阵环境中，不同的列用符号 & 分隔，行用\\分隔，矩阵每列中元素居中对齐

$A = \begin{pmatrix} a_{11} & a_{12} & a_{13} \\ 0 & a_{22} & a_{23} \\ 0 & 0 & a_{33} \end{pmatrix}$ `A = \begin{pmatrix} a_{11} & a_{12} & a_{13} \\ 0 & a_{22} & a_{23} \\ 0 & 0 & a_{33} \end{pmatrix}`

在矩阵中经常使用各种省略号，即dots，vdots，ddots等

$A = \begin{pmatrix} a_{11} & \dots & a_{1n} \\ & \ddots & \vdots \\ 0 & & a_{nn} \end{pmatrix}_{n \times n}$ `A = \begin{pmatrix} a_{11} & \dots & a_{1n} \\ & \ddots & \vdots \\ 0 & & a_{nn} \end{pmatrix}_{n \times n}`

还有跨多行的省略号 \hdotsfor{<列数>}，反向斜省略号\iddots，方便排版一些矩阵

矩阵可以嵌套使用，比如分块矩阵

$\begin{pmatrix} \begin{matrix} 1 & 0 \\ 0 & 1 \end{matrix} & \text{\large 0} \\ \text {\lagre 0} & \begin{matrix} 1 & 0 \\ 0 & -1 \end{matrix} \end{pmatrix}$ `\begin{pmatrix} \begin{matrix} 1 & 0 \\ 0 & 1 \end{matrix} & \text{\large 0} \\ \text {\large 0} & \begin{matrix} 1 & 0 \\ 0 & -1 \end{matrix} \end{pmatrix}` 可能掘金不支持字体大小的渲染

20. 在上下标特别是求和式的上下限中，有时需要好几行的内容，此时可以使用\substack命令排版

$\sum_{\substack{0<i<n \\ 0<j<i}} A_{ij}$ `\sum_{\substack{0<i<n \\ 0<j<i}} A_{ij}`

## 数学公式中经常使用符号大全

1. 小写希腊字母

2. 大写希腊字母

3. 数学普通符号

4. 可同时用在文本和数学模式中的符号

5. 数学算子

6. 不带上下限的数学算子名

7. 带上下限的数学算子名

8. Latex中的二元运算符

9. 二元关系符及其否定形式

10. 箭头符号

11. 括号定界符

12. 非括号定界符

13. 手工调整定界符大小

14. 数学标点符号

15. 数学省略号
