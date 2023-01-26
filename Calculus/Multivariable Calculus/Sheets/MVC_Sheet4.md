# MVC4
#ProblemSheet #MVC 
>*[[Div Grad Curl]]. Physical Interpretation. Identities.*

1. Show directly that $\nabla^{2}(\phi \psi)=\phi \nabla^{2} \psi+2 \nabla \phi \cdot \nabla \psi+\psi \nabla^{2} \phi$ for scalar fields $\phi$ and $\psi$. ==[[Laplacian]]== [Solutions to 1](#(1))
2. (i) Let $\phi(x, y, z)=y^{2}-x z$ and $\mathbf{f}(x, y, z)=\left(z^{2}, x^{2}, y^{2}\right)$. Find $\nabla \phi$ and $\nabla \cdot \mathbf{f}$.
(ii) For the orthonormal basis $\mathbf{e}_{1}=(0,-1,0), \mathbf{e}_{2}=(1,0,-1) / \sqrt{2}, \mathbf{e}_{3}=(1,0,1) / \sqrt{2}$, create new
co-ordinates $X, Y, Z$ such that
$$
X \mathbf{e}_{1}+Y \mathbf{e}_{2}+Z \mathbf{e}_{3}=x \mathbf{i}+y \mathbf{j}+z \mathbf{k}
$$
Determine $x, y, z$ in terms of $X, Y, Z$.
(iii) Find $\Phi, F_{1}, F_{2}, F_{3}$ such that $\Phi(X, Y, Z)=\phi(x, y, z)$ and $F_{1} \mathbf{e}_{1}+F_{2} \mathbf{e}_{2}+F_{3} \mathbf{e}_{3}=f_{1} \mathbf{i}+f_{2} \mathbf{j}+f_{3} \mathbf{k}$.
Verify, by direct calculation, that
$$
\nabla \phi=\Phi_{X} \mathbf{e}_{1}+\Phi_{Y} \mathbf{e}_{2}+\Phi_{Z} \mathbf{e}_{3} ; \quad \nabla \cdot \mathbf{f}=\left(F_{1}\right)_{X}+\left(F_{2}\right)_{Y}+\left(F_{3}\right)_{Z}
$$
3. Let $r$ and $\theta$ denote [[plane polar coordinates]] and set $\mathbf{e}_{r}=(\cos \theta, \sin \theta, 0)$ and $\mathbf{e}_{\theta}=(-\sin \theta, \cos \theta, 0)$.
Let $\mathbf{F}(r, \theta)=F_{r} \mathbf{e}_{r}+F_{\theta} \mathbf{e}_{\theta}$ be a vector field. Prove that
$$
\nabla \cdot \mathbf{F}=\frac{1}{r} \frac{\partial}{\partial r}\left(r F_{r}\right)+\frac{1}{r} \frac{\partial F_{\theta}}{\partial \theta} .
$$
4. Let $\mathbf{f}(x, y, z)=\left(y /\left(x^{2}+y^{2}\right),-x /\left(x^{2}+y^{2}\right), 0\right)$ where $(x, y) \neq(0,0)$.
(i) Show that $\operatorname{curl} \mathbf{f}=\mathbf{0}$.
(ii) Find $\int_{C} \mathbf{f} \cdot \mathrm{d} \mathbf{r}$ for each of the following closed curves $C$.
(a) $C$ is parametrised by $\mathbf{r}(t)=(\cos t, \sin t, 0)$ for $0 \leqslant t \leqslant 2 \pi$.
(b) $C$ is parametrised by
$$
\mathbf{r}(t)=\left\{\begin{array}{cc}
(\cos t, \sin t, t) & 0 \leqslant t \leqslant 4 \pi \\
(1,0,8 \pi-t) & 4 \pi \leqslant t \leqslant 8 \pi
\end{array}\right.
$$
(c) $C$ is the square with vertices $(0,1),(1,1),(1,2),(0,2)$ with an anticlockwise orientation.
(iii) Find a scalar field $\phi$ such that $\mathbf{f}=\nabla \phi$ on $R_{1}=\{(x, y, z): y>0\}$. How does the existence of $\phi$ relate to your answer to 4(ii)c?
(iv) Show that there does not exist $\psi$ such that $\mathbf{f}=\nabla \psi$ on $R_{2}=\{(x, y, z):(x, y) \neq(0,0)\}$.
5. (i) With $\mathbf{f}$ as in Exercise 4 , show that $\operatorname{div} \mathbf{f}=0$.
(ii) Suppose that a particle $(x(t), y(t))$ moves according to the flow
$$
\mathrm{d} x / \mathrm{d} t=y /\left(x^{2}+y^{2}\right), \quad \mathrm{d} y / \mathrm{d} t=-x /\left(x^{2}+y^{2}\right) .
$$
Show that, on changing to [[plane polar coordinates]] $(r, \theta)$ these differential equations become
$$
\mathrm{d} r / \mathrm{d} t=0, \quad \mathrm{~d} \theta / \mathrm{d} t=-1 / r^{2}
$$
(iii) Suppose that particles initially occupy the region $R_{0}=\{(r, \theta): 0<a<r<b, 0<\theta<\alpha<\pi / 2\}$. If the particles move according to the above flow, describe the region $R_{t}$ which they occupy a short time $t$ afterwards. Sketch $R_{0}$ and $R_{t}$, and show that the regions have the same area.

6. (Optional) (i) In [[spherical polar coordinates]]
$$
\mathbf{r}(r, \theta, \phi)=(r \sin \theta \cos \phi, r \sin \theta \sin \phi, r \cos \theta)
$$
Show that we can write
$$
\mathrm{d} \mathbf{r}=h_{r} \mathrm{~d} r \mathbf{e}_{r}+h_{\theta} \mathrm{d} \theta \mathbf{e}_{\theta}+h_{\phi} \mathrm{d} \phi \mathbf{e}_{\phi}
$$
where $\mathbf{e}_{r}, \mathbf{e}_{\theta}, \mathbf{e}_{\phi}$ are a right-handed orthonormal basis and $h_{r}, h_{\theta}, h_{\phi}>0 .$ Show that $h_{r} h_{\theta} h_{\phi}=r^{2} \sin \theta=\partial(x, y, z) / \partial(r, \theta, \phi) .$
(ii) More generally $\mathbf{r}\left(u_{1}, u_{2}, u_{3}\right)$ is a parametrization of space by orthogonal curvilinear co-ordinates if
$$
\mathrm{d} \mathbf{r}=h_{1} \mathrm{~d} u_{1} \mathbf{e}_{1}+h_{2} \mathrm{~d} u_{2} \mathbf{e}_{2}+h_{3} \mathrm{~d} u_{3} \mathbf{e}_{3}
$$
where $\mathbf{e}_{1}, \mathbf{e}_{2}, \mathbf{e}_{3}$ are a right-handed orthonormal basis. Show in this case that
$$
\frac{\partial(x, y, z)}{\partial\left(u_{1}, u_{2}, u_{3}\right)}=h_{1} h_{2} h_{3}
$$
(iii) Show further for a scalar field $\Phi\left(u_{1}, u_{2}, u_{3}\right)$ that
$$
\nabla \Phi=\frac{1}{h_{1}} \frac{\partial \Phi}{\partial u_{1}} \mathbf{e}_{1}+\frac{1}{h_{2}} \frac{\partial \Phi}{\partial u_{2}} \mathbf{e}_{2}+\frac{1}{h_{3}} \frac{\partial \Phi}{\partial u_{3}} \mathbf{e}_{3}
$$

### Solutions
#### (1)
$$
\begin{aligned}
\nabla^2 (\phi \psi) &=\nabla \cdot(\phi \nabla \psi)+\nabla \cdot(\psi \nabla \phi) \\
&=\nabla \phi \nabla \psi+\phi \nabla^{2} \psi+\nabla \psi D \phi+\psi \nabla^{2} \phi \\
&=2 \nabla \phi \nabla \psi+\phi \nabla^{2} \psi+\psi \nabla^{2} \phi .
\end{aligned}
$$

#### (4)
(iii)
Consider $\phi$ as a potential of $\bf f$. Then as the function in 4(ii)(c) is a closed curve contained in $R_1$, then $\int_C \mathbf{f}\mathrm{d}r=\int_C\nabla\phi \mathrm{d}r=0$.
(iv)
A counterexample in 4(ii)(b).

