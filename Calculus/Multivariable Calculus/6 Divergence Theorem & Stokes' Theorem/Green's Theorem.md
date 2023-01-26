## Green's Theorem
#MVC
### Green's Theorem in the Plane
Let $D$ be a closed bounded region in the $(x, y)$ plane, whose boundary $C$ is a piecewise smooth simple closed curve, and that $p(x, y), q(x, y)$ have continuous first-order derivatives in $D .$ Then
$$
\iint_{D}\left(\frac{\partial p}{\partial x}+\frac{\partial q}{\partial y}\right) \mathrm{d} x \mathrm{~d} y=\int_{C}(p, q) \cdot \mathbf{n} \mathrm{d} s=\int_{C} p \mathrm{~d} y-q \mathrm{~d} x
$$
where $\mathbf{n}$ is the outward pointing unit normal to $C$ in the $(x, y)$ plane. 
#### Proof
- The first equality is a simple corollary of the [[divergence theorem]] and is effectively the *divergence theorem in a plane*. Let the vector field $\mathbf{F}$ be given by
$$
\mathbf{F}=(p(x, y), q(x, y), 0)
$$
and define the three dimensional region $R$ to be
$$
R=\left\{(x, y, z) \in \mathbb{R}^{3} \mid(x, y) \in D, \quad z \in[0,1]\right\}
$$
with boundary $\partial R$. Noting $\nabla \cdot \mathbf{F}$ has no dependence on $z$, we have
$$
\iint_{D}\left(\frac{\partial p}{\partial x}+\frac{\partial q}{\partial y}\right) \mathrm{d} x \mathrm{~d} y=\iint_{D} \nabla \cdot \mathbf{F} \mathrm{d} x \mathrm{~d} y \int_{0}^{1} d z=\iint_{R} \nabla \cdot \mathbf{F} \mathrm{d} V=\int_{\partial R} \mathbf{F} \cdot \mathbf{n} \mathrm{d} S
$$
The contribution to the surface integral from the surfaces at $z=0,1$ are zero as the integrand is zero. For the surface
$$
\left\{(x, y, z) \in \mathbb{R}^{3} \mid(x, y) \in D, z \in[0,1]\right\}
$$
the outward pointing unit normal to $R$ coincides with the outward pointing unit normal to $C$; also we can write the surface element $\mathrm{d} S$ as
$$
\mathrm{d} S=\mathrm{d} s \mathrm{~d} z
$$
where $\mathrm{d} s$ is the arclength element of the curve $C$ since the $\mathbf{k}$ direction and the plane of the region $D$ are perpendicular. Hence
$$
\int_{\partial R} \mathbf{F} \cdot \mathbf{n} \mathrm{d} S=\int_{0}^{1}\left\{\int_{C} \mathbf{F} \cdot \mathbf{n} \mathrm{d} s\right\} \mathrm{d} z=\int_{0}^{1}\left\{\int_{C}(p, q) \cdot \mathbf{n} \mathrm{d} s\right\} \mathrm{d} z=\int_{C}(p, q) \cdot \mathbf{n} \mathrm{d} s,
$$
with the final equality from the fact the integrand $(p, q) \cdot \mathbf{n}$ has no dependence on $z$.

- For the second equality, we parameterize the curve $C$ in the form $(x(s), y(s))$, where $s$ is arc length, increasing on moving anticlockwise around $C$ when viewed from above. The unit tangent, $\mathbf{t}$, and the outward unit normal $\mathbf{n}$ are given by
$$
\mathbf{t}=\left(\frac{\mathrm{d} x}{\mathrm{~d} s}, \frac{\mathrm{d} y}{\mathrm{~d} s}\right), \quad \mathbf{n}=\left(\frac{\mathrm{d} y}{\mathrm{~d} s},-\frac{\mathrm{d} x}{\mathrm{~d} s}\right)
$$
Using the expression for $\mathbf{n}$, we have
$$
\int_{C}(p, q) \cdot \mathbf{n} \mathrm{d} s=\int_{C}(p, q) \cdot\left(\frac{\mathrm{d} y}{\mathrm{~d} s},-\frac{\mathrm{d} x}{\mathrm{~d} s}\right) \mathrm{d} s=\int_{C} p \mathrm{~d} y-q \mathrm{~d} x
$$
and so we have the second equality, namely
$$
\iint_{D}\left(\frac{\partial p}{\partial x}+\frac{\partial q}{\partial y}\right) \mathrm{d} x \mathrm{~d} y=\int_{C} p \mathrm{~d} y-q \mathrm{~d} x
$$
where $C$ is positively oriented, i.e. the integration around $C$ is anticlockwise.

