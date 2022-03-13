## 矩阵、条件表达式、方程组

语法：

```latex
\begin{类型}
公式内容
\end{类型}
```

类型可以是：矩阵 `matrix` `pmatrix` `bmatrix` `Bmatrix` `vmatrix` `Vmatrix`、条件表达式 `cases`、多行对齐方程式 `aligned`、数组 `array`。

在公式内容中：在每一行中插入 `&` 来指定需要**对齐**的内容，在每行结尾处使用 `\\` **换行**。

### 无框矩阵

在开头使用 `begin{matrix}`，在结尾使用 `end{matrix}`，在中间插入矩阵元素，每个元素之间插入 `&` ，并在每行结尾处使用 `\\` 。

```latex
\begin{matrix}
x & y \\
z & v
\end{matrix}
```

${\displaystyle {\begin{matrix}x&y\\z&v\end{matrix}}}$

### 有框矩阵

在开头将 `matrix` 替换为 `pmatrix` 或 `bmatrix` 或 `Bmatrix` 或 `vmatrix` 或 `Vmatrix` 。

```latex
\begin{vmatrix}
x & y \\
z & v
\end{vmatrix}
```

${\displaystyle {\begin{vmatrix}x&y\\z&v\end{vmatrix}}}$

```latex
\begin{Vmatrix}
x & y \\
z & v
\end{Vmatrix}
```

${\displaystyle {\begin{Vmatrix}x&y\\z&v\end{Vmatrix}}}$

使用 `\cdots` $\cdots$ , `\ddots` $\ddots$ , `\vdots` $\vdots$ 来输入**省略符号**。

```latex
\begin{bmatrix}
0      & \cdots & 0      \\
\vdots & \ddots & \vdots \\
0      & \cdots & 0
\end{bmatrix}
```

${\displaystyle {\begin{bmatrix}0&\cdots &0\\\vdots &\ddots &\vdots \\0&\cdots &0\end{bmatrix}}}$

```latex
\begin{Bmatrix}
x & y \\
z & v
\end{Bmatrix}
```

${\displaystyle {\begin{Bmatrix}x&y\\z&v\end{Bmatrix}}}$

```latex
\begin{pmatrix}
x & y \\
z & v
\end{pmatrix}
```

${\displaystyle {\begin{pmatrix}x&y\\z&v\end{pmatrix}}}$

### 条件表达式

```latex
f(n) =
\begin{cases} 
n/2,  & \text{if }n\text{ is even} \\
3n+1, & \text{if }n\text{ is odd}
\end{cases}
```

${\displaystyle f(n)={\begin{cases}n/2,&{\text{if }}n{\text{ is even}}\\3n+1,&{\text{if }}n{\text{ is odd}}\end{cases}}}$

### 多行等式、同余式

人们经常想要一列整齐且居中的方程式序列。使用 `\begin{aligned}…\end{aligned}`。

```latex
\begin{aligned}
f(x) & = (m+n)^2 \\
     & = m^2+2mn+n^2 \\
\end{aligned}
```

${\displaystyle {\begin{aligned}f(x)&=(m+n)^{2}\\&=m^{2}+2mn+n^{2}\\\end{aligned}}}$

```latex
\begin{aligned}
3^{6n+3}+4^{6n+3} 
& \equiv (3^3)^{2n+1}+(4^3)^{2n+1}\\  
& \equiv 27^{2n+1}+64^{2n+1}\\  
& \equiv 27^{2n+1}+(-27)^{2n+1}\\ 
& \equiv 27^{2n+1}-27^{2n+1}\\
& \equiv 0 \pmod{91}\\
\end{aligned}
```

${\displaystyle {\begin{aligned}3^{6n+3}+4^{6n+3}&\equiv (3^{3})^{2n+1}+(4^{3})^{2n+1}\\&\equiv 27^{2n+1}+64^{2n+1}\\&\equiv 27^{2n+1}+(-27)^{2n+1}\\&\equiv 27^{2n+1}-27^{2n+1}\\&\equiv 0{\pmod {91}}\\\end{aligned}}}$

```latex
\begin{alignedat}{3}
f(x) & = (m-n)^2 \\
f(x) & = (-m+n)^2 \\
     & = m^2-2mn+n^2 \\
\end{alignedat}
```

${\displaystyle {\begin{alignedat}{3}f(x)&=(m-n)^{2}\\f(x)&=(-m+n)^{2}\\&=m^{2}-2mn+n^{2}\\\end{alignedat}}}$

### 方程组

```latex
\begin{cases}
3x + 5y +  z \\
7x - 2y + 4z \\
-6x + 3y + 2z
\end{cases}
```

$${\displaystyle {\begin{cases}3x+5y+z\\7x-2y+4z\\-6x+3y+2z\end{cases}}}$$

或

```latex
\left\{\begin{aligned}
3x + 5y +  z \\
7x - 2y + 4z \\
-6x + 3y + 2z
\end{aligned}\right.
```

