### 线性代数之矩阵求导

      线性代数L小组
      Group members omitted in this public archive  

### 一. 函数与标量、向量、矩阵

考虑一个函数

$$
\text{function}(\text{input})
$$

针对 $\text{function}$ 的类型、 $\text{input}$ 的类型，我们可以将这个函数 $\text{funcion}$ 分为不同的种类。

##### 1. $\text{function}$ 是一个标量

   我们称 $\text{function}$ 是一个实值标量函数。用细体小写字母 $f$ 表示。

###### 1.1) $\text{input}$ 是一个标量

   我们称 $\text{function}$ 的变元是标量。用细体小写字母 $x$ 表示。

      例1：

$$
f(x)=x+2
$$

###### 1.2) $\text{input}$ 是一个向量

我们称 $\text{function}$ 的变元是向量。用粗体小写字母 $\pmb{x}$ 表示。

      例2：

$$
设 \pmb{x}=[x_1,x_2,x_3]^T
$$

$$
f(\pmb{x})=a_1x_1^2+a_2x_2^2+a_3x_3^2+a_4x_1x_2
$$

###### 1.3) $\text{input}$ 是一个矩阵

我们称 $\text{function}$ 的变元是矩阵。用粗体大写字母 $\pmb{X}$ 表示。

      例3：

$$
设 \pmb{X}_{3\times 2}=(x_{ij})_{i=1,j=1}^{3,2}
$$

$$
f(\pmb{X})=a_1x_{11}^2+a_2x_{12}^2+a_3x_{21}^2+a_4x_{22}^2+a_5x_{31}^2+a_6x_{32}^2
$$

##### 2. $\text{function}$ 是一个向量

   我们称 $\text{function}$ 是一个实向量函数。用粗体小写字母 $\pmb{f}$ 表示。

   含义：$\pmb{f}$ 是由若干个 $f$ 组成的一个向量。

   同样地，变元分三种：标量、向量、矩阵。这里的符号仍与上面相同。

###### 2.1) 标量变元

      例4：

$$
\pmb{f}_{3\times1}(x) = 
\begin{bmatrix}
f_1(x) \\ 
f_2(x) \\ 
f_3(x)
\end{bmatrix} = 
\begin{bmatrix}
x + 1 \\ 
2x + 1 \\ 
3x^2 + 1
\end{bmatrix}
$$

###### 2.2) 向量变元

      例5：

$$
设\pmb{x} = [x_1, x_2, x_3]^T
$$

$$
\pmb{f}_{3\times1}(\pmb{x}) = 
\begin{bmatrix}
f_1(\pmb{x}) \\ 
f_2(\pmb{x}) \\ 
f_3(\pmb{x})
\end{bmatrix} = 
\begin{bmatrix}
x_{1} + x_{2} + x_{3} \\ 
x_{1}^2 + 2x_{2} + 2x_{3} \\ 
x_{1}x_{2} + x_{2} + x_{3}
\end{bmatrix}
$$

###### 2.3) 矩阵变元

      例6：

$$
设\pmb{X}_{3\times 2} = (x_{ij})_{i=1,j=1}^{3,2}
$$

$$
\pmb{f}_{3\times1}(\pmb{X}) = 
\begin{bmatrix}
f_1(\pmb{X}) \\ 
f_2(\pmb{X}) \\ 
f_3(\pmb{X})
\end{bmatrix} = 
\begin{bmatrix}
x_{11} + x_{12} + x_{21} + x_{22} + x_{31} + x_{32} \\ 
x_{11} + x_{12} + x_{21} + x_{22} + x_{31} + x_{32} + x_{11}x_{12} \\ 
2x_{11} + x_{12} + x_{21} + x_{22} + x_{31} + x_{32} + x_{11}x_{12}
\end{bmatrix}
$$

##### 3. $\text{function}$ 是一个矩阵

   我们称 $\text{function}$ 是一个实矩阵函数。用粗体大写字母 $\pmb{F}$ 表示。

   含义：$\pmb{F}$ 是由若干个 $f$ 组成的一个矩阵。

   同样地，变元分三种：标量、向量、矩阵。这里的符号仍与上面相同。

###### 3.1) 标量变元

      例7：

$$
\pmb{F}_{3\times2}(x) = 
\begin{bmatrix}
f_{11}(x) & f_{12}(x) \\ 
f_{21}(x) & f_{22}(x) \\ 
f_{31}(x) & f_{32}(x)
\end{bmatrix} = 
\begin{bmatrix}
x + 1 & 2x + 2 \\ 
x^2 + 1 & 2x^2 + 1 \\ 
x^3 + 1 & 2x^3 + 1
\end{bmatrix}
$$

