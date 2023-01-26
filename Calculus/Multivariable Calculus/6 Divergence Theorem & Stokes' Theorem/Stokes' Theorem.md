## Stokes' Theorem
#MVC #MostCrucial 
#### Definition: Orientation
>At each point of a smooth [[surface]] there are two unit normal vectors $\pm \mathbf{n} .$ Given a smooth surface $\Sigma$, then by an **orientation** of $\Sigma$ we shall mean a continuous choice of unit normal $\mathbf{n}$ for the whole surface $\Sigma .$

For the bounding curve, which we shall denote as $\partial \Sigma$, there are two possible orientations. Given a certain orientation of $\partial \Sigma$ and an oriented tangent vector $\mathbf{t}$ along $\partial \Sigma$ then the vector $\mathbf{t} \wedge \mathbf{n}$ lies in the tangent plane of $\Sigma$ at the boundary point and is normal to the bounding curve $\partial \Sigma$. So $\mathbf{t} \wedge \mathbf{n}$ points either towards the surface $\Sigma$ or away from $\Sigma$. We shall always choose to orient a surface $\Sigma$ and its boundary $\partial \Sigma$ in such a way that $\mathbf{t} \wedge \mathbf{n}$ **points away from** $\Sigma$.
>The two consistent ways to orient the surface and boundary are
$(\mathbf{n}$ on $\Sigma$ and $\mathbf{t}$ on $\partial \Sigma)$ or $(-\mathbf{n}$ on $\Sigma$ and $-\mathbf{t}$ on $\partial \Sigma)$.

>Not all surfaces have an orientation, such surfaces being called **non-orientable**. Examples of non-orientable surfaces are the ***Möbius strip*** and the ***Klein bottle***.

### Stokes' Theorem
Let $\Sigma$ be a smooth oriented [[surface]] in $\mathbb{R}^{3}$ whose boundary is the [[curve]] $\partial \Sigma .$ Let $\mathbf{F}$ be a smooth vector field defined on $\Sigma \cup \partial \Sigma$. Then
$$
\int_{\partial \Sigma} \mathbf{F} \cdot \mathrm{d} \mathbf{r}=\iint_{\Sigma} \operatorname{curl} \mathbf{F} \cdot \mathrm{d} \mathbf{S}.
$$

#### Proof
#NonExaminable #TODO 
>Stokes' Theorem and the [[Divergence Theorem]] are in fact statements of a more general theorem, also known as [[Stokes' Theorem]], which applies in all dimensions. It more generally reads:
>$$
\int_{M} \mathrm{~d} \omega=\int_{\partial M} \omega
>$$
where $M$ is a (compact) oriented $n$ -dimensional manifold (i.e. the $n$-dimensional equivalent of a surface) with boundary $\partial M$ and $\omega$ is a differential form of degree $n-1 .$ A proper appreciation of this result is approximately at fourth year undergraduate level. 

>Note, though, that when $n=1$ Stokes' Theorem reads
>$$
\int_{a}^{b} f^{\prime}(x) \mathrm{d} x=f(b)-f(a)
>$$

### Lemma 117
>If $\mathbf{c} \cdot \mathbf{v}=\mathbf{c} \cdot \mathbf{w}$ for all $\mathbf{c} \in \mathbb{R}^{3}$ then $\mathbf{v}=\mathbf{w}$.
#### Proof
We have $\mathbf{c} \cdot(\mathbf{v}-\mathbf{w})=0$ for all $\mathbf{c}$ and thus for all basis vectors. Thus all the components of $\mathbf{v}, \mathbf{w}$ are equal, hence so are the vectors.

