[TOC]
# 一级标题
## 二级标题
### 三级标题
生成标题采用如下代码：
```markdown
# 一级标题
## 二级标题
### 三级标题
```

# 语法
## 文章结构
### 目录
生成目录采用如下代码
```markdown
[TOC]
```
### 列表
* 无序列表
  * 嵌套无序列表
  * 嵌套无序列表
* 无序列表
* 无序列表
1. 有序列表 1
   1. 嵌套有序列表 1
   2. 嵌套有序列表 2
2. 有序列表 2
3. 有序列表 3
<br>
代码如下：
```markdown
* 无序列表
  * 嵌套无序列表
  * 嵌套无序列表
* 无序列表
* 无序列表
1. 有序列表 1
   1. 嵌套有序列表 1
   2. 嵌套有序列表 2
2. 有序列表 2
3. 有序列表 3
```
### 链接
插入链接：
[百度搜索]("www.baidu.com")

<br>

采用代码如下：

```markdown
[百度搜索]("www.baidu.com")
```

### 注释
<!-- 你看不见我 -->
```markdown
<!-- 你看不见我 -->
```
==快捷键 Ctrl + / 将当前行注释和反注释==
## 外观
### 字体
效果如下：
*斜体* 或者 _斜体_
**粗体**
***加粗斜体***
~~删除线~~

<br>

采用代码如下：
```markdown
*斜体* 或者 _斜体_
**粗体**
***加粗斜体***
~~删除线~~
```
### 引用
效果如下：
> 引用内容

<br>

采用代码如下：

```markdown
> 引用内容
```
### 代码环境
效果如下：
```python{.line-numbers}
    #!/usr/bin/python3
    print("Hello, World!");
```
<br>
采用代码如下：（其中“/”是多余的）

```markdown
/```python{.line-numbers}
    #!/usr/bin/python3
    print("Hello, World!");
/```
```

行内代码引用用一对`即可
## 图表
### 图片
[超链接名称](链接地址)

![图片提示语](图片地址)

==已应用插件：快捷键Ctrl+alt+V粘贴图片==
![示例](image/2021-07-09-21-59-23.png)
###表格

| 表头 | 表头 |
| ---- | ---- |
| 内容 | 内容 |
| 内容 | 内容 |

采用代码如下：
```markdown
[超链接名称](链接地址)

![图片提示语](图片地址)

| 表头 | 表头 |
| ---- | ---- |
| 内容 | 内容 |
| 内容 | 内容 |
```
## LaTeX
本文中VS CODE插件据来自于
[这篇文章]("https://orangex4.cool/post/notes-in-markdown/#%E5%9C%A8%E7%BA%BF%E6%B5%8F%E8%A7%88")
### 插入公式 
行内公式：
$\int ^1_0 f(x)dx$
行间公式：
$$
\begin{align}
&\int ^1_0 [f(x)+g(x)]dx \\
=&\int ^1_0 f(x)dx+\int ^1_0 g(x)dx\end{align}
$$
<br>采用代码如下：

```markdown
行内公式：
$\int ^1_0 f(x)dx$
行间公式：
$$
\begin{align}
&\int ^1_0 [f(x)+g(x)]dx \\
=&\int ^1_0 f(x)dx+\int ^1_0 g(x)dx\end{align}
$$
```

### 自动补全
#### 关于下标
$$
\begin{align*}
x^{-1}\\
\alpha_1,\alpha_2,\cdots,\alpha_n
\end{align*}
$$
```
\\-1 ⇒ ^{-1}
\\comma ⇒ \alpha_1,\alpha_2,\cdots,\alpha_n
```

#### 关于分式

选中文本时:
```
x+1 + \\frac ⇒ \frac{x+1}{}
```
在自动补全之后, 按下 Tab 键可以切换到下一个位置

对于根式有类似的补全:
$$
\sqrt[n]{x+1}
$$
```
x+1 + \\sqrt ⇒ \sqrt{x+1}
x+1 + \\sqrt ⇒ \sqrt[n]{x+1}
```
#### 关于巨算符
$$\lim_{n\to \infty}x_n$$
```
\\sum ⇒ \sum_{i=1}
\\prod ⇒ \prod_{i=1}
\\lim ⇒ \lim_{x\to \infty}
```

#### 括号
$$
\begin{aligned}
    \langle x,y\rangle\\
    \{x_1,x_2,\cdots,x_n\}\\
    \left( \alpha \right)
\end{aligned}
$$
```
\\angel ⇒ \langle \rangle
\\set ⇒ \{ \}
\\bracket ⇒ \left( \right)
\\square_bracket ⇒ \left[ \right]
\\curly_bracket ⇒ \left\{ \right}
```
#### 方程组
$$
\begin{cases}
    x_{11}+x_{12}+\cdots+x_{1n}=b_1\\
    x_{11}+x_{12}+\cdots+x_{1n}=b_2\\
    \quad \cdots\\
    x_{m1}+x_{m2}+\cdots+x_{mn}=b_m
\end{cases}
$$
```
$$
\begin{cases}
    x_{11}+x_{12}+\cdots+x_{1n}=b_1\\
    x_{11}+x_{12}+\cdots+x_{1n}=b_2\\
    \quad \cdots\\
    x_{m1}+x_{m2}+\cdots+x_{mn}=b_m
\end{cases}
$$
```
#### 矩阵
$$
\begin{pmatrix}x_1\\x_2\\\vdots\\x_n\end{pmatrix}
$$

$$
\begin{pmatrix}1&1&1\\1&1&1\\1&1&1\end{pmatrix}
$$
矩阵自动补全
```\\p22matrix ⇒ \begin{pmatrix}1&1\\1&1\end{pmatrix}
\\b22matrix ⇒ \begin{bmatrix}1&1\\1&1\end{bmatrix}
\\v22matrix ⇒ \begin{vmatrix}1&1\\1&1\end{vmatrix}
\\c3vector ⇒ \begin{pmatrix}1\\1\\1\end{pmatrix}
\\r3vector ⇒ \begin{pmatrix}1&1&1\end{pmatrix}
```

### 自定义快捷键
Ctrl+Shift+P搜索open snippet directory

已经copy文件markdown.hsnips