###### 3.2) 向量变元

      例8：

$$
设\pmb{x} = [x_1, x_2, x_3]^T
$$

$$
\pmb{F}_{3\times2}(\pmb{x}) = 
\begin{bmatrix}
f_{11}(\pmb{x}) & f_{12}(\pmb{x}) \\ 
f_{21}(\pmb{x}) & f_{22}(\pmb{x}) \\ 
f_{31}(\pmb{x}) & f_{32}(\pmb{x})
\end{bmatrix} = 
\begin{bmatrix}
2x_{1} + x_{2} + x_{3} & 2x_{1} + 2x_{2} + x_{3} \\ 
2x_{1} + 2x_{2} + x_{3} & x_{1} + 2x_{2} + x_{3} \\ 
2x_{1} + x_{2} + 2x_{3} & x_{1} + 2x_{2} + 2x_{3}
\end{bmatrix}
$$

###### 3.3) 矩阵变元

      例9：

$$
设\pmb{X}_{3\times 2} = (x_{ij})_{i=1,j=1}^{3,2}
$$

$$
\begin{align*}
\pmb{F}_{3\times2}(\pmb{X}) &= 
\begin{bmatrix}
f_{11}(\pmb{X}) & f_{12}(\pmb{X}) \\ 
f_{21}(\pmb{X}) & f_{22}(\pmb{X}) \\ 
f_{31}(\pmb{X}) & f_{32}(\pmb{X})
\end{bmatrix} \\
&= 
\begin{bmatrix}
x_{11} + x_{12} + x_{21} + x_{22} + x_{31} + x_{32} & 2x_{11} + x_{12} + x_{21} + x_{22} + x_{31} + x_{32} \\ 
3x_{11} + x_{12} + x_{21} + x_{22} + x_{31} + x_{32} & 4x_{11} + x_{12} + x_{21} + x_{22} + x_{31} + x_{32} \\ 
5x_{11} + x_{12} + x_{21} + x_{22} + x_{31} + x_{32} & 6x_{11} + x_{12} + x_{21} + x_{22} + x_{31} + x_{32}
\end{bmatrix}
\end{align*}
$$

---

### 二. 矩阵求导

#### 2.1 矩阵求导的本质

我们在高等数学中学过，对于一个多元函数

      例10：

$$
f(x_1,x_2,x_3)=x_1^2+x_1x_2+x_2x_3
$$

我们可以将 $f$ 对 $x_1,x_2,x_3$ 的偏导分别求出来，即：

