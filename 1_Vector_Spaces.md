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

> Let: $\alpha = a + bi$, $\beta = c + di$, $\gamma=e+fi$ where $a,b,c,d,e,f\in\mathbb{R}$
>
> Then:
> $(\alpha + \beta) +\gamma = (a + c + e) + (b + d + f)i = \alpha + (\beta + \gamma)$
>
> $(\alpha\beta)\gamma = (ace-adf-bcf-bde)+(acf+ade+bce-bdf)i = \alpha(\beta\gamma)$
>
> $\blacksquare$

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
> $\alpha+\beta = (a-a) + (b-b)i = 0$
>
> $\blacksquare$

乘法逆：

> For any $\alpha = a+bi \in \mathbb{C}$ such that $\alpha\ne 0$, we can construct $\beta = \frac{a-bi}{a^2+b^2}$, then:
>
> $\alpha\beta = (a+bi)\frac{a-bi}{a^2+b^2}=\frac{a^2+b^2}{a^2+b^2}=1$
>
> $\blacksquare$

分配律：

> Let: $\alpha = a + bi$, $\beta = c + di$, $\gamma=e+fi$, where $a,b,c,d,e,f\in\mathbb{R}$
>
> $\gamma(\alpha+\beta)=(ae+ce-bf-df)+(af+be+cf+de)i=\gamma\alpha+\gamma\beta$
>
> $\blacksquare$

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
> $x + y = (x_1+y_1,...,x_n+y_n)$
> $=(y_1+x_1,...,y_n+x_n)$
> $=y+x$
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

### $\mathbb{F}^S$ 

$\mathbb{F}^S$ 是定义域为集合 $S$，值域为数域 $\mathbb{F}$ 的函数的集合。

$\mathbb{F}^S$ 是一个向量空间。

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

## 子空间

### 子空间的定义与条件

如果向量空间 $V$ 的子集 $U$ 也是一个向量空间，那么称 $U$ 是 $V$ 的**子空间**。

子集为子空间的条件：

* 存在加法单位元
* 在加法下封闭
* 在数乘下封闭

证明：

> Suppose $U$ is a subset of vector space $V$ and satisfy the conditions above.
>
> The additive identity exist.
>
> Since $U$ is closed under addition and scalar multiplication, these 2 operation over this set exists.
>
> If $u\in U$, then $-u$ must also in $U$ because $U$ is closed under scalar multiplication, so the additive inverse exists.
>
> The reset of definition, associativity, commutativity, multiplicative identity, distributive properties, they hold on the larger space $V$, so they also hold in $U$.
>
> $\blacksquare$

一个例子：所有定义在 $(0,3)$ 上，且满足 $f'(2) = b$ 的可微实值函数集合是 $\mathbb{R}^{(0,3)}$ 的子空间，当且仅当 $b = 0$。因为零函数需要在子空间中，且需要满足 $f'(2) = b$ 的条件。

### 子空间的和

假如 $U_1,...,U_m$ 是 $V$ 的子空间，那么 $U_1,...,U_m$ 的**和**记作 $U_1+...+U_m$，定义为所有可能的来自这些子空间的元素的和的集合，即：

$U_1+...+U_m=\{u_1+...+u_m:u_1\in U_1,...,u_m\in U_m\}$

一个例子是，平面直角坐标系中，横轴和竖轴是平面的两个子空间，它们的和为整个平面，而它们的并为两个数轴组成的十字区域。

子空间的和是包含这些子空间的最小子空间。

证明：

> Easy to see that $0\in U_1+...+U_m$ and $U_1+...+U_m$ is closed under addition and scalar multiplication, thus the sum of subspaces is a subspace.
>
> Clearly $U_1,...,U_m$ are all contained in $U_1+...+U_m$. Conversely, every subspace of $V$ containing $U_1,...,U_m$ contains $U1+...+U_m$. 
>
> Thus $U_1+...+U_m$ is the smallest subspace of $V$ containing $U_1,...,U_m$.

### 直和

假设 $U_1,...,U_m$ 是 $V$ 的子空间。如果 $U_1+...+U_m$ 中的元素只能以一种方式表示为 $u_1+...+u_m$（$u_i\in U_i$），那么称 $U_1+...+U_m$ 为**直和**。记作 $U_1\oplus ...\oplus U_m$。

直和的条件（当且仅当）：只有一种方式将 $0$ 表示为 $u_1+...+u_m$（$u_i\in U_i$），那就是取每个 $u_i = 0$。

证明：(当方向，仅当方向显然)

> When there is only one way to represent $0$ as $u_1+...+u_m$ （$u_i\in U_i$）:
>
> Suppose there is 2 ways to represent an arbitary element $v$ in the sum as $u_i+...+u_m$, then we have:
>
> $v = u_1+...+u_m$
>
> $v = v_1+...+v_m$
>
> substract these 2 equation, we get:
>
> $0 = (u_1-v_1) + ... + (u_m-v_m)$
>
> Since $0$ can be only write in one way as $0 = 0 +... + 0$, we have:
>
> $u_1 = v_1, ..., u_m = v_m$
>
> So an arbitary element can be only write in one way.
>
> Thus this is a direct sum.
>
> $\blacksquare$

直和的条件（当且仅当）：$U\cap W = \{0\}$（$U$ 与 $W$ 为子空间 ）

证明：

> only if direction: If $v\in U\cap W$, $0 = v + (-v)$ where $v \in U$ and $-v \in W$, because the representation is unique of zero, we have: $v=0$
>
> if direction:
>
> Suppose $U\cap W = \{0\}$ and $0 = u + w, u\in U, w\in W$
>
> then we have: $u= -w \in W$, thus $u\in U\cap W$, thus $u = 0$, thus $w = 0$, thus $0=0+0$ is the only representation.
>
> $\blacksquare$

