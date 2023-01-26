## Surface Area
#MVC 
### Definition
Let $\mathbf{r}: U \rightarrow \mathbb{R}^{3}$ be a smooth parameterized [[surface]] with
$$
\mathbf{r}(u, v)=(x(u, v), y(u, v), z(u, v))
$$
and consider the small element of the plane that is bounded by the co-ordinate lines $u=u_{0}$ and $u=u_{0}+\delta u$ and $v=v_{0}$ and $v=v_{0}+\delta v$. Then $\mathbf{r}$ maps this to a small region of the surface $\mathbf{r}(U)$ and we are interested in calculating the surface area of this small region. Note
$$
\begin{array}{l}
\mathbf{r}(u+\delta u, v)-\mathbf{r}(u, v) \approx \frac{\partial \mathbf{r}}{\partial u}(u, v) \delta u \\
\mathbf{r}(u, v+\delta v)-\mathbf{r}(u, v) \approx \frac{\partial \mathbf{r}}{\partial v}(u, v) \delta v
\end{array}
$$
Recall that the area of a parallelogram with sides a and $\mathbf{b}$ is $|\mathbf{a} \wedge \mathbf{b}| .$ So the element of surface area we are considering is approximately
$$
\left|\frac{\partial \mathbf{r}}{\partial u} \delta u \wedge \frac{\partial \mathbf{r}}{\partial v} \delta v\right|=\left|\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right| \delta u \delta v
$$
Thus, at this point we proceed as with double integrals. Partitioning $U$ by smaller and smaller elements, of area $\delta A=\delta u \delta v$, we have in the limit $\delta A \rightarrow 0$
$$
\lim _{\text {elements }}\left|\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right| \delta u \delta v \stackrel{\text { def }}{=} \iint_{U}\left|\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right| \mathrm{d} u \mathrm{~d} v
$$
This gives the **surface area of the parameterized [[surface]]**; as with double integrals the pre-limit summation can be weighted with a scalar function $\psi(\mathbf{r}(u, v))$ evaluated at the centre of the elements to yield
$$
\color{yellow}
\text{Area of surface }\textbf{r}=
\iint_{U} \psi(\mathbf{r}(u, v))\left|\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right| \mathrm{d} u \mathrm{~d} v.
$$

### Definition: Infinitesimal Part
>[[dS]]

We will often write
$$
\mathrm{d} S=\left|\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right| \mathrm{d} u \mathrm{~d} v
$$
to denote an infinitesimal part of [[surface area]]. We will also write
$$
\mathrm{d} \mathbf{S}=\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v} \mathrm{~d} u \mathrm{~d} v
$$
This is also commonly written as $\mathbf{n} \mathrm{d} S$ where $\mathbf{n}$ is the choice of [unit normal](Surface#Definition%2035) in the direction of $\partial \mathbf{r} / \partial u \wedge \partial \mathbf{r} / \partial v$.

### Proposition 37
#TBV 
>The [[surface area]] of $\mathbf{r}(U)$ is **independent** of the choice of parameterization.
#### Proof
Let $\Sigma=\mathbf{r}(U)=\mathbf{s}(W)$ be two different parameterizations of a surface $X ;$ take $u, v$ as the co-ordinates on $U$ and $p, q$ as the co-ordinates on $W .$ Let $f=\left(f_{1}, f_{2}\right): U \rightarrow W$ be the co-ordinate change map - i.e. for any $(u, v) \in U$ we have
$$
\mathbf{r}(u, v)=\mathbf{s}(f(u, v))=\mathbf{s}\left(f_{1}(u, v), f_{2}(u, v)\right)=\mathbf{s}(p, q).
$$

Then
$$
\frac{\partial \mathbf{r}}{\partial u}=\frac{\partial \mathbf{s}}{\partial p} \frac{\partial f_{1}}{\partial u}+\frac{\partial \mathbf{s}}{\partial q} \frac{\partial f_{2}}{\partial u}, \quad \frac{\partial \mathbf{r}}{\partial v}=\frac{\partial \mathbf{s}}{\partial p} \frac{\partial f_{1}}{\partial v}+\frac{\partial \mathbf{s}}{\partial q} \frac{\partial f_{2}}{\partial v}
$$
Hence
$$
\begin{aligned}
\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v} &=\frac{\partial \mathbf{s}}{\partial p} \frac{\partial f_{1}}{\partial u} \wedge \frac{\partial \mathbf{s}}{\partial q} \frac{\partial f_{2}}{\partial v}+\frac{\partial \mathbf{s}}{\partial q} \frac{\partial f_{2}}{\partial u} \wedge \frac{\partial \mathbf{s}}{\partial p} \frac{\partial f_{1}}{\partial v} \\
&=\left(\frac{\partial f_{1}}{\partial u} \frac{\partial f_{2}}{\partial v}-\frac{\partial f_{1}}{\partial v} \frac{\partial f_{2}}{\partial u}\right) \frac{\partial \mathbf{s}}{\partial p} \wedge \frac{\partial \mathbf{s}}{\partial q} \\
&=\frac{\partial(p, q)}{\partial(u, v)} \frac{\partial \mathbf{s}}{\partial p} \wedge \frac{\partial \mathbf{s}}{\partial q}
\end{aligned}
$$
Finally
$$
\begin{aligned}
\iint_{U}\left|\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v}\right| \mathrm{d} u \mathrm{~d} v &=\iint_{U}\left|\frac{\partial(p, q)}{\partial(u, v)} \frac{\partial \mathbf{s}}{\partial p} \wedge \frac{\partial \mathbf{s}}{\partial q}\right| \mathrm{d} u \mathrm{~d} v \\
&=\iint_{U}\left|\frac{\partial \mathbf{s}}{\partial p} \wedge \frac{\partial \mathbf{s}}{\partial q}\right|\left|\frac{\partial(p, q)}{\partial(u, v)}\right| \mathrm{d} u \mathrm{~d} v \\
&=\iint_{W}\left|\frac{\partial \mathbf{s}}{\partial p} \wedge \frac{\partial \mathbf{s}}{\partial q}\right| \mathrm{d} p \mathrm{~d} q
\end{aligned}
$$
by the [two-dimensional rule for the change of variables](Change%20of%20Variables#Theorem%2016) in integrals.