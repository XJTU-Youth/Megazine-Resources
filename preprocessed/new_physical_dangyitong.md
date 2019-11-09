# 构建新物理体系的思考

作者：少科二班    党一桐

## 绪论

在历史中，运动学中关于速度的定义一直是位移比时间。如果将速度定义为时间比位移，那么整个运动学体系将会如何描述？这是这篇论文要解决的首要问题。

## 定义

要解决这一问题，首先要对各大物理量作出合适的定义。首先考虑速度v = Δt / Δx，在这一定义下，出现了数学困难：没有定义向量作为分母的运算。在2016.1北京航空航天大学发表的文章 复矢量空间及矢量除法讨论 中，第一次具体的讨论了类似运算，然而该文章中的运算并不适合我们这里的需求。所以我们需要严谨的定义这个运算。

考虑以下定义：若有标量λ和两同向向量a，b，且a≠0，有a•b=λ，则λ/a＝b。

然而，这一定义用于我们的体系中是有很大问题的。比如，当一段时间内没有位移或位移为零时，这一定义就不适用了。且新得到的向量不符合向量的运算法则。这就造成了很大的问题。

那么，考虑如下定义：$λ/a＝arctan(λ/|a|)\underline{a}$，$\underline{a}$是与$a$同向的单位向量，则避免了无穷大，然而这一变换是非线性的，及结果仍不遵循向量运算法则。

故这一问题先放下不谈，考虑加速度的定义。

对此，加速度有三种容易想到的定义方法，分别列举如下：

$$
a = \frac{\Delta\frac{\Delta x}{\Delta t}}{\Delta t}
$$
即
$$
a=\frac{1}{\Delta v \Delta t}
$$



$$
a=\frac{\Delta v}{\Delta x}
$$



$$
a=\frac{\Delta v}{\Delta t}
$$
对于这三种定义，都可以引出一套运动学-力学体系。

考虑(2)，则这一体系中的描述与经典牛顿体系一致，不加以讨论。

考虑(3)，对这一描述进行量纲分析，则a的量纲为$TL^{-2}$，物理意义为单位距离内通过单位距离的时间的变化量。

考虑(4)，仍进行量纲分析，a的量纲为$L^{-1}$，物理意义为单位时间内通过单位距离的时间的变化量。

从直觉上考虑，2和3中2明显更好一些。然而，不论是采用(3)或是(4)，a都不满足常用的线性运算。

这个体系本身有很大问题，问题主要来源于新的体系中参照与坐标系有关，这可能和相对论有相似之处。下面我们定义一些不严谨的系统，这个系统把经典系统与新系统揉和在了一起。

对于速度，在一维上，定义

$$
u = \frac{dt}{\text{dx}}
$$

则有：
$$
t = x \bullet u
$$
$$
x = \frac{t}{u}
$$
特别的，当u不变时，运动可以称为匀速直线运动。

对于变速度运动，我们先考虑速度差的概念。

直观地，我们会直接想到：

$$
\mathrm{\Delta}u = u\left( 末 \right) - u\left( 初 \right)
$$

但是，我们继续考察这个式子：

$$
\mathrm{\Delta}u \bullet x = u\left( 末 \right) \bullet x - u\left( 初 \right) \bullet x
$$

也即
$$
\mathrm{\Delta}u = \frac{t\left( 末 \right) - t\left( 初 \right)}{x}=\frac{\mathrm{\Delta}t}{x}
$$
这表明$\mathrm{\Delta}u$反映了通过单位位移所用时间

那么我们为什么不可以把$\mathrm{\Delta}u$定义为$\frac{t}{\Delta x}$呢？

所以有：

$$
\mathrm{\Delta}u‘ = \frac{t}{\Delta x} = \frac{t}{x\left( \right) - x\left( \right)} = \frac{t}{\frac{1}{u\left( 末 \right)}t - \frac{1}{u\left( 初 \right)}t}$=$\frac{1}{\frac{1}{u\left( 末 \right)} - \frac{1}{u\left( 初 \right)}}
$$

我们暂且同时保留两种"速度差"的定义 为以下加速度的定义作出准备。

对于2.4， 仿照原来运动学体系中的$a=\frac{d^{2}x}{dt^{2}}$，我们作出新的$\alpha＝\frac{d^{2}t}{dx^{2}}$