$$
\left\{
\begin{align*}
\frac{\partial f}{\partial x_1} & = 2x_1+x_2 \\
\frac{\partial f}{\partial x_2} & = x_1+x_3 \\
\frac{\partial f}{\partial x_3} & = x_2
\end{align*}
\right.
$$

矩阵求导也是一样的，本质就是 $\text{function}$ 中的每个 $f$ 分别对变元中的每个元素逐个求偏导，只不过写成了向量、矩阵形式而已。

对于 (e.g.10)，我们把得出的3个结果写成列向量形式：

$$
\frac{\partial f(\pmb{x})}{\partial \pmb{x}_{3\times1}} = 
\begin{bmatrix}
\frac{\partial f}{\partial x_1} \\ 
\frac{\partial f}{\partial x_2} \\ 
\frac{\partial f}{\partial x_3}
\end{bmatrix} = 
\begin{bmatrix}
2x_1 + x_2 \\ 
x_1 + x_3 \\ 
x_2
\end{bmatrix}
$$

一个矩阵求导以列向量形式展开的雏形就出现了。

当然我们也可以以行向量形式展开：

$$
\frac{\partial f(\pmb{x})}{\partial \pmb{x}_{3\times1}^T}= \left[ \frac{\partial f}{\partial x_1}, \frac{\partial f}{\partial x_2}, \frac{\partial f}{\partial x_3} \right] = \left[ 2x_1+x_2, x_1+x_3, x_2 \right]
$$

所以，如果 $\text{function}$ 中有 $m$ 个 $f$，变元中有 $n$ 个元素，那么，每个 $f$ 对变元中的每个元素逐个求偏导后，我们就会产生 $m \times n$ 个结果。

这就是矩阵求导的本质。

至于这 $m \times n$ 个结果的布局，是写成行向量，还是写成列向量，还是写成矩阵，就是我们接下来要讨论的事情。

#### 2.2 矩阵求导的布局

不严谨地说，从直观上看：

- **分子布局**，就是分子是列向量形式，分母是行向量形式，如 (2) 式。如果这里的 $\text{function}$ 是实向量函数 $\pmb{f}_{2\times 1}$ 的话，结果就是 $2 \times 3$ 的矩阵了：
  
  $$
  \frac{\partial \pmb{f}_{2\times1}(\pmb{x})}{\partial \pmb{x}^T_{3\times1}} = 
\begin{bmatrix}
\frac{\partial f_1}{\partial x_1} & \frac{\partial f_1}{\partial x_2} & \frac{\partial f_1}{\partial x_3} \\ 
\frac{\partial f_2}{\partial x_1} & \frac{\partial f_2}{\partial x_2} & \frac{\partial f_2}{\partial x_3}
\end{bmatrix}_{2\times 3}
  $$

- **分母布局**，就是分母是列向量形式，分子是行向量形式，如 (1) 式。如果这里的 $\text{function}$ 是实向量函数 $\pmb{f}_{2\times 1}$ 的话，结果就是 $3 \times 2$ 的矩阵了：

$$
\frac{\partial \pmb{f}^T_{2\times1}(\pmb{x})}{\partial \pmb{x}_{3\times1}} = 
\begin{bmatrix}
\frac{\partial f_1}{\partial x_1} & \frac{\partial f_2}{\partial x_1} \\ 
\frac{\partial f_1}{\partial x_2} & \frac{\partial f_2}{\partial x_2} \\ 
\frac{\partial f_1}{\partial x_3} & \frac{\partial f_2}{\partial x_3}
\end{bmatrix}_{3\times 2}
$$

---

### 三. 求导法则

#### 3.1 常数求导：

与一元函数常数求导相同：结果为零向量

$$
\frac{\partial c}{ \partial \pmb{x}}=\pmb{0}_{n \times 1}
$$

其中， $c$ 为常数。

证明：

$$
\begin{align}
\frac{\partial{c}}{\partial{\pmb{x}}} &= \begin{bmatrix} \frac{\partial{c}}{\partial{x_1}} \\ \frac{\partial{c}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{c}}{\partial{x_n}} \end{bmatrix} \\
&= \begin{bmatrix} 0 \\ 0 \\ \vdots \\ 0\end{bmatrix} \\
&=\pmb{0}_{n \times 1}
\end{align}
$$

证毕。

#### 3.2 线性法则

与一元函数求导线性法则相同：相加再求导等于求导再相加，常数提外面

$$
\frac{\partial{[c_1f(\pmb{x})+c_2g(\pmb{x})]}}{\partial{\pmb{x}}} = c_1\frac{\partial f(\pmb{x})}{\partial{\pmb{x}}} + c_2\frac{\partial g(\pmb{x})}{\partial{\pmb{x}}}
$$

其中， $c_1,c_2$ 为常数。

证明：

$$
\begin{align}
\frac{\partial{[c_1f(\pmb{x})+c_2g(\pmb{x})]}}{\partial{\pmb{x}}} &= \begin{bmatrix} \frac{\partial{(c_1f+c_2g)}}{\partial{x_1}} \\ \frac{\partial{(c_1f+c_2g)}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{(c_1f+c_2g)}}{\partial{x_n}} \end{bmatrix} \\
&= \begin{bmatrix} c_1\frac{\partial{f}}{\partial{x_1}}+c_2\frac{\partial{g}}{\partial{x_1}} \\ c_1\frac{\partial{f}}{\partial{x_2}}+c_2\frac{\partial{g}}{\partial{x_2}} \\ \vdots \\ c_1\frac{\partial{f}}{\partial{x_n}}+c_2\frac{\partial{g}}{\partial{x_n}} \end{bmatrix} \\
&=c_1\begin{bmatrix} \frac{\partial{f}}{\partial{x_1}} \\ \frac{\partial{f}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{f}}{\partial{x_n}} \end{bmatrix} + c_2\begin{bmatrix} \frac{\partial{g}}{\partial{x_1}} \\ \frac{\partial{g}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{g}}{\partial{x_n}} \end{bmatrix} \\
&=c_1\frac{\partial f(\pmb{x})}{\partial{\pmb{x}}} + c_2\frac{\partial g(\pmb{x})}{\partial{\pmb{x}}}
\end{align}
$$

证毕。

#### 3.3 乘积法则

与一元函数求导乘积法则相同：前导后不导 加 前不导后导

$$
\frac{\partial{[f(\pmb{x})g(\pmb{x})]}}{\partial{\pmb{x}}} = \frac{\partial f(\pmb{x})}{\partial{\pmb{x}}}g(\pmb{x}) +f(\pmb{x})\frac{\partial g(\pmb{x})}{\partial{\pmb{x}}}
$$

证明：

$$
\begin{align}
\frac{\partial{[f(\pmb{x})g(\pmb{x})]}}{\partial{\pmb{x}}} &= \begin{bmatrix} \frac{\partial{(fg)}}{\partial{x_1}} \\ \frac{\partial{(fg)}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{(fg)}}{\partial{x_n}} \end{bmatrix} \\
&= \begin{bmatrix} \frac{\partial{f}}{\partial{x_1}}g+f\frac{\partial{g}}{\partial{x_1}} \\ \frac{\partial{f}}{\partial{x_2}}g+f\frac{\partial{g}}{\partial{x_2}}\\ \vdots \\ \frac{\partial{f}}{\partial{x_n}}g+f\frac{\partial{g}}{\partial{x_n}} \end{bmatrix} \\
&=\begin{bmatrix} \frac{\partial{f}}{\partial{x_1}} \\ \frac{\partial{f}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{f}}{\partial{x_n}} \end{bmatrix}g + f\begin{bmatrix} \frac{\partial{g}}{\partial{x_1}} \\ \frac{\partial{g}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{g}}{\partial{x_n}} \end{bmatrix} \\
&=\frac{\partial f(\pmb{x})}{\partial{\pmb{x}}}g(\pmb{x}) +f(\pmb{x})\frac{\partial g(\pmb{x})}{\partial{\pmb{x}}}
\end{align}
$$

证毕。

#### 3.4 商法则

与一元函数求导商法则相同：（上导下不导 减 上不导下导）除以（下的平方）：

$$
\frac{\partial{\left[\frac{f(\pmb{x})}{g(\pmb{x})}\right]}}{\partial{\pmb{x}}} = \frac{1}{g^2(\pmb{x})}\left[ \frac{\partial f(\pmb{x})}{\partial{\pmb{x}}}g(\pmb{x}) -f(\pmb{x})\frac{\partial g(\pmb{x})}{\partial{\pmb{x}}} \right]
$$

其中， $g(\pmb{x})\neq0$ 。

证明：

$$
\begin{align}
\frac{\partial{\left[\frac{f(\pmb{x})}{g(\pmb{x})}\right]}}{\partial{\pmb{x}}} &= \begin{bmatrix} \frac{\partial{(\frac{f}{g})}}{\partial{x_1}} \\ \frac{\partial{(\frac{f}{g})}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{(\frac{f}{g})}}{\partial{x_n}} \end{bmatrix} \\
&= \begin{bmatrix} \frac{1}{g^2}\left( \frac{\partial f}{\partial{x_1}}g -f\frac{\partial g}{\partial{x_1}} \right) \\ \frac{1}{g^2}\left( \frac{\partial f}{\partial{x_2}}g -f\frac{\partial g}{\partial{x_2}} \right)\\ \vdots \\ \frac{1}{g^2}\left( \frac{\partial f}{\partial{x_n}}g -f\frac{\partial g}{\partial{x_n}} \right) \end{bmatrix} \\
&= \frac{1}{g^2}\left( \begin{bmatrix} \frac{\partial{f}}{\partial{x_1}} \\ \frac{\partial{f}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{f}}{\partial{x_n}} \end{bmatrix}g - f\begin{bmatrix} \frac{\partial{g}}{\partial{x_1}} \\ \frac{\partial{g}}{\partial{x_2}} \\ \vdots \\ \frac{\partial{g}}{\partial{x_n}} \end{bmatrix} \right) \\
&=\frac{1}{g^2(\pmb{x})}\left[ \frac{\partial f(\pmb{x})}{\partial{\pmb{x}}}g(\pmb{x}) -f(\pmb{x})\frac{\partial g(\pmb{x})}{\partial{\pmb{x}}} \right]
\end{align}
$$

#### 3.5 链式求导法则

##### 1. 标量对向量的链式求导法则

设 \( y \) 是标量，\( u = (u_1, u_2, \cdots, u_m)^T \) 是中间向量，\( x = (x_1, x_2, \cdots, x_n)^T \) 是自变量向量，且 \( y = f(u) \)，\( u = g(x) \)。

那么 \( \frac{\partial y}{\partial x} \) 是一个 \( n \) 维向量，其第 \( i \) 个元素为：
\[
\frac{\partial y}{\partial x_i} = \sum_{j = 1}^{m} \frac{\partial y}{\partial u_j} \frac{\partial u_j}{\partial x_i}
\]

**示例：**

设 \( y = u_1^2 + u_2 \)，\( u_1 = x_1 + x_2 \)，\( u_2 = 2x_1 \)。

首先，计算偏导数：
\[
\frac{\partial y}{\partial u_1} = 2u_1, \quad \frac{\partial y}{\partial u_2} = 1
\]
\[
\frac{\partial u_1}{\partial x_1} = 1, \quad \frac{\partial u_1}{\partial x_2} = 1, \quad \frac{\partial u_2}{\partial x_1} = 2, \quad \frac{\partial u_2}{\partial x_2} = 0
\]

根据链式法则：
\[
\frac{\partial y}{\partial x_1} = \frac{\partial y}{\partial u_1} \frac{\partial u_1}{\partial x_1} + \frac{\partial y}{\partial u_2} \frac{\partial u_2}{\partial x_1} = 2u_1 \times 1 + 1 \times 2 = 2(x_1 + x_2) + 2 = 2x_1 + 2x_2 + 2
\]
\[
\frac{\partial y}{\partial x_2} = \frac{\partial y}{\partial u_1} \frac{\partial u_1}{\partial x_2} + \frac{\partial y}{\partial u_2} \frac{\partial u_2}{\partial x_2} = 2u_1 \times 1 + 1 \times 0 = 2(x_1 + x_2)
\]

##### 2. 向量对向量的链式求导法则

设 \( y = (y_1, y_2, \cdots, y_p)^T \) 是向量，\( u = (u_1, u_2, \cdots, u_m)^T \) 是中间向量，\( x = (x_1, x_2, \cdots, x_n)^T \) 是自变量向量，且 \( y = f(u) \)，\( u = g(x) \)。

那么 \( \frac{\partial y}{\partial x} \) 是一个 \( p \times n \) 矩阵，其 \((i, j)\) 元素为：
\[
\frac{\partial y_i}{\partial x_j} = \sum_{k = 1}^{m} \frac{\partial y_i}{\partial u_k} \frac{\partial u_k}{\partial x_j}
\]

**示例：**

设：
\[
y = \begin{bmatrix} u_1^2 \\ u_1 + u_2 \end{bmatrix}, \quad u = \begin{bmatrix} x_1 + x_2 \\ 2x_1 \end{bmatrix}
\]

首先，计算偏导数：
\[
\frac{\partial y_1}{\partial u_1} = 2u_1, \quad \frac{\partial y_1}{\partial u_2} = 0
\]
\[
\frac{\partial y_2}{\partial u_1} = 1, \quad \frac{\partial y_2}{\partial u_2} = 1
\]
\[
\frac{\partial u_1}{\partial x_1} = 1, \quad \frac{\partial u_1}{\partial x_2} = 1, \quad \frac{\partial u_2}{\partial x_1} = 2, \quad \frac{\partial u_2}{\partial x_2} = 0
\]

根据链式法则：
\[
\frac{\partial y}{\partial x} = \begin{bmatrix}
\frac{\partial y_1}{\partial u_1} \frac{\partial u_1}{\partial x_1} + \frac{\partial y_1}{\partial u_2} \frac{\partial u_2}{\partial x_1} & \frac{\partial y_1}{\partial u_1} \frac{\partial u_1}{\partial x_2} + \frac{\partial y_1}{\partial u_2} \frac{\partial u_2}{\partial x_2} \\
\frac{\partial y_2}{\partial u_1} \frac{\partial u_1}{\partial x_1} + \frac{\partial y_2}{\partial u_2} \frac{\partial u_2}{\partial x_1} & \frac{\partial y_2}{\partial u_1} \frac{\partial u_1}{\partial x_2} + \frac{\partial y_2}{\partial u_2} \frac{\partial u_2}{\partial x_2}
\end{bmatrix}
\]

代入计算可得：
\[
\frac{\partial y}{\partial x} = \begin{bmatrix}
2u_1 \times 1 + 0 \times 2 & 2u_1 \times 1 + 0 \times 0 \\
1 \times 1 + 1 \times 2 & 1 \times 1 + 1 \times 0
\end{bmatrix} = \begin{bmatrix}
2(x_1 + x_2) & 2(x_1 + x_2) \\
3 & 1
\end{bmatrix}
\]

---
###  四.矩阵求导法则的应用场景

- **神经网络中的应用**

- **最小二乘法中的应用**
---