### Corollary 118
==Stokes' Theorem for a scalar field==
>Let $\Sigma$ be a smooth oriented surface in $\mathbb{R}^{3}$ whose boundary is the curve $\partial \Sigma$. Let $\psi$ be a smooth scalar field defined on $\Sigma \cup \partial \Sigma$. Then
> $$
\iint_{\Sigma} \nabla \psi \wedge \mathrm{d} \mathbf{S}=-\int_{\partial \Sigma} \psi \mathrm{d} \mathbf{r}
> $$
#### Proof
Let $\mathrm{c}$ be an arbitrary constant vector and set $\mathbf{F}=\psi \mathbf{c} .$ In this case, and using the [curl product rule](Curl#Identities), [[#Stokes' Theorem]] reads
$$
\iint_{\Sigma} \operatorname{curl}(\psi \mathbf{c}) \cdot \mathrm{d} \mathbf{S}=\iint_{\Sigma}(\psi \operatorname{curl} \mathbf{c}+\nabla \psi \wedge \mathbf{c}) \cdot \mathrm{d} \mathbf{S}=\int_{\partial \Sigma} \psi \mathbf{c} \cdot \mathrm{d} \mathbf{r}
$$
As $\mathbf{c}$ is constant then curl $\mathbf{c}=\mathbf{0}$ and we have
$$
\mathbf{c} \cdot\left(-\iint_{\Sigma} \nabla \psi \wedge \mathrm{d} \mathbf{S}\right)=\iint_{\Sigma} \nabla \psi \wedge \mathbf{c} \cdot \mathrm{d} \mathbf{S}=\mathbf{c} \cdot\left(\int_{\partial \Sigma} \psi \mathrm{d} \mathbf{r}\right)
$$
As $\mathbf{c}$ is arbitrary then by [[#Lemma 117]] we have
$$
-\iint_{\Sigma} \nabla \psi \wedge \mathrm{d} \mathbf{S}=\int_{\partial \Sigma} \psi \mathrm{d} \mathbf{r}
$$
and the result follows.
### Examples: Verifying Stokes' Theorem
#### Example 119
Verify [[Stokes' Theorem]] when $\mathbf{F}=(y, z, x)$ on the hemisphere
$$
\Sigma=\left\{(x, y, z): x^{2}+y^{2}+z^{2}=a^{2}, z \geqslant 0\right\} .
$$
##### Solution
- We can parameterize the sphere as
$$
\mathbf{r}(\theta, \phi)=(a \sin \theta \cos \phi, a \sin \theta \sin \phi, a \cos \theta) \quad 0 \leqslant \theta \leqslant \pi, 0 \leqslant \phi \leqslant 2 \pi
$$
Then
$$
\frac{\partial \mathbf{r}}{\partial \theta} \wedge \frac{\partial \mathbf{r}}{\partial \phi}=\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
a \cos \theta \cos \phi & a \cos \theta \sin \phi & -a \sin \theta \\
-a \sin \theta \sin \phi & a \sin \theta \cos \phi & 0
\end{array}\right|=a^{2} \sin \theta(\sin \theta \cos \phi, \sin \theta \sin \phi, \cos \theta)
$$
Now $\operatorname{curl} \mathbf{F}=(-1,-1,-1)$ and hence
$$
\begin{aligned}
\iint_{\Sigma} \operatorname{curl} \mathbf{F} \cdot \mathrm{d} \mathbf{S} &=\int_{\theta=0}^{\pi / 2} \int_{\phi=0}^{2 \pi}(-1,-1,-1) \cdot a^{2} \sin \theta(\sin \theta \cos \phi, \sin \theta \sin \phi, \cos \theta) \mathrm{d} \phi \mathrm{d} \theta \\
&=-a^{2} \int_{\theta=0}^{\pi / 2} \int_{\phi=0}^{2 \pi} \sin \theta(\sin \theta \cos \phi+\sin \theta \sin \phi+\cos \theta) \mathrm{d} \phi \mathrm{d} \theta \\
&=-2 \pi a^{2} \int_{\theta=0}^{\pi / 2} \sin \theta \cos \theta \mathrm{d} \theta=-2 \pi a^{2}\left[\frac{\sin ^{2} \theta}{2}\right]_{0}^{\pi / 2} \\
&=-\pi a^{2} .
\end{aligned}
$$
- On the other hand, once we parameterize and orient $\partial \Sigma$ as $\mathbf{r}(\theta)=(a \cos \theta, a \sin \theta, 0)$, we have
$$
\begin{aligned}
\int_{\partial \Sigma} \mathbf{F} \cdot \mathrm{d} \mathbf{r} &=\int_{0}^{2 \pi}(a \sin \theta, 0, a \cos \theta) \cdot(-a \sin \theta, a \cos \theta, 0) \mathrm{d} \theta \\
&=-a^{2} \int_{0}^{2 \pi} \sin ^{2} \theta \mathrm{d} \theta=-\pi a^{2}
\end{aligned}
$$

#### Example 120
Verify Stokes' Theorem when $\mathbf{F}=\left(2 y, 3 x, x^{2}+y^{2}+z^{2}\right)$ and $\Sigma$ is the lower half of the ellipsoid $x^{2} / 4+y^{2} / 9+z^{2} / 27=1$.

##### Solution
Here $\partial \Sigma$ is the ellipse $x^{2} / 4+y^{2} / 9=1$ in the $x y$ -plane. If $\partial \Sigma$ is oriented anticlockwise then we need to take the upward pointing normal on $\Sigma$. We may parameterize $\partial \Sigma$ by $\mathbf{r}(t)=(2 \cos t, 3 \sin t, 0)$ and so
$$
\begin{aligned}
\int_{\partial \Sigma} \mathbf{F} \cdot \mathrm{d} \mathbf{r} &=\int_{0}^{2 \pi}\left(6 \sin t, 6 \cos t, 4 \cos ^{2} t+9 \sin ^{2} t\right) \cdot(-2 \sin t, 3 \cos t, 0) \mathrm{d} t \\
&=\int_{0}^{2 \pi}\left(-12 \sin ^{2} t+18 \cos ^{2} t\right) \mathrm{d} t \\
&=\int_{0}^{2 \pi}((-6-6 \cos 2 t)+(9+9 \cos 2 t)) \mathrm{d} t \\
&=6 \pi .
\end{aligned}
$$
On the other hand we can parameterize the lower half of the ellipsoid as
$$
\mathbf{r}(\theta, \phi)=(2 \sin \theta \cos \phi, 3 \sin \theta \sin \phi, 3 \sqrt{3} \cos \theta)
$$
So
$$
\begin{aligned}
\mathbf{r}_{\theta} \wedge \mathbf{r}_{\phi} &=\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
2 \cos \theta \cos \phi & 3 \cos \theta \sin \phi & -3 \sqrt{3} \sin \theta \\
-2 \sin \theta \sin \phi & 3 \sin \theta \cos \phi & 0
\end{array}\right| \\
&=\left(9 \sqrt{3} \sin ^{2} \theta \cos \phi, 6 \sqrt{3} \sin ^{2} \theta \sin \phi, 6 \sin \theta \cos \theta\right),
\end{aligned}
$$
but this points **downwards**, so we will take its negative. Also
$$
\operatorname{curl} \mathbf{F}=\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
2 y & 3 x & x^{2}+y^{2}+z^{2}
\end{array}\right|=(2 y,-2 x, 1) .
$$
Finally, then
$$
\begin{aligned}
& \iint_{\Sigma} \operatorname{curl} \mathbf{F} \cdot \mathrm{d} \mathbf{S} \\
=& \int_{\theta=\pi / 2}^{\pi} \int_{\phi=0}^{2 \pi}(6 \sin \theta \sin \phi,-4 \sin \theta \cos \phi, 1) \cdot\left(-9 \sqrt{3} \sin ^{2} \theta \cos \phi,-6 \sqrt{3} \sin ^{2} \theta \sin \phi,-6 \sin \theta \cos \theta\right) \mathrm{d} \phi \mathrm{d} \theta \\
=& \int_{\theta=\pi / 2}^{\pi} \int_{\phi=0}^{2 \pi}\left(-54 \sqrt{3} \sin ^{2} \theta \sin \phi \cos \phi+24 \sqrt{3} \sin ^{3} \theta \cos \phi \sin \phi-6 \sin \theta \cos \theta\right) \mathrm{d} \phi \mathrm{d} \theta \\
=&-2 \pi \int_{\theta=\pi / 2}^{\pi} 6 \sin \theta \cos \theta \mathrm{d} \theta \\
=& 2 \pi\left[\frac{3 \cos 2 \theta}{2}\right]_{\pi / 2}^{\pi} \\
=& 3 \pi(1+1)=6 \pi .
\end{aligned}
$$
#### Example 121
>Verify Stokes' Theorem for $\mathbf{F}=\left(x^{2}+3 y z,-2 x z, 7 y\right)$ on $\Sigma$, where $\Sigma$ is that part of the cylindrical surface $x^{2}+y^{2}=a^{2}$ between the planes $x+y+z=0$ and $x+y+z=h$, where $h \geqslant 0 .$
##### Solution
We may parameterize the cylinder as
$$
\mathbf{r}(\theta, z)=(a \cos \theta, a \sin \theta, z)
$$
and orient it with outward pointing normal $\mathrm{d} \mathbf{S}=(\cos \theta, \sin \theta, 0) a \mathrm{~d} \theta \mathrm{d} z .$ So
$$
\mathbf{F}=\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
x^{2}+3 y z & -2 x z & 7 y
\end{array}\right|=(7+2 x, 3 y,-5 z)
$$
$$
\begin{aligned}
\iint_{\Sigma} \operatorname{curl} \mathbf{F} \cdot \mathrm{d} \mathbf{S} &=\int_{\theta=0}^{2 \pi} \int_{z=-a \cos \theta-a \sin \theta}^{h-a \cos \theta-a \sin \theta}(7+2 a \cos \theta, 3 a \sin \theta,-5 z) \cdot(\cos \theta, \sin \theta, 0) a \mathrm{~d} z \mathrm{~d} \theta \\
&=\int_{\theta=0}^{2 \pi} \int_{z=-a \cos \theta-a \sin \theta}^{h-a \cos \theta-a \sin \theta}\left(7 \cos \theta+2 a \cos ^{2} \theta+3 a \sin ^{2} \theta\right) a \mathrm{~d} z \mathrm{~d} \theta \\
&=\int_{\theta=0}^{2 \pi}\left(7 \cos \theta+2 a \cos ^{2} \theta+3 a \sin ^{2} \theta\right) a h \mathrm{~d} \theta \\
&=(2 a \pi+3 a \pi) a h \\
&=5 \pi a^{2} h .
\end{aligned}
$$
On the other side, we have a disconnected boundary $\partial \Sigma$ made up of
$$
\begin{array}{l}
C_{1}=\{(a \cos \theta, a \sin \theta,-a \cos \theta-a \sin \theta): 0 \leqslant \theta \leqslant 2 \pi\} \\
C_{2}=\{(a \cos \theta, a \sin \theta, h-a \cos \theta-a \sin \theta): 0 \leqslant \theta \leqslant 2 \pi\}
\end{array}
$$
As we used the outward pointing normal to orient $\Sigma$ then we need to orient $C_{1}$ in the direction of increasing $\theta$ but orient $C_{2}$ in the direction of decreasing $\theta$. If we write $x(\theta)=a \cos \theta, y(\theta)=a \sin \theta, z(\theta)=-a \cos \theta-a \sin \theta$ then we have
$$
\begin{aligned}
\int_{C_{1}} \mathbf{F} \cdot \mathrm{d} \mathbf{r} &=\int_{0}^{2 \pi}\left(x(\theta)^{2}+3 y(\theta) z(\theta),-2 x(\theta) z(\theta), 7 y(\theta)\right) \cdot \mathrm{d} \mathbf{r}(\theta) \\
\int_{C_{2}} \mathbf{F} \cdot \mathrm{d} \mathbf{r} &=-\int_{0}^{2 \pi}\left(x(\theta)^{2}+3 y(\theta)[z(\theta)+h],-2 x(\theta)[z(\theta)+h], 7 y(\theta)\right) \cdot \mathrm{d} \mathbf{r}(\theta) .
\end{aligned}
$$
Hence
$$
\begin{aligned}
\int_{\partial \Sigma} \mathbf{F} \cdot \mathrm{d} \mathbf{r} &=\int_{0}^{2 \pi}(-3 h y(\theta), 2 h x(\theta), 0) \cdot \mathrm{d} \mathbf{r}(\theta) \\
&=a h \int_{0}^{2 \pi}(-3 a \sin \theta, 2 a \cos \theta, 0) \cdot(-\sin \theta, \cos \theta, \sin \theta-\cos \theta) \mathrm{d} \theta \\
&=a^{2} h \int_{0}^{2 \pi}\left(3 \sin ^{2} \theta+2 \cos ^{2} \theta\right) \mathrm{d} \theta \\
&=5 \pi a^{2} h .
\end{aligned}
$$

### Example 122
Let $C$ be a closed curve bounding a smooth surface $\Sigma$. Show that
$$
\int_{C} \mathbf{r} \wedge \mathrm{d} \mathbf{r}=2 \iint_{\Sigma} \mathrm{d} \mathbf{S}
$$
Hence, or otherwise, evaluate $\iint_{\Sigma} \mathrm{d} \mathbf{S}$ where $\Sigma$ is the surface
$$
\Sigma=\left\{(x, y, z): z=\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}, x^{2}+y^{2}<1\right\}
$$
> You may assume that $\nabla \wedge(\mathbf{u} \wedge \mathbf{v})=(\mathbf{v} \cdot \nabla) \mathbf{u}-(\nabla \cdot \mathbf{u}) \mathbf{v}+(\nabla \cdot \mathbf{v}) \mathbf{u}-(\mathbf{u} \cdot \nabla) \mathbf{v} .$

#### Solution
If we set $\mathbf{F}=\mathbf{c} \wedge \mathbf{r}$ where $\mathbf{c}$ is an arbitrary constant vector, then we have
$$
\begin{aligned}
\nabla \wedge(\mathbf{c} \wedge \mathbf{r}) &=(\mathbf{r} \cdot \nabla) \mathbf{c}-(\nabla \cdot \mathbf{c}) \mathbf{r}+(\nabla \cdot \mathbf{r}) \mathbf{c}-(\mathbf{c} \cdot \nabla) \mathbf{r} \\
&=(\nabla \cdot \mathbf{r}) \mathbf{c}-(\mathbf{c} \cdot \nabla) \mathbf{r} \quad[\operatorname{as} \mathbf{c} \text { is constant }] \\
&=3 \mathbf{c}-\mathbf{c} \\
&=2 \mathbf{c}
\end{aligned}
$$
as
$$
(\mathbf{c} \cdot \nabla) \mathbf{r}=\left(c_{1} \frac{\partial}{\partial x}+c_{2} \frac{\partial}{\partial y}+c_{3} \frac{\partial}{\partial z}\right)(x, y, z)=\left(c_{1}, c_{2}, c_{3}\right)=\mathbf{c}
$$
So, by [[Stokes' Theorem]],
$$
\int_{C}(\mathbf{c} \wedge \mathbf{r}) \cdot \mathrm{d} \mathbf{r} =\iint_{\Sigma} 2 \mathbf{c} \cdot \mathrm{d} \mathbf{S} 
\Longrightarrow \mathbf{c} \cdot\left(\int_{C} \mathbf{r} \wedge \mathrm{d} \mathbf{r}\right)=\mathbf{c} \cdot \left(\iint_{\Sigma} 2 \mathrm{~d} \mathbf{S}\right) .
$$
As $\mathbf{c}$ is arbitrary then by [[#Lemma 117]]
$$
\int_{C} \mathbf{r} \wedge \mathrm{d} \mathbf{r}=2 \iint_{\Sigma} \mathrm{d} \mathbf{S}
$$
The bounding curve of the given surface $\Sigma$ is
$$
z=\frac{x^{2}}{a^{2}}+\frac{y^{2}}{b^{2}}, \quad x^{2}+y^{2}=1
$$
which can naturally be parameterized as
$$
\mathbf{r}(\theta)=\left(\cos \theta, \sin \theta, \frac{\cos ^{2} \theta}{a^{2}}+\frac{\sin ^{2} \theta}{b^{2}}\right), \quad 0 \leqslant \theta \leqslant 2 \pi
$$
(writing $c=\cos \theta, s=\sin \theta$)
$$
\begin{aligned}
\iint_{\Sigma} \mathrm{d} \mathbf{S} &=\frac{1}{2} \int_{0}^{2 \pi}\left(c, s, \frac{c^{2}}{a^{2}}+\frac{s^{2}}{b^{2}}\right) \wedge\left(-s, c,\left(\frac{-1}{a^{2}}+\frac{1}{b^{2}}\right) 2 c s\right) \mathrm{d} \theta \\
&=\frac{1}{2} \int_{0}^{2 \pi}\left(\frac{c s^{2}}{b^{2}}+\frac{\left(-2 c s^{2}-c^{3}\right)}{a^{2}}, \frac{c^{2} s}{a^{2}}+\frac{\left(-s^{3}-2 c^{2} s\right)}{b^{2}}, 1\right) \mathrm{d} \theta \\
&=\frac{1}{2} \int_{0}^{2 \pi}\left(\frac{c s^{2}}{b^{2}}+\frac{\left(-c s^{2}-c\right)}{a^{2}}, \frac{c^{2} s}{a^{2}}+\frac{\left(-s-c^{2} s\right)}{b^{2}}, 1\right) \mathrm{d} \theta \\
&=\frac{1}{2}\left[\left(\frac{s^{3}}{3 b^{2}}+\frac{\left(-s^{3} / 3-s\right)}{a^{2}},\right), \frac{-c^{3}}{3 a^{2}}+\frac{\left(c+c^{3} / 3\right)}{b^{2}}, \theta\right]_{0}^{2 \pi} \\
&=\frac{1}{2}[(0,0,2 \pi)] \\
&=\pi \mathbf{k} .
\end{aligned}
$$

### Definition: Simply Connected
>A region $R \subseteq \mathbb{R}^{3}$ is said to be **simply connected** if every simple, [[Closed]] [[curve]] $C$ can be continuously deformed to a single point.

Specifically, if $\mathbf{r}:[0,1] \rightarrow R$ is a simple closed curve beginning and ending in $\mathbf{p}$ then there exists a map $H:[0,1] \times[0,1] \rightarrow R$ such that $H(t, 1)=\mathbf{r}(t)$ and $H(t, 0)=\mathbf{p}$.

>$\mathbb{R}^{3}$ is simply connected, as is any plane or line. $\mathbb{R}^{2}-\{\mathbf{0}\}$ is not simply connected, nor is the cylinder $x^{2}+y^{2}=a^{2}$, nor a torus. $\mathbb{R}^{3}-\{\mathbf{0}\}$ is simply connected though.

### Corollary 125
==Existence of a [[Potential]]==
>Let $R$ be a simply connected region and let $\mathbf{F}$ be a smooth vector field on $R$ for which $\operatorname{curl} \mathbf{F}=\mathbf{0}$. Then $\mathbf{F}$ is [[conservative]], i.e. there exists a [[potential]] $\phi$ on $R$ such that $\mathbf{F}=\nabla \phi$.

#### Remark 126
Firstly note that if $\mathbf{F}$ is [[conservative]] then $\mathbf{F}=\nabla \phi$ and hence $\operatorname{curl} \mathbf{F}=\mathbf{0} .$ Combining this observation with corollary 125 gives, by use of [Theorem 69](Conservative#Theorem%2069), that:
>*with a restriction to simply connected regions, $\operatorname{curl} \mathbf{F}=\mathbf{0}$ is **equivalent** to (i), (ii) and (iii):*
>1) $\mathbf{F}$ is [[conservative]] - i.e. $\mathbf{F}=\nabla \phi$ for some scalar field $\phi: S \rightarrow \mathbb{R}$.
>2) Given any two points $\mathbf{p}, \mathbf{q} \in S$ and curve $\gamma$ in $S$, starting at $\mathbf{p}$ and ending at $\mathbf{q}$, then the integral
>$$
\int_{C} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}
>$$
is **independent** of the choice of curve $C$.
>3) For any simple closed curve $C$ then
>$$
\int_{C} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}=0
>$$
##### Proof
#TBV 
Let $\mathbf{p}$ be a fixed point in $R$ and define for any $\mathbf{q} \in R$,
$$
\phi(\mathbf{q})=\int_{C_{1}} \mathbf{F} \cdot \mathrm{d} \mathbf{r}
$$
where $C_{1}$ is a curve in $S$ from $\mathbf{p}$ to q. If $C_{2}$ is a second such curve then there is a simple closed curve $C$ formed by $C_{1}$ followed by $C_{2}$ in reverse orientation. As $R$ is simply connected then $C$ is the boundary of a [[surface]] $\Sigma$. By [[Stokes' Theorem]] then
$$
\int_{C} \mathbf{F} \cdot \mathrm{d} \mathbf{r}=\iint_{\Sigma} \operatorname{curl} \mathbf{F} \cdot \mathrm{d} \mathbf{S}=0
$$

But this is not generally equivalent. #Q 
[[MVC_Sheet7]]