## Divergence
#MVC 
### Definition
Let $\mathbf{F}: \mathbb{R}^{3} \rightarrow \mathbb{R}^{3}$ be a vector field with $\mathbf{F}=\left(F_{1}, F_{2}, F_{3}\right) .$ Then the [[divergence]] of $\mathbf{F}$ written $\operatorname{div} \mathbf{F}$ or $\nabla \cdot \mathbf{F}$ equals
$$
\operatorname{div} \mathbf{F}=\nabla \cdot \mathbf{F}=\frac{\partial F_{1}}{\partial x}+\frac{\partial F_{2}}{\partial y}+\frac{\partial F_{3}}{\partial z} .
$$
> Div takes vector fields to scalar fields.

### Identities
$\nabla \cdot(\mathbf{A}+\mathbf{B})=\nabla \cdot \mathbf{A}+\nabla \cdot \mathbf{B}$
$\nabla \cdot(\psi \mathbf{A})=\psi \nabla \cdot \mathbf{A}+\mathbf{A} \cdot \nabla \psi$
$\nabla \cdot(\mathbf{A} \times \mathbf{B})=(\nabla \times \mathbf{A}) \cdot \mathbf{B}-(\nabla \times \mathbf{B}) \cdot \mathbf{A}$

### Divergence in Different Coordinate Systems
#### [[Plane Polar Coordinates]] $(r,\theta)$
$$
\nabla \cdot \mathbf{F}=\frac{1}{r} \frac{\partial}{\partial r}\left(r F_{r}\right)+\frac{1}{r} \frac{\partial F_{\theta}}{\partial \theta} .
$$
#### [[Cylindrical Polar Coordinates]] $(\rho,\varphi,z)$

$$
\nabla \cdot\mathbf{A} =
\frac{1}{\rho} \frac{\partial\left(\rho\mathbf{A}_{\rho}\right)}{\partial \rho}+\frac{1}{\rho} \frac{\partial\mathbf{A}_{\varphi}}{\partial \varphi}+\frac{\partial\mathbf{A}_{z}}{\partial z}
$$
#### [[Spherical Polar Coordinates]] $(r,\theta,\varphi)$ 
$$
\begin{aligned}
\nabla \cdot\mathbf{A} = & \frac{1}{r \sin \theta}\left(\frac{\partial}{\partial \theta}\left(\mathbf{A}_{\varphi} \sin \theta\right)-\frac{\partial\mathbf{A}_{\theta}}{\partial \varphi}\right) \hat{\mathbf{r}} \\
&+  \frac{1}{r}\left(\frac{1}{\sin \theta} \frac{\partial\mathbf{A}_{r}}{\partial \varphi}-\frac{\partial}{\partial r}\left(r\mathbf{A}_{\varphi}\right)\right) \hat{\boldsymbol{\theta}} \\
&+  \frac{1}{r}\left(\frac{\partial}{\partial r}\left(r\mathbf{A}_{\theta}\right)-\frac{\partial\mathbf{A}_{r}}{\partial \theta}\right) \hat{\boldsymbol{\varphi}}
\end{aligned}
$$
