## Volume Integral
#MVC 
### Informal Definition
Consider a scalar field $\psi(x, y, z)$, and a three-dimensional region $R$.
Partition $R$ into $N$ cubic elements, of volume $\delta V=\delta x \delta y \delta z$ and let $\psi_{i}$ denote the value of $\psi$ at the centre of the $i^{t h}$ cubic element, $i \in\{1, \ldots N\}$.
Then, on partitioning with smaller and smaller cubes, and taking the limit $\delta V \rightarrow 0$,
$$
\lim \sum_{i=1}^{N} \psi_{i} \delta V \stackrel{\text { def }}{=} \iiint_{R} \psi \mathrm{d} V=\iiint_{R} \psi \mathrm{d} x \mathrm{~d} y \mathrm{~d} z
$$
>This is an **informal** definition. For the regions $R$ and functions $\psi$ we shall meet there will never be any issue about whether the integral exists and we will usually determine such integrals by calculating three definite integrals separately over co-ordinates $x, y, z$ (or other more appropriate co-ordinates). Again, complexities can emerge but these are not our focus.

>If the scalar field $\psi(x, y, z)=1$ then the integral $\iiint_{R} \psi \mathrm{d} V=\iiint_{R} \mathrm{~d} V$ gives the volume of the region $R$.

### Example 20
>A cone of height $h$ occupies the region $x^{2}+y^{2} \leqslant z^{2}, \quad 0 \leqslant z \leqslant h$ and has density $\rho(x, y, z)=\left(x^{2}+y^{2}\right) z$ at each point. Find the **mass** of the cone using Cartesian co-ordinates.

**Solution.** If we use $z$ as our first variable to divide up the cone, then the cross-section of the cone with a plane $z=z_{0}$ gives a disc $x^{2}+y^{2} \leqslant\left(z_{0}\right)^{2}, z=z_{0}\left(\right.$ at least if $\left.0 \leqslant z_{0} \leqslant h\right)$. We can then, say, take cross-sections of such discs with the line $y=y_{0}$ to produce horizontal slithers
$$
\left.x^{2} \leqslant\left(z_{0}\right)^{2}-\left(y_{0}\right)^{2}, y=y_{0}, z=z_{0} \quad \text { (at least if }\left|y_{0}\right| \leqslant z_{0}\right)
$$
and calculating their contribution to the mass is a simple one-dimensional integral. So, the mass $M$ is given by the triple integral
$$
\begin{aligned}
M &=\int_{z=0}^{h} \int_{y=-z}^{z} \int_{x=-\sqrt{z^{2}-y^{2}}}^{\sqrt{z^{2}-y^{2}}} \rho(x, y, z) \mathrm{d} x \mathrm{~d} y \mathrm{~d} z \\
&=\int_{z=0}^{h} \int_{y=-z}^{z} \int_{x=-\sqrt{z^{2}-y^{2}}}^{\sqrt{z^{2}-y^{2}}}\left(x^{2}+y^{2}\right) z \mathrm{~d} x \mathrm{~d} y \mathrm{~d} z
\end{aligned}
$$
We calculate the internal integrals in turn. We define
$$
\begin{aligned}
I_{1}(z, y)=\int_{x=-\sqrt{z^{2}-y^{2}}}^{\sqrt{z^{2}-y^{2}}}\left(x^{2}+y^{2}\right) z \mathrm{~d} x &=\left[z\left(\frac{x^{3}}{3}+y^{2} x\right)\right]_{-\sqrt{z^{2}-y^{2}}}^{\sqrt{z^{2}-y^{2}}} \\
&=2 z\left(\frac{\left(z^{2}-y^{2}\right)^{3 / 2}}{3}+y^{2} \sqrt{z^{2}-y^{2}}\right) \\
&=\frac{2 z}{3}\left(z^{2}+2 y^{2}\right) \sqrt{z^{2}-y^{2}}.
\end{aligned}
$$
The next internal integral is then
$$
I_{2}(z)=\int_{y=-z}^{z} \frac{2 z}{3}\left(z^{2}+2 y^{2}\right) \sqrt{z^{2}-y^{2}} \mathrm{~d} y
$$
If we make the substitution $y=z \sin t$, where $-\pi / 2 \leqslant t \leqslant \pi / 2$, then $I_{2}(z)$ becomes
$$
\begin{aligned}
I_{2}(z) &=\int_{t=-\pi / 2}^{\pi / 2} \frac{2 z}{3}\left(z^{2}+2 z^{2} \sin ^{2} t\right) \sqrt{z^{2}-z^{2} \sin ^{2} t}(z \cos t \mathrm{~d} t) \\
&=\int_{t=-\pi / 2}^{\pi / 2} \frac{2 z^{3}}{3}\left(1+2 \sin ^{2} t\right)|z \cos t|(z \cos t \mathrm{~d} t) \\
&=\frac{2 z^{5}}{3} \int_{t=-\pi / 2}^{\pi / 2}\left(1+2 \sin ^{2} t\right) \cos ^{2} t \mathrm{~d} t
\end{aligned}
$$
Now
$$
\begin{aligned}
& \int_{t=-\pi / 2}^{\pi / 2}\left(\cos ^{2} t+2 \sin ^{2} t \cos ^{2} t\right) \mathrm{d} t=\int_{t=-\pi / 2}^{\pi / 2}\left(\frac{1}{2}(1+\cos 2 t)+\frac{1}{2} \sin ^{2} 2 t\right) \mathrm{d} t \\
=& \int_{t=-\pi / 2}^{\pi / 2}\left[\frac{1}{2}(1+\cos 2 t)+\frac{1}{4}(1-\cos 4 t)\right] \mathrm{d} t=\left[\frac{3 t}{4}+\frac{1}{4} \sin 2 t-\frac{1}{8} \sin 4 t\right]_{-\pi / 2}^{\pi / 2}=\frac{3 \pi}{4} .
\end{aligned}
$$
Finally, we have
$$
M=\int_{z=0}^{h} I_{2}(z) \mathrm{d} z=\int_{z=0}^{h} \frac{2 z^{5}}{3} \times \frac{3 \pi}{4} \mathrm{~d} z=\frac{\pi}{2}\left[\frac{z^{6}}{6}\right]_{0}^{h}=\frac{\pi h^{6}}{12} .
$$
#### Alternative Solution
**Solution.** (Alternative method with [[Cylindrical Polar Coordinates]]). If $D(0, z)$ denotes the disc $x^{2}+y^{2} \leqslant z^{2}$, then the mass $M$ could be written as
$$
M=\int_{z=0}^{h} \iint_{D(0, z)} \rho(x, y, z) \mathrm{d} x \mathrm{~d} y \mathrm{~d} z=\int_{z=0}^{h} \iint_{D(0, z)}\left(x^{2}+y^{2}\right) z \mathrm{~d} x \mathrm{~d} y \mathrm{~d} z
$$
We know how to change from Cartesian co-ordinates $(x, y)$ to planar polar co-ordinates $(r, \theta)$ :
the change of variable rule is
$$
\iint \phi \mathrm{d} A=\iint \phi \mathrm{d} x \mathrm{~d} y=\iint \phi(r \mathrm{~d} r \mathrm{~d} \theta)
$$
where the $r$ appears as it is the [[Jacobian]] $\partial(x, y) / \partial(r, \theta)$. Thus
$$
\iint_{D(0, z)}\left(x^{2}+y^{2}\right) z \mathrm{~d} x \mathrm{~d} y=\int_{r=0}^{z} \int_{\theta=0}^{2 \pi} r^{2} z(r \mathrm{~d} \theta \mathrm{d} r)=2 \pi z \int_{r=0}^{z} r^{3} \mathrm{~d} r=2 \pi z\left[\frac{r^{4}}{4}\right]_{0}^{z}=\frac{\pi z^{5}}{2}
$$
Hence,
$$
M=\int_{z=0}^{h} \frac{\pi z^{5}}{2} \mathrm{~d} z=\left[\frac{\pi z^{6}}{12}\right]_{0}^{h}=\frac{\pi h^{6}}{12}.
$$
#### Remark 21
In the above example, we essentially used [[Cylindrical Polar Coordinates]], appreciating that the volume element $d V$ is given by
$$
\mathrm{d} V=\mathrm{d} x \mathrm{~d} y \mathrm{~d} z=r \mathrm{~d} r \mathrm{~d} \theta \mathrm{d} z
$$

