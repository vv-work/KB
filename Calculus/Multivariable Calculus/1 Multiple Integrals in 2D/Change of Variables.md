## Change of Variables
#MVC
### Theorem 16
Let $\mathbf{f}: R \rightarrow S$ be a bijection between two regions of $\mathbb{R}^{2}$, which is differentiable and has differentiable inverse with
$$
\frac{\partial(u, v)}{\partial(x, y)}, \quad \frac{\partial(x, y)}{\partial(u, v)},
$$
defined and non-zero everywhere. Further, write $(u, v)=\mathbf{f}(x, y)$ and let $\psi(x, y)=\Psi(u, v) .$ Then
$$
\begin{aligned}
\iint_{(u, v) \in S} \Psi(u, v) d u d v &=\iint_{(x, y) \in R} \psi(x, y)\left|\frac{\partial(u, v)}{\partial(x, y)}\right| d x d y, \\
\iint_{(x, y) \in R} \psi(x, y) d x d y &=\iint_{(u, v) \in S} \Psi(u, v)\left|\frac{\partial(x, y)}{\partial(u, v)}\right| d u d v .
\end{aligned}
$$
### Exercise 17
>Evaluate $\iint_{\mathbb{R}^{2}} \exp \left[-\left(x^{2}+y^{2}\right)\right] \mathrm{d} A$,and hence determine $\int_{-\infty}^{\infty} \exp \left[-t^{2}\right] \mathrm{d} t$.

**Solution.**
$$
\begin{aligned}
I &=\iint_{\mathbb{R}^{2}} \exp \left[-\left(x^{2}+y^{2}\right)\right] \mathrm{d} A=\iint_{\mathbb{R}^{2}} \exp \left[-\left(x^{2}+y^{2}\right)\right] \mathrm{d} x \mathrm{~d} y \\
&=\iint \exp \left[-\left(r^{2}\right)\right]\left|\frac{\partial(x, y)}{\partial(r, \theta)}\right| \mathrm{d} r \mathrm{~d} \theta=\int_{0}^{\infty}\left\{\int_{0}^{2 \pi} \mathrm{d} \theta\right\} \exp \left[-\left(r^{2}\right)\right] r \mathrm{~d} r=\pi \int_{0}^{\infty} 2 r \exp \left[-\left(r^{2}\right)\right] \mathrm{d} r \\
&=\pi\left[\exp \left[-\left(r^{2}\right)\right]\right]_{0}^{\infty}=\pi
\end{aligned}
$$
Furthermore let $J=\int_{-\infty}^{\infty} \exp \left[-t^{2}\right] \mathrm{d} t$. Then
$$
J^{2}=\int_{-\infty}^{\infty} \exp \left[-x^{2}\right] \mathrm{d} x \int_{-\infty}^{\infty} \exp \left[-y^{2}\right] \mathrm{d} y=\iint_{\mathbb{R}^{2}} \exp \left[-\left(x^{2}+y^{2}\right)\right] \mathrm{d} x \mathrm{~d} y=I
$$
Noting $J>0$ to give the sign of the root, we thus have $J=\sqrt{\pi}$.
[[Plane Polar Coordinates]]
### Example 18
Calculate the area bounded by the curves
$$
2 x=1-y^{2}, \quad 2 x=y^{2}-1, \quad 8 x=16-y^{2}, \quad 8 x=y^{2}-16 \text { . }
$$
![Figure 11 | 300](MVC_11.png)
**Solution.** We now change to $(u, v)$, [[Parabolic Coordinates]]
$$
x=\frac{1}{2}\left(u^{2}-v^{2}\right), \quad y=u v
$$
Note that when $u=1$ then $v=y$ and so $2 x=1-y^{2}$, which is the equation of the first curves. Likewise if $u=2$ then $v=y / 2$ and so $2 x=4-y^{2} / 4$ which is the third curve. By symmetry the second and fourth curves correspond to $v=1$ and $v=2$. The region of interest is therefore $1 \leqslant u \leqslant 2, \quad 1 \leqslant v \leqslant 2 .$ The Jacobian is given by
$$
\frac{\partial(x, y)}{\partial(u, v)}=\operatorname{det}\left(\begin{array}{cc}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
\end{array}\right)=\operatorname{det}\left(\begin{array}{cc}
u & -v \\
v & u
\end{array}\right)=u^{2}+v^{2} .
$$

Hence, the area is given by
$$
\begin{aligned}
A &=\int_{u=1}^{u=2} \int_{v=1}^{v=2}\left|\frac{\partial(x, y)}{\partial(u, v)}\right| \mathrm{d} v \mathrm{~d} u=\int_{u=1}^{u=2} \int_{v=1}^{v=2}\left(u^{2}+v^{2}\right) \mathrm{d} v \mathrm{~d} u \\
&=\int_{u=1}^{u=2}\left[u^{2} v+\frac{v^{3}}{3}\right]_{v=1}^{v=2} \mathrm{~d} u=\int_{u=1}^{u=2}\left(u^{2}+\frac{7}{3}\right) \mathrm{d} u \\
&=\left[\frac{u^{3}}{3}+\frac{7 u}{3}\right]_{1}^{2}=\frac{7}{3}+\frac{7}{3}=\frac{14}{3}
\end{aligned}
$$

### Example 19
>The cardioid with equation $r=a(1+\cos \theta)$ bounds a region $S .$ Find the mean value of $r$ in $S$.

**Solution.** This mean value equals
$$
\frac{1}{\operatorname{area}(S)} \iint_{S} r \mathrm{~d} A
$$
The area of $S$ equals
$$
\begin{aligned}
\operatorname{area}(S) &=\int_{\theta=0}^{2 \pi} \int_{r=0}^{a(1+\cos \theta)} r \mathrm{~d} r \mathrm{~d} \theta \\
&=\frac{a^{2}}{2} \int_{\theta=0}^{2 \pi}(1+\cos \theta)^{2} \mathrm{~d} \theta \\
&=\frac{a^{2}}{2} \int_{\theta=0}^{2 \pi}\left(1+2 \cos \theta+\cos ^{2} \theta\right) \mathrm{d} \theta \\
&=\frac{a^{2}}{2}(2 \pi+0+\pi)=\frac{3 \pi a^{2}}{2} .
\end{aligned}
$$
And
$$
\begin{aligned}
\iint_{S} r \mathrm{~d} A &=\int_{\theta=0}^{2 \pi} \int_{r=0}^{a(1+\cos \theta)} r(r \mathrm{~d} r \mathrm{~d} \theta) \\
&=\frac{a^{3}}{3} \int_{\theta=0}^{2 \pi}(1+\cos \theta)^{3} \mathrm{~d} \theta \\
&=\frac{a^{3}}{3} \int_{\theta=0}^{2 \pi}\left(1+3 \cos \theta+3 \cos ^{2} \theta+\cos ^{3} \theta\right) \mathrm{d} \theta \\
&=\frac{a^{3}}{3}(2 \pi+0+3 \pi+0)=\frac{5 \pi a^{3}}{3}
\end{aligned}
$$
Hence the mean value of $r$ within the cardioid equals
$$
\frac{5 \pi a^{3} / 3}{3 \pi a^{2} / 2}=\frac{10 a}{9} .
$$