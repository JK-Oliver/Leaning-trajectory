# Latex

[toc]

## 基础知识

### 读法

TEX 读作“Tech” ，其中“ch” 的发音类似于“h” ，与汉字“泰赫”的发音类似。

LATEX 读作“Lah-tech” 或者“Lay-tech” ，近似于汉字“拉泰赫”或“雷泰赫”。

### 命令和环境

LATEX 命令以反斜线\开头，为以下两种形式之一：
			• 反斜线和后面的一串字母，如\LaTeX。它们以任意非字母符号（空格、数字、标点等）作为分隔符。
			• 反斜线和后面的一个非字母符号，如\$。它们无需分隔符。
			• LATEX 命令是对**大小写敏感**

字母形式的LATEX 命令忽略其后的所有空格。如果要人为引入空格，需要在命令后面加一对括号阻止其忽略空格：

```latex
Shall we call ourselves
\TeX users

or \TeX{} users?

//结果
Shall we call ourselves TEXusers
or TEX users?
```

*另外也可以在命令后面紧跟一个\␣ 命令（反斜线加空格），代表插入一个间距。比如\TeX\␣user 的输出效果就是TEX user。*



LATEX 命令中**每个参数用花括号{  和  } 包裹**。**带可选参数以方括号[  和   ] 包裹**。在命令名称后可以带一个星号*，带星号和不带星号的命令效果有一定差异。
	LATEX 的**花括号本身也起到分组的作用**，可以将字体、格式等的更改限制在大括号范围之内。
LATEX 还引入了环境的用法，用以令一些效果在局部生效，或是生成特定的文档元素。LATEX
环境的用法为一对命令\begin 和\end：

## 编译

### 分段函数

```latex
\documentclass[UTF8]{ctexart}

\begin{document}

\begin{equation}
R(x)=\left\{
\begin{array}{rcl}
\frac 1q & & {x = \frac pq ($p,q都属于正整数$)}\\
0 & & {x = 0,1$和无理数$}
\end{array} \right.
\end{equation}

\end{document}
```

![img](E:\FILE\MARKDOWN\IRQ%1XL1_42M62DNTU@9O8.png)

```latex
\documentclass[12pt]{article}

\begin{document}

\begin{equation}
R(x)=\left\{
\begin{array}{rcl}
\frac 1q & & {x = \frac pq (p,q \in N)}\\
0 & & {x = 0,1 \quad and \quad x \in R\setminus Q}
\end{array} \right.
\end{equation}

\end{document}
```

![QQ图片20200827205022](E:\FILE\MARKDOWN\QQ图片20200827205022.png)

### 公式编号问题

[CSDN](https://blog.csdn.net/qq_38526623/article/details/103704728)