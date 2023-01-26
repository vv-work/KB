## Divergence Theorem
#MostCrucial #MVC 
>Let $R$ be a region of $\mathbb{R}^{3}$ with a piecewise smooth boundary $\partial R$, and let $\mathbf{F}$ be a differentiable vector field on $R$. Then
>$$
\iiint_{R} \operatorname{div} \mathbf{F} \mathrm{d} V=\iint_{\partial R} \mathbf{F} \cdot \mathrm{d} \mathbf{S}
>$$
where [$\mathrm{d} \mathbf{S}$](Surface%20Integral#Definition%20dS) is oriented in the direction of the outward pointing normal from $R$.
#### Definition: Convex
We say that a region $R$ is **convex** if for any $\mathbf{p}, \mathbf{q} \in R$ the line segment connecting $\mathbf{p}$ and $\mathbf{q}$ is contained in $R$.
### Proof
#TODO #NonExaminable
### Corollary 99
 ==[[Divergence Theorem]] for a scalar field.==

Let $\phi$ be a smooth scalar field defined on a region $R \subseteq \mathbb{R}^{3}$ with a piecewise smooth boundary. Then
>$$
\iiint_{R} \nabla \phi \mathrm{d} V=\iint_{\partial R} \phi \mathrm{d} \mathbf{S} .
>$$
#### Proof
Let $\mathrm{c}$ be a constant vector and $\mathbf{F}=\mathbf{c} \phi$. Then
$$
\operatorname{div}(\mathbf{c} \phi)=\mathbf{c} \cdot \nabla \phi+\phi \operatorname{div} \mathbf{c}=\mathbf{c} \cdot \nabla \phi
$$
as $\mathbf{c}$ is constant. By the [[Divergence Theorem]]
$$
\iiint_{R} \mathbf{c} \cdot \nabla \phi \mathrm{d} V=\iint_{\partial R} \mathbf{c} \phi \cdot \mathrm{d} \mathbf{S}, \Longrightarrow \mathbf{c} \cdot\left(\iiint_{R} \nabla \phi \mathrm{d} V\right)=\mathbf{c} \cdot\left(\iint_{\partial R} \phi \mathrm{d} \mathbf{S}\right)
$$
As $\mathbf{c}$ is an arbitrary vector then
$$
\iiint_{R} \nabla \phi \mathrm{d} V=\iint_{\partial R} \phi \mathrm{d} \mathbf{S} .
$$

### Example 101
>Verify the Divergence Theorem when $R$ is the finite region bounded by the paraboloid $z=x^{2}+y^{2}$ and the plane $x+y+z=1$, and $\mathbf{F}=(x, y, z)$.

#### Solution
We already met this region in [[Volume Integral#Example 22]]. We showed that the top surface of $R$ projects vertically down to the set
$$
W=\left\{(x, y) \in \mathbb{R}^{2}:(x+1 / 2)^{2}+(y+1 / 2)^{2} \leqslant 3 / 2\right\}
$$
which is a disc, centre $(-1 / 2,-1 / 2)$ and radius $\sqrt{3 / 2}$. Further we calculated the volume of the region to be $9 \pi / 8$. As $\operatorname{div} \mathbf{F}=3$ then
$$
\iiint_{R} \operatorname{div} F \mathrm{~d} V=3 \operatorname{Vol}(R)=\frac{27 \pi}{8} .
$$
The boundary $\partial R$ is made up of two surfaces
$$
\begin{array}{l}
\Sigma_{1}=\left\{(x, y, z): z \geqslant x^{2}+y^{2}, x+y+z=1\right\}=\{(x, y, z):(x, y) \in W, x+y+z=1\} \\
\Sigma_{2}=\left\{(x, y, z): z=x^{2}+y^{2}, x+y+z \leqslant 1\right\}=\left\{(x, y, z):(x, y) \in W, z=x^{2}+y^{2}\right\}
\end{array}
$$
We can parameterize $\Sigma_{1}$ and $\Sigma_{2}$ as
$$
\mathbf{r}_{1}(u, v)=(u, v, 1-u-v) ; \quad \mathbf{r}_{2}(u, v)=\left(u, v, u^{2}+v^{2}\right)
$$
Note
$$
\left(\mathbf{r}_{1}\right)_{u} \wedge\left(\mathbf{r}_{1}\right)_{v}=\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 0 & -1 \\
0 & 1 & -1
\end{array}\right|=(1,1,1)
$$
which is outward-pointing from $R$, and
$$
\left(\mathbf{r}_{2}\right)_{u} \wedge\left(\mathbf{r}_{2}\right)_{v}=\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
1 & 0 & 2 u \\
0 & 1 & 2 v
\end{array}\right|=(-2 u,-2 v, 1)
$$
which is inward-pointing and so we will take its negative. So
$$
\iint_{\Sigma_{1}} \mathbf{F} \cdot \mathrm{d} \mathbf{S}=\iint_{W}(u, v, 1-u-v) \cdot(1,1,1) \mathrm{d} u \mathrm{~d} v=\iint_{W} \mathrm{~d} u \mathrm{~d} v=\pi(\sqrt{3 / 2})^{2}=3 \pi / 2 .
$$
For the second surface
$$
\begin{aligned}
\iint_{\Sigma_{2}} \mathbf{F} \cdot \mathrm{d} \mathbf{S} &=\iint_{W}\left(u, v, u^{2}+v^{2}\right) \cdot(2 u, 2 v,-1) \mathrm{d} A \\
&=\iint_{W}\left(u^{2}+v^{2}\right) \mathrm{d} A \\
&=\int_{r=0}^{\sqrt{3} / 2} \int_{\theta=0}^{2 \pi}\left\{(-1 / 2+r \cos \theta)^{2}+(-1 / 2+r \sin \theta)^{2}\right\} r \mathrm{~d} \theta \mathrm{d} r \\
&=\int_{r=0}^{\sqrt{3} / 2} \int_{\theta=0}^{2 \pi}\left\{r^{2}-r \cos \theta-r \sin \theta+1 / 2\right\} r \mathrm{~d} \theta \mathrm{d} r \\
&=2 \pi \int_{r=0}^{\sqrt{3} / 2}\left\{r^{3}+\frac{r}{2}\right\} \mathrm{d} \theta \mathrm{d} r \\
&=2 \pi\left[\frac{r^{4}}{4}+\frac{r^{2}}{4}\right]_{0}^{\sqrt{3 / 2}} \\
&=2 \pi(9 / 16+3 / 8)=\frac{15 \pi}{8}
\end{aligned}
$$
Hence, in total, we have
$$
\iint_{\partial R} \mathbf{F} \cdot \mathrm{d} \mathbf{S}=\frac{3 \pi}{2}+\frac{15 \pi}{8}=\frac{12 \pi}{8}+\frac{15 \pi}{8}=\frac{27 \pi}{8}.
$$

### Example 102
The twice continuously differentiable function $f(x, y, z)$ is homogeneous of degree $n$, so that
$$
f(t x, t y, t z)=t^{n} f(x, y, z) \quad \text { for all } t \in \mathbb{R}
$$
Prove [[Euler's Theorem]], which states that
$$
\mathbf{r} \cdot \nabla f=n f \text { . }
$$
Let $B$ be the unit ball $x^{2}+y^{2}+z^{2}<1$ and let $\partial B$ be its boundary. Show that
$$
\iiint_{B} f \mathrm{~d} V=\frac{1}{n(n+3)} \iiint_{B} \nabla^{2} f \mathrm{~d} V
$$
and hence show that
$$
\iiint_{B}(x-y+z)^{4} \mathrm{~d} V=\frac{36 \pi}{35}.
$$

#### Solution
If we differentiate the identity (6.4) with respect to $t$ then we find
$$
x \frac{\partial f}{\partial x}(t x, t y, t z)+y \frac{\partial f}{\partial y}(t x, t y, t z)+z \frac{\partial f}{\partial z}(t x, t y, t z)=n t^{n-1} f(x, y, z)
$$
If we set $t=1$ then we arrive at Euler's Theorem $\mathbf{r} \cdot \nabla f=n f$. By the [[Divergence Theorem]], with $B$ as the unit ball, and $\partial B$ its boundary, then
$$
\iiint_{B} \nabla^{2} f \mathrm{~d} V=\iiint_{B} \nabla \cdot \nabla f \mathrm{~d} V=\iint_{\partial B} \nabla f \cdot \mathbf{n} \mathrm{d} S=\iint_{\partial B} \nabla f \cdot \mathbf{r} \mathrm{d} S=n \iint_{\partial B} f \mathrm{~d} S
$$
as $\mathbf{n}=\mathbf{r}$ on $\partial B$. On the other hand
$$
\nabla \cdot(f \mathbf{r})=(\nabla f) \cdot \mathbf{r}+f(\nabla \cdot \mathbf{r})=n f+3 f=(n+3) f .
$$
and so, by the [[Divergence Theorem]] again,
$$
(n+3) \iiint_{B} f \mathrm{~d} V=\iiint_{B} \nabla \cdot(f \mathbf{r}) \mathrm{d} V=\iint_{\partial B} f \mathbf{r} \cdot \mathbf{n} \mathrm{d} S=\iint_{\partial B} f \mathrm{~d} S
$$
as $\partial B$ is the unit sphere. Hence
$$
\iiint_{B} f \mathrm{~d} V=\frac{1}{n(n+3)} \iiint_{B} \nabla^{2} f \mathrm{~d} V.
$$

The function $(x-y+z)^{4}$ is homogeneous of degree 4 in $x, y, z$ and so that
$$
\begin{aligned}
& \iiint_{B}(x-y+z)^{4} \mathrm{~d} V \\
=& \frac{1}{4 \times 7} \iiint_{B} \nabla^{2}(x-y+z)^{4} \mathrm{~d} V
\end{aligned}
$$
[which is again homogeneous]
$$
\begin{array}{l}
=\frac{1}{4 \times 7} \iiint_{B} 36(x-y+z)^{2} \mathrm{~d} V \\
=\frac{36}{4 \times 7} \times \frac{1}{2 \times 5} \iiint_{B} \nabla^{2}(x-y+z)^{2} \mathrm{~d} V \\
=\frac{36}{4 \times 7} \times \frac{1}{2 \times 5} \iiint_{B} 6 \mathrm{~d} V \\
=\frac{36}{4 \times 7} \times \frac{6}{2 \times 5} \times \frac{4 \pi}{3} \\
=\frac{36 \pi}{35}
\end{array}
$$
## Applications of the Divergence Theorem
### Uniqueness of the [[Dirichlet Problem]]
Let $R \subseteq \mathbb{R}^{3}$ be a path-connected region with piecewise smooth boundary $\partial R$ and let $f$ be a continuous function defined on $\partial R$. Suppose that $\phi_{1}$ and $\phi_{2}$ are such that
$$
\begin{array}{r}
\nabla^{2} \phi_{1}=0=\nabla^{2} \phi_{2} \text { in } R ; \\
\phi_{1}=f=\phi_{2} \text { on } \partial R
\end{array}
$$
#### Proof
Let $\psi=\phi_{1}-\phi_{2}$, so that
$$
\nabla^{2} \psi=0 \text { in } R, \quad \psi=0 \text { on } \partial R
$$
If we consider the function $\psi^{2}$ then, by the [[Divergence Theorem]] and as $\nabla^{2}=\nabla \cdot \nabla$,
$$
\iint_{\partial R} \nabla\left(\psi^{2}\right) \cdot \mathrm{d} \mathbf{S}=\iiint_{R} \nabla^{2}\left(\psi^{2}\right) \mathrm{d} V
$$
Looking at the LHS,
$$
\iint_{\partial R} \nabla\left(\psi^{2}\right) \cdot \mathrm{d} \mathbf{S}=\iint_{\partial R} 2 \psi \nabla \psi \cdot \mathrm{d} \mathbf{S}=0 \quad \text { as } \psi=0 \text { on } \partial R
$$
On the RHS we have
$$
\nabla^{2}\left(\psi^{2}\right)=2 \psi \nabla^{2} \psi+2 \nabla \psi \cdot \nabla \psi=2|\nabla \psi|^{2} \quad \text { as } \nabla^{2} \psi=0 \text { in } R
$$
Hence
$$
\iiint_{R} 2|\nabla \psi|^{2} \mathrm{~d} V=0 \Longrightarrow \nabla \psi=\mathbf{0} \text { in } R
$$
As $\nabla \psi=\mathbf{0}$ in $R$ and $R$ is path-connected then $\psi$ is constant throughout $R$. But $\psi=0$ on $\partial R$ and so by continuity $\psi=0$ throughout $R$.

### Uniqueness, up to a constant, of the [[Neumann Problem]]
Let $R \subseteq \mathbb{R}^{3}$ be a path-connected region with piecewise smooth boundary $\partial R$ and let $f$ be a continuous function defined on $\partial R$. Suppose that $\phi_{1}$ and $\phi_{2}$ are such that
$$
\begin{aligned}
\nabla^{2} \phi_{1} &=0=\nabla^{2} \phi_{2} \text { in } R \\
\frac{\partial \phi_{1}}{\partial n} &=f=\frac{\partial \phi_{2}}{\partial n} \text { on } \partial R
\end{aligned}
$$
Then $\phi_{1}-\phi_{2}$ is constant in $R$.
Proof. Let $\psi=\phi_{1}-\phi_{2}$, so that
$$
\nabla^{2} \psi=0 \text { in } R, \quad \frac{\partial \psi}{\partial n}=\nabla \psi \cdot \mathbf{n}=0 \text { on } \partial R
$$
If we **consider the function $\bf\psi^{2}$**, then by the [[Divergence Theorem]] and as $\nabla^{2}=\nabla \cdot \nabla$,
$$
\iint_{\partial R} \nabla\left(\psi^{2}\right) \cdot \mathrm{d} \mathbf{S}=\iiint_{R} \nabla^{2}\left(\psi^{2}\right) \mathrm{d} V
$$
Looking at the LHS,
$$
\iint_{\partial R} \nabla\left(\psi^{2}\right) \cdot \mathrm{d} \mathbf{S}=\iint_{\partial R} 2 \psi \nabla \psi \cdot \mathbf{n} \mathrm{d} S=0 \quad \text { as } \nabla \psi \cdot \mathbf{n}=0 \text { on } \partial R .
$$
On the RHS we have
$$
\nabla^{2}\left(\psi^{2}\right)=2 \psi \nabla^{2} \psi+2 \nabla \psi \cdot \nabla \psi=2|\nabla \psi|^{2} \quad \text { as } \nabla^{2} \psi=0 \text { in } R
$$
Hence
$$
\iiint_{R} 2|\nabla \psi|^{2} \mathrm{~d} V=0 \Longrightarrow \nabla \psi=\mathbf{0} \text { in } R
$$
As $\nabla \psi=0$ in $R$ then $\psi$ is constant throughout $R$.

### Robin (or Mixed) Boundary Problem
[[Robin Boundary Problem]]
Let $R \subseteq \mathbb{R}^{3}$ be a path-connected region with piecewise smooth boundary $\partial R$ and let $f$ be a continuous function defined on $\partial R$. Further let $\beta$ be a real constant. Suppose that $\phi_{1}$ and $\phi_{2}$ are such that
$$
\begin{aligned}
\nabla^{2} \phi_{1} &=0=\nabla^{2} \phi_{2} \quad \text { in } R \\
\beta \phi_{1}+\frac{\partial \phi_{1}}{\partial n} &=f=\beta \phi_{2}+\frac{\partial \phi_{2}}{\partial n} \text { on } \partial R .
\end{aligned}
$$
1) If $\beta>0$ then $\phi_{1}=\phi_{2}$ in $R$.
2) If $\beta=0$ then $\phi_{1}-\phi_{2}$ is constant in $R$.
3) If $\beta<0$ then the solution need not be unique, even up to a constant.
#### Proof
Let $\psi=\phi_{1}-\phi_{2}$, so that
$$
\nabla^{2} \psi=0 \text { in } R, \quad \beta \psi+\frac{\partial \psi}{\partial n}=\beta \psi+\nabla \psi \cdot \mathbf{n}=0 \text { on } \partial R
$$
If we consider the function $\psi^{2}$ then, by the Divergence Theorem and as $\nabla^{2}=\nabla \cdot \nabla$,
$$
\iint_{\partial R} \nabla\left(\psi^{2}\right) \cdot \mathrm{d} \mathbf{S}=\iiint_{R} \nabla^{2}\left(\psi^{2}\right) \mathrm{d} V
$$
Looking at the LHS and noting $\beta \psi+\nabla \psi \cdot \mathbf{n}=0$ on $\partial R$ we have
$$
\iint_{\partial R} \nabla\left(\psi^{2}\right) \cdot \mathrm{d} \mathbf{S}=\iint_{\partial R} 2 \psi(\nabla \psi \cdot \mathbf{n}) \mathrm{d} S=\iint_{\partial R} 2 \psi(-\beta \psi) \mathrm{d} S=-2 \beta \iint_{\partial R} \psi^{2} \mathrm{~d} S
$$
On the RHS we have as before
$$
\nabla^{2}\left(\psi^{2}\right)=2 \psi \nabla^{2} \psi+2 \nabla \psi \cdot \nabla \psi=2|\nabla \psi|^{2} \quad \text { as } \nabla^{2} \psi=0 \text { in } R
$$
Hence
$$
-2 \beta \iint_{\partial R} \psi^{2} \mathrm{~d} S=\iiint_{R} 2|\nabla \psi|^{2} \mathrm{~d} V
$$
If $\beta>0$ then the LHS is non-positive and the RHS is non-negative $-$ consequently both are zero and $\nabla \psi=\mathbf{0}$ in $R$ and $\psi=0$ on $\partial R$. Hence $\psi=0$ throughout $R$. If $\beta=0$ then the [[Robin Boundary Problem]] is just the [[Neumann Problem]], with which we have already dealt. 
> The following example shows that solutions need not be unique if $\beta<0 .$

### Example 106
>$ Let $R$ be the interior of the cylinder $x^{2}+y^{2}=1$. Find two solutions to the [[Robin Boundary Problem]]
>$$
\nabla^{2} \psi=0 \text { in } R, \quad \psi=\frac{\partial \psi}{\partial n} \text { on } \partial R.
>$$
#### Solution
[[Laplace's equation]] in [[Cylindrical Polar Coordinates]] reads
$$
\nabla^{2} \psi=\frac{1}{r} \frac{\partial}{\partial r}\left(r \frac{\partial \psi}{\partial r}\right)+\frac{1}{r^{2}} \frac{\partial^{2} \psi}{\partial \theta^{2}}+\frac{\partial^{2} \psi}{\partial z^{2}}=0
$$
We know for $\psi=r^{n} \sin n \theta$, where $n$ is a non-negative integer, that $\nabla^{2} \psi=0$ and on the boundary $r=1$ we have
$$
\frac{\partial \psi}{\partial n}=\frac{\partial \psi}{\partial r}=n r^{n-1} \sin n \theta=n \sin n \theta ; \quad \psi=\sin n \theta
$$
Hence when $n=1$, we see $r \sin \theta$ satisfies the given boundary problem. Other solutions are 0 , $r \cos \theta$ and $r \sin (\theta-\alpha)$ for arbitrary $\alpha$ so we see this solution is far from unique.

### Derivation of balance equations in 3D: the heat equation
> we use the [[Divergence Theorem]] to rederive the [[heat equation]], but now in 3D.

#### Lemma 107
>If $\phi: \mathbb{R}^{3} \rightarrow \mathbb{R}$ is a continuous scalar field such that
>$$
\iiint_{R} \phi \mathrm{d} V=0
>$$
for all bounded subsets $R$, then $\phi \equiv 0$.
##### Proof
Suppose, for a contradiction that $\phi(\mathbf{p}) \neq 0$ for some point $p$. Without any loss of generality let's suppose $\phi(\mathbf{p})>0$. Let $\varepsilon=\frac{1}{2} \phi(\mathbf{p})>0$. Then, by the continuity of $\phi$ at $\mathbf{p}$, there exists $\delta>0$ such that
$$
|\phi(\mathbf{x})-\phi(\mathbf{p})|<\varepsilon \quad \text { when } \quad|\mathbf{x}-\mathbf{p}|<\delta
$$
In particular, $\phi(\mathbf{x})>\frac{1}{2} \phi(\mathbf{p})$ on all of $B(\mathbf{p}, \delta)=\left\{\mathbf{x} \in \mathbb{R}^{3}:|\mathbf{x}-\mathbf{p}|<\delta\right\}$ and so
$$
\iiint_{B(\mathbf{p}, \delta)} \phi \mathrm{d} V>\frac{1}{2} \phi(\mathbf{p}) \times \operatorname{Vol}(B(\mathbf{p}, \delta))>0
$$
which is a contradiction.
#### Theorem 108
>Let $T(\mathbf{x}, t)$ denote the temperature at position $\mathbf{x}$ and at time $t$ in an isotropic medium $R$ with thermal conductivity $k$, density $\rho$, specific heat $c$ with heat flow determined by Fourier's Law which states that
>$$
\mathbf{q}=-k \nabla T
>$$
where $\mathbf{q}$ is the heat **flux**. Then T satisfies the [[heat equation]]
>$$
\frac{\partial T}{\partial t}=\frac{k}{\rho c} \nabla^{2} T .
>$$
##### Proof
Let $S \subseteq R$ be an arbitrary subset of $R$. The total heat energy in $S$ equals
$$
\iiint_{S} \rho c T \mathrm{~d} V.
$$
The amount of heat flowing out of $S$ is given by the flux integral
$$
\iint_{\partial S} \mathbf{q} \cdot \mathrm{d} \mathbf{S}.
$$

So if no heat is generated within $S$ then the only heat loss or gain is via the boundary $\partial S$. Hence we have
$$
\frac{\mathrm{d}}{\mathrm{d} t} \iiint_{S} \rho c T \mathrm{~d} V=-\iint_{\partial S} \mathbf{q} \cdot \mathrm{d} \mathbf{S}
$$
$$
=\iint_{\partial S} k \nabla T \cdot \mathrm{d} \mathbf{S}
$$
==by [[Fourier's Law]]==
$$
\begin{aligned}
&=\iiint_{S} \nabla \cdot(k \nabla T) \mathrm{d} V \\
&=\iiint_{S} k \nabla^{2} T \mathrm{~d} V
\end{aligned}
$$
==by the [[Divergence Theorem]]==
So
$$
\begin{aligned}
& \iiint_{S} \rho c \frac{\partial T}{\partial t} \mathrm{~d} V=\iiint_{S} k \nabla^{2} T \mathrm{~d} V, \\
\Longrightarrow & \iiint_{S}\left(\rho c \frac{\partial T}{\partial t}-k \nabla^{2} T\right) \mathrm{d} V=0 .
\end{aligned}
$$
As this is true for an arbitrary subset $S$ of $R$ then it follows, from [[#Lemma 107]] , that
$$
\rho c \frac{\partial T}{\partial t}-k \nabla^{2} T=0 \quad \text { throughout } R \text { . }
$$

[[MVC_Sheet5]]
[[MVC_Sheet6]]