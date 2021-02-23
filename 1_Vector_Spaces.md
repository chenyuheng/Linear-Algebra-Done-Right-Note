## $\R^n$ 与 $\C^n$

### 复数

**复数**的定义：

* 有序实数对，写作 $a+bi$
* 复数集合记作 $\C$
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

> For any $\alpha = a+bi \in \C$, we can construct $\beta = -a - bi$, then:
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

$\mathbb{F}$：域，在本书中表示 $\C$ 或 $\R$。

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
>
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

