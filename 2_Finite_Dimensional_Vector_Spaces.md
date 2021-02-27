# Finite-Dimensional Vector Spaces

## Section 2.A. Span and Linear Independence

向量的组的记号，一般不在最外面加括号，比如：$(4, 1, 6), (9, 5, 7)$

### Linear Combinations and Span

向量组 $v_1, ...,v_m$ 的一个**线性组合**是形式为 $a_1v_1+...+a_mv_m$ （$a_1,...,a_m\in \mathbb{F}$）的一个向量。

$V$ 中一个向量组 $v_1,...,v_m$ 的**张成空间**（span，或者 linear span）是该向量组所有线性组合的集合，记为 $span(v_1,...,v_m)$。

​	规定空组的张成空间为 $\{0\}$

张成空间是包含这组向量的最小子空间。

证明：

> Suppose $v_1,...,v_m$ is a vector list in $V$.
>
> First to prove: $span(v_1,...,v_m)$ is a subspace.
>
> $0 = 0*v_1+...+0*v_m\in span(v_1,...,v_m)$
>
> $(a_1v_1+...+a_mv_m) + (c_1v_1+...+c_mv_m) = (a_1+c_1)v_1+...+(a_m+c_m)v_m$, so $span(v_1,...,v_m)$ is closed under addition.
>
> $\lambda(a_1v_1+...+a_mv_m) = \lambda a_1v_1 + ... +\lambda a_mv_m$, so $span(v_1,...,v_m)$ is closed under scalar multiplication.
>
> Thus $span(v_!,...,v_m)$ is a subspace of $V$.
>
> Then to prove that is smallest.
>
> As each $v_j$ is a linear combination of $v_1,...,v_m$, we have $v_j\in span(v_1,...,v_m)$.
>
> As subspaces are closed under addition and scalar multiplication, so each subspace containing all $v_1,...,v_m$ also contains $span(v_1,...,v_m)$.
>
> Thus $span(v_!,...,v_m)$ is the smallest containing subspace.
>
> $\blacksquare$

如果 $span(v_1,...,v_m)$ 等价于 $V$，那么我们说 $v_1,...v_m$ **张成**（spans）$V$。 

如果一个向量空间可以由该空间内的某个向量组张成，那么该向量空间是**有限维的**。（根据定义，组的长度是有限的）

形如 $p(z)=a_0+a_1z+a_2z^2+...+a_mz^m$ 的函数称为**多项式**。

所有系数都属于 $F$ 的所有多项式的集合记为 $\mathcal{P}(F)$。

对于多项式 $p\in\mathcal{P}(F)$，如果存在标量 $a_1,...,a_m\in F$ （$a_m\ne 0$） 使得对于任意的 $z\in F$ 都有：

$p(z)=a_0+a_1z+...+a_mz^m$

那么我们说 $p$ 的**次数**为 $m$，记作 $deg\ p = m$ 

对于非负整数 $m$，所有系数在 $F$ 中且次数不超过 $m$ 的多项式的集合记作 $\mathcal{P}_m(F)$ 。

* 对于非负整数 $m$，$\mathcal{P}_m(F)$ 是有限维向量空间。

如果一个向量空间不是有限维的，则称为**无限维的**。

证明：$\mathcal{P}(F)$ 是无限维向量空间。

> Consider any vector list in $\mathcal{P}(F)$, suppose it has a maximum degree of $m$, so the span of this vector list also have a maximum degree of $m$, thus $p(z)=z^{m+1}$ is not in the span, so $\mathcal{P}(F)$ cannot been spanned from a vector list in it, so it is not finite-dimensional, so it is infinite-dimensional.
>
> $\blacksquare$

### Linear Independence

对于 $V$ 中的一个向量组 $v_1,...,v_m$，如果使 $a_1v_1+...+a_mv_m$ 为 $0$ 的唯一方式是 $a_1=...=a_m=0$，那么称该向量组**线性无关**。

​	规定空组线性无关。

$V$ 中的一个向量组如果不是线性无关的，那么该向量组是**线性相关**的。

**线性相关性引理**（2.21）：如果从 $v_1,...,v_m$ 是一个线性相关的向量组，那么存在 $j\in\{1,...,m\}$，使得：

* $v_j\in span(v_1,...,v_{j-1})$
* 若从向量组中去除 $v_j$，那么剩余向量组的张成空间等于 $span(v_1,...,v_m)$

证明：

> Since $v_1,...,v_m$ is linear dependent, there exist a list $(a_1,...,a_m)$, which is not equal to (0,...,0), such that:
>
> $a_1v_1+...+a_mv_m = 0$
>
> Let $j$ be the largest number in $\{1,...,m\}$ such that $a_j\ne0$.
>
> Then we can write: $a_1v_1  + ... + a_{j-1}v_{j-1} = -a_jv_j$, then, $v_j = -\frac{a_1}{a_j}v_1-...-\frac{a_{j-1}}{a_j}v_{j-1}$. (as equation 2.22)
>
> Thus $v_j\in span(v_1,...,v_{j-1})$
>
> For any $u\in span(v_1,...,v_m)$, we can write as $u=c_1v_1+...+c_mv_m$.
>
> If we remove $v_j$ from the vector list, we can still rewrite $u$ using the equation 2.22 without involving $v_j$. So $u$ is still in $span(v_1,...,v_m)$.
>
> $\blacksquare$

（此证明没有考虑 $j$ 取 1 时的特例）

（2.23）在有限维向量空间中，线性无关组的长度小于等于向量空间的张成组的长度。

证明：

> Suppose $u_1,...,u_n$ is a linear independent list in $V$, and  $w_1,...,w_m$ spans $V$. We need to prove $n\le m$.
>
> Let list $B$ be the list $w_1,...,w_m$.
>
> Step 1:
>
> ​	Add $u_1$ in the beginning of $B$, we get $B=u_1,w_1,...,w_m$, which is linearly independent as $u_1$ is a linear combination of the rest vectors.
>
> ​	According to 2.21, we can find a vector $w_i$ in $B$, with removing that vector, $span(B)$ remains the same, equals to $V$.
>
> Step j:
>
> ​	As the $B$ list produced in the step $j-1$ spans $V$, we add $v_j$ in the beginning of $B$ and get $v_j, v_{j-1},...,v_1,...$, which is a linearly dependent list.
>
> ​	According to 2.21, we can find a vector in $B$, with removing that vector, $span(B)$ remains the same, equals to $V$. As $v_j, v_{j-1}, ...,v_1$ is a linearly independent list, the removing vector in $B$ must be a vector o $w$.
>
> As 2.21 imply, at each step j, we can successfully add a $v_j$ and remove a $w$. At last, we have $B$ with at most $m$ $v$s in it. So $n\le m$.
>
> $\blacksquare$

 （2.26）所有有限维向量空间的子空间也是有限维的。

证明：

> Suppose $U$ is a subspace of $V$.
>
> Step 1:
>
> ​	If $U=\{0\}$, it's finite-dimensional, we are done. If not, we choose $v_1\in U$ and form a linear independent list $v_1$.
>
> Step j:
>
> ​	If $U=span(v_1,...,v_{j-1})$, it's finite-dimensional, we are done. If not, we choose $v_j\in U$ but $v_j\notin span(v_1,...,v_{j-1})$, add to the list.
>
> As this steps not done, we constructed a list of vectors such that, no vector is in the span of the previous vectors. (2.21) According to 2.23, the length of the current constructed list of vectors is less than or equal to the length of the spanning vector list of $V$, so these steps can terminate at last.
>
> $\blacksquare$

