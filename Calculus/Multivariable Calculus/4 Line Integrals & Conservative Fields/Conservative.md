## Conservative
#MVC 
### Proposition 64
If $\mathbf{F}=\nabla \phi$ and $\gamma:[a, b] \rightarrow S$ is any [[curve]] such that $\gamma(a)=\mathbf{p}, \gamma(b)=\mathbf{q}$ then
$$
\int_{\gamma} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}=\phi(\mathbf{q})-\phi(\mathbf{p})
$$
In particular, the integral [$\int_{\gamma} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}$](Line%20Integral) depends only on the endpoints of the curve $\gamma .$
#### Proof
If $\gamma(t)=(x(t), y(t), z(t))$ then
$$
\begin{aligned}
\int_{\gamma} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r} &=\int_{a}^{b} \mathbf{F}(\gamma(t)) \cdot \gamma^{\prime}(t) \mathrm{d} t \\
&=\int_{a}^{b} \nabla \phi(\gamma(t)) \cdot \gamma^{\prime}(t) \mathrm{d} t \\
&=\int_{a}^{b}\left(\frac{\partial \phi}{\partial x} \frac{\mathrm{d} x}{\mathrm{~d} t}+\frac{\partial \phi}{\partial y} \frac{\mathrm{d} y}{\mathrm{~d} t}+\frac{\partial \phi}{\partial z} \frac{\mathrm{d} z}{\mathrm{~d} t}\right) \mathrm{d} t \\
&=\int_{a}^{b}\left[\frac{\mathrm{d}}{\mathrm{d} t}(\phi(\gamma(t)))\right] \mathrm{d} t \quad[\text { by the }
\end{aligned}
$$
by the [[chain rule]]
$$
\begin{array}{l}
=\phi(\gamma(b))-\phi(\gamma(a)) \\
=\phi(\mathbf{q})-\phi(\mathbf{p}) .
\end{array}
$$
### Definition 65
Let $S$ be an open subset of $\mathbb{R}^{3} .$ A vector field $\mathbf{F}: S \rightarrow \mathbb{R}^{3}$ is said to be [[conservative]] if there exists a scalar field $\phi: S \rightarrow \mathbb{R}$ such that $\mathbf{F}=\nabla \phi$.
### Definition 66
 If $\mathbf{F}=\nabla \phi$ then $\phi$ is said to be a [[potential]] (or scalar potential) for $\mathbf{F}$.
### Definition 67
> A subset $S$ of $\mathbb{R}^{3}$ is said to be [[path-connected]] if for any points $\mathbf{p}, \mathbf{q} \in S$ there exists a curve $\gamma:[a, b] \rightarrow S$ such that $\gamma(a)=\mathbf{p}$ and $\gamma(b)=\mathbf{q} .$

### Corollary 68
If $\nabla \phi=0$ on a [[path-connected]] set $S$ then $\phi$ is constant. In particular, if $\phi$ and $\psi$ are potentials of the [[conservative]] field $\mathbf{F}$, defined on $S$, then $\phi$ and $\psi$ differ by a constant.
#### Proof
If $\nabla \phi=0$ then for any curve, with endpoints $\mathbf{p}, \mathbf{q}$, we have
$$
\phi(\mathbf{q})-\phi(\mathbf{p})=\int_{\gamma} \nabla \phi \cdot \mathrm{d} \mathbf{r}=0
$$
Given a fixed point $\mathbf{p}$ in $S$, any $\mathbf{q}$ in $S$ is connected to $\mathbf{p}$ by a curve, and so $\phi$ is constant. If $\mathbf{F}=\nabla \phi=\nabla \psi$ then $\nabla(\phi-\psi)=0$ and the result follows.

### Theorem 69
>Let $S$ be an open path-connected subset of $\mathbb{R}^{3}$ and let $\mathbf{F}: S \rightarrow \mathbb{R}^{3}$ be a vector field. Then the following three statements are equivalent.
(i) $\mathbf{F}$ is [[conservative]] $-i . e . \mathbf{F}=\nabla \phi$ for some scalar field $\phi: S \rightarrow \mathbb{R}$.
(ii) Given any two points $\mathbf{p}, \mathbf{q} \in S$ and curve $\gamma$ in $S$, starting at $\mathbf{p}$ and ending at $\mathbf{q}$, then the integral
>$$
\int_{\gamma} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}
>$$
is independent of the choice of curve $\gamma$.
(iii) For any simple closed curve $\gamma$ then
>$$
\int_{\gamma} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}=0
>$$

