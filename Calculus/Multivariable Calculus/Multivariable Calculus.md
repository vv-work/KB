# Multivariable Calculus
#Subject 
# 1 Multiple Integrals in 2D
## 1.1 Preliminaries
### Definition 1: Scalar Field
By a [[scalar field]] $\phi$ on $\mathbb{R}^{3}$ we shall mean a map $\phi: \mathbb{R}^{3} \rightarrow \mathbb{R}$.

### Definition 2: Vector Field
By a [[vector field]] $\mathbf{F}$ on $\mathbb{R}^{3}$ we shall mean a map $\mathbf{F}: \mathbb{R}^{3} \rightarrow \mathbb{R}^{3}$.

>We will typically assume that scalar and vector fields are **smooth** $-$ their partial derivatives **exist** with respect to $x, y$ and $z$ to all orders $-$ for brevity, this will not always be stated.

>Occasionally we may consider more general scalar fields $\phi: \mathbb{R}^{n} \rightarrow \mathbb{R}$ and vector fields $\mathbf{F}: \mathbb{R}^{n} \rightarrow \mathbb{R}^{m}$.

We shall also consider scalar and vector fields defined on proper subsets of $\mathbb{R}^{3}$ (or more generally $\left.\mathbb{R}^{n}\right)$. The domains of these fields will usually be open, so we can define their partial derivatives.
### Definition 4

A set $U \subseteq \mathbb{R}^{n}$ is said to be ***open*** if for every $\mathbf{x} \in U$ there exists $\varepsilon>0$ such that
$$
B(\mathbf{x}, \varepsilon)=\left\{\mathbf{y} \in \mathbb{R}^{n}:|\mathbf{y}-\mathbf{x}|<\varepsilon\right\} \subseteq U
$$
and where
$$
|\mathbf{y}-\mathbf{x}|^{2}=\sum_{i=1}^{n}\left|y_{i}-x_{i}\right|^{2}
$$
We refer to $B(\mathbf{x}, \varepsilon)$ as the ***open ball*** of radius $r$, centred at $\mathbf{x}$.

### Integral in One Dimension
An informal definition of the integral
$$
\int_{a}^{b} f(x) \mathrm{d} x
$$
is as follows: 
Suppose $f:[a, b] \rightarrow \mathbb{R}$ is a function. Subdivide $[a, b]$ into $m$ sub-intervals of equal length $\delta x$ and let $x_{1}, \ldots, x_{m}$ be points in the respective intervals. On partitioning with smaller and smaller intervals by taking the limit $\delta x \rightarrow 0$, we have
$$
\int_{a}^{b} f(x) \mathrm{d} x=\lim _{\delta x \rightarrow 0} \sum_{r=1}^{m} f\left(x_{r}\right) \delta x
$$
provided the limit exists. This will always be the case if $f$ is continuous (also, alternative subdivisions will not change the limit when $f$ is continuous). $A$ rigorous treatment of the Riemann integral will be given next term in Analysis III.

