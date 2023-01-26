## Gravitational Potential
#MVC 
### Newton's Law of Gravity 
>[[Newton's Law of Universal Gravitation]]

The gravitational field associated with a point mass $M$ at the origin $O$ is
$$
\mathbf{f}=-\frac{G M}{r^{3}} \mathbf{r}=-\frac{G M}{r^{2}} \mathbf{e}_{r}=\nabla\left(\frac{G M}{r}\right) .
$$
The gravitational force on a particle of mass $m$ at the point $\mathbf{r}$
$$
\mathbf{F}=-\frac{G M m}{r^{2}} \mathbf{e}_{r}
$$
Here G is the [[Newton's gravitational constant]].
Note that the gravitational field $\mathbf{f}$ is [[conservative]] with [[gravitational potential]]
$$
\phi=\frac{G M}{r} .
$$
Recall that potentials are determined by the field only up to a constant. This choice of [[potential]] is such that $\phi \rightarrow 0$ as $r \rightarrow \infty$. In addition to  $\operatorname{curl}\mathbf{f}=\mathbf{0}$, we also have that that
$$
\operatorname{div} \mathbf{f}=\nabla^{2} \phi=\frac{1}{r^{2}} \frac{\mathrm{d}}{\mathrm{d} r}\left(r^{2} \frac{\mathrm{d} \phi}{\mathrm{d} r}\right)=\frac{1}{r^{2}} \frac{\mathrm{d}}{\mathrm{d} r}\left(r^{2}\left(\frac{-G M}{r^{2}}\right)\right)=0, \quad r \neq 0
$$
and 
$$
\nabla^{2} \phi=0 \quad \text{ for gravitational potential in vacuo.}
$$
This is physically intuitive as, aside from at the origin, there is no other mass contributing to the gravitational field.

### Proposition 128
The [[gravitational potential]] $\phi=G M / r$ is the amount of work gravity does per unit mass to bring a point object from $\infty$ to $\mathbf{r}$.
#### Proof
The [[work done]] by gravity to bring a unit point mass from $\infty$ to $\mathbf{r}$ is
$$
\frac{1}{m} \int_{\infty}^{\mathbf{r}} \mathbf{F} \cdot \mathrm{d} \mathbf{r}=\int_{\infty}^{\mathbf{r}} \mathbf{f} \cdot \mathrm{d} \mathbf{r}=[\phi(\mathbf{r})-\phi(\infty)]=\phi(\mathbf{r}) .
$$

### Definition: Gravitational Potential Energy
>The gravitational potential energy of a point mass $m$ at $\mathbf{r}$ equals $-m \phi(\mathbf{r})$.

### Discrete Case
Given $n$ particles of mass $M_{i}$ at points with position vectors $\mathbf{r}_{i}$, the gravitational potential $\phi$ and field $\mathbf{f}$ are then given by
$$
\phi(\mathbf{p})=\sum_{i=1}^{n} \frac{G M_{i}}{\left|\mathbf{p}-\mathbf{r}_{i}\right|}, \quad \mathbf{f}(\mathbf{p})=-\sum_{i=1}^{n} \frac{G M_{i}\left(\mathbf{p}-\mathbf{r}_{i}\right)}{\left|\mathbf{p}-\mathbf{r}_{i}\right|^{3}}
$$
### Continuous Case
Suppose instead, in the continuous case, we have matter of density $\rho(\mathbf{r})$ occupying a region $R$; then the potential $\phi$ and field $\mathbf{f}$ are given by
$$
\phi(\mathbf{p})=\iiint_{R} \frac{G \rho(\mathbf{r}) \mathrm{d} V}{|\mathbf{p}-\mathbf{r}|}, \quad \mathbf{f}(\mathbf{p})=-\iiint_{R} \frac{G \rho(\mathbf{r})(\mathbf{p}-\mathbf{r}) \mathrm{d} V}{|\mathbf{p}-\mathbf{r}|^{3}}
$$
In the above we have an integral relationship between the mass density $\rho$ and the potential $\phi$. Our objective is find an equivalent relationship in terms of a partial differential equation. To proceed we first need to informally consider the Dirac delta function.