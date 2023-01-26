# MVC5
#ProblemSheet #MVC 
>Green’s theorems. Divergence theorem.
1. (i) Let $\mathbf{F}(x, y, z)=\left(3 x^{2} y^{2} z, 2 x^{3} y z, x^{3} y^{2}\right)$. Show that $\nabla \wedge \mathbf{F}=\mathbf{0}$ and find a potential $\phi$ such that $\mathbf{F}=\nabla \phi$. To what extent is $\phi$ unique?
Verify by direct calculation that
$$
\int_{C} \mathbf{F} \cdot \mathrm{d} \mathbf{r}=\phi(\mathbf{q})-\phi(\mathbf{p})
$$
where $\mathbf{p}=(0,0,0), \mathbf{q}=(1,1,1)$ and $C$ is the twisted cubic $\mathbf{r}(t)=\left(t, t^{2}, t^{3}\right)$ with $0 \leqslant t \leqslant 1$.
(ii) Let $\mathbf{F}(x, y, z)=(0, x y-1, y-x z)$. Show that $\nabla \cdot \mathbf{F}=0$ and that $\mathbf{f}(x, y, z)=(x y z, x y, x)$ is
vector potential - that is $\mathbf{F}=\nabla \wedge \mathbf{f}$. To what extent is $\mathbf{f}$ unique?
2. Use [[Green's theorem]] to find the simple closed curve $C$ in the $x y$ -plane that maximises the integral
$$
\int_{C} y^{3} \mathrm{~d} x+\left(3 x-x^{3}\right) \mathrm{d} y
$$
and determine this maximum.
3. Let $R$ be a closed bounded region, bounded by a closed surface $\partial R$. Let $\phi, \psi$ be smooth scalar fields on $R$. Use the [[divergence theorem]] to prove:
(i) Green's First Theorem:
$$
\iiint_{R}\left(\psi \nabla^{2} \phi+\nabla \phi \cdot \nabla \psi\right) \mathrm{d} R=\iint_{\partial R} \psi \nabla \phi \cdot \mathrm{d} \mathbf{S}
$$
(ii) Green's Second Theorem:
$$
\iiint_{R}\left(\psi \nabla^{2} \phi-\phi \nabla^{2} \psi\right) \mathrm{d} R=\iint_{\partial R}(\psi \nabla \phi-\phi \nabla \psi) \cdot \mathrm{d} \mathbf{S} .
$$

4. Verify the [[divergence theorem]] where $\mathbf{F}(x, y, z)=(y, x y,-z)$, and $R$ is the region enclosed below the plane $z=4$, and the paraboloid $z=x^{2}+y^{2}$.
5. Let $f$ be a smooth scalar field defined on a region $R \subseteq \mathbb{R}^{3}$ with a smooth boundary $\partial R$. Show that
$$
\iint_{\partial R} f \mathbf{r} \wedge \mathrm{d} \mathbf{S}=\iiint_{R} \mathbf{r} \wedge \nabla f \mathrm{~d} V
$$
6. (Optional) A one-dimensional blob of compressible fluid starts at $t=0$ with uniform density $\rho=1$ in the interval $1 \leqslant x \leqslant 2$ and moves with velocity given by
$$
u(x, t)=2 x^{2} t
$$
(i) Find the position $x(t)$ at time $t$ of a fluid particle that starts at $x(0)=a$ where $1 \leqslant a \leqslant 2$.
(ii) Hence show that the density of the fluid is given by
$$
\rho(x, t)=\frac{1}{\left(1+x t^{2}\right)^{2}}
$$
(iii) Verify that $\rho(x, t)$ satisfies the continuity equation
$$
\frac{\partial \rho}{\partial t}+\frac{\partial(\rho u)}{\partial x}=0
$$
(iv) Use the continuity equation to find a condition on $u(x, t)$ for a fluid to be incompressible.

### Solutions

#### (6)
(iv) When a fluid with velocity $u(x,t)$ is incompressible, $\nabla\cdot u = 0$.