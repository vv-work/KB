# MVC6
#ProblemSheet #MVC 
>Divergence theorem. Examples. Consequences.
1. Let $C$ be a closed, positively oriented curve in $\mathbb{R}^{2}$ bounding a region $D$. Show that
$$
D=\frac{1}{2} \int_{C} x \mathrm{~d} y-y \mathrm{~d} x .
$$
Hence find the area of the ellipse $x^{2} / a^{2}+y^{2} / b^{2}=1$
2. Let $D \subseteq \mathbb{R}^{2}$ be a closed, boundary region with smooth boundary $\partial D$, and $f$ be a smooth function defined in $D$. By applying [[Green's theorem]] in the plane with suitable functions $P$ and $Q$, show that
$$
\iint_{D} \nabla^{2} f \mathrm{~d} x \mathrm{~d} y=\int_{\partial D} \frac{\partial f}{\partial n} \mathrm{~d} s
$$
3. Let $R$ be the region $1<a<r<b$, where $r$ is the distance from the origin in $\mathbb{R}^{2}$. Find a solution of the [boundary-value problem](Divergence%20Theorem#Applications%20of%20the%20Divergence%20Theorem)
$$
\nabla^{2} f+1=0 \text { in } R, \quad \frac{\partial f}{\partial n}+f=0 \text { on } \partial R
$$
which is a function of $r$ only. Show that this is the only solution, even within the class of not necessarily radial functions.
4. The temperature $T(r, \theta)$ in an annulus $a \leqslant r \leqslant b$ satisfies $\nabla^{2} T=1$ inside the annulus. On the inner boundary $\partial T / \partial n=k$, where $k>0$ and the outer boundary is insulated.
(i) Use Exercise 2 to show the uniqueness, up to a constant, of any solution to this [boundary value problem](Divergence%20Theorem#Applications%20of%20the%20Divergence%20Theorem).
(ii) Find all circularly symmetric solutions $T(r)$ to
$$
\nabla^{2} T=\frac{\mathrm{d}^{2} T}{\mathrm{~d} r^{2}}+\frac{1}{r} \frac{\mathrm{d} T}{\mathrm{~d} r}=1
$$
in the annulus.
(iii) For what value of $k$ is there a circularly symmetric solution to this boundary value problem? Interpret this value physically.
5. Let $R$ be the region $x^{2} / a^{2}+y^{2} / b^{2}+z^{2} / c^{2} \leqslant 1$ with boundary $\partial R$ and $a, b, c>0 .$ Suppose $u(x, y, z)$ satisfies $\nabla^{2} u=-1$ in $R$ and $u=0$ on $\partial R$.
(i) Show that the solution $u$ is [unique](Divergence%20Theorem#Applications%20of%20the%20Divergence%20Theorem).
(ii) Show that the solution $u$ is a quadratic function of $x, y, z$ and evaluate
$$
\iint_{\partial R} \nabla u \cdot \mathrm{d} \mathbf{S}.
$$
6. (Optional) *Differentiation under the integral sign* relates to the theorem that
$$
\frac{\mathrm{d}}{\mathrm{d} t} \int_{I} f(x, t) \mathrm{d} x=\int_{I} \frac{\partial f}{\partial t}(x, t) \mathrm{d} x
$$
which holds, under quite general hypotheses, for a function $f(x, t)$ and an interval $I \subseteq \mathbb{R}$.
(i) By differentiating with respect to $a$, reproduce a solution to [Sheet 1, Exercise 1](MVC_Sheet1).
(ii) Let $a \in \mathbb{R}$. Determine and solve a differential equation involving
$$
I(a)=\int_{-\infty}^{\infty} e^{-x^{2}} \cos 2 a x \mathrm{~d} x
$$
and hence show that $I(a)=\sqrt{\pi} e^{-a^{2}}$.
(iii) A *compressible* fluid of density $\rho(x, t)$ moves with velocity $u(x, t)$ in and out of an interval $I=[\alpha, \beta] .$ Explain why
$$
\frac{\mathrm{d}}{\mathrm{d} t} \int_{\alpha}^{\beta} \rho(x, t) \mathrm{d} t=\rho(\alpha, t) u(\alpha, t)-\rho(\beta, t) u(\beta, t)
$$
interpreting each term physically. Hence derive the continuity equation [(Sheet 5 , Exercise 6)](MVC_Sheet5).