$$
\left\{\begin{aligned}
3x + 5y +  z \\
7x - 2y + 4z \\
-6x + 3y + 2z
\end{aligned}\right.
$$


## 数组与表格

通常，一个格式化后的表格比单纯的文字或排版后的文字更具有可读性。数组和表格均以 `\begin{array}` 开头，并在其后定义列数及每一列的文本对齐属性，`c` `l` `r` 分别代表居中、左对齐及右对齐。若需要插入垂直分割线，在定义式中插入 `|` ，若要插入水平分割线，在下一行输入前插入 `\hline` 。与矩阵相似，每行元素间均须要插入 `&` ，每行元素以 `\\` 结尾，最后以 `\end{array}` 结束数组。

- 例子：
```latex
\begin{array}{c|lcr}
n & \text{左对齐} & \text{居中对齐} & \text{右对齐} \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i
\end{array}
```

- 显示：
$$
\begin{array}{c|lcr}
n & \text{左对齐} & \text{居中对齐} & \text{右对齐} \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i
\end{array}
$$

- 例子：

```latex
\begin{array}{lcl}
z        & = & a \\
f(x,y,z) & = & x + y + z 
\end{array}
```

- 显示：

${\displaystyle {\begin{array}{lcl}z&=&a\\f(x,y,z)&=&x+y+z\end{array}}}$

- 例子：

```latex
\begin{array}{lcr}
z        & = & a \\
f(x,y,z) & = & x + y + z    
\end{array}
```

- 显示：

${\displaystyle {\begin{array}{lcr}z&=&a\\f(x,y,z)&=&x+y+z\end{array}}}$

- 例子：

```latex
\begin{array}{ccc}
a & b & S \\
\hline
0&0&1\\
0&1&1\\
1&0&1\\
1&1&0\\
\end{array}
```

- 显示：

$${\displaystyle {\begin{array}{ccc}a&b&S\\\hline 0&0&1\\0&1&1\\1&0&1\\1&1&0\\\end{array}}}$$

### 嵌套数组或表格

多个数组/表格可 **互相嵌套** 并组成一组数组/一组表格。
使用嵌套前必须声明 `$$` 符号。

- 例子：
```latex
% outer vertical array of arrays 外层垂直表格
\begin{array}{c}
    % inner horizontal array of arrays 内层水平表格
    \begin{array}{cc}
        % inner array of minimum values 内层"最小值"数组
        \begin{array}{c|cccc}
        \text{min} & 0 & 1 & 2 & 3\\
        \hline
        0 & 0 & 0 & 0 & 0\\
        1 & 0 & 1 & 1 & 1\\
        2 & 0 & 1 & 2 & 2\\
        3 & 0 & 1 & 2 & 3
        \end{array}
    &
        % inner array of maximum values 内层"最大值"数组
        \begin{array}{c|cccc}
        \text{max}&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 1 & 2 & 3\\
        2 & 2 & 2 & 2 & 3\\
        3 & 3 & 3 & 3 & 3
        \end{array}
    \end{array}
    % 内层第一行表格组结束
    \\
    % inner array of delta values 内层第二行 Delta 值数组
        \begin{array}{c|cccc}
        \Delta&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 0 & 1 & 2\\
        2 & 2 & 1 & 0 & 1\\
        3 & 3 & 2 & 1 & 0
        \end{array}
        % 内层第二行表格组结束
\end{array}
```

- 显示：
$$
% outer vertical array of arrays 外层垂直表格
\begin{array}{c}
    % inner horizontal array of arrays 内层水平表格
    \begin{array}{cc}
        % inner array of minimum values 内层"最小值"数组
        \begin{array}{c|cccc}
        \text{min} & 0 & 1 & 2 & 3\\
        \hline
        0 & 0 & 0 & 0 & 0\\
        1 & 0 & 1 & 1 & 1\\
        2 & 0 & 1 & 2 & 2\\
        3 & 0 & 1 & 2 & 3
        \end{array}
    &
        % inner array of maximum values 内层"最大值"数组
        \begin{array}{c|cccc}
        \text{max}&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 1 & 2 & 3\\
        2 & 2 & 2 & 2 & 3\\
        3 & 3 & 3 & 3 & 3
        \end{array}
    \end{array}
    % 内层第一行表格组结束
    \\
    % inner array of delta values 内层第二行 Delta 值数组
        \begin{array}{c|cccc}
        \Delta&0&1&2&3\\
        \hline
        0 & 0 & 1 & 2 & 3\\
        1 & 1 & 0 & 1 & 2\\
        2 & 2 & 1 & 0 & 1\\
        3 & 3 & 2 & 1 & 0
        \end{array}
        % 内层第二行表格组结束
\end{array}
$$

### 用数组实现带分割符号的矩阵

- 例子：
```latex
$$
\left[
    \begin{array}{cc|c}
      1&2&3\\
      4&5&6
    \end{array}
\right]
$$
```

- 显示：
$$
\left[
    \begin{array}{cc|c}
      1&2&3\\
      4&5&6
    \end{array}
\right]
$$

其中 `cc|c` 代表在一个三列矩阵中的第二和第三列之间插入分割线。