### Example 22
>Find the volume of the region $R$ that lies above the paraboloid $z=x^{2}+y^{2}$ and beneath the plane $x+y+z=1$.
![Figure 15 | 400](MVC_15.png)

**Solution.** The $(x, y)$ co-ordinates of a point $(x, y, z)$ on the top planar surface of $R$ satisfy
$$
1-x-y \geqslant x^{2}+y^{2}
$$
and, so, the top planar surface projects vertically down to the set
$$
\begin{aligned}
W &=\left\{(x, y) \in \mathbb{R}^{2}: x+y+x^{2}+y^{2} \leqslant 1\right\} \\
&=\left\{(x, y) \in \mathbb{R}^{2}:\left(x+\frac{1}{2}\right)^{2}+\left(y+\frac{1}{2}\right)^{2} \leqslant \frac{3}{2}\right\}
\end{aligned}
$$
which is a disc, centre $(-1 / 2,-1 / 2)$ and radius $\sqrt{3 / 2}$. Hence we can determine the volume of the region $R$ as
$$
\begin{aligned}
V &=\iint_{(x, y) \in W}\left(\int_{z=x^{2}+y^{2}}^{1-x-y} \mathrm{~d} z\right) \mathrm{d} A \\
&=\iint_{(x, y) \in W}\left(1-x-y-x^{2}-y^{2}\right) \mathrm{d} A \\
&=\iint_{(x, y) \in W}\left(\frac{3}{2}-\left(x+\frac{1}{2}\right)^{2}-\left(y+\frac{1}{2}\right)^{2}\right) \mathrm{d} A .
\end{aligned}
$$
Natural co-ordinates for parameterizing $W$ are $(r, \theta)$ where
$$
x=-\frac{1}{2}+r \cos \theta, \quad y=-\frac{1}{2}+r \sin \theta, \quad 0 \leqslant \theta<2 \pi, 0 \leqslant r \leqslant \sqrt{3 / 2} .
$$
Hence, we have
$$
\begin{aligned}
V &=\int_{r=0}^{\sqrt{3 / 2}} \int_{\theta=0}^{2 \pi}\left(\frac{3}{2}-r^{2} \cos ^{2} \theta-r^{2} \sin ^{2} \theta\right)(r \mathrm{~d} \theta \mathrm{d} r) \\
&=2 \pi \int_{r=0}^{\sqrt{3 / 2}}\left(\frac{3 r}{2}-r^{3}\right) \mathrm{d} r=2 \pi\left[\frac{3 r^{2}}{4}-\frac{r^{4}}{4}\right]_{0}^{\sqrt{3 / 2}} \\
&=2 \pi\left(\frac{9}{8}-\frac{9}{16}\right) \\
&=\frac{9 \pi}{8} .
\end{aligned}
$$