#### Proof
- $(i) \Longrightarrow(i i):$ This was just proved in [[#Proposition 64]] as $\phi(\mathbf{q})-\phi(\mathbf{p})$ is dependent only on the endpoints $\mathbf{p}$ and $\mathbf{q}$ and not on the path taken. 
- $(ii) \Longrightarrow(i):$ Let $\mathbf{p} \in S$ be a fixed point and define for any $\mathbf{q} \in S$
$$
\phi(\mathbf{q})=\int_{\mathbf{p}}^{\mathbf{q}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}
$$
which, by assumption, is independent of the curve taken and is a function only of $\mathbf{q}$. As $S$ is open there is an $r>0$ small enough that $\mathbf{q}+t \mathbf{i}$ is in $S$ for $0 \leqslant t \leqslant r$. Then
$$
\phi(\mathbf{q}+t \mathbf{i})-\phi(\mathbf{q})=\int_{\mathbf{q}}^{\mathbf{q}+t \mathbf{i}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}
$$
where the curve from $\mathbf{q}$ to $\mathbf{q}+t \mathbf{i}$ can be taken to be a straight line. So
$$
\phi(\mathbf{q}+t \mathbf{i})-\phi(\mathbf{q})=\int_{s=0}^{s=t} \mathbf{F}(\mathbf{q}+s \mathbf{i}) \cdot(\mathbf{i} \mathrm{d} s)=\int_{s=0}^{s=t} F_{1}(\mathbf{q}+s \mathbf{i}) \mathrm{d} s
$$
where $\mathbf{F}=\left(F_{1}, F_{2}, F_{3}\right)$. Hence
$$
\frac{\partial \phi}{\partial x}(\mathbf{q})=\lim _{t \rightarrow 0} \frac{\phi(\mathbf{q}+t \mathbf{i})-\phi(\mathbf{q})}{t}=\lim _{t \rightarrow 0} \frac{1}{t} \int_{s=0}^{s=t} F_{1}(\mathbf{q}+s \mathbf{i}) \mathrm{d} s=F_{1}(\mathbf{q})
$$
by the continuity of $F_{1}$ at $\mathbf{q}$. Similarly
$$
\frac{\partial \phi}{\partial y}(\mathbf{q})=F_{2}(\mathbf{q}), \quad \frac{\partial \phi}{\partial z}(\mathbf{q})=F_{3}(\mathbf{q})
$$
and so $\nabla \phi=\mathbf{F}$ as required.
- $(i i) \Longrightarrow(i i i):$ Suppose now that for any two points $\mathbf{p}$ and $\mathbf{q}$ the line integral $\int_{\mathbf{p}}^{\mathbf{q}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}$ is **independent** of the curve taken. Let $\gamma$ be a [[simple]] [[closed]] [[curve]] in $S$ and let $\mathbf{p}$ and $\mathbf{q}$ be two distinct points on $\gamma$. Then $\mathbf{p}$ and q split $\gamma$ into two curves $\gamma_{1}$ and $\gamma_{2}$, with $\gamma_{1}$ running from $\mathbf{p}$ to $\mathbf{q}$ and $\gamma_{2}$ running from $\mathbf{q}$ to $\mathbf{p}$. So, by (ii) and [[Line Integral#Remark 55]],
$$
\int_{\gamma} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}=\int_{\gamma_{1}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}+\int_{\gamma_{2}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}=\int_{\mathbf{p}}^{\mathbf{q}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}-\int_{\mathbf{p}}^{\mathbf{q}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}=0
$$
- $(i i i) \Longrightarrow(i i):$ Let $\mathbf{p}, \mathbf{q} \in S$ and let $\gamma_{1}, \gamma_{2}$ be two curves in $S$, starting at $\mathbf{p}$ and ending at $\mathbf{q}$. If $\gamma$ is the curve which follows $\gamma_{1}$ and comes back around $\gamma_{2}$, so that we have returned to $\mathbf{p}$ then, by assumption and [[Line Integral#Remark 55]],
$$
0=\int_{\gamma} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}=\int_{\gamma_{1}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}-\int_{\gamma_{2}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r} \Longrightarrow \int_{\gamma_{1}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}=\int_{\gamma_{2}} \mathbf{F}(\mathbf{r}) \cdot \mathrm{d} \mathbf{r}
$$
and the line integral of $\mathbf{F}$ from $\mathbf{p}$ to $\mathbf{q}$ is independent of the choice of path taken.