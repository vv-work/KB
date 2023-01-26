## Median
#MVC 
### Definition
Given a function $f$ on a region $R \subseteq \mathbb{R}^{3}$, the [[Median]] of $f$ is the value of $m$ that satisfies
$$
\operatorname{Vol}(\{(x, y, z): f(x, y, z) \leqslant m\})=\frac{1}{2} \operatorname{Vol}(R)
$$
### Example 29
Find the [[Median]] value of $z$ on the upper hemisphere of $x^{2}+y^{2}+z^{2} \leqslant a^{2} .$
**Solution.** We will use [[cylindrical polar coordinates]]. $\operatorname{Vol}(R)=2 \pi a^{3} / 3$. And the volume of the hemisphere with $0 \leqslant z \leqslant h$ equals
$$
\begin{aligned}
& \int_{z=0}^{h} \int_{\theta=0}^{2 \pi} \int_{r=0}^{\sqrt{a^{2}-z^{2}}} r \mathrm{~d} r \mathrm{~d} \theta \mathrm{d} z \\
=& 2 \pi \int_{z=0}^{h}\left[\frac{r^{2}}{2}\right]_{0}^{\sqrt{a^{2}-z^{2}}} \mathrm{~d} z \\
=& \pi \int_{z=0}^{h}\left(a^{2}-z^{2}\right) \mathrm{d} z \\
=& \pi\left[a^{2} z-\frac{z^{3}}{3}\right]_{0}^{h} \\
=& \pi\left(a^{2} h-\frac{h^{3}}{3}\right) .
\end{aligned}
$$
So we need that
$$
\pi\left(a^{2} h-\frac{h^{3}}{3}\right)=\frac{\pi a^{3}}{3} .
$$
So we can rearrange to
$$
0=h^{3}-3 a^{2} h+a^{3} \text { . }
$$
There is one solution to this in the range $0<h<a$ and this approximately equals
$$
h=0.347296 a .
$$