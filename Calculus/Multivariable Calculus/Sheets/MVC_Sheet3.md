# MVC3
#ProblemSheet #MVC 
1. Parameterize the surface of a cone, with base radius $a$ and height $h$, and so express its surface area as a multiple integral. Hence show its [[surface area]] equals
$$
\pi a \sqrt{a^{2}+h^{2}}
$$
Re-evaluate this surface area by considering how a sector of a disc may be folded to make a cone.
>[[Surface Integral]]
2. Show that the [[solid angle]] at the apex of a cone with semiangle $\alpha$ is $2 \pi(1-\cos \alpha)$.
If a sphere has radius $R$ and its centre at distance $D$ from an observer, with $D \gg R$, show that the sphere occupies, as a fraction
$$
\frac{1}{2}\left(1-\frac{\sqrt{D^{2}-R^{2}}}{D}\right) \approx \frac{R^{2}}{4 D^{2}}
$$
of the observer's view.
Use this to explain how the sun (at radius $7 \times 10^{5} \mathrm{~km}$ and distance $\left.1.5 \times 10^{8} \mathrm{~km}\right)$ and moon (at radius $1.8 \times 10^{3} \mathrm{~km}$ and distance $3.8 \times 10^{5} \mathrm{~km}$ ) occupy roughly the same amount of the sky.
3. Evaluate
$$
\iint_{\Sigma} \mathbf{F} \cdot \mathrm{d} \mathbf{S}
$$
where $\mathbf{F}=\left((x-1) x^{2} y,(y-1)^{2} x y, z^{2}-1\right)$ and $\Sigma$ is the surface of the unit cube $[0,1]^{3}$.
4. Two points are chosen at random on the surface of the sphere $\Sigma$ with equation $x^{2}+y^{2}+z^{2}=a^{2}$. Explain why the mean distance $\mu$ between the points equals the integral
$$
\mu=\frac{1}{4 \pi a^{2}} \iint_{\Sigma} \sqrt{x^{2}+y^{2}+(z-a)^{2}} \mathrm{~d} S
$$
and hence determine $\mu$.
5. (i) Calculate the surface integrals $\iint_{\Sigma} f \mathrm{~d} S$ and $\iint_{\Sigma} f \mathrm{~d} \mathbf{S}$ where
$$
f(x, y, z)=\left(x^{2}+y^{2}+z^{2}\right)^{2}
$$
and
$$
\Sigma=\left\{(x, y, z) \in \mathbb{R}^{3}: x^{2}+y^{2}=z^{2}, y \geqslant 0,0 \leqslant z \leqslant 2\right\} \text { . }
$$
(ii) Parametrise the various parts of the boundary $\partial \Sigma$ and determine $\int_{\partial \Sigma} f \mathrm{~d} s$ and $\int_{\partial \Sigma} f \mathrm{~d} \mathbf{r}$.
6. (Optional) A spherical shell $\Sigma$ with equation $x^{2}+y^{2}+z^{2}=1$ has density $\rho(x, y, z) \geqslant 0$. Show that its moment of inertia about an axis through the points $(\pm a, \pm b, \pm c)$ on the shell equals
$$
I(a, b, c)=\iint_{\Sigma}\left(1-(a x+b y+c z)^{2}\right) \rho(x, y, z) \mathrm{d} S
$$
Find this value when $\rho$ is constant. Conversely, if $I(a, b, c)$ is constant for all $(a, b, c) \in \Sigma$, need $\rho(x, y, z)$ be constant?