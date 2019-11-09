# On $\mathbf{u =}\frac{\mathbf{t}}{\mathbf{x}}$

作者：少科二班 高铭原

## 摘要：

我们尝试使用$u = \frac{t}{x}$来描述物体的运动状态。我们从一维上的运动开始研究，在几次尝试后采用$c= \frac{1}{du' \bullet dt}$来定义一个描述慢度变化快慢的物理量，称为"减慢度"，并被证明等价于加速度。之后我们又证明了慢度的加减都是以倒数求和求差的方式。将慢度运用到三维中时，我们发现并不能写成形同$u = \frac{t}{x}$的式子，所以我们将慢度写成矩阵，将时间写成向量（数组）。

最后将u应用在一些基础公式上。

经过反思，我们发现这种定义存在一定问题，且形式也极其复杂，并未发现优点。于是笔者得出结论，之所以在物理学史中放弃u这个概念不只是因为历史原因，很大程度上或许是因为它的复杂性。

## 1 导言

通常情况下，有两种比较物体运动快慢的方法，即在两物体运动时间相等的情况下比较它们的位移大小，或者是在两物体位移大小相等的时候比较它们的运动时间。对于两个因素没有一个相等时，就比较单位时间或位移内所行位移或所用时间，这两个量的大小可以分别用=$\frac{x}{t}$和$\frac{t}{x}$来表示。所以我们就可以定义出速度（$v = \frac{x}{t}$）和"慢度"（$u = \frac{t}{x}$）来描述物体运动的快慢。（至少）部分地由于历史原因，第一个速度的定义得到了较为普遍的采纳，并以此为基础建立了运动学体系。但是另一个定义，$u = \frac{t}{x}$似乎被忽略掉了，其原因是否只是局限在历史方面上这个问题却未经反思。所以本文将尝试着类比原来的运动学体系，以$u = \frac{t}{x}$为基础，建立新的运动学系统，旨在探究以$u = \frac{t}{x}$为基础的新运动学体系是否相较$v = \frac{x}{t}$过于复杂，并且即使过于复杂，是否仍会有方便之处这两个问题。

## 2 基础概念的研究

三维、二维上的运动均可分别分解为三个和两个方向上的一维上的运动，所以先从一维上的运动开始研究。

### 2.1 一维上

#### 2.1.1 慢度

仿照速度的定义，我们有慢度的定义：

$$
u = \frac{dt}{\text{dx}}
$$

其中x是一个矢量，其方向用正负来表示。

显而易见，有$u = \frac{1}{v}$。所以当u不变时，v，也不发生变化，所以当u保持不变时，是一个匀速直线运动，有：

$$
t = x \bullet u
$$

$$
x = \frac{t}{u}
$$

#### 2.1.2 描述慢度变化的快慢

类比加速度，我们考虑定义一个用于描述物体慢度变化快慢的物理量。首先，我们需要解决慢度差的定义的问题。

##### 2.1.2.1 慢度差

直观地，我们会直接想到：

$$
\mathrm{\Delta}u = u\left( 末 \right) - u\left( 初 \right)
$$

但是，我们继续考察这个式子：

$$
\mathrm{\Delta}u \bullet x = u\left( 末 \right) \bullet x - u\left( 初 \right) \bullet x
$$

也即$\mathrm{\Delta}u = \frac{t(末) - t(初)}{x}=\frac{\mathrm{\Delta}t}{x}$.，这表明$\mathrm{\Delta}u$反映了通过单位位移所用时间

那么我们为什么不可以把$\mathrm{\Delta}u$定义为$\frac{t}{\Delta x}$呢？

所以有：

$$
\mathrm{\Delta}u‘ = \frac{t}{\Delta x} = \frac{t}{x() - x()} = \frac{t}{\frac{1}{u(末)}t - \frac{1}{u(初)}t}=\frac{1}{\frac{1}{u(末)} - \frac{1}{u(初)}}
$$

我们暂且同时保留两种"慢度差"的定义。

2.1.2.2 加慢度------根据第一种慢度差定义得出

首先，我们从$\mathrm{\Delta}u = u\left( 末 \right) - u\left( 初 \right)入手$。仿照原来运动学体系中的a=$\frac{d^{2}x}{dt^{2}}$，作为位移对时间的二阶导数（因为在一维上位移虽然是向量，但是因为它可以只有一个用其正负性代表方向的数来表示，所以可以被看作标量），来定义出"加慢度",用字母"b"来表示，也即：
$$
b=\frac{d^{2}t}{dx^{2}}
$$

2.1.2.3 减慢度------根据第二种慢度的定义得出

接着我们来尝试$\mathrm{\Delta}u‘ = \frac{1}{\frac{1}{u(末)} - \frac{1}{u(初)}}$。因为在定义这个物理量时，我们考虑的是一定时间t内位移x的变化量，我们尝试把这个对应加速度的物理量定义为：
$$
c=\frac{du'}{\text{dt}}
$$

但是，因为在$\mathrm{\Delta}t \rightarrow 0$时，u(末)趋近于趋近于u(初)，所以$\frac{1}{u(末)} - \frac{1}{u(初)}$就会趋近于零，那么$\mathrm{\Delta}u‘$也会趋近于无穷大，那么在这种情况下，c本身更会趋近于无穷大，无论u变化的快慢。所以这里定义出来的c就根本无法被用来描述物体慢度变化的情况。

但是，在$\frac{1}{\frac{1}{u(末)} - \frac{1}{u(初)}}$趋近于无穷大的时候，它的倒数会趋近于零，那么它的倒数除以趋近于零的$\mathrm{\Delta}t$（看上去）不会出现原来趋近于无穷大的问题所以我们尝试如下的新定义，即：

$$
c = \frac{1}{du'} \div dt
$$

即：

$$
c = \frac{1}{\text{du}' \bullet dt}
$$

当c\0的情况下，$\frac{1}{u(末)} - \frac{1}{u(初)}$也会\0，即$\frac{1}{u(末)} \frac{1}{u(初)}$。因为dt本身趋近于0且运动的快慢程度变化一定会是连续的，所以u(末)和u(初)一定同号。对于同号两个数，倒数越大，其本身的绝对值越小。所以在这种情况下\|u(初)\|一定是大于\|u(末)\|的且二者同向。那么即当c\0时，慢度的大小是变小的。按照同样的方式，我们可以证明，当c\<0的时候，慢度的大小变大。所以根据c的正负性和慢度大小变化方向相反，将c命名为"减慢度"。

另外，c的绝对值越大，每个dt内，$\frac{1}{u(末)} - \frac{1}{u(初)}$的绝对值也会越大，即前后慢度差的绝对值也会变大。所以不仅c的正负性可以反映出慢度变化的趋势，它的大小还可以反映出慢度变化的快慢程度。

2.1.2.4 当b和c不变时------类比匀变速直线运动

速度变化时最简单的运动状态就是加速度a的方向和大小保持不变，也即匀变速直线运动。类比这种情况，作为对加慢度和减慢度两个新概念的试用，我们就先研究一下当b和c保持不变时的情况。

先考虑"匀加慢度直线运动"。因为b=$\frac{d^{2}t}{dx^{2}}$，在b保持不变时，设b=$b_{0}$，则有：

$$
\int_{}^{}{b_{0} \bullet dx = \int_{}^{}d^{2}}t \div dx
$$

即
$$
{\ b}_{0}x + m = \frac{dt}{\text{dx}}
$$

即
$$
u={\ b}_{0}x + m
$$
其中m为初慢度

继续两边积分：

$$
\int_{}^{}{（\text{\ b}_{0}x + m） \bullet dx = \int_{}^{}\frac{dt \bullet dx}{\text{dx}}}\ 
$$

即
$$
t=\text{\ b}_{0}x^{2}+mx+n
$$

同时，仿照匀速直线运动，我们还能得出公式：

$\overline{u} \bullet x = t\ $;${\ \ \ \ \ \ \ \ 2\ b}_{0} \bullet \mathrm{\Delta}t = t^{2} - {t_{0}}^{2}$ 等

解决b不变的情况之后，我们来考虑c不变时会是怎么样的。

$$
\int_{}^{}\frac{1}{du' \bullet dt} \bullet dt=\int_{}^{}{c \bullet dt}
$$
$$
\int_{}^{}\frac{1}{du'} = \int_{}^{}{c \bullet dt}
$$
$$
(\frac{1}{u_{t_{1}}}-\frac{1}{u_{t_{1 - dt}}})+(\frac{1}{u_{t_{1 - dt}}}-\frac{1}{u_{t_{1 - 2dt}}})+ (\frac{1}{u_{t_{1 - dt}}}-\frac{1}{u_{t_{1 - 2dt}}})+...+(\frac{1}{u_{t_{2 + dt}}}-\frac{1}{u_{t_{2}}})=c\bullet dt\bullet \frac{t_{1} - t_{2}}{\text{dt}}
$$
$$
\frac{1}{u_{t1}}-\frac{1}{u_{t2}}=c(t_{1} - t_{2})
$$

也即：

$$
v_{t1}-v_{t2}=c\bullet \Delta t
$$

我们可以敏锐地发现，当c不变的时候，这个运动就是在原来运动学体系里面的匀速直线运动，其中加速度a就完全等价于c。我们还可以从另外一个思路得出这个结论：

因为$\frac{1}{du'dt}=c$，所以有$\frac{1}{du'}=cdt$，等价于$1 \div \frac{1}{\frac{1}{u} - \frac{1}{u_{0}}}=cdt$

即$\frac{1}{u}$-$\frac{1}{u0}$=cdt 即v-v0=cdt

这里我们得出来等价的结论。

从原来的公式我们可以得出以下公式：

$u(末)=\frac{u(初)}{1 + ct \bullet u(初)}$，但是这个公式对于初慢度为无穷大（即初速度为零的情况）时并不适用。

比对匀变速直线运动的位移-时间公式（$x=\frac{1}{2}at^{2} + v_{0} \bullet t$）,我们还有：

$x=\frac{t}{u_{0}}+ct^{2}$

##### 2.1.2.5 用加慢度来描述匀加速直线运动

在现实世界中，因为F=ma，加速度a对于描述现实世界中存在的运动和力起到比较重要的·作用；同时通常情况下摩擦力和地球表面附近重力附近提供的加速度几乎保持不变，这样的运动可以看作匀加速直线运动。所以在新的运动学体系对建立中，我们一定需要用新概念对匀加速直线运动做考察。上一个章节中我们已经证明了匀减慢度直线运动即完全等价于匀变速直线运动。那么在这一节中，我们将尝试用加慢度里描述匀加速直线运动。

回顾一下加慢度定义的公式：

$b=\frac{d^{2}t}{dxdx}$，它等价于                       ~~这里啥都没写,原文如此~~

所以我们有$b=\frac{\frac{dt\left( x + dx \right)}{\text{dx}} - \frac{\text{dt}}{\text{dx}}}{\text{dx}}$

$b=\frac{u(x + dx) - u(x)}{\text{dx}}=\frac{\frac{1}{v(x + dx)} - \frac{1}{v(x)}}{\text{dx}}=\frac{1}{a}\frac{\frac{1}{t(x + dx)} - \frac{1}{t(x)}}{\text{dx}}$，对于a\0，有：

$$
b=\frac{1}{a} \bullet \frac{\sqrt{\frac{2dx}{a}}(\frac{1}{\sqrt{\frac{x}{\text{dx}} + 1}}\_\_\frac{1}{\sqrt{\frac{x}{\text{dx}}}})}{\text{dx}}
$$

$$
b=\frac{\sqrt{\frac{2\text{dx}}{a}}(\frac{1}{\sqrt{\frac{x}{\text{dx}} - + 1}}\_\_\frac{1}{\sqrt{\frac{x}{\text{dx}}}})}{\text{dx}}
$$

$$
b=\frac{\sqrt{\frac{2}{a}}(\frac{1}{\sqrt{x + dx}}\_\_\frac{1}{\sqrt{x}})}{\text{dx}}
$$

$$
b=\sqrt{\frac{2}{a}} \bullet {(x)}^{{- \frac{1}{2}}^{'}}
$$

$$
b=- \sqrt{\frac{2}{a}} \bullet \frac{1}{\sqrt{x^{3}}}
$$

同理，当a\<0时，有：

$$
b=\sqrt{\frac{2}{- a}} \bullet \frac{1}{\sqrt{- x^{3}}}
$$

事实上我们仅仅考虑了x和a同向的情况，不同向的则更加复杂。

其他公式因为其形式过于复杂就不在这里涉及了。

在研究现实世界中的物理现象时，加慢度的概念一定会被抛弃。因为假如我们在研究一个物体受力而存在加速度时引入加慢度b，计算这个b的值还需要已有的位移，过于复杂。所以在2.2开始的三维运动描述和力学部分就不再采用加慢度b以及引出这个概念的$\mathrm{\Delta}u = u\left( 末 \right) - u\left( 初 \right)$

#### 2.1.3 慢度的合成与相对运动

##### 2.1.3.1 慢度的合成

一个物体，初慢度为$u_{1}$，叠加了一个慢度$u_{2}$,这里我们来推导这个物体的等效慢度。

物体，以$u_{1}$的慢度，时间t内位移是$\frac{t}{u1}$；同样的在这个时间t内，以$u_{2}$的慢度，时间t内位移为。那么它的总位移为$\frac{t}{u1} + \frac{t}{u2}$。所以这个物体等效的慢度为

$$
u_{等效}=\frac{t}{\frac{t}{u1} + \frac{t}{u2}}=\frac{1}{\frac{1}{u1} + \frac{1}{u_{2}}}
$$

我们于是定义慢度和为

$$
u_{和}=\frac{1}{\frac{1}{u1} + \frac{1}{u_{2}}}
$$

这个结论也可以推广到任意个慢度求等效慢度（或者"慢度和"）：

$$
u_{\text{sum}} = \frac{1}{\sum_{}^{}\frac{1}{u}}
$$

##### 2.1.3.2相对运动（相对慢度）

一个A，它相对于某个参照系的慢度是$u_{a}$；另一个物体相对于这一个共同的参考系的慢度为$u_{b}$。那么，我们来计算物体A相对于物体B之间的的相对的慢度。

经过时间间隔t后，物体A的位移为$\frac{t}{u_{a}}$;在这个同样的时间间隔t内，物体B的位移是$\frac{t}{u_{b}}$。因为我们要计算A相对于物体B的相对速度，所以我们把要计算A相对于B的位移，即：$\frac{t}{u_{a}}-\frac{t}{u_{b}}$。

所以相对速度为 $u_{a - b} = \frac{t}{\frac{t}{u_{a}} - \frac{t}{u_{b}}}=\frac{1}{\frac{1}{u_{a}} - \frac{1}{u_{b}}}$

我们还可以留意到，所有有实际意义的公式内的慢度差慢度和都是它们的倒数差或倒数和的倒数，并没有使用直接相加减者。

### 2.2 一维上运动的推广------二维&三维

先放下上一章节最后的分析，继续建立更高维度的运动学体系。二维和三维上的运动可分别分解为两个不共线的运动和三个不共面的一维上的运动，而二维只是比三维上运动少一个分运动，与三维没有本质性区别，所以我们直接研究三维上的运动。

#### 2.2.1位矢和位移

指定一个点作为原点之后，一个物体的位置可以由一个从先前指定原点指向物体的矢量来描述，称之为"位矢"。在三维空间中，一个矢量可以分解为三个不共面的向量，为了方便，把每一个位矢都分解为三个互相垂直的向量，可以记作：

$$
\overrightarrow{r} = \ \lbrack\begin{matrix}
x \\
y \\
z \\
\end{matrix}\rbrack
$$

位矢的变化量即为位移，即：

$$
\Delta\overrightarrow{r} = \overrightarrow{r}\  - \ \overrightarrow{r_{0}}=\[\begin{matrix}
\mathrm{\Delta}x \\
\text{Δy} \\
\Delta z \\
\end{matrix}
$$

#### 2.2.2 三维慢度

##### 2.2.2.1 向量速度

仿照速度的定义（$\overrightarrow{v} = \frac{\text{\ Δ}\overrightarrow{r}}{t}$）以及一维上慢度的定义，我们很容易想到这样一个定义，即：

$$
\overrightarrow{u} = \frac{t}{\Delta\overrightarrow{r}}
$$

也就等价于：

$$
\Delta\overrightarrow{r} \bullet \overrightarrow{u} = t
$$

但是，一个常数（就像这里的t）可以是写成不止一组的两个向量的点积，即使有一个向量是固定的。所以在知道了$\Delta\overrightarrow{r}$和t时，我们仍然无法写出一个确定的慢度向量$\overrightarrow{u}。$

存在一种尝试是去规定取$\overrightarrow{u}$的方向与$\Delta\overrightarrow{r}$的方向相同，即设
$$
\overrightarrow{u} = u \bullet \lbrack\begin{matrix}
\frac{\mathrm{\Delta}x}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} \\
\frac{\mathrm{\Delta}x}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} \\
\frac{\mathrm{\Delta}x}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} \\
\end{matrix}\rbrack
$$
那么我们就有

$$
u \bullet \lbrack\begin{matrix}
\frac{\mathrm{\Delta}x}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} \\
\frac{\mathrm{\Delta}x}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} \\
\frac{\mathrm{\Delta}x}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} \\
\end{matrix}\rbrack \bullet \Delta\overrightarrow{r} = u \bullet \frac{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z}=t。
$$
因为在这个定义中，慢度$\overrightarrow{u}$是所以一个向量，我们把这种定义出来的三维上慢度称为"向量慢度"，以与下一节中将定义的"矩阵慢度"相区别。

我们再来尝试推导向量速度的计算公式。因为
$$
u \bullet \frac{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z}=t
$$
所以
$$
u=\frac{t(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}}
$$
于是顺利地有：

$$
\overrightarrow{u} =\begin{matrix}
\frac{t\Delta x(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\frac{t\Delta y(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\frac{t\Delta z(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\end{matrix}
$$
同样的，在二维中有：

$$
\overrightarrow{u} = \lbrack\begin{matrix}
u_{x} \\
u_{y} \\
\end{matrix}\rbrack=\lbrack\begin{matrix}
t\mathrm{\Delta}x\frac{\mathrm{\Delta}x + \mathrm{\Delta}y}{{\mathrm{\Delta}x}^{2} + \mathrm{\Delta}y^{2}} \\
t\mathrm{\Delta}y\frac{\mathrm{\Delta}x + \mathrm{\Delta}y}{{\mathrm{\Delta}x}^{2} + \mathrm{\Delta}y^{2}} \\
\end{matrix}\rbrack
$$

##### 2.2.2.2 矩阵慢度

在定义三维运动的慢度时，我们不妨再回顾一下我们对三维运动分析的大概思路：即我们先研究一维上的运动，然后将三维运动分解为三个一维运动。我们不妨严格按照这个思路进行分析：

在x轴的方向上，位移为$\mathrm{\Delta}x$，时间为t，所以x轴方向上慢度为$u_{x} = \frac{t}{\mathrm{\Delta}x}$

在y轴的方向上，位移为$\mathrm{\Delta}y$，时间为t，所以x轴方向上慢度为$u_{y} = \frac{t}{\mathrm{\Delta}y}$

在z轴的方向上，位移为$\mathrm{\Delta}z$，时间为t，所以x轴方向上慢度为$u_{z} = \frac{t}{\mathrm{\Delta}z}$

所以它在三维上的慢度为：

$$
\overrightarrow{u} = \lbrack\begin{matrix}
\frac{t}{\mathrm{\Delta}x} \\
\frac{t}{\mathrm{\Delta}x} \\
\frac{t}{\mathrm{\Delta}x} \\
\end{matrix}\rbrack
$$

但是这样定义出来的慢度$\overrightarrow{u}$，并不满足t=$\Delta\overrightarrow{r} \bullet \overrightarrow{u}$，实际上，应该是3t=$\Delta\overrightarrow{r} \bullet \overrightarrow{u}$。所以我们考虑另一种记法，把时间t写成一个向量$\overrightarrow{t} = \lbrack\begin{matrix}
t \\
t \\
t \\
\end{matrix}\rbrack$.此时仍不能写成形式近于t=ux的式子。所以我们尝试着去把慢度定义成一个矩阵U：
$$
U=\begin{matrix}
u_{x} & 0 & 0 \\
0 & u_{y} & 0 \\
0 & 0 & u_{z} \\
\end{matrix}
$$
此时则有：

$$
U \bullet \Delta\overrightarrow{r} = \overrightarrow{t}
$$

并且当$\overrightarrow{t}$和$\Delta\overrightarrow{r}$确定时，U也是可以计算出来的。

因为这个慢度U是由一个矩阵来描述的，所以我们命名其为"矩阵慢度"。（此后矩阵慢度用大写字母U表示，而向量慢度则由$\overrightarrow{u}$来表示）。另外，有时为了表示方便，把矩阵慢度U记成一个向量，即
$$
U=\begin{matrix}
u_{x} \\
u_{y} \\
u_{z} \\
\end{matrix}
$$
矩阵慢度U的向量形式的方向一般与位移方向不同，因为它在与三条坐标轴分别平行的分量比例为$\frac{1}{\Delta x}:\frac{1}{\Delta y}:\frac{1}{\Delta z}$而非$\Delta x：\Delta y：\Delta z$。但是向量形式的方向并没有实际意义。

二维中的矩阵慢度为
$$
\begin{matrix}
u_{x1} & 0 \\
0 & u_{x2} \\
\end{matrix}
$$

##### 2.2.2.3 慢度合成

我们继续来研究三维中慢度合成。

矩阵慢度U的合成可以直接套用一维中慢度和的结论，即：
$$
U_{1} + U_{2}=\begin{matrix}
\frac{1}{\frac{1}{u_{x1}} + \frac{1}{u_{x2}}} & 0 & 0 \\
0 & \frac{1}{\frac{1}{u_{y1}} + \frac{1}{u_{y2}}} & 0 \\
0 & 0 & \frac{1}{\frac{1}{u_{z1}} + \frac{1}{u_{z2}}} \\
\end{matrix}
$$

对于向量慢度$\overrightarrow{u}$的合成，我们也按照之前计算一维上速度合成的基本思路，即先计算出分别以两个慢度运动相同时间后的位移，再求和。以如下的例子为例：已知物体慢度为$\overrightarrow{u1}=\lbrack\begin{matrix}
u_{x1} \\
u_{y1} \\
u_{z1} \\
\end{matrix}\rbrack$，叠加一个慢度$\overrightarrow{u2}=\lbrack\begin{matrix}
u_{x2} \\
u_{y2} \\
u_{z2} \\
\end{matrix}\rbrack$。求解它的慢度和

解：t时间内，以慢度$\overrightarrow{u1}$运动的位移$\overrightarrow{r1}$满足$\overrightarrow{u1} \bullet \overrightarrow{r1} = t$

所以$\left\{ \begin{matrix}
u_{x1} \bullet \mathrm{\Delta}x1 + u_{y1} \bullet \mathrm{\Delta}y1 + u_{z1} \bullet \mathrm{\Delta}z1 = t \\
u_{x1}:\mathrm{\Delta}x1 = u_{y1}:\mathrm{\Delta}y1 = u_{z1}:\mathrm{\Delta}z1 \\
\end{matrix} \right.\ $

解得$\left\{ \begin{matrix}
x1 = t \bullet \frac{u_{x}1}{{u_{x1}}^{2} + {u_{y1}}^{2} + {u_{z1}}^{2}} \\
y1 = t \bullet \frac{u_{y}1}{{u_{x1}}^{2} + {u_{y1}}^{2} + {u_{z1}}^{2}} \\
z1 = t \bullet \frac{u_{z}1}{{u_{x1}}^{2} + {u_{y1}}^{2} + {u_{z1}}^{2}} \\
\end{matrix} \right.\ $

同理$\left\{ \begin{matrix}
x2 = t \bullet \frac{u_{x}2}{{u_{x2}}^{2} + {u_{y2}}^{2} + {u_{z2}}^{2}} \\
y2 = t \bullet \frac{u_{y2}}{{u_{x1}}^{2} + {u_{y1}}^{2} + {u_{z1}}^{2}} \\
z2 = t \bullet \frac{u_{z}2}{{u_{x2}}^{2} + {\text{uz}2}^{2} + uy2^{2}} \\
\end{matrix} \right.\ $

所以$\mathrm{\Delta}\overrightarrow{r_{\text{sum}}} = t\lbrack\begin{matrix}
\frac{u_{x}1}{{u_{x1}}^{2} + {u_{y1}}^{2} + {u_{z1}}^{2}} + \frac{u_{x}2}{{u_{x2}}^{2} + {u_{y2}}^{2} + {u_{z2}}^{2}} \\
\frac{u_{y}1}{{u_{x1}}^{2} + {u_{y1}}^{2} + {u_{z1}}^{2}} + \frac{u_{y2}}{{u_{x1}}^{2} + {u_{y1}}^{2} + {u_{z1}}^{2}} \\
\frac{u_{z}1}{{u_{x1}}^{2} + {u_{y1}}^{2} + {u_{z1}}^{2}} + \frac{u_{z}2}{{u_{x2}}^{2} + {\text{uz}2}^{2} + uy2^{2}} \\
\end{matrix}\rbrack$

设$u_{\text{sum}} = \lbrack\begin{matrix}
u_{1} \\
u_{2} \\
u_{3} \\
\end{matrix}\rbrack$,可带入公式$\overrightarrow{u} =\begin{matrix}
\frac{t\Delta x(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\frac{t\Delta y(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\frac{t\Delta z(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\end{matrix}$计算出$\overrightarrow{u_{\text{sum}}}$

我们发现，这种对慢度的定义在求解慢度和时结果极其复杂。原因在于为了使得向量慢度的方向与运动方向相同，向量慢度的分量必须满足某个特定的比例关系，在带入这个比例关系求解时需要解形式较为复杂的方程，从而不论是已知慢度求位移还是已知位移求慢度其结果都是复杂的分式，在求慢度和时因为既需要解一次位移又需要解一次慢度更加复杂。所以舍弃向量速度这个概念，正如我们舍弃加慢度一样。

#### 2.2.3 三维中的匀减慢度运动

直接套用一维上公式 $u(末)=\frac{u(初)}{1 + ct \bullet u(初)}\text{\ \ \ }$，可以得到
$$
U=\begin{matrix}
\frac{u_{x0}}{1 + c_{x}tu_{x0}} & 0 & 0 \\
0 & \frac{u_{y0}}{1 + c_{y}tu_{y0}} & 0 \\
0 & 0 & \frac{u_{z0}}{1 + c_{z}tu_{z0}} \\
\end{matrix}
$$

再继续套用一维上的时间-位移公式x=$\frac{t}{u_{0}}$+c$t^{2}$得到：

$$
\mathrm{\Delta}\overrightarrow{r} = \lbrack\begin{matrix}
\frac{t}{u_{x0}} + c_{x}t^{2} \\
\frac{t}{u_{y0}} + c_{y}t^{2} \\
\frac{t}{u_{z0}} + c_{z}t^{2} \\
\end{matrix}\rbrack
$$

我们可以发现，矩阵慢度的好处就在于可以直接套用一维中已经建立了的结论性公式。

另外，我们可以把三个方向上的减慢度写成一个向量，即：

$$
\overrightarrow{c} = \lbrack\begin{matrix}
c_{x} \\
c_{y} \\
c_{z} \\
\end{matrix}\rbrack
$$

#### 2.2.4 速率的转换

在原运动学体系之中，速率被用来描述速度的 大小，即$v = |\overrightarrow{v}|$。在我们将在下一个小节中考察的匀速率圆周运动，速率是一个重要的概念。所以我们将在本节中将速率用慢度来表示：
$$
v=\|v\|=\sqrt{{v_{x}}^{2} + {v_{y}}^{2} + {v_{z}}^{2}}=\sqrt{\frac{1}{{u_{x}}^{2}} + \frac{1}{{u_{y}}^{2}} + \frac{1}{{u_{z}}^{2}}}
$$
## 3 慢度的应用

**因篇幅原因，此处省略**

## 4 结论

我们从慢度的定义$u = \frac{dt}{\text{dx}}$出发，从一维上的运动开始研究，选定了$c=\frac{1}{du' \bullet dt}$作为描述慢度变化快慢的物理量。接着我们又把慢度的概念拓广到三维中去，并在最后对一些比较基础的物理公式进行了变换。

在进行的过程中，我们发现，我们经常需要在定义某个量时抛弃最简单直接的线性关系（比如我们在定义慢度差时没有使用$\mathrm{\Delta}u = u - u_{0}$），而是经常使用倒数和/差的倒数。这点使得许多公式在形式上和使用上较为复杂。而较为直觉地引出的物理量，比如$b=\frac{d^{2}t}{dx^{2}}$，在使用上没有实际意义。类比匀变速直线运动的匀加慢度直线运动并没有现实物理世界中的现象与之对应。

还有一点，当一个物体保持静止的时候，它的慢度即可以看作正无穷大（因为它通过一段正位移所用时间趋于无穷大），又可以看作负无穷大（同理可知）。

但是对于具体物理现象的描述，比如匀变速直线运动和最后一章节中变换的物理公式，只是把应该出现v的地方改成了$\frac{1}{u}$了，并没有特别的不方便之处。至于其特别的优点，笔者并没有探究得出。

另外，对于定义三维空间上运动的慢度时，若仍按照速度体系中把它定义成一个向量会遭遇极大的不便，只能把它定义成一个矩阵。

综上得出结论，据笔者目前所考察的来看，用$u = \frac{dt}{\text{dx}}$为基础·来描述运动及物理现象的体系虽并没有造成极大的不便，但在简洁性上严重逊于以$v=\frac{\text{dx}}{\text{dt}}$为基础的运动学体系。
