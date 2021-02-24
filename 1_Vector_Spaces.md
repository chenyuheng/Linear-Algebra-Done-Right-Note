# Chapter 1: Vector Spaces

## $\mathbb{R}^n$ 与 $\mathbb{C}^n$

### 复数

**复数**的定义：

* 有序实数对，写作 $a+bi$
* 复数集合记作 $\mathbb{C}$
* 复数加法与乘法按多项式定义

复数的性质：

* 交换律（加法、乘法）
* 结合律（加法、乘法）
* 单位元（加法、乘法）
* 加法逆
* 乘法逆
* 分配律

证明：

交换律：

> Let: $\alpha = a + bi$, $\beta = c + di$
>
> Then:
> $\alpha + \beta = (a + c) + (b + d)i = \beta + \alpha$
>
> $\alpha\beta = (ac-bd) + (ad+bc)i = \beta\alpha$
>
> $\blacksquare$

结合律：

> 

单位元：

> Let $\gamma = a+bi$
>
> Then: 
>
> $\gamma + 0 = a + bi + 0 = (a + 0) + bi = a + bi = \gamma$
>
> $\gamma1=(a+bi)*1=a+bi=\gamma$
>
> $\blacksquare$

加法逆：

> For any $\alpha = a+bi \in \mathbb{C}$, we can construct $\beta = -a - bi$, then:
>
> $\alpha+\beta = (a-a) + (b-b)i$ = 0
>
> $\blacksquare$

乘法逆：

> 

分配律：

> 

$-\alpha$、减法、$1/\alpha$、除法：

* 记加法逆与乘法逆为$-\alpha$、$1/\alpha$
* 记减法为加上加法逆，除法为乘上乘法逆

$\mathbb{F}$：域，在本书中表示 $\mathbb{C}$ 或 $\mathbb{R}$。

### 组（Lists）

**组**的定义：

* 长度为 $n$ 的组有 $n$ 个有顺序的元素
* 一般用括号与逗号的记法
* 两个组相等，当且仅当两个组长度相等、元素相同、顺序一样

长度为 2 的组为**对**，长度为 3 的组为**三元组**，长度为 $n$ 的组为“**n 元组**”。

组的长度有限

### $\mathbb{F}^n$

$\mathbb{F}^n$ 定义：$\mathbb{F}$ 中长度为 $n$ 的组的集合，即 $\mathbb{F}^n=\{(x_1,...,x_n):x_j\in\mathbb{F}, j = 1,...,n\}.$

$\mathbb{F}^n$ 加法：对应坐标相加：$(x_1,...,x_n)+(y1,...,yn)=(x_1+y_1,...,x_n+y_n).$

$\mathbb{F}^n$ 加法交换律证明：

> Let $x = (x_1,...,x_n)$, $y=(y_1,...,y_n)$
>
> Then:
> $$
> \begin{aligned}x + y &= (x_1+y_1,...,x_n+y_n)\\
>&=(y_1+x_1,...,y_n+x_n)\\
>  &=y+x
>\end{aligned}
> $$
> $\blacksquare$

$\mathbb{F}^n$ 里面的元素可以称为**向量**。

$0$ 向量的定义： $0=(0,...,0)$

加法逆元的定义：$x+(-x)=0$，即：$x = (x_1,...,x_n)$，则$-x=(-x_1,...,-x_n)$

标量乘法的定义：$\gamma(x_1,...,x_n) = (\gamma x_1,...,\gamma x_n)$

## Definition of Vector Spaces

### 向量空间

首先定义集合内的加法与数乘：

* 加法：从集合中的两个元素到集合中的一个元素的函数
* 数乘：从集合中的一个元素与 $\mathbb{F}$ 中的一个数到集合中的一个元素的函数

**向量空间**的定义：

* 满足集合加法与集合数乘的集合
* 交换律（加法）
* 结合律（加法与数乘）
* 加法单位元
* 加法逆
* 数乘单位元
* 分配律

向量空间内的元素可称为向量或者点。

在 $\mathbb{R}$ 上的向量空间为实向量空间，在 $\mathbb{C}$ 上的向量空间为复向量空间。

### $\mathbb{F}^\mathbb{S}$ 

$\mathbb{F}^\mathbb{S}$ 是定义域为集合 $\mathbb{S}$，值域为 $\mathbb{F}$ 的函数的集合。

$\mathbb{F}^\mathbb{S}$ 是一个向量空间。

### 向量空间的基本性质

* 唯一加法单位元
* 唯一加法逆
* 0 数乘任何向量得向量 0
* 任何数数乘向量 0 得向量 0
* -1 数乘向量得到该向量的加法逆

证明：

唯一加法单位元：

> Suppose $0$ and $0'$ are both the additive identities for a vector space $V$.
>
> Then: $0' = 0' + 0 = 0 + 0' = 0$
>
> So the additive identity is unique for a vector space.
>
> $\blacksquare$

唯一加法逆：

> Suppose $V$ is a vector space, $v\in V$, $w$ and $w'$ are both additive inverse of $v$.
>
> Then: $w' = w' + 0 = w' + (v + w) = (w' + v) + w = = 0 + w = w$
>
> So the additive inverse is unique in a vector space.
>
> $\blacksquare$

0 数乘任何向量得向量 0：

> For $v\in V$, we have:
>
> $0v=(0+0)v=0v+0v$
>
> add the additive inverse of $0v$ to both side of the equation, we get:
>
> $0 = 0v$
>
> $\blacksquare$

任何数数乘向量 0 得向量 0:

> For $a\in F$, we have:
>
> $a0 = a(0+0) = a0+a0$
>
> add the additive inverse of $a0$ to both side of the equation, we get:
>
> $0 = a0$
>
> $\blacksquare$

-1 数乘向量得到该向量的加法逆:

> For $v\in V$, we have:
>
> $v + (-1)v =1v + (-1)v = (1+(-1))v=0v=0$
>
> So $(-1)v$ is the additive inverse of $v$.
>
> So $(-1)v = -v$
>
> $\blacksquare$