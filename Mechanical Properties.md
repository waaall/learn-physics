# Mechanical Properties 

`郑旭 2018年6月15日`

* 我们对待任何知识都应该有追根溯源的兴趣和能力，比如当我问自己这样一个宽泛的问题时———什么是力学性能？我会试着把问题具体化：我手里拿着一只笔，对它施力，它会有什么规律性的反应呢？这种规律性的适用条件是什么呢？怎么定量的描述这种规律性？

* 我们如果Google力学性能，会得到刚度，强度，塑形，弹性等这类专有名词。液体的力学和固体力学并不是有太大差距，我们不应该说这类的话：我学过弹性力学，但我没学好流体力学。那只能得出结论，要么是不懂F=ma，要么不懂

## Tensor——Nature of Stress

我们在说弹性假设之前，需要知道，应力或者说压强是什么？在理论力学中，我们把质点的牛顿力学应用到刚体中，告诉我们，物体实际上是三维的，我们由此接触到力矩，因为一个质点'变'成了刚体之后，不仅会走，还会原地打转了。$T=\overrightarrow{F}\times\overrightarrow{r}$向量的外积到底是什么，甚至我们会问向量是什么，为什么我们说一个物理量是向量，为什么有的是标量，而为什么有的物理量是用外积定义(像力矩T，角动量L，磁场强度B)，有的用内积定义(如功W等)，这背后是否存在着一个相同的数学架构？答案当然是，是的，叫张量。
	
现在我们只谈笛卡尔坐标系下的空间结构，也就是三维正交空间，这是惯性坐标系下的假定，实际上，物质的质量会引起时空的弯曲(广义相对论)，那时我们必须用黎曼几何来处理弯曲时空问题。

### 1.Scalar and Vector

我们在笛卡尔坐标系里，有一种量不随任何坐标变换而改变，我们称为标量(scalar——0阶张量)，还有一种量随着坐标变换和我们的空间坐标矢量一起变的，我们称为矢量(vector——1阶张量)。类似的我们可以给出2阶张量，这些量作为物理量，就会自然使我们的物理定律不会因为坐标系的建立而不同，这是科学的前提。举例说明Rank 1 tensor：
\begin{equation}\label{r}
	\boldsymbol{r}=x_{1}\boldsymbol{e}_{1}+ x_{2}\boldsymbol{e}_{2}+ x_{3}\boldsymbol{e}_{3}
