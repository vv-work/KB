## Gauss' Flux Theorem
#MVC 
For a smooth and bounded region $R$, which contains matter of total mass $M$, then
$$
\iint_{\partial R} \mathbf{f} \cdot \mathrm{d} \mathbf{S}=-4 \pi G M.
$$
This result is in fact equivalent to [[Poisson's equation]].
### Proof
[[Poisson's equation]] gives us that
$$
\nabla^{2} \phi=-4 \pi G \rho
$$
where $\rho(\mathbf{r})$ is the density of the matter. Applying the [[Divergence Theorem]] we have
$$
\iint_{\partial R} \mathbf{f} \cdot \mathrm{d} \mathbf{S}=\iiint_{R} \nabla \cdot \mathbf{f} \mathrm{d} V=\iiint_{R} \nabla^{2} \phi \mathrm{d} V=-4 \pi G \iiint_{R} \rho \mathrm{d} V=-4 \pi G M
$$
Conversely suppose that we know
$$
\iint_{\partial R} \mathbf{f} \cdot \mathrm{d} \mathbf{S}=-4 \pi G M
$$
for any bounded region $R$. Then
$$
\iiint_{R} \nabla^{2} \phi \mathrm{d} V=-4 \pi G \iiint_{R} \rho \mathrm{d} V
$$
and so $\iiint_{R}\left(\nabla^{2} \phi+4 \pi G \rho\right) \mathrm{d} V=0$ for any bounded region $R$.
Hence (at least if $\nabla^{2} \phi$ and $\rho$ are piecewise continuous) we have
$$
\nabla^{2} \phi+4 \pi G \rho \equiv 0
$$