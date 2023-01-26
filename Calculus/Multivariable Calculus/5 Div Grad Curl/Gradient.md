## Gradient
#MVC 
### Definition
Let $\phi: \mathbb{R}^{3} \rightarrow \mathbb{R}$ be a scalar field. Then the [[gradient]] of $\phi$ written $\operatorname{grad} \phi$ or $\nabla \phi$ equals
$$
\operatorname{grad} \phi=\nabla \phi=\left(\frac{\partial \phi}{\partial x}, \frac{\partial \phi}{\partial y}, \frac{\partial \phi}{\partial z}\right)
$$
>Grad takes scalar fields to vector fields.

### Identities
$\nabla(\psi+\phi)=\nabla \psi+\nabla \phi$
$\nabla(\psi \phi)=\phi \nabla \psi+\psi \nabla \phi$
$\nabla(\psi \mathbf{A})=\nabla \psi \otimes \mathbf{A}+\psi \nabla \mathbf{A}$
$\nabla(\mathbf{A} \cdot \mathbf{B})=(\mathbf{A} \cdot \nabla) \mathbf{B}+(\mathbf{B} \cdot \nabla) \mathbf{A}+\mathbf{A} \times(\nabla \times \mathbf{B})+\mathbf{B} \times(\nabla \times \mathbf{A})$

### Gradient in Different Coordinate Systems
#### [[Cylindrical Polar Coordinates]] $(\rho,\varphi,z)$
$$
\nabla f=\frac{\partial f}{\partial \rho} \hat{\boldsymbol{\rho}}+\frac{1}{\rho} \frac{\partial f}{\partial \varphi} \hat{\boldsymbol{\varphi}}+\frac{\partial f}{\partial z} \hat{\mathbf{z}}
$$
#### [[Spherical Polar Coordinates]] $(r,\theta,\varphi)$ 
$$
\nabla f=\frac{\partial f}{\partial r} \hat{\mathbf{r}}+\frac{1}{r} \frac{\partial f}{\partial \theta} \hat{\boldsymbol{\theta}}+\frac{1}{r \sin \theta} \frac{\partial f}{\partial \varphi} \hat{\boldsymbol{\varphi}}
$$