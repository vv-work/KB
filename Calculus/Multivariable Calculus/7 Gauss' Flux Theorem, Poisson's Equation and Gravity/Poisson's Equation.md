## Poisson's Equation
#MVC 
### Poisson's Equation
Let $\phi$ be the [[gravitational potential]] associated with a non-uniform material of density $\rho(\mathbf{r})$ occupying a region $R$. Then
$$
\nabla^{2} \phi=-4 \pi G \rho(\mathbf{r})
$$
#### Proof
#NonExaminable 
The gravitational field associated with this matter is given by
$$
\mathbf{f}(\mathbf{p})=\nabla \phi(\mathbf{p})=-\iiint_{R} \frac{G \rho(\mathbf{r})(\mathbf{p}-\mathbf{r})}{|\mathbf{p}-\mathbf{r}|^{3}} \mathrm{~d} V
$$
Then $\nabla^{2} \phi(\mathbf{p})$ equals
$$
\nabla \cdot \mathbf{f}(\mathbf{p})=-\iiint_{R} G \rho(\mathbf{r}) \nabla \cdot\left(\frac{(\mathbf{p}-\mathbf{r})}{|\mathbf{p}-\mathbf{r}|^{3}}\right) \mathrm{d} V=-\iiint_{R} G \rho(\mathbf{r}) \delta(\mathbf{r}-\mathbf{p}) \mathrm{d} V=-4 \pi G \rho(\mathbf{p}).
$$
### Example 132
A spherical shell, centred at $O$ and with internal and external radii $a$ and $b$ respectively, has matter distribution with density $\rho$ given by
$$
\rho(r)=\left\{\begin{array}{cc}
1 / r & 0<a \leqslant r \leqslant b \\
0 & \text { otherwise. }
\end{array}\right.
$$
Find the gravitational potential at all points in space. [You may assume that the spherically symmetric form of Laplace's equation is such that 
$$
\nabla^{2} \phi(r)=
\frac{1}{r^{2}} \frac{\mathrm{d}}{\mathrm{d} r}\left(r^{2} \frac{\mathrm{d} \phi}{\mathrm{d} r}\right) \cdot
$$
#### Solution
##### Method One - Poisson's Equation.
By [[Poisson's equation]] gravitational potential $\phi$ satisfies
$$
\nabla^{2} \phi=\frac{1}{r^{2}} \frac{\mathrm{d}}{\mathrm{d} r}\left(r^{2} \frac{\mathrm{d} \phi}{\mathrm{d} r}\right)=\left\{\begin{array}{cc}
0 & r<a \\
-4 \pi G / r & a<r<b \\
0 & b<r
\end{array}\right.
$$
Solving $\nabla^{2} \phi=0$ in the region $r<a$ we get
$$
\begin{aligned}
\frac{1}{r^{2}} \frac{\mathrm{d}}{\mathrm{d} r}\left(r^{2} \frac{\mathrm{d} \phi}{\mathrm{d} r}\right) &=0, \\
& \Longrightarrow r^{2} \frac{\mathrm{d} \phi}{\mathrm{d} r}=-A \Longrightarrow \frac{\mathrm{d} \phi}{\mathrm{d} r}=\frac{-A}{r^{2}}, \\
& \Longrightarrow \phi=\frac{A}{r}+B
\end{aligned}
$$
Similarly $\phi=E / r+B$ in the region $r>b$ for constants $E$ and $F$
In the middle region $a<r<b$ we have
$$
\begin{aligned}
\frac{1}{r^{2}} \frac{\mathrm{d}}{\mathrm{d} r}\left(r^{2} \frac{\mathrm{d} \phi}{\mathrm{d} r}\right)=& \frac{-4 \pi G}{r} \\
& \Longrightarrow \quad \frac{\mathrm{d}}{\mathrm{d} r}\left(r^{2} \frac{\mathrm{d} \phi}{\mathrm{d} r}\right)=-4 \pi G r \Longrightarrow r^{2} \frac{\mathrm{d} \phi}{\mathrm{d} r}=-2 \pi G r^{2}-C \\
& \Longrightarrow \frac{\mathrm{d} \phi}{\mathrm{d} r}=-2 \pi G-\frac{C}{r^{2}} \\
& \Longrightarrow \phi=-2 \pi G r+\frac{C}{r}+D .
\end{aligned}
$$
So, for constants $A, B, C, D, E, F$, we have
$$
\phi(r)=\left\{\begin{array}{cc}
\frac{A}{r}+B & r<a \\
-2 \pi G r+\frac{C}{r}+D & a<r<b, \\
\frac{E}{r}+F & b<r .
\end{array}\right.
$$
We can use certain conditions now to determine these constants:
(i) because of physical considerations $\phi$ is finite at $r=0$,
(ii) $\phi$ is both continuous and differentiable at both $r=a$ and at $r=b$,
(iii) $\phi$ is unique only up to addition by a constant $-$ to specify $\phi$ uniquely we typically stipulate that $\phi(r) \rightarrow 0$ as $r \rightarrow \infty$.
From condition (i) we have that $A=0$ and from (iii) that $F=0$. The two boundary conditions at $r=a$, namely that $\phi\left(a_{-}\right)=\phi\left(a_{+}\right)$ and $\phi^{\prime}\left(a_{-}\right)=\phi^{\prime}\left(a_{+}\right)$, tell us that
$$
B=-2 \pi G a+\frac{C}{a}+D, \quad 0=-2 \pi G-\frac{C}{a^{2}} \text { . }
$$
Similar conditions at $r=b$ give us that
$$
-2 \pi G b+\frac{C}{b}+D=\frac{E}{b}, \quad-2 \pi G-\frac{C}{b^{2}}=-\frac{E}{b^{2}} \text { . }
$$
We have four linear equations in the four unknowns $B, C, D, E$ in terms of the radii $a, b$ and the gravitational constant $G$. The second equation immediately gives $C$ and thus the fourth equation gives $E$. Then the third equation gives $D$ and the first finally gives $B$. Thus one can then deduce:
$$
\phi(r)=\left\{\begin{array}{cc}
4 \pi G(b-a) & r<a \\
-2 \pi G r-\frac{2 \pi G a^{2}}{r}+4 \pi G b & a<r<b, \\
\frac{2 \pi G\left(b^{2}-a^{2}\right)}{r} & b<r .
\end{array}\right.
$$
Because of the symmetry of the above problem, we can take another approach using [[Gauss' Flux Theorem]].

##### Method Two - Gauss' Flux Theorem.
Alternatively, we may use [[Gauss' Flux Theorem]] applied to concentric spheres centred on the shell's centre.

Now, $\phi$ is only dependent on $r$ and, so, is constant on the sphere $r=R$, which has surface area $4 \pi R^{2}$
So, if we apply the flux theorem to the region $r \leqslant R$ we have
$$
\iint_{r=R} \nabla \phi \cdot \mathrm{d} \mathbf{S}=\iint_{r=R} \phi^{\prime}(R) \mathbf{e}_{r} \cdot \mathrm{d} \mathbf{S}=\iint_{r=R} \phi^{\prime}(R) \mathrm{d} S=4 \pi R^{2} \phi^{\prime}(R)=-4 \pi G M(R)
$$
where $M(R)$ is the total mass within the region $r \leqslant R$. For $a \leqslant R \leqslant b$ we have
$$
\begin{aligned}
M(R) &=\int_{r=a}^{R} \int_{\theta=0}^{\pi} \int_{\alpha=0}^{2 \pi} \frac{1}{r} r^{2} \sin \theta \mathrm{d} \alpha \mathrm{d} \theta \mathrm{d} r \\
&=2 \pi \times[-\cos \theta]_{0}^{\pi} \times \int_{r=a}^{R} r \mathrm{~d} r \\
&=2 \pi\left(R^{2}-a^{2}\right)
\end{aligned}
$$
Hence
$$
\phi^{\prime}(R)=\left\{\begin{array}{cc}
0 & R<a \\
2 \pi G\left(\frac{a^{2}}{R^{2}}-1\right) & a<R<b \\
\frac{2 \pi G\left(a^{2}-b^{2}\right)}{R^{2}} & b<R
\end{array}\right.
$$
If we integrate we have
$$
\phi(R)=\left\{\begin{array}{cc}
A & R<a \\
B-2 \pi G\left(\frac{a^{2}}{R}+R\right) & a<R<b, \\
\frac{2 \pi G\left(b^{2}-a^{2}\right)}{R}+C & b<R
\end{array}\right.
$$
As $\phi(\infty)=0$ then $C=0 .$ As $\phi\left(b_{-}\right)=\phi\left(b_{+}\right)$ then
$$
B-2 \pi G\left(\frac{a^{2}}{b}+b\right)=\frac{2 \pi G\left(b^{2}-a^{2}\right)}{b} \Longrightarrow B=4 \pi G b
$$
Finally as $\phi\left(a_{-}\right)=\phi\left(a_{+}\right)$ then
$$
A=4 \pi G b-2 \pi G\left(\frac{a^{2}}{a}+a\right)=4 \pi G(b-a)
$$
and we have the same expressions for $\phi$ as were achieved by the previous method.