`郑旭 2018年6月30日`
# Abstract
嗯……想起相对论，就想起了小时候的我，还傻傻分不清楚爱迪生和爱因斯坦，就像分不清楚刘翔和姚明。
# The Special Relativity
### the Speed of Light
$$
  \delta_{mn}
$$

# What is Time?Space-Time?
## Lorentz Transformation
http://authors.aps.org/revtex4/
# Tensors
Why we use coordinates to describe the world，and what is tensor？
## What are Scalars and Vectors?
有一种量不随任何坐标变换而改变，我们称为标量(scalar——0阶张量)，还有一种量随着坐标变换和我们的空间坐标矢量一起变的，我们称为矢量(vector——1阶张量)。类似的我们可以给出2阶张量，这些量作为物理量，就会自然使我们的物理定律不会因为坐标系的建立而不同，这是科学的前提。举例说明Rank 1 tensor：
$$
\boldsymbol{r}=x_{1}\boldsymbol{e}_{1}+ x_{2}\boldsymbol{e}_{2}+ x_{3}\boldsymbol{e}_{3}
$$
$$
\boldsymbol{r}=x_{1}\boldsymbol{e'}_{1}+ x_{2}\boldsymbol{e'}_{2}+ x_{3}\boldsymbol{e'}_{3}
$$
式(\ref{r})中，我们在原坐标系中有一个空间坐标向量，再通过坐标变换得到式(\ref{r'})，变换是通过$a_{ij}$这个正交矩阵变换实现。
$$
  x'_{i}=\sum_{j}a_{ij}x_{j}
$$
$$
  a_{ij}\equiv\frac{\partial x'_{i}}{\partial x_{j}}= \boldsymbol{e'}_{i}\cdot\boldsymbol{e}_{j}
$$

我们把上述这样形式的物理量叫做向量，或者1阶张量。这看起来好像跟废话一样，但是当你不把向量当作理所应当时，或者想想我们刚开始接触向量的困惑，而且，只有这样，我们才能更深刻的理解张量及所有物理量。
如，我们常说的保守力场，为什么是向量场，为什么势场是标量场？这其实背后的意义就在这里。
$$
\boldsymbol F \equiv\frac{\partial V}{\partial\boldsymbol{r}}
$$很容易就能证明，F是一个向量，那我们也知道了力做功为什么是内积，因为这两个向量运算只有内积才能在坐标变换下不变！
我们比着葫芦画瓢，就能写出2阶张量的定义如下：
$$
 T'_{ij}=\sum_{k}\sum_{l}a_{ik}a_{jl}T_{kl}
$$
## Contravarient and Covarient Tensor
## The nature of Our Physics
$$
\sigma=\left(
  \begin{array}{ccc}
  \sigma_{x} & \tau_{xy} & \tau_{xz}\\
  \tau_{yx} & \sigma_{y} & \tau_{yz}\\
  \tau_{zx} & \tau_{yz} & \sigma_{z} 
\end{array}
\right)\equiv\frac{d\boldsymbol{F}}{d\boldsymbol{A}}
$$
但只有二阶张量可以写成矩阵，三阶成了'立方体'了。
## Electromagnetic Tensor
下面讲：外积实际上是一个反对称的二阶张量！
首先，我们需要一找到Isotropic Tensor，再说它的意义——$\delta_{ij}$和$\epsilon_{lmn}$
有如下定义：
$$
  T_{ij}\equiv A_{i}B_{j}-A_{j}B_{i}
$$
我们的二阶张量在三维空间里是一个3 $\times$ 3的矩阵，是因为w我们认为，空间随我们坐标系变化，但时间不会，但如果我们相信光速不变原理，我们就知道时间也是相对的，随坐标变换而变，所以我们都把时间也纳为我们的时空架构里，这种架构就是tensor！在狭义相对论里，这个变换就是洛伦兹变换(其实就是相对运动速度决定的不同惯性坐标系)，那我们在这个变换里，重新调整我们的物理量定义，其中电磁场就是这个四维时空中的anti-symmetry rank 2 tensor！所以我们自然也就理解了，电动生磁，磁动生电。

## Metric Tensor and Coordinates
相对论$g_{\mu\nu}$
# The Curved Space-Time
## Euclidian Geometry or Raman
正如第一章所讲的那样，我们其实没有惯性坐标系，也不存在一个flat space，因为我们生活的时空处处都有万有引力。但是这引起的时空弯曲程度很小，我们暂且忽略。但什么叫小，什么时候忽略，这都是我们要考虑的问题。