接着我们来尝试$\mathrm{\Delta}u‘ = \frac{1}{\frac{1}{u\left( 末 \right)} - \frac{1}{u\left( 初 \right)}}$。因为在定义这个物理量时，我们考虑的是一定时间t内位移x的变化量，我们尝试把这个对应加速度的物理量定义为：
$$
c=\frac{du^{'}}{\text{dt}}
$$
但是，这一定义是不好的。因为当Δt趋向于零时，Δu'不收敛。然而，下式收敛，且有实际意义：

$а= \frac{1}{du^{'}} \div dt$

即：
$$
а= \frac{1}{du^{'} \bullet dt}
$$
仔细考虑α和а，发现对于α，整个定义是不均匀的，即当α不变时，质点并没有按照经典的匀变速运动运动，而相反，а可以很好的的描述物体的运动。

从此，我们将а（西里尔字符）记作a（拉丁字符）

那么现在，我们用加速度a描述匀加速直线运动。可以发现，$\mathrm{\Delta}t \bullet a = \mathrm{\Delta}u$.

所以，现在我们确定了现有加速度a的正统地位。

我们现在来考虑速度叠加的情景：

一个物体，初速度为$u_{1}$，叠加了一个速度$u_{2}$,这里我们来推导这个物体的等效速度。

这个物体，以$u_{1}$的速度，时间t内位移是$\frac{t}{u1}$；同样的在这个时间t内，以$u_{2}$的速度，时间t内位移为。那么它的总位移为$\frac{t}{u1} + \frac{t}{u2}$。所以这个物体等效的速度为

$$
u_{等效}=\frac{t}{\frac{t}{u1} + \frac{t}{u2}}=\frac{1}{\frac{1}{u1} + \frac{1}{u_{2}}}
$$

我们于是定义速度和为

$$
u_{sum12}=\frac{1}{\frac{1}{u1} + \frac{1}{u_{2}}}
$$

推广这个定义，我们定义任意个速度的叠加公式为：
$$
u_{\text{sum}} = \frac{1}{\sum_{}^{}\frac{1}{u_{n}}}
$$

对于选取不同参考系的情景，可类比此进行分析。如下设运动参考系速度为v，静止参考系中物体速度为u，在运动参考系中物体速度为w，得：

$$
w = \frac{1}{\frac{1}{u} + \frac{1}{v}}
$$

我们继续考虑更高维度的运动，在三维中，质点位置可以用三维向量或者三阶矩阵来描述。所以我们考虑的速度也有这两种形式。

对于向量速度，我们参考一开始定义的除法，定义
$$
\overrightarrow{u} = \frac{t}{\Delta\overrightarrow{r}}
$$
就此完成。我们看对其更严谨的定义： 
$$
u \bullet \begin{bmatrix}
\frac{\mathrm{\Delta}x}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} \\
\frac{\mathrm{\Delta}x}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} \\
\frac{\mathrm{\Delta}x}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} \\
\end{bmatrix} \bullet \Delta\overrightarrow{r} = u \bullet \frac{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z} = t
$$
这里的u即为速度的向量化定义。

对于其计算公式，因为
$$
u \bullet \frac{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}}{\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z}=t
$$
所以
$$
u=\frac{t\left( \mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z \right)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}}
$$

于是顺利地有：

$$
\overrightarrow{u} =\begin{matrix}
\frac{t\Delta x\left( \mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z \right)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\frac{t\Delta y\left( \mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z \right)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\frac{t\Delta z\left( \mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z \right)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\end{matrix}
$$

那么我们再来定义矩阵形式的速度：

定义
$$
\overrightarrow{u} = \lbrack\begin{matrix}
\frac{t}{\mathrm{\Delta}x} \\
\frac{t}{\mathrm{\Delta}x} \\
\frac{t}{\mathrm{\Delta}x} \\
\end{matrix}\rbrack
$$
来表示速度。然而，这一速度不满足$t=\Delta\overrightarrow{r} \bullet \overrightarrow{u}$，实际上，应该是$3t=\Delta\overrightarrow{r} \bullet \overrightarrow{u}$，所以，考虑将时间定义为向量
$$
\overrightarrow{t} = \lbrack\begin{matrix}
t \\
t \\
t \\
\end{matrix}\rbrack
$$
此时仍不能写成形式近于t=ux的式子。所以我们尝试着去把慢度定义成一个矩阵U： 
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

我们再来考虑三维空间内的速度合成：

三维空间内的速度的合成可以直接套用一维空间的结论，即

$$
U_{1} + U_{2}=\begin{matrix}
\frac{1}{\frac{1}{u_{x1}} + \frac{1}{u_{x2}}} & 0 & 0 \\
0 & \frac{1}{\frac{1}{u_{y1}} + \frac{1}{u_{y2}}} & 0 \\
0 & 0 & \frac{1}{\frac{1}{u_{z1}} + \frac{1}{u_{z2}}} \\
\end{matrix}
$$

这是矩阵形式的。对于向量形式的，我们有如下推导过程：

已知物体速度为$\overrightarrow{u1}$=$\lbrack\begin{matrix}
u_{x1} \\
u_{y1} \\
u_{z1} \\
\end{matrix}\rbrack$，叠加一个速度$\overrightarrow{u2} = \lbrack\begin{matrix}
u_{x2} \\
u_{y2} \\
u_{z2} \\
\end{matrix}\rbrack$。t时间内，以速度$\overrightarrow{u1}$运动的位移$\overrightarrow{r1}$满足$\overrightarrow{u1} \bullet \overrightarrow{r1} = t$

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
\end{matrix}\rbrack$,可带入公式$\overrightarrow{u} =$\[$\begin{matrix}
\frac{t\Delta x(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\frac{t\Delta y(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\frac{t\Delta z(\mathrm{\Delta}x + \mathrm{\Delta}y + \mathrm{\Delta}z)}{{\Delta x}^{2} + {\Delta y}^{2} + {\Delta z}^{2}} \\
\end{matrix}$\]计算出$\overrightarrow{u_{\text{sum}}}$

经上述推导过程，我们发现，向量形式的速度在求解方面极为困难，究其原因在于其方向需保证为一定，在求解中带来了一定困难。故我们舍弃向量速度，在之后的过程中不用。

而对于速率，我们采用速度的模进行定义。

有了这些定义，我们就可以用新的定义解决实际问题了，例如重新描述物理学中的公式描述。

相似的，我们也可以对角速度、角加速度等概念进行相似的定义，对刚体运动学进行相似的外延。因篇幅有限，本篇文章就此打住。

## 总结

对于这样一个新的速度定义方式，在中国知网上并没有检索到有关信息。究其原因，应当是这个定义方法不能保证简洁性。对于目前的物理公式定律，尚未发现将v换为1/v能带来简洁性的。故本文只是讨论了这种新型的速度定义方法，并对其加以分析。总而言之，本篇论文所描述的体系构建是不好的，原因在于这一体系还没有能力替代现有体系，且其自洽性还有待检验。
