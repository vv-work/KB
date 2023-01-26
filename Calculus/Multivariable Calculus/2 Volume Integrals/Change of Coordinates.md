## Change of Coordinates
#MVC 
### Theorem 23
Let $\mathbf{f}: R \rightarrow S$ be a bijection between subsets of $\mathbb{R}^{3}$ which is differentiable and has **differentiable** inverse. Take coordinates $x_{i}$ on $R$ and $u_{i}$ on $S$ related by the formula
$$
\left(u_{1}, u_{2}, u_{3}\right)=\mathbf{f}\left(x_{1}, x_{2}, x_{3}\right)
$$
and let $\psi\left(x_{1}, x_{2}, x_{3}\right)=\Psi\left(u_{1}, u_{2}, u_{3}\right)$ be scalar fields. Then

$$
\iiint_{S} \Psi\left(u_{1}, u_{2}, u_{3}\right) \mathrm{d} u_{1} \mathrm{~d} u_{2} \mathrm{~d} u_{3}=\iiint_{R} \psi\left(x_{1}, x_{2}, x_{3}\right)\left|\frac{\partial\left(u_{1}, u_{2}, u_{3}\right)}{\partial\left(x_{1}, x_{2}, x_{3}\right)}\right| \mathrm{d} x_{1} \mathrm{~d} x_{2} \mathrm{~d} x_{3} .
$$
#### Sketch Proof
Partition the region $R$ into $N$ cubic elements and let the $i^{t h}$ cubic element given by
$$
\left[x_{1}, x_{1}+\delta x_{1}\right] \times\left[x_{2}, x_{2}+\delta x_{2}\right] \times\left[x_{3}, x_{3}+\delta x_{3}\right]
$$
which has volume $\delta x_{1} \delta x_{2} \delta x_{3}$. The value of the scalar field at the centre of the mapped eleme is
$$
\Psi_{i}=\Psi\left(\mathbf{f}\left(x_{1}+\delta x_{1} / 2, x_{2}+\delta x_{2} / 2, x_{3}+\delta x_{3} / 2\right)\right)=\psi_{i}=\psi\left(x_{1}+\delta x_{1} / 2, x_{2}+\delta x_{2} / 2, x_{3}+\delta x_{3} /\right.
$$
Also, under the map $\mathbf{f}$, the $i^{t h}$ cubic element maps to a deformed parallelepiped, denoted below, with sides
$$
\begin{array}{l}
\mathbf{f}\left(x_{1}+\delta x_{1}, x_{2}, x_{3}\right)-\mathbf{f}\left(x_{1}, x_{2}, x_{3}\right) \approx \frac{\partial \mathbf{f}}{\partial x_{1}} \delta x_{1} \\
\mathbf{f}\left(x_{1}, x_{2}+\delta x_{2}, x_{3}\right)-\mathbf{f}\left(x_{1}, x_{2}, x_{3}\right) \approx \frac{\partial \mathbf{f}}{\partial x_{2}} \delta x_{2} \\
\mathbf{f}\left(x_{1}, x_{2}, x_{3}+\delta x_{3}\right)-\mathbf{f}\left(x_{1}, x_{2}, x_{3}\right) \approx \frac{\partial \mathbf{f}}{\partial x_{3}} \delta x_{3} .
\end{array}
$$
The volume of a parallelepiped with sides $\mathbf{a}, \mathbf{b}, \mathbf{c}$ is $|\mathbf{a} \cdot(\mathbf{b} \wedge \mathbf{c})|$ and, so, as a first approximati the volume of the image of the $i^{t h}$ element is
$$
\left|\left[\frac{\partial \mathbf{f}}{\partial x_{1}}, \frac{\partial \mathbf{f}}{\partial x_{2}}, \frac{\partial \mathbf{f}}{\partial x_{3}}\right]\right| \delta x_{1} \delta x_{2} \delta x_{3}=\left|\frac{\partial\left(u_{1}, u_{2}, u_{3}\right)}{\partial\left(x_{1}, x_{2}, x_{3}\right)}\right| \delta x_{1} \delta x_{2} \delta x_{3} .
$$
Thus, before taking limits, partitioning $S$ by the images $I M_{i}$, an approximation for
$$
\iiint_{S} \Psi\left(u_{1}, u_{2}, u_{3}\right) \mathrm{d} u_{1} \mathrm{~d} u_{2} \mathrm{~d} u_{3}
$$
is
$$
\sum_{i=1}^{N} \Psi_{i} \text { Volume }\left(I M_{i}\right)=\sum_{i=1}^{N} \Psi_{i}\left|\frac{\partial\left(u_{1}, u_{2}, u_{3}\right)}{\partial\left(x_{1}, x_{2}, x_{3}\right)}\right| \delta x_{1} \delta x_{2} \delta x_{3}=\sum_{i=1}^{N} \psi_{i}\left|\frac{\partial\left(u_{1}, u_{2}, u_{3}\right)}{\partial\left(x_{1}, x_{2}, x_{3}\right)}\right| \delta x_{1} \delta x_{2} \delta x_{3} .
$$

Taking limits gives
$$
\iiint_{\left(u_{1}, u_{2}, u_{3}\right) \in S} \Psi\left(u_{1}, u_{2}, u_{3}\right) \mathrm{d} u_{1} \mathrm{~d} u_{2} \mathrm{~d} u_{3}=\iiint_{\left(x_{1}, x_{2}, x_{3}\right) \in R} \psi\left(x_{1}, x_{2}, x_{3}\right)\left|\frac{\partial\left(u_{1}, u_{2}, u_{3}\right)}{\partial\left(x_{1}, x_{2}, x_{3}\right)}\right| \mathrm{d} x_{1} \mathrm{~d} x_{2} \mathrm{~d} x_{3}
$$

note that the [[chain rule]] for [Jacobians](Jacobian) ensures that it is impossible to obtain diﬀerent answers for a [[volume integral]] by using diﬀerent sets of variables.

### Example 24
[[Cylindrical Polar Coordinates]]
$\frac{\partial(x, y, z)}{\partial(r, \theta, z)}=\left|\begin{array}{ccc}\frac{\partial x}{\partial r} & \frac{\partial x}{\partial \theta} & \frac{\partial x}{\partial z} \\ \frac{\partial y}{\partial r} & \frac{\partial y}{\partial \theta} & \frac{\partial y}{\partial z} \\ \frac{\partial z}{\partial r} & \frac{\partial z}{\partial \theta} & \frac{\partial z}{\partial r}\end{array}\right|=\left|\begin{array}{ccc}\cos \theta & -r \sin \theta & 0 \\ \sin \theta & r \cos \theta & 0 \\ 0 & 0 & 1\end{array}\right|=\left|\begin{array}{cc}\cos \theta & -r \sin \theta \\ \sin \theta & r \cos \theta\end{array}\right|=r$
### Example 25
For [[Spherical Polar Coordinates]]
$$
\mathrm{d} V=\mathrm{d} x \mathrm{~d} y \mathrm{~d} z=r^{2} \sin \theta \mathrm{d} r \mathrm{~d} \theta \mathrm{d} \phi
$$

### Example 30
Evaluate the integral $\iiint x \mathrm{~d} V$ over the intersection of the unit ball $x^{2}+y^{2}+z^{2} \leqslant 1$ with the half-space $x+y \geqslant 3 \sqrt{2} / 5$.
**Solution.** If we take as an [[Orthonormal Basis]]
$$
\mathbf{e}_{1}=\frac{1}{\sqrt{2}}(1,-1,0), \quad \mathbf{e}_{2}=(0,0,1), \quad \mathbf{e}_{3}=\frac{1}{\sqrt{2}}(1,1,0),
$$
with corresponding co-ordinates $X, Y, Z$ so that
$$
X \mathbf{e}_{1}+Y \mathbf{e}_{2}+Z \mathbf{e}_{3}=x \mathbf{i}+y \mathbf{j}+z \mathbf{k}
$$
then we have $x=(X+Z) / \sqrt{2}$ and $x+y=Z \sqrt{2}$.
So we are left considering the integral
$$
\iiint\left(\frac{X+Z}{\sqrt{2}}\right) \mathrm{d} V
$$
over the region $X^{2}+Y^{2}+Z^{2} \leqslant 1, Z \geqslant 3 / 5$. By symmetry the integral
$$
\iiint X \mathrm{~d} V=0
$$
so we are left to calculate
$$
\begin{aligned}
\frac{1}{\sqrt{2}} \iiint Z \mathrm{~d} V &=\frac{1}{\sqrt{2}} \int_{\phi=0}^{2 \pi} \int_{\theta=0}^{\cos ^{-1}(3 / 5)} \int_{r=(3 / 5) \sec \theta}^{1}(r \cos \theta) r^{2} \sin \theta \mathrm{d} r \mathrm{~d} \theta \mathrm{d} \phi \\
&=\frac{2 \pi}{\sqrt{2}} \int_{\theta=0}^{\cos ^{-1}(3 / 5)} \int_{r=(3 / 5) \sec \theta}^{1} r^{3} \cos \theta \sin \theta \mathrm{d} r \mathrm{~d} \theta \\
&=\pi \sqrt{2} \int_{\theta=0}^{\cos ^{-1}(3 / 5)}\left[\frac{r^{4}}{4}\right]_{(3 / 5) \sec \theta}^{1} \cos \theta \sin \theta \mathrm{d} \theta \\
&=\frac{\pi \sqrt{2}}{4} \int_{\theta=0}^{\cos ^{-1}(3 / 5)}\left(1-\frac{81}{625} \sec ^{4} \theta\right) \cos \theta \sin \theta \mathrm{d} \theta \\
&=\frac{\pi \sqrt{2}}{4} \int_{\theta=0}^{\cos ^{-1}(3 / 5)}\left(\cos \theta \sin \theta-\frac{81}{625} \frac{\sin \theta}{\cos ^{3} \theta}\right) \mathrm{d} \theta \\
&=\frac{\pi \sqrt{2}}{4}\left[-\frac{1}{2} \cos ^{2} \theta-\frac{81}{1250} \frac{1}{\cos ^{2} \theta}\right]_{0}^{\cos ^{-1}(3 / 5)}\\
&=\frac{\pi \sqrt{2}}{4}\left[-\frac{1}{2} \times \frac{9}{25}-\frac{81}{1250} \times \frac{25}{9}+\frac{1}{2}+\frac{81}{1250}\right]\\
&=\frac{\pi \sqrt{2}}{4}\left[\frac{128}{625}\right]=\frac{32 \pi \sqrt{2}}{625} \\
\end{aligned}
$$
### Example 31
By a suitable **rotation** of co-ordinates, or otherwise, evaluate
$$
\iiint(a x+b y+c z)^{4} \mathrm{~d} V
$$
taken over the region $x^{2}+y^{2}+z^{2} \leqslant 1$, where $a, b, c$ are positive constants.
**Solution.** Consider instead this integral as
$$
\iiint((a, b, c) \cdot \mathbf{r})^{4} \mathrm{~d} V
$$
We can rotate the axes to create new coordinates $X, Y, Z$ in such a way that the $Z$ axis points in the direction of vector $(a, b, c)$ and under this change of coordinates the integral becomes
$$
\iiint_{\text {unit ball }}\left(\sqrt{a^{2}+b^{2}+c^{2}} \mathbf{e}_{3} \cdot \mathbf{r}\right)^{4} \mathrm{~d} V=\iiint_{\text {unit ball }}\left(a^{2}+b^{2}+c^{2}\right)^{2} Z^{4} \mathrm{~d} V
$$
where $\mathbf{e}_{3}$ is the unit vector pointing down the $Z$ -axis; notice that we are still integrating over the unit sphere as we have simply rotated the axes about the origin. Now, by a change to [[Spherical Polar Coordinates]],
$$
\begin{aligned}
& \iiint_{\text {unit ball }}\left(a^{2}+b^{2}+c^{2}\right)^{2} Z^{4} \mathrm{~d} V \\
=&\left(a^{2}+b^{2}+c^{2}\right)^{2} \int_{r=0}^{1} \int_{\phi=0}^{2 \pi} \int_{\theta=0}^{\pi}(r \cos \theta)^{4}\left(r^{2} \sin \theta\right) \mathrm{d} \theta \mathrm{d} \phi \mathrm{d} r \\
=& 2 \pi\left(a^{2}+b^{2}+c^{2}\right)^{2}\left[\frac{r^{7}}{7}\right]_{0}^{1}\left[-\frac{\cos ^{5} \theta}{5}\right]_{0}^{\pi} \\
=& 2 \pi\left(a^{2}+b^{2}+c^{2}\right)^{2} \times \frac{1}{7} \times \frac{2}{5} \\
=& \frac{4 \pi}{35}\left(a^{2}+b^{2}+c^{2}\right)^{2}.
\end{aligned}
$$

### Example 32
Let $a, b, c \in \mathbb{R} .$ Determine
$$
I=\iiint_{\text {unit ball }} \cos (a x+b y+c z) \mathrm{d} x \mathrm{~d} y \mathrm{~d} z \text { . }
$$
>Show that your answer is consistent with the volume of the unit sphere being $4 \pi / 3 .$


**Solution.** We can rewrite the integral as
$$
I=\iiint_{\text {unit ball }} \cos (\mathbf{a} \cdot \mathbf{r}) \mathrm{d} x \mathrm{~d} y \mathrm{~d} z
$$
where $\mathbf{a}=(a, b, c)$.
The vector
$$
\mathbf{e}_{3}=\frac{\mathbf{a}}{|\mathbf{a}|}=\frac{(a, b, c)}{\sqrt{a^{2}+b^{2}+c^{2}}}
$$
is of unit length and so we can extend it to an orthonormal basis $\left(\mathbf{e}_{1}, \mathbf{e}_{2}, \mathbf{e}_{3}\right)$, with associated co-ordinates $(X, Y, Z)$. In terms of these co-ordinates
$$
\mathbf{a} \cdot \mathbf{r}=(0,0,|\mathbf{a}|) \cdot(X, Y, Z)=|\mathbf{a}| Z
$$
The unit sphere $x^{2}+y^{2}+z^{2}<1$ is still given as $X^{2}+Y^{2}+Z^{2}<1$ as $\mathbf{e}_{1}, \mathbf{e}_{2}, \mathbf{e}_{3}$ are an orthonormal basis and $\mathrm{d} V=\mathrm{d} X \mathrm{~d} Y \mathrm{~d} Z$. So
$$
I=\iiint_{\text {unit ball }} \cos (|\mathbf{a}| Z) \mathrm{d} X \mathrm{~d} Y \mathrm{~d} Z
$$

If we now change to [[Spherical Polar Coordinates]] $(r, \theta, \phi)$ associated with $(X, Y, Z)$, then
$$
\begin{aligned}
I &=\int_{r=0}^{1} \int_{\theta=0}^{\pi} \int_{\phi=0}^{2 \pi} \cos (|\mathbf{a}| r \cos \theta) r^{2} \sin \theta \mathrm{d} \phi \mathrm{d} \theta \mathrm{d} r \\
&=2 \pi \int_{r=0}^{1} \int_{\theta=0}^{\pi} \cos (|\mathbf{a}| r \cos \theta) r^{2} \sin \theta \mathrm{d} \theta \mathrm{d} r \\
&=2 \pi \int_{r=0}^{1}\left[\frac{-\sin (|\mathbf{a}| r \cos \theta)}{|\mathbf{a}| r} r^{2}\right]_{0}^{\pi} \mathrm{d} r \\
&=2 \pi \int_{r=0}^{1} \frac{r}{|\mathbf{a}|}(2 \sin (|\mathbf{a}| r)) \mathrm{d} r \\
&=\frac{4 \pi}{|\mathbf{a}|}\left\{\left[\frac{-r \cos (|\mathbf{a}| r)}{|\mathbf{a}|}\right]_{r=0}^{1}+\int_{r=0}^{1} \frac{\cos (|\mathbf{a}| r)}{|\mathbf{a}|} \mathrm{d} r\right\} \\
&=\frac{4 \pi}{|\mathbf{a}|}\left[\frac{-r \cos (|\mathbf{a}| r)}{|\mathbf{a}|}+\frac{\sin (|\mathbf{a}| r)}{|\mathbf{a}|^{2}}\right]_{r=0}^{1} \\
&=\frac{4 \pi}{|\mathbf{a}|}\left[\frac{-\cos |\mathbf{a}|}{|\mathbf{a}|}+\frac{\sin (|\mathbf{a}|)}{|\mathbf{a}|^{2}}\right] \\
&=\frac{4 \pi}{|\mathbf{a}|^{3}}(\sin |\mathbf{a}|-|\mathbf{a}| \cos |\mathbf{a}|).
\end{aligned}
$$

We determine the volume of the unit sphere by setting $a=b=c=0$. So letting $|\mathbf{a}| \rightarrow 0$ we see (by [[Taylor Expansion]])
$$
\begin{aligned}
\frac{4 \pi}{|\mathbf{a}|^{3}}(\sin |\mathbf{a}|-|\mathbf{a}| \cos |\mathbf{a}|) &=\frac{4 \pi}{|\mathbf{a}|^{3}}\left(\left(|\mathbf{a}|-\frac{|\mathbf{a}|^{3}}{6}+O\left(|\mathbf{a}|^{5}\right)\right)-|\mathbf{a}|\left(1-\frac{|\mathbf{a}|^{2}}{2}+O\left(|\mathbf{a}|^{4}\right)\right)\right) \\
&=\frac{4 \pi}{|\mathbf{a}|^{3}}\left(\frac{|\mathbf{a}|^{3}}{3}+O\left(|\mathbf{a}|^{4}\right)\right) \\
&=\frac{4 \pi}{3}+O(|\mathbf{a}|) \rightarrow \frac{4 \pi}{3} \text { as }|\mathbf{a}| \rightarrow 0. 
\end{aligned}
$$
