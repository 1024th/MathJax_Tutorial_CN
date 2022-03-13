# 颜色

## [Cmd Markdown 公式指导手册](https://www.zybuluo.com/codeep/note/163962#%E4%B8%83%E4%BA%A4%E6%8D%A2%E5%9B%BE%E8%A1%A8%E4%BD%BF%E7%94%A8%E5%8F%82%E8%80%83)里是这样写的：

使用 `\color{颜色}{文字}` 来更改特定的文字颜色。
更改文字颜色 **需要浏览器支持** ，如果浏览器不知道你所需的颜色，那么文字将被渲染为黑色。

对于较旧的浏览器（HTML4 与 CSS2），以下颜色是被支持的：

| 输入   | 显示                   | 输入    | 显示                    |
|--------|------------------------|---------|-------------------------|
| black  | $\color{black}{text}$  | grey    | $\color{grey}{text}$    |
| silver | $\color{silver}{text}$ | white   | $\color{white}{text}$   |
| maroon | $\color{maroon}{text}$ | red     | $\color{red}{text}$     |
| yellow | $\color{yellow}{text}$ | lime    | $\color{lime}{text}$    |
| olive  | $\color{olive}{text}$  | green   | $\color{green}{text}$   |
| teal   | $\color{teal}{text}$   | auqa    | $\color{auqa}{text}$    |
| blue   | $\color{blue}{text}$   | navy    | $\color{navy}{text}$    |
| purple | $\color{purple}{text}$ | fuchsia | $\color{fuchsia}{text}$ |

对于较新的浏览器（HTML5 与 CSS3），额外的 124 种颜色将被支持：

输入 `\color {#rgb} {text}` 来自定义更多的颜色，其中 `#rgb` 的 `r` `g` `b` 可输入 `0-9` 和 `a-f` 来表示红色、绿色和蓝色的纯度（饱和度）。

- 例子：
```latex
\begin{array}{|rrrrrrrr|}\hline
\verb+#000+ & \color{#000}{text} & & &
\verb+#00F+ & \color{#00F}{text} & & \\
& & \verb+#0F0+ & \color{#0F0}{text} &
& & \verb+#0FF+ & \color{#0FF}{text}\\
\verb+#F00+ & \color{#F00}{text} & & &
\verb+#F0F+ & \color{#F0F}{text} & & \\
& & \verb+#FF0+ & \color{#FF0}{text} &
& & \verb+#FFF+ & \color{#FFF}{text}\\
\hline
\end{array}
```

- 显示：
$$
\begin{array}{|rrrrrrrr|}\hline
\verb+#000+ & \color{#000}{text} & & &
\verb+#00F+ & \color{#00F}{text} & & \\
& & \verb+#0F0+ & \color{#0F0}{text} &
& & \verb+#0FF+ & \color{#0FF}{text}\\
\verb+#F00+ & \color{#F00}{text} & & &
\verb+#F0F+ & \color{#F0F}{text} & & \\
& & \verb+#FF0+ & \color{#FF0}{text} &
& & \verb+#FFF+ & \color{#FFF}{text}\\
\hline
\end{array}
$$

- 例子：
```latex
\begin{array}{|rrrrrrrr|}
\hline
\verb+#000+ & \color{#000}{text} & \verb+#005+ & \color{#005}{text} & \verb+#00A+ & \color{#00A}{text} & \verb+#00F+ & \color{#00F}{text}  \\
\verb+#500+ & \color{#500}{text} & \verb+#505+ & \color{#505}{text} & \verb+#50A+ & \color{#50A}{text} & \verb+#50F+ & \color{#50F}{text}  \\
\verb+#A00+ & \color{#A00}{text} & \verb+#A05+ & \color{#A05}{text} & \verb+#A0A+ & \color{#A0A}{text} & \verb+#A0F+ & \color{#A0F}{text}  \\
\verb+#F00+ & \color{#F00}{text} & \verb+#F05+ & \color{#F05}{text} & \verb+#F0A+ & \color{#F0A}{text} & \verb+#F0F+ & \color{#F0F}{text}  \\
\hline
\verb+#080+ & \color{#080}{text} & \verb+#085+ & \color{#085}{text} & \verb+#08A+ & \color{#08A}{text} & \verb+#08F+ & \color{#08F}{text}  \\
\verb+#580+ & \color{#580}{text} & \verb+#585+ & \color{#585}{text} & \verb+#58A+ & \color{#58A}{text} & \verb+#58F+ & \color{#58F}{text}  \\
\verb+#A80+ & \color{#A80}{text} & \verb+#A85+ & \color{#A85}{text} & \verb+#A8A+ & \color{#A8A}{text} & \verb+#A8F+ & \color{#A8F}{text}  \\
\verb+#F80+ & \color{#F80}{text} & \verb+#F85+ & \color{#F85}{text} & \verb+#F8A+ & \color{#F8A}{text} & \verb+#F8F+ & \color{#F8F}{text}  \\
\hline
\verb+#0F0+ & \color{#0F0}{text} & \verb+#0F5+ & \color{#0F5}{text} & \verb+#0FA+ & \color{#0FA}{text} & \verb+#0FF+ & \color{#0FF}{text}  \\
\verb+#5F0+ & \color{#5F0}{text} & \verb+#5F5+ & \color{#5F5}{text} & \verb+#5FA+ & \color{#5FA}{text} & \verb+#5FF+ & \color{#5FF}{text}  \\
\verb+#AF0+ & \color{#AF0}{text} & \verb+#AF5+ & \color{#AF5}{text} & \verb+#AFA+ & \color{#AFA}{text} & \verb+#AFF+ & \color{#AFF}{text}  \\
\verb+#FF0+ & \color{#FF0}{text} & \verb+#FF5+ & \color{#FF5}{text} & \verb+#FFA+ & \color{#FFA}{text} & \verb+#FFF+ & \color{#FFF}{text}  \\
\hline
\end{array}
```

- 显示：
$$
\begin{array}{|rrrrrrrr|}
\hline
\verb+#000+ & \color{#000}{text} & \verb+#005+ & \color{#005}{text} & \verb+#00A+ & \color{#00A}{text} & \verb+#00F+ & \color{#00F}{text}  \\
\verb+#500+ & \color{#500}{text} & \verb+#505+ & \color{#505}{text} & \verb+#50A+ & \color{#50A}{text} & \verb+#50F+ & \color{#50F}{text}  \\
\verb+#A00+ & \color{#A00}{text} & \verb+#A05+ & \color{#A05}{text} & \verb+#A0A+ & \color{#A0A}{text} & \verb+#A0F+ & \color{#A0F}{text}  \\
\verb+#F00+ & \color{#F00}{text} & \verb+#F05+ & \color{#F05}{text} & \verb+#F0A+ & \color{#F0A}{text} & \verb+#F0F+ & \color{#F0F}{text}  \\
\hline
\verb+#080+ & \color{#080}{text} & \verb+#085+ & \color{#085}{text} & \verb+#08A+ & \color{#08A}{text} & \verb+#08F+ & \color{#08F}{text}  \\
\verb+#580+ & \color{#580}{text} & \verb+#585+ & \color{#585}{text} & \verb+#58A+ & \color{#58A}{text} & \verb+#58F+ & \color{#58F}{text}  \\
\verb+#A80+ & \color{#A80}{text} & \verb+#A85+ & \color{#A85}{text} & \verb+#A8A+ & \color{#A8A}{text} & \verb+#A8F+ & \color{#A8F}{text}  \\
\verb+#F80+ & \color{#F80}{text} & \verb+#F85+ & \color{#F85}{text} & \verb+#F8A+ & \color{#F8A}{text} & \verb+#F8F+ & \color{#F8F}{text}  \\
\hline
\verb+#0F0+ & \color{#0F0}{text} & \verb+#0F5+ & \color{#0F5}{text} & \verb+#0FA+ & \color{#0FA}{text} & \verb+#0FF+ & \color{#0FF}{text}  \\
\verb+#5F0+ & \color{#5F0}{text} & \verb+#5F5+ & \color{#5F5}{text} & \verb+#5FA+ & \color{#5FA}{text} & \verb+#5FF+ & \color{#5FF}{text}  \\
\verb+#AF0+ & \color{#AF0}{text} & \verb+#AF5+ & \color{#AF5}{text} & \verb+#AFA+ & \color{#AFA}{text} & \verb+#AFF+ & \color{#AFF}{text}  \\
\verb+#FF0+ & \color{#FF0}{text} & \verb+#FF5+ & \color{#FF5}{text} & \verb+#FFA+ & \color{#FFA}{text} & \verb+#FFF+ & \color{#FFF}{text}  \\
\hline
\end{array}
$$

## 维基百科的[数学公式教程](https://zh.wikipedia.org/wiki/Help:%E6%95%B0%E5%AD%A6%E5%85%AC%E5%BC%8F)里是这样写的：

语法：`{\color{颜色}表达式}`

**作者实测：在部分浏览器中，上面的语法可能是错误的**（只将表达式的第一个字符着色），`\color{颜色}{文字}`的语法才是正确的。例如：

`{\color{Red}abc}`显示${\color{Red}abc}$  
`\color{Red}{abc}`显示$\color{Red}{abc}$

**支持色调表：**

${\displaystyle \color {Apricot}{\text{Apricot}}}$

${\displaystyle \color {Aquamarine}{\text{Aquamarine}}}$

${\displaystyle \color {Bittersweet}{\text{Bittersweet}}}$

${\displaystyle \color {Black}{\text{Black}}}$

${\displaystyle \color {Blue}{\text{Blue}}}$

${\displaystyle \color {BlueGreen}{\text{BlueGreen}}}$

${\displaystyle \color {BlueViolet}{\text{BlueViolet}}}$

${\displaystyle \color {BrickRed}{\text{BrickRed}}}$

${\displaystyle \color {Brown}{\text{Brown}}}$

${\displaystyle \color {BurntOrange}{\text{BurntOrange}}}$

