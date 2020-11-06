# Implementation-of-Pearson-Correlation
皮尔逊相关系数算法实现

# 协方差公式

这里的$E$表示的是期望，$E$在这里可以看成求和。


$$
\operatorname{Cov}(X, Y)=E\left[\left(X-\mu_{x}\right)\left(Y-\mu_{y}\right)\right]
$$

# 皮尔逊公式

$$
\operatorname{pearson}(u, v)=\frac{x和y的协方差}{(x的标准差 * y的标准差)}
$$

具体可以表示成下面这种形式：

$$ 
\operatorname{pearson}(u, v)=\frac{\sum_{k \in I_{v} \cap I_{v}}\left(r_{u k}-\mu_{u}\right)\left(r_{v k}-\mu_{v}\right)}{\sqrt{\sum_{k \in I_{u} \cap I_{v}}\left(r_{u k}-\mu_{u}\right)^{2}} \cdot \sqrt{\sum_{k \in I_{u} \cap I_{v}}\left(r_{u k}-\mu_{u}\right)^{2}}} 
$$


也可以表示成为下面的形式：

$$
P_{x, y}=\frac{\operatorname{cov}(x, y)}{\sigma_{x} \sigma_{y}}=\frac{E\left[\left(x-x_{i}\right)\left(y-y_{i}\right)\right]}{\sigma_{x} \sigma_{y}}
$$

这里的$\sigma_{x}$和$\sigma_{y}$分别表示$x$和$y$的标准差，但是比较奇怪的是网上查询出来的标准差应该是下面的形式，需要除于总数，而这上面并没有。

$$
\sigma=\sqrt{\frac{\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}}{n}}
$$

所以综上所述，这里的$\sigma_{x}$其实是下面的公式：
$$
\sigma=\sqrt{\sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}}
$$
