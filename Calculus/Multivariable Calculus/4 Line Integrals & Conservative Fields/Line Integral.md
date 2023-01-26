## Line Integral
#MVC 
### Definition
Let $C$ be a [[curve]] in $\mathbb{R}^{3}$, parameterized by $\gamma:[a, b] \rightarrow \mathbb{R}^{3}$ and let $\mathbf{F}$ be a vector field, whose domain includes $C .$ We define the $\color{orange}\textbf{line integral }\mathbf{F}\textit{ along }\mathit{C}$ as
$$
\color{yellow}
\int_{C} \mathbf{F} \cdot \mathrm{d} \mathbf{r}=\int_{a}^{b} \mathbf{F}(\mathbf{r}(t)) \cdot \mathbf{r}^{\prime}(t) \mathrm{d} t .
$$
> Also see [[#Definition 57]]
### Proposition 54
>If **oriented** the same, the [[line integral]] $\int_{C} \mathbf{F} \cdot \mathrm{d} \mathbf{r}$ is **independent** of the choice of parameterization.

#### Proof
Suppose that $\gamma_{1}:\left[a_{1}, b_{1}\right] \rightarrow \mathbb{R}^{3}$ and $\gamma_{2}:\left[a_{2}, b_{2}\right] \rightarrow \mathbb{R}^{3}$ are two parameterizations of $C$ with $\gamma_{1}\left(a_{1}\right)=\gamma_{2}\left(a_{2}\right)$ and $\gamma_{1}\left(b_{1}\right)=\gamma_{2}\left(b_{2}\right)$, so that $\gamma_{1}$ and $\gamma_{2}$ give $C$ the same orientation.
Then $\gamma_{2}=\gamma_{1} \circ \psi$ where $\psi:\left[a_{2}, b_{2}\right] \rightarrow\left[a_{1}, b_{1}\right]$ associates the $\gamma_{2}$ co-ordinates of points on $C$ with their $\gamma_{1}$ co-ordinate.
We now define $I:\left[a_{1}, b_{1}\right] \rightarrow \mathbb{R}$ and $J:\left[a_{2}, b_{2}\right] \rightarrow \mathbb{R}$ by
$$
I(t)=\int_{a_{1}}^{t} \mathbf{F}\left(\gamma_{1}(s)\right) \cdot \gamma_{1}^{\prime}(s) \mathrm{d} s, \quad J(t)=\int_{a_{2}}^{t} \mathbf{F}\left(\gamma_{2}(s)\right) \cdot \gamma_{2}^{\prime}(s) \mathrm{d} s
$$
By the [[Fundamental Theorem of Calculus]]
$$
I^{\prime}(t)=\mathbf{F}\left(\gamma_{1}(t)\right) \cdot \gamma_{1}^{\prime}(t), \quad J^{\prime}(t)=\mathbf{F}\left(\gamma_{2}(t)\right) \cdot \gamma_{2}^{\prime}(t)
$$
Further, for $\psi(t)$ a function of $t$ we have, by the chain rule,
$$
\begin{aligned}
\frac{\mathrm{d}}{\mathrm{d} t} I(\psi(t)) &=\psi^{\prime}(t) I^{\prime}(\psi(t)) \\
&=\psi^{\prime}(t) \mathbf{F}\left(\gamma_{1}(\psi(t))\right) \cdot \gamma_{1}^{\prime}(\psi(t)) .
\end{aligned}
$$
Recall
$$
\gamma_{2}(t)=\gamma_{1}(\psi(t)) \text { . }
$$
Thus $\gamma_{2}^{\prime}(t)=\psi^{\prime}(t) \gamma_{1}^{\prime}(\psi(t))$ and hence
$$
\begin{aligned}
\frac{\mathrm{d}}{\mathrm{d} t} I(\psi(t)) &=\mathbf{F}\left(\gamma_{2}(t)\right) \cdot\left(\gamma_{1}^{\prime}(\psi(t)) \psi^{\prime}(t)\right) \\
&=\mathbf{F}\left(\gamma_{2}(t)\right) \cdot \gamma_{2}^{\prime}(t)=J^{\prime}(t) .
\end{aligned}
$$
It follows that $I(\psi(t))$ and $J(t)$ differ by a constant and, as they agree at $t=a_{2}$ (when they are both zero), then $I(\psi(t))=J(t)$ and in particular when $t=b_{2}$ we have
$$
\int_{a_{1}}^{b_{1}} \mathbf{F}\left(\gamma_{1}(s)\right) \cdot \gamma_{1}^{\prime}(s) \mathrm{d} s=\int_{a_{2}}^{b_{2}} \mathbf{F}\left(\gamma_{2}(s)\right) \cdot \gamma_{2}^{\prime}(s) \mathrm{d} s.
$$

#### Remark 55
>If we parameterized $C$ in the **reverse** orientation then the integral $\int_{C} \mathbf{F} \cdot \mathrm{d} \mathbf{r}$ would give negative what had been previously calculated.
### Example 56
Let $\mathbf{F}=\mathbf{c} \wedge \mathbf{r}$ where $\mathbf{c}$ is a constant vector and let $C$ be the circular helix parameterized by
$$
\mathbf{r}(t)=(\cos t, \sin t, t), \quad 0 \leqslant t \leqslant 2 \pi
$$

Then
$$
\begin{aligned}
\int_{C} \mathbf{F} \cdot \mathrm{d} \mathbf{r} &=\int_{0}^{2 \pi}\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
c_{1} & c_{2} & c_{3} \\
\cos t & \sin t & t
\end{array}\right| \cdot(-\sin t, \cos t, 1) \mathrm{d} t \\
&=\int_{0}^{2 \pi}\left|\begin{array}{ccc}
-\sin t & \cos t & 1 \\
c_{1} & c_{2} & c_{3} \\
\cos t & \sin t & t
\end{array}\right| \mathrm{d} t \\
&=\int_{0}^{2 \pi}\left(-c_{2} t \sin t+c_{3} \cos ^{2} t+c_{1} \sin t-c_{2} \cos t+c_{3} \sin ^{2} t-c_{1} t \cos t\right) \mathrm{d} t \\
&=\int_{0}^{2 \pi}\left(-c_{2} t \sin t+c_{3}-c_{1} t \cos t\right) \mathrm{d} t \\
&=2 \pi c_{3}-c_{1}[t \sin t+\cos t]_{0}^{2 \pi}-c_{2}[-t \cos t+\sin t]_{0}^{2 \pi} \\
&=2 \pi\left(c_{2}+c_{3}\right)
\end{aligned}
$$

### Definition 57
If $\phi$ is a scalar field defined on a curve $C$ with parameterization $\gamma:[a, b] \rightarrow \mathbb{R}^{3}$, 'hen we also define the line integral
$$
\int_{C} \phi \mathrm{d} s=\int_{a}^{b} \phi(t)\left|\gamma^{\prime}(t)\right| \mathrm{d} t
$$
$\mathbf{F}=\left(F_{1}, F_{2}, F_{3}\right)$ is a ** vector field** defined on the curve $C$ then we define
$$
\int_{C} \mathbf{F} \mathrm{d} s=\left(\int_{C} F_{1} \mathrm{~d} s, \int_{C} F_{2} \mathrm{~d} s, \int_{C} F_{3} \mathrm{~d} s\right)
$$

>Note that if $\mathbf{t}$ is the unit **tangent vector field** along $C$, in the same direction as the parameterization, then
>$$
\int_{C} \phi \mathrm{d} s=\int_{C}(\phi \mathbf{t}) \cdot \mathrm{d} \mathbf{r}
>$$
*and so, by inheritance, these line integrals [do not depend on the choice of parameterization](#Proposition%2054). Note further that the two types of integral defined above are also independent of the choice of orientation of $C$, as they are independent of the sign of $\gamma^{\prime}(t)$.*

### Definition: Arc Length
If $C$ is a curve with parameterization $\gamma:[a, b] \rightarrow \mathbb{R}^{3}$ then the [[arc length]] of the curve is
$$
\int_{C} \mathrm{~d} s=\int_{a}^{b}\left|\gamma^{\prime}(t)\right| \mathrm{d} t.
$$
### Notation: $\mathrm{d} \mathbf{r}$
We will standardly use the notation
$$
\mathrm{d} \mathbf{r}=(\mathrm{d} x, \mathrm{~d} y, \mathrm{~d} z) \quad \text { and } \quad \mathrm{d} s=|\mathrm{d} \mathbf{r}|.
$$
### Definition: Work Done
With notation as in the [Definition 53](Line%20Integral#Definition), if the vector field $\mathbf{F}$ represents a force on a particle then
$$
\int_{C} \mathbf{F} \cdot \mathrm{d} \mathbf{r}
$$
is the [[work done]] by the force in moving the particle along $C$.
This is a generalization of the formula

$$\rm Work = Force \times Distance$$
which applies to constant forces acting parallel to the direction of the motion. More generally, we have $$\text{Work = Component of force in direction of travel} \times \text{Distance}$$ if the force and movement are not parallel. The work integral is just an integral of such infinitesimal contributions of work.
