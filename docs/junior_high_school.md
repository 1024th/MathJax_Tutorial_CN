# 初中

**注意：这里不含小学已经学过的符号。**

## 运算符号/函数符号

- 绝对值 $\left\vert s \right\vert$ `\left\vert s \right\vert`
- 乘方/指数/上标
  $a^n$ `a^n`或`a^{n}`；$a^{10}$ `a^{10}`
- 方根/根号  
  - 平方根 $\sqrt{x},\sqrt[2]{x}$ `\sqrt{x},\sqrt[2]{x}`  
  - 立方根/n次方根 $\sqrt[3]{x+y},\sqrt[n]{x}$ `\sqrt[3]{x+y},\sqrt[n]{x}`  
  - 根号 $\surd$ `\surd`
- 三角函数
  - 正弦 $\sin x$ `\sin x`
  - 余弦 $\cos \left(x+\frac \pi 2 \right)$ `\cos \left( x+\frac{\pi}{2} \right)`
  - 正切 $\tan x$ `\tan x`

## 一元二次方程

- 判别式 $\Delta = b^2-4ac$ `\Delta = b^2-4ac`

## 方程组/不等式组

$$\begin{cases}3x+5y+z\\7x-2y+4z\\-6x+3y+2z\end{cases}$$

```LaTeX
\begin{cases}
  3x + 5y +  z \\
  7x - 2y + 4z \\
  -6x + 3y + 2z
\end{cases}
```

或

$$
\left\{\begin{aligned}
3x + 5y +  z \\
7x - 2y + 4z \\
-6x + 3y + 2z
\end{aligned}\right.
$$

```
\left\{\begin{aligned}
  3x + 5y +  z \\
  7x - 2y + 4z \\
  -6x + 3y + 2z
\end{aligned}\right.
```

## 几何

- 因为、所以 $\because$ `\because` $\therefore$ `\therefore`
- 角的符号 $\angle A$ `\angle A`
- 平行符号
  - 自带的是竖直样式 $\parallel$ `\parallel`
  - 用斜杆+紧贴造一个倾斜的平行符号 $/\!/$ `/\!/`
  - 更繁琐的 $\mathrel{/\mskip-2.5mu/}$ `\mathrel{/\mskip-2.5mu/}`
- 垂直 $\perp$ `\perp`
- 平行且相等 LaTeX中没有这个符号
- 三角形符号 $\triangle$ `\triangle`（注意和一元二次方程的判别式 $\Delta$ 不同）
- 平行四边形的符号 LaTeX中没有这个符号，只能用Unicode字符`▱`
- 全等
  - 自带的与国内教科书方向相反 $\cong$
  - 想要 $≌$ 只能用Unicode字符`≌`
- 相似 
  - 国内教科书写法 $\backsim$ `\backsim`
  - 国外常见写法 $\sim$ `\sim`
- 圆的符号 $\odot,\bigodot$ `\odot,\bigodot`
- 弧的符号 MathJax里没有现成的符号，只能造一个 $\overset {\frown}{AB}$ `\overset {\frown}{AB}`

## 统计

- 平均数 $\bar{x}$ `\bar{x}`

## 希腊字母

常用于表示角的字母：阿尔法，贝塔，伽马 $\alpha \beta \gamma$ `\alpha \beta \gamma`  
一元二次方程的判别式 $\Delta$ `\Delta`

密度 $\rho$ `\rho`  
电阻单位 欧姆 $\Omega$ `\Omega`  
效率/机械效率/热效率 $\eta$ `\eta`  
电磁波 $c=\lambda\nu$：波长 $\lambda$ `\lambda`；频率 $\nu$ `\nu`

更多希腊字母参见[这里](document.md#希腊字母)
