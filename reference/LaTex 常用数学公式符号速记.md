LaTex 常用数学公式符号速记
================

2019-01-24

[](# "公式")公式
------------

LaTex的行内公式和行间公式区别如下：  

1  
2  
3  
4  
5  
6  
7  
8  
9  

\\usepackage{amsmath}  % 此处引入数学公式的包  
  
% 行内公式  
This is an inline formula. $a = \\sqrt{b + c}$.  
  
% 行间公式, 带编号  
\\begin{equation}  
E = mc^2  
\\end{equation}  

以下均以行内公式呈现。  
| 数学公式类型 | 例子 | LaTex代码 |  
| ————– | ———————————————————— | ———————————————————— |  
| 分式 | 1+2x3+2y1+2x3+2y\\frac{1+ 2x}{3 + 2y} | \\frac{1+ 2x}{3 + 2y} |  
| 下标 | a2a2a\_{2} | a\_{2} |  
| 上标 | a2a2a^{2} | a^{2} |  
| 平均数 | ¯aa¯\\bar{a} | \\bar{a} |  
| 向量 | ⃗aa→\\vec{a} | \\vec{a} |  
| 二项式系数 | (ab+c)(ab+c)\\binom{a}{b + c} | \\binom{a}{b + c} |  
| 变量省略号 | F(x1,x2,…,xn)F(x1,x2,…,xn)F(x\_{1}, x\_{2}, \\ldots , x\_{n}) | F(x\_{1}, x\_{2}, \\ldots , x\_{n}) |  
| 公式内省略号 | x1+x2+⋯+xnx1+x2+⋯+xnx\_{1} + x\_{2} + \\cdots + x\_{n} | x\_{1} + x\_{2} + \\cdots + x\_{n} |  
| 矩阵(无修饰) | a+b+cuvx−y27\\a+bu+vz134a+b+cuvx−y27\\a+bu+vz134\\begin{matrix}a + b + c & uv & x - y & 27\\a + b & u + v & z & 134\\end{matrix} | \\ begin{matrix}a + b + c & uv & x - y & 27\\ \\a + b & u + v & z & 134\\ end{matrix} |  
| 矩阵(带小括号) | (a+b+cuv\\a+bu+v)(a+b+cuv\\a+bu+v)\\begin{pmatrix}a + b + c & uv\\a + b & u + v\\end{pmatrix} | \\ begin{pmatrix}a + b + c & uv \\\\a + b&u + v \\ end{pmatrix} |  
| 矩阵(带竖号) | |a+b+cuv\\a+bu+v||a+b+cuv\\a+bu+v|\\begin{vmatrix}a + b + c & uv\\a + b & u + v\\end{vmatrix} | \\ begin{vmatrix}a + b + c & uv \\\\ a + b&u + v \\ end{vmatrix} |  
| 开方 | n√ttn\\sqrt\[n\]{t} | \\sqrt\[n\]{t} |  
| 累加 | ∑ni\=1x2i∑i\=1nxi2\\sum\_{i=1}^{n} x\_{i}^{2} | \\sum\_{i=1}^{n} x\_{i}^{2} |  
| 累积 | ∏ni\=1x2i∏i\=1nxi2\\prod\_{i=1}^{n} x\_{i}^{2} | \\prod\_{i=1}^{n} x\_{i}^{2} |  
| 极限 | limx→af(x)−f(a)x−alimx→af(x)−f(a)x−a\\lim\_{x \\to a}{ \\frac{f(x) - f(a)}{x - a}} | \\lim\_{x \\to a}{ \\frac{f(x) - f(a)}{x - a}} |  
| 积分 | ∫baf(x)dx∫abf(x)dx\\int\_{a}^b f(x)\\, dx | \\int\_{a}^b f(x) \\, dx |  
（注：矩阵表示中 ‘\\’ 和begin，end之间无空格。因为如果有空格，csdn渲染无法显示源码。。  
更多内容访问[链接](http://tex.loria.fr/general/mil.pdf)。

* * *

[](# "符号")符号
============

![](https://raw.githubusercontent.com/JoshuaQYH/blogImage/master/20190121225011.png)

![](https://raw.githubusercontent.com/JoshuaQYH/blogImage/master/20190121225100.png)

![](https://raw.githubusercontent.com/JoshuaQYH/blogImage/master/20190121225115.png)

![](https://img-blog.csdnimg.cn/20190121225156326.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0NWU3ZzdnN2c3Zz,size_16,color_FFFFFF,t_70)

更多符号访问[链接\[PDF\]](http://math.ecnu.edu.cn/~latex/docs/others/mathsymb.pdf), 或[博客](https://blog.csdn.net/ws_20100/article/details/49159291)。

需要美赛LaTex模板及使用方法，请访问此[博文](https://blog.csdn.net/CVSvsvsvsvs/article/details/86555582)。

> Last updated: 2019-05-16 22:01:09  
> Thanks for your reading :) | URL [https://joshuaqyh.github.io/2019/01/24/LaTex-常用数学公式符号速记/](https://joshuaqyh.github.io/2019/01/24/LaTex-常用数学公式符号速记/)
> 
>  [![Qiuyihao](https://joshuaqyh.github.io/img/avatar.jpg) Qiuyihao](https://joshuaqyh.github.io) 

*   [LaTex](https://joshuaqyh.github.io/tags/LaTex/)
*   [Writing](https://joshuaqyh.github.io/tags/Writing/)