${\displaystyle \color {CadetBlue}{\text{CadetBlue}}}$

${\displaystyle \color {CarnationPink}{\text{CarnationPink}}}$

${\displaystyle \color {Cerulean}{\text{Cerulean}}}$

${\displaystyle \color {CornflowerBlue}{\text{CornflowerBlue}}}$

${\displaystyle \color {Cyan}{\text{Cyan}}}$

${\displaystyle \color {Dandelion}{\text{Dandelion}}}$

${\displaystyle \color {DarkOrchid}{\text{DarkOrchid}}}$

${\displaystyle \color {Emerald}{\text{Emerald}}}$

${\displaystyle \color {ForestGreen}{\text{ForestGreen}}}$

${\displaystyle \color {Fuchsia}{\text{Fuchsia}}}$

${\displaystyle \color {Goldenrod}{\text{Goldenrod}}}$

${\displaystyle \color {Gray}{\text{Gray}}}$

${\displaystyle \color {Green}{\text{Green}}}$

${\displaystyle \color {GreenYellow}{\text{GreenYellow}}}$

${\displaystyle \color {JungleGreen}{\text{JungleGreen}}}$

${\displaystyle \color {Lavender}{\text{Lavender}}}$

${\displaystyle \color {LimeGreen}{\text{LimeGreen}}}$

${\displaystyle \color {Magenta}{\text{Magenta}}}$

${\displaystyle \color {Mahogany}{\text{Mahogany}}}$

${\displaystyle \color {Maroon}{\text{Maroon}}}$

${\displaystyle \color {Melon}{\text{Melon}}}$

${\displaystyle \color {MidnightBlue}{\text{MidnightBlue}}}$

${\displaystyle \color {Mulberry}{\text{Mulberry}}}$

${\displaystyle \color {NavyBlue}{\text{NavyBlue}}}$

${\displaystyle \color {OliveGreen}{\text{OliveGreen}}}$

${\displaystyle \color {Orange}{\text{Orange}}}$

${\displaystyle \color {OrangeRed}{\text{OrangeRed}}}$

${\displaystyle \color {Orchid}{\text{Orchid}}}$

${\displaystyle \color {Peach}{\text{Peach}}}$

${\displaystyle \color {Periwinkle}{\text{Periwinkle}}}$

${\displaystyle \color {PineGreen}{\text{PineGreen}}}$

${\displaystyle \color {Plum}{\text{Plum}}}$

${\displaystyle \color {ProcessBlue}{\text{ProcessBlue}}}$

${\displaystyle \color {Purple}{\text{Purple}}}$

${\displaystyle \color {RawSienna}{\text{RawSienna}}}$

${\displaystyle \color {Red}{\text{Red}}}$

${\displaystyle \color {RedOrange}{\text{RedOrange}}}$

${\displaystyle \color {RedViolet}{\text{RedViolet}}}$

${\displaystyle \color {Rhodamine}{\text{Rhodamine}}}$

${\displaystyle \color {RoyalBlue}{\text{RoyalBlue}}}$

${\displaystyle \color {RoyalPurple}{\text{RoyalPurple}}}$

${\displaystyle \color {RubineRed}{\text{RubineRed}}}$

${\displaystyle \color {Salmon}{\text{Salmon}}}$

${\displaystyle \color {SeaGreen}{\text{SeaGreen}}}$

${\displaystyle \color {Sepia}{\text{Sepia}}}$

${\displaystyle \color {SkyBlue}{\text{SkyBlue}}}$

${\displaystyle \color {SpringGreen}{\text{SpringGreen}}}$

${\displaystyle \color {Tan}{\text{Tan}}}$

${\displaystyle \color {TealBlue}{\text{TealBlue}}}$

${\displaystyle \color {Thistle}{\text{Thistle}}}$

${\displaystyle \color {Turquoise}{\text{Turquoise}}}$

${\displaystyle \color {Violet}{\text{Violet}}}$

${\displaystyle \color {VioletRed}{\text{VioletRed}}}$

${\displaystyle \color {White}{\text{White}}}$

${\displaystyle \color {WildStrawberry}{\text{WildStrawberry}}}$

${\displaystyle \color {Yellow}{\text{Yellow}}}$

${\displaystyle \color {YellowGreen}{\text{YellowGreen}}}$

${\displaystyle \color {YellowOrange}{\text{YellowOrange}}}$

<sup>＊</sup>注︰输入时第一个字母必需以大写输入，如`\color{OliveGreen}`。

例子

*   `{\color{Blue}x^2}+{\color{Brown}2x} - {\color{OliveGreen}1}`

    ${\displaystyle {\color {Blue}x^{2}}+{\color {Brown}2x}-{\color {OliveGreen}1}}$ 

*   `x_{\color{Maroon}1,2}=\frac{-b\pm\sqrt{{\color{Maroon}b^2-4ac}}}{2a}`

    ${\displaystyle x_{\color {Maroon}1,2}={\frac {-b\pm {\sqrt {\color {Maroon}b^{2}-4ac}}}{2a}}}$ 