#### Green's First Identity:
$$
\iiint_{R}\left(\psi \nabla^{2} \phi+\nabla \phi \cdot \nabla \psi\right) \mathrm{d} R=\iint_{\partial R} \psi \nabla \phi \cdot \mathrm{d} \mathbf{S}
$$
#### Green's Second Identity:
$$
\iiint_{R}\left(\psi \nabla^{2} \phi-\phi \nabla^{2} \psi\right) \mathrm{d} R=\iint_{\partial R}(\psi \nabla \phi-\phi \nabla \psi) \cdot \mathrm{d} \mathbf{S} .
$$

---
[[MVC_Sheet5]]
[[MVC_Sheet6]]
[[MVC_Sheet7]]

---
### Another Insight
> Related Chapter: [[2D-Curl]]
 - $\color{green}\bf{F}$ is a two-dimensional vector field.
 - $\color{red} R$ is some region in the $xy$-plane.
 - $\color{red} C$ is the boundary of that region, oriented anticlockwise.
 
 ![ | 250](https://cdn.kastatic.org/ka-perseus-images/bc4ea2aa1028ca7855fdd6e9fd08fe037c6d9e22.svg)
 
 ---
 > [[Green's Theorem]] sates that, the [[Line Integral]] of $\color{green}\bf{F}$ around the boundary of $\color{red} R$ equals the double integral of the [[curl]] of $\color{green}\bf{F}$ within $\color{red} R$: $$\iint_{R} \operatorname{2d-curl} \mathbf{F} d A=\int_{C} \mathbf{F} \cdot d \mathbf{r}$$

- Often  $\color{green}\bf{F}$ is written component-wise as follows: $\mathbf{F}(x, y)=P(x, y) \hat{\mathbf{i}}+Q(x, y) \hat{\mathbf{j}}.$
- Then [[Green's Theorem]] becomes $\int_{C} P d x+Q d y=\iint_{R}\left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}\right) d A$.

> One way to interpret the line integral $\int_{C} \mathbf{F} \cdot d \mathbf{r}$. Imaging rowing a boat around the curve $C$, anticlockwise. Then $\mathbf{F} \cdot d \mathbf{r}$ will be positive at points where the fluid flow is with you, and negative at points against you.
On the whole, the line integral adds up all these dot products to tell you if the flow was generally helpful or burdensome.

#### Bringing the boundary to the interior
##### Cut the Region
- Imagine chopping up the region $R$ with a line straight down the middle, giving two subregions $R_{1}$ and $R_{2}$ .

![|150](https://cdn.kastatic.org/ka-perseus-images/6515d6d0315c3a16e6edafa7d046d521f698905c.svg)
- Name the boundaries of these two regions $\color{green}C_{1}$ and $\color{yellow}C_{2}$. What happens if we take the line integral of $\mathrm{F}$ around these two boundaries, and add them up?
$$
\oint_{\color{green}C_{1}} F \cdot d \mathbf{r}+\oint_{\color{yellow}C_{2}} F \cdot d \mathbf{r}
$$

![ | 150](https://cdn.kastatic.org/ka-perseus-images/a7c670b0aba015bfccb340dd972d53638678c026.svg)

- These line integrals will **cancel out** along the vertical line cut that you made.
- This means the sum of our two integrals is the same as just going around the
full boundary $C$.
$$
\oint_{C_{1}} F \cdot d \mathbf{r}+\oint_{C_{2}} F \cdot d \mathbf{r}=\oint_{C} F \cdot d \mathbf{r}
$$
- Cutting again, again and again.

![|150](https://cdn.kastatic.org/ka-perseus-images/1be0b2744b522103013ff45a60094c4e12307e07.svg)
And finally we will have
$$\sum_{k=1}^{n}\left(\oint_{C_{k}} F \cdot d \mathbf{r}\right)=\oint_{C} F \cdot d \mathbf{r}$$

![|250](https://cdn.kastatic.org/ka-perseus-images/80609b95bf36ee48df1fa641cb8e5f2ca7383796.svg)

##### Integrating Curl
- another way to interpret each of these line integrals around a tiny piece using [[2D-Curl]].

![|300](https://cdn.kastatic.org/ka-perseus-images/cb562ae956918dfc18d3ffba839be4c35928c9e6.svg)
- This line integral can be approximated by taking the $2 \mathrm{~d}$ -curl of $\mathrm{F}$ at any point
within $R_{k}$, and multiplying it by the (tiny) area $\left|R_{k}\right|$
$$
\underbrace{\oint_{C_{k}} \mathbf{F} \cdot d \mathbf{r}}_{\text {Integral around a tiny piece }R_k} \approx(\operatorname{2d-curl} \mathbf{F} \underbrace{\left(x_{k}, y_{k}\right)}_{\text {Point in } R_{k}}) \underbrace{\left|R_{k}\right|}_{\text {Area of } R_{k}}
$$
And then gives
$$\oint_{C} \mathbf{F} \cdot d \mathbf{r} \approx \sum_{k=1}^{n}(2 \mathrm{~d}-\operatorname{curl} \mathbf{F} \underbrace{\left(x_{k}, y_{k}\right)}_{\text {Point in } R_{k}}\left|R_{k}\right|)$$
which is just a double integral when $n$ goes to infinity. i.e.:
$\begin{aligned} \oint_{C} \mathbf{F} \cdot d \mathbf{r} &=\sum_{k=1}^{n}\left(\oint_{C_{k}} \mathbf{F} \cdot d \mathbf{r}\right) \\ & \approx \sum_{k=1}^{n}(\operatorname{2d-curl} \mathbf{F} \underbrace{\left(x_{k}, y_{k}\right)}_{\text {Point in } R_{k}}\left|R_{k}\right|) \\ & \rightarrow \iint_{R} \operatorname{2d-curl} \mathbf{F} d A. \end{aligned}$


### Example: Calculating Area by Line Integral
> Consider the spiral defined by the following parametric equations in the range
>$$
\begin{aligned}
x(t) &=t \cos (t) \\
y(t) &=t \sin (t) \\
t&\in[0,2\pi]
\end{aligned}
>$$
![| 250](https://cdn.kastatic.org/ka-perseus-graphie/83e58541f4b6638526919002a5ef28812168a596.svg)
Calculate its area.

1) Choose the appropriate $P$ and $Q$. 
We first find a pair of functions $P$ and $Q$ that satisfy $$\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}=1.$$

2) Taking $P=-y/2$ and $Q=x/2$, then we want to solve $$\oint_{C} \underbrace{-\frac{1}{2} y d x}_{P d x}+\underbrace{\frac{1}{2} x d y}_{Q d y}.$$
3) Then $$\begin{aligned} \int_{\text {Spiral }} \frac{1}{2} \underbrace{(x d y-y d x)}_{t^{2} d t} &=\int_{0}^{2 \pi} \frac{1}{2} t^{2} d t \\ &=\left[\frac{1}{6} t^{3}\right]_{t=0}^{t=2 \pi} \\ &=\frac{(2 \pi)^{3}}{6}-\frac{0^{3}}{6} \\ &=\frac{8 \pi^{3}}{6} \end{aligned}$$

#### Remark
- Green's theorem can turn tricky line integrals into more straight-forward double integrals.
- To know if Green's theorem will actually make a line integral simpler, ask the following two questions:
$$
\oint_{C} \overbrace{P(x, y)}^{\text {Is } \frac{\partial}{\partial y} \text { simple? }} d x+\overbrace{Q(x, y)}^{\text {Is } \frac{\partial}{\partial x} \text { simple? }} d y
$$
- Also, consider if the region encompassed by the curve $C$ will be easy to describe with a double integral, or if it has a known area.
- You can compute the area of a region with the following line integral around its counterclockwise-oriented boundary:
$$
\oint_{C} \frac{1}{2}(x d y-y d x)
$$

> From [Green's theorem examples](https://www.khanacademy.org/math/multivariable-calculus/greens-theorem-and-stokes-theorem/greens-theorem-articles/a/greens-theorem-examples).

### Example: Prove the Uniqueness of Laplace's Equation in 2d by Green's Theorem
[[Collection2021TT#9]]