\end{equation}
\begin{equation}\label{r'}
	\boldsymbol{r}=x_{1}\boldsymbol{e'}_{1}+ x_{2}\boldsymbol{e'}_{2}+ x_{3}\boldsymbol{e'}_{3}
\end{equation}
式(\ref{r})中，我们在原坐标系中有一个空间坐标向量，再通过坐标变换得到式(\ref{r'})，变换是通过$a_{ij}$这个正交矩阵变换实现。
\begin{equation}
  x'_{i}=\sum_{j}a_{ij}x_{j}
\end{equation}
\begin{equation}
  a_{ij}\equiv\frac{\partial x'_{i}}{\partial x_{j}}= \boldsymbol{e'}_{i}\cdot\boldsymbol{e}_{j}
\end{equation}

我们把上述这样形式的物理量叫做向量，或者1阶张量。这看起来好像跟废话一样，但是当你不把向量当作理所应当时，或者想想我们刚开始接触向量的困惑，而且，只有这样，我们才能更深刻的理解张量及所有物理量。如，我们常说的保守力场，为什么是向量场，为什么势场是标量场？这其实背后的意义就在这里。
\begin{equation}
\boldsymbol F \equiv\frac{\partial V}{\partial\boldsymbol{r}}
\end{equation}
	很容易就能证明，F是一个向量，那我们也知道了力做功为什么是内积，因为这两个向量运算只有内积才能在坐标变换下不变！
	
### 2.Rank 2 Tensor

我们比着葫芦画瓢，就能写出2阶张量的定义如下：
\begin{equation}\label{2tensor}
 T'_{ij}=\sum_{k}\sum_{l}a_{ik}a_{jl}T_{kl}
\end{equation}

* Stress Tensor

此时，很容易证明两个向量的direct product就是一个2阶张量，如应力：
\begin{equation}\label{stresstensor}
	\sigma=\left(
  \begin{array}{ccc}
  \sigma_{x} & \tau_{xy} & \tau_{xz}\\
  \tau_{yx} & \sigma_{y} & \tau_{yz}\\
  \tau_{zx} & \tau_{yz} & \sigma_{z} 
\end{array}
\right)\equiv\frac{d\boldsymbol{F}}{d\boldsymbol{A}}
\end{equation}
但只有二阶张量可以写成矩阵，三阶成了'立方体'了。

* Electromagnetic Tensor

下面讲：外积实际上是一个反对称的二阶张量！
首先，我们需要一找到Isotropic Tensor，再说它的意义——$\delta_{ij}$和$\epsilon_{lmn}$
有如下定义：
\begin{equation}
  T_{ij}\equiv A_{i}B_{j}-A_{j}B_{i}
\end{equation}
我们的二阶张量在三维空间里是一个3$\times$3的矩阵，是因为w我们认为，空间随我们坐标系变化，但时间不会，但如果我们相信光速不变原理，我们就知道时间也是相对的，随坐标变换而变，所以我们都把时间也纳为我们的时空架构里，这种架构就是tensor！在狭义相对论里，这个变换就是洛伦兹变换(其实就是相对运动速度决定的不同惯性坐标系)，那我们在这个变换里，重新调整我们的物理量定义，其中电磁场就是这个四维时空中的anti-symmetry rank 2 tensor！所以我们自然也就理解了，电动生磁，磁动生电

* Metric Tensor


## Postulates or Approximations


任何构想实际落实下来，理论吻合了实验，预测了实验，我们首先要讲的不应该是数学工具，更不应该是计算过程，而是问它的假设是什么？进一步还要思考，为什么可以做这样的假设？这才是至关重要的！
	
因为有些假设会避免一些结果，如果你做出了明明假设中被忽略的条件才能得出的结果，那这将是一个rubbish。

### 1.Euclidian Geometry

正如第一章所讲的那样，我们其实没有惯性坐标系，也不存在一个flat space，因为我们生活的时空处处都有万有引力。但是这引起的时空弯曲程度很小，我们暂且忽略。
\subsection{\sffamily Hooke’s Law}
这也就是第五章要讲的线弹性假设，这是非常重要的假设，本质就是泰勒级数，当然，事实上几乎没有作用力是线性的，但是即使到了量子力学解释世界，我们依然可以用这个近似，复杂的电磁力由于电子波函数的叠加，或者电子轨域的重叠所造成的，在小位移下，依然是线性的，这就如我在这一章开头所说，假设很重要，这个假设，并没有基于牛顿力学，或者我们的粒子观念，也没有基于我们对绝对时空的观念，这是一个纯数学的近似，所以当量子力学和相对论推翻了很多古典的定律时，它依然适用！

### 2.Newton's Laws of Motion

正如上节所说，量子力学和相对论彻底推翻了牛顿力学，但它仍是很好的近似，尤其是低速宏观尺度。但需要注意的是，这个近似和我们推导出弹性张量没有关系，只是后面的动力学，所以这也就理解了，我们可以{\bfseries 用Schrödinger方程来精确计算弹性张量}，而不仅仅是实验测得。

### 3.Continuity and Homogenization

连续性假设和均匀性假设，让我很容易想起流体力学和材料力学，这样我们在使用微积分时，计算简单很多。

### 4.Equilibrium equations

我们能站在地上是因为我们的鞋子和地面，脚和鞋子之间存在一种力，叫范德华力，是由于即使我们呈电中性，还是存在瞬时偶极矩，它产生的电磁力在两电中性物体靠近时产生强大的排斥力，当我们体内分子键不至于被这个力拆开时，我们就活生生的站在了地上，这种力还被称为表面力，因为它看似是两个相接触表面受到的，而与之相对应的力是体积力，是一种物理内部各个原子都会受到的力，如重力。
$$
  \sigma=\left(
  \begin{array}{ccc}
  \sigma_{x} & \tau_{xy} & \tau_{xz}\\
  \tau_{yx} & \sigma_{y} & \tau_{yz}\\
  \tau_{zx} & \tau_{yz} & \sigma_{z} 
\end{array}
\right)
$$
### 4.Force

建立x方向的力平衡方程：
\begin{equation}
	\left( \sigma _{x}+\frac {\partial \sigma _{x}}{\partial x}dx\right) dydz-\sigma _{x}dydz+\left( \tau_{yx}+\frac {\partial \tau_{yx} }{\partial y}dy\right) dxdz-\tau_{yx}dxdz+ \left( \tau_{zx}+\frac {\partial \tau_{zx} }{\partial z}dz\right) dxdy-\tau_{zx}dxdy=-Xdv
\end{equation}
整理得：
\begin{equation}
  \frac{\partial\sigma_{x}}{\partial x}+\frac{\partial\tau_{yx}}{\partial y}+ \frac{\partial\tau_{zx}}{\partial z}+X=0
\end{equation}
同理我们也可以得到y方向和z方向的力平衡

## Compatibility equations for displacements

\begin{equation}\label{straintensor}
\varepsilon=\left(
  \begin{array}{ccc}
  \varepsilon_{x} & \gamma_{xy} & \gamma_{xz}\\
  \gamma_{yx} & \varepsilon_{y} & \gamma_{yz}\\
  \gamma_{zx} & \gamma_{yz} & \varepsilon_{z} 
\end{array}
\right)
\end{equation}

### 1.Hooke‘law

由于上文中的受力平衡和变形协调方程，我们得出，应变张量和应力张量只有六个独立常数，我们把它写成向量的形式，依据Hooke's law，得出下式：
\begin{equation}\label{Hooke}
\boldsymbol{\sigma}= \left(
  \begin{array}{c}
  \sigma_{x}\\
  \sigma_{y}\\
  \sigma_{z}\\
  \tau_{xy}\\
  \tau_{yz}\\
  \tau_{zx}
\end{array}
\right)=\left(
  \begin{array}{cccccc}
C_{11} & C_{12} & C_{13} & C_{14} & C_{15} & C_{16}\\
C_{21} & C_{22} & C_{23} & C_{24} & C_{25} & C_{26}\\
C_{31} & C_{32} & C_{33} & C_{34} & C_{35} & C_{36}\\
C_{41} & C_{42} & C_{43} & C_{44} & C_{45} & C_{46}\\ C_{51} & C_{52} & C_{53} & C_{54} & C_{55} & C_{56}\\ C_{61} & C_{62} & C_{63} & C_{64} & C_{65} & C_{66}\\
\end{array}
\right)\left(
  \begin{array}{c}
  \varepsilon_{x}\\
  \varepsilon_{y}\\
  \varepsilon_{z}\\
  \gamma_{xy}\\
  \gamma_{yz}\\
  \gamma_{zx}
\end{array}
\right)
\end{equation}
容易证明，弹性张量是对称阵，所以，它最多有21个独立常数，我们根据材料对称性的不同，独立弹性常数有不同程度的缩小，比如六角晶系的晶体，独立的弹性常数只有五个：$C_{11},C_{12},C_{13},C_{33},C_{44}$。
我们同样可以像分析保守力场一样从能量角度去理解应力应变关系——即应变能：
\begin{equation}
  \sigma_{i}=\frac{1}{V}\left[\frac{\partial E(V,\varepsilon_{j})}{\partial\varepsilon_{i}}
  \right]_{\varepsilon=0}
\end{equation}
则弹性常数可表示为：
\begin{equation}
  C_{ij}= \frac{1}{V}\left[\frac{\partial^2 E(V,\varepsilon_{k})}{\partial\varepsilon_{i} \partial\varepsilon_{j}}
  \right]_{\varepsilon=0}
\end{equation}
这是用量子力学计算弹性常数的基本思想。

## 参考文献


1. 看看是科学
2. 大口袋空空的开始
3. 上课上课上课时

<style type="text/css">
img{
text-align: 
center; margin: 0 auto; 
}
</style>