## 1.2 Multiple Integrals in Two Dimensions: A Brief Introduction
#TODO 
### Remark 8
Given a continuous, bounded function $f(x, y)$ on a rectangular domain $\left(a_{1}, b_{1}\right) \times$ $\left(a_{2}, b_{2}\right)$ then it is the case that
$$
\int_{x=a_{1}}^{x=b_{1}} \int_{y=a_{2}}^{y=b_{2}} f(x, y) \mathrm{d} y \mathrm{~d} x=\int_{y=a_{2}}^{y=b_{2}} \int_{x=a_{1}}^{x=b_{1}} f(x, y) \mathrm{d} x \mathrm{~d} y
$$
but this need not be the case if the integrand is continuous, but unbounded (Sheet 1, Exercise
2). However if either of the integrals
$$
\int_{x=a_{1}}^{x=b_{1}} \int_{y=a_{2}}^{y=b_{2}}|f(x, y)| \mathrm{d} y \mathrm{~d} x \quad \text { or } \quad \int_{y=a_{2}}^{y=b_{2}} \int_{x=a_{1}}^{x=b_{1}}|f(x, y)| \mathrm{d} x \mathrm{~d} y
$$
exist, then we do have equality of the integrals in (1.1). This is a consequence of Tonelli's and [Fubini's](Fubini's%20Theorem) theorems.

## 1.3 Change of Variables and Jacobians
### [[Moment of Inertia]]
Given a plate occupying a region $R$ of the plane, with density $\rho(x, y)$ per unit area, then the [[Moment of Inertia]] of the plate about an axis vertically through a point $\left(x_{0}, y_{0}\right)$ equals
$$
\iint_{R} \rho(x, y)\left(\left(x-x_{0}\right)^{2}+\left(y-y_{0}\right)^{2}\right) \mathrm{d} A.
$$
### [[Jacobian]]
### [[Change of Variables]]
>[[MVC_Sheet1]]
# 2 Volume Integrals
## 2.1&2.2 Volume Integrals
### [[Volume Integral]]
## 2.3 Changing Coordinates in Volume Integrals
### [[Change of Coordinates]]
[[Change of Coordinates]]
> 
An #important kind of changing coordinate: ***change to orthonormal basis & rotating the axes.***  
**See** 
> - [[Change of Coordinates#Example 30]]
> - [[Change of Coordinates#Example 31]]
> - [[Change of Coordinates#Example 32]]
### [[Centre of Mass#Definition MVC]]
### [[Median]]
>[[MVC_Sheet2]]
# 3 Surface Integrals
## 3.1 Parameterized Surfaces
[[Surface]]
## 3.2 Surface Integrals
[[Surface Area]]
### Surface Integral
If $\mathbf{F}$ and $\phi$ are a *vector field* and *scalar field* defined on a parameterized [[surface]] $\Sigma=\mathbf{r}(U)$, then we may define the following [surface integrals](Surface%20Integral.md):
$$
\begin{aligned}
\iint_{\Sigma} \mathbf{F} \cdot \mathrm{d} \mathbf{S} &=\iint_{U} \mathbf{F}(\mathbf{r}(u, v)) \cdot\left(\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right) \mathrm{d} u \mathrm{~d} v \\
\iint_{\Sigma} \mathbf{F} \mathrm{d} S &=\iint_{U} \mathbf{F}(\mathbf{r}(u, v))\left|\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right| \mathrm{d} u \mathrm{~d} v \\
\iint_{\Sigma} \phi \mathrm{d} \mathbf{S} &=\iint_{U} \phi(\mathbf{r}(u, v))\left(\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right) \mathrm{d} u \mathrm{~d} v \\
\iint_{\Sigma} \phi \mathrm{d} S &=\iint_{U} \phi(\mathbf{r}(u, v))\left|\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right| \mathrm{d} u \mathrm{~d} v .
\end{aligned}
$$

### Solid Angle
If $\Sigma^{*}$ is a [[surface]] and $\Sigma$ is the subset of $\Sigma^{*}$ facing the unit sphere, then the [[solid angle]] $\Omega$ subtended at $O$ by $\Sigma^{*}$ equals, by definition,
$$
\Omega=\iint_{\Sigma} \frac{\mathbf{e}_{r} \cdot \mathrm{d} \mathbf{S}}{r^{2}}=\iint_{\Sigma} \frac{\mathbf{r} \cdot \mathrm{d} \mathbf{S}}{r^{3}}.
$$
>[[MVC_Sheet3]]
# 4 Line Integrals & Conservative Fields
## 4.1 Curves
### Curve
By a **curve** we shall mean a **piecewise smooth** function $\gamma: I \rightarrow \mathbb{R}^{3}$ defined on an interval $I$ of $\mathbb{R}$. Notice that order on $I$ also gives the curve $\gamma$ an **orientation**.
## 4.2 Line Integrals
### [[Line Integral]]
Let $C$ be a [[curve]] in $\mathbb{R}^{3}$, parameterized by $\gamma:[a, b] \rightarrow \mathbb{R}^{3}$ and let $\mathbf{F}$ be a vector field, whose domain includes $C .$ We define the $\color{orange}\textbf{line integral }\mathbf{F}\textit{ along }\mathit{C}$ as
$$
\color{yellow}
\int_{C} \mathbf{F} \cdot \mathrm{d} \mathbf{r}=\int_{a}^{b} \mathbf{F}(\mathbf{r}(t)) \cdot \mathbf{r}^{\prime}(t) \mathrm{d} t .
$$
> Also see [[#Definition 57]]
### Arc length
If $C$ is a curve with parameterization $\gamma:[a, b] \rightarrow \mathbb{R}^{3}$ then the [[arc length]] of the curve is
$$
\int_{C} \mathrm{~d} s=\int_{a}^{b}\left|\gamma^{\prime}(t)\right| \mathrm{d} t.
$$
## 4.3 Conservative Fields
### Conservative
Let $S$ be an open subset of $\mathbb{R}^{3} .$ A vector field $\mathbf{F}: S \rightarrow \mathbb{R}^{3}$ is said to be [[conservative]] if there exists a scalar field $\phi: S \rightarrow \mathbb{R}$ such that $\mathbf{F}=\nabla \phi$.
### Potential
 If $\mathbf{F}=\nabla \phi$ then $\phi$ is said to be a [[potential]] (or scalar potential) for $\mathbf{F}$.
# 5 Div, Grad, Curl
## 5.1 Definitions
 [[Gradient]]
 [[Divergence]]
 [[Curl]]
## 5.2 Identities
[[Div Grad Curl]]
## 5.3 Physical Interpretations
>[[MVC_Sheet4]]

#TODO 
# 6 Divergence Theorem & Stokes' Theorem
##  6.1 The [[Divergence Theorem]]
Let $R$ be a region of $\mathbb{R}^{3}$ with a piecewise smooth boundary $\partial R$, and let $\mathbf{F}$ be a differentiable vector field on $R$. Then
$$
\iiint_{R} \operatorname{div} \mathbf{F} \mathrm{d} V=\iint_{\partial R} \mathbf{F} \cdot \mathrm{d} \mathbf{S}
$$
where [$\mathrm{d} \mathbf{S}$](Surface%20Integral#Definition%20dS) is oriented in the direction of the outward pointing normal from $R$.
### [[Green's Theorem]] in the Plane
Let $D$ be a closed bounded region in the $(x, y)$ plane, whose boundary $C$ is a piecewise smooth simple closed curve, and that $p(x, y), q(x, y)$ have continuous first-order derivatives in $D .$ Then
$$
\iint_{D}\left(\frac{\partial p}{\partial x}+\frac{\partial q}{\partial y}\right) \mathrm{d} x \mathrm{~d} y=\int_{C}(p, q) \cdot \mathbf{n} \mathrm{d} s=\int_{C} p \mathrm{~d} y-q \mathrm{~d} x
$$
where $\mathbf{n}$ is the outward pointing unit normal to $C$ in the $(x, y)$ plane. 
>[[MVC_Sheet5]]
[[MVC_Sheet6]]
## 6.3 [[Stokes' Theorem]]
Let $\Sigma$ be a smooth oriented [[surface]] in $\mathbb{R}^{3}$ whose boundary is the [[curve]] $\partial \Sigma .$ Let $\mathbf{F}$ be a smooth vector field defined on $\Sigma \cup \partial \Sigma$. Then
$$
\int_{\partial \Sigma} \mathbf{F} \cdot \mathrm{d} \mathbf{r}=\iint_{\Sigma} \operatorname{curl} \mathbf{F} \cdot \mathrm{d} \mathbf{S}.
$$
>[[MVC_Sheet7]]
# 7 Gauss' Flux Theorem, Poisson's Equation and Gravity
### Poisson's Equation
Let $\phi$ be the [[gravitational potential]] associated with a non-uniform material of density $\rho(\mathbf{r})$ occupying a region $R$. Then
$$
\nabla^{2} \phi=-4 \pi G \rho(\mathbf{r})
$$
### Gauss' Flux Theorem
For a smooth and bounded region $R$, which contains matter of total mass $M$, then
$$
\iint_{\partial R} \mathbf{f} \cdot \mathrm{d} \mathbf{S}=-4 \pi G M,
$$
where $\bf{f}$ is the [[gravitational potential]].
>[[MVC_Sheet8]]