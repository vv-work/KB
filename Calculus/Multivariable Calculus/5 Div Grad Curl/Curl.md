## Curl
#MVC 
### Definition
Let $\mathbf{F}: \mathbb{R}^{3} \rightarrow \mathbb{R}^{3}$ be a vector field with $\mathbf{F}=\left(F_{1}, F_{2}, F_{3}\right) .$ Then the curl of $\mathbf{F}$ written curl $\mathbf{F}$ or $\nabla \wedge \mathbf{F}$ equals
$$
\operatorname{curl} \mathbf{F}=\nabla \wedge \mathbf{F}=\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
F_{1} & F_{2} & F_{3}
\end{array}\right|=\left(\begin{array}{c}
\frac{\partial F_{3}}{\partial y}-\frac{\partial F_{2}}{\partial z} \\
\frac{\partial F_{1}}{\partial z}-\frac{\partial F_{3}}{\partial x} \\
\frac{\partial F_{2}}{\partial x}-\frac{\partial F_{1}}{\partial y}
\end{array}\right).
$$
>Curl takes vector fields to vector fields.

### Identities
$\nabla \times(\mathbf{A}+\mathbf{B})=\nabla \times \mathbf{A}+\nabla \times \mathbf{B}$
$\nabla \times(\psi \mathbf{A})=\psi(\nabla \times \mathbf{A})+\nabla \psi \times \mathbf{A}$
$\nabla \times(\psi \nabla \phi)=\nabla \psi \times \nabla \phi$
$\nabla \times(\mathbf{A} \times \mathbf{B})=\mathbf{A}(\nabla \cdot \mathbf{B})-\mathbf{B}(\nabla \cdot \mathbf{A})+(\mathbf{B} \cdot \nabla) \mathbf{A}-(\mathbf{A} \cdot \nabla) \mathbf{B}$

---
- Div of Curl is 0: The Div of the Curl of any vector field is 0.
$\nabla \cdot(\nabla \times \mathbf{A})=0$
- Curl of Grad is $\bf0$: The Curl of the Grad of any continuously twice-differentiable scalar field $\varphi$ is $\bf0$.
$\nabla \times(\nabla \varphi)=\mathbf{0}$
- Curl of Curl:
$\nabla \times(\nabla \times \mathbf{A})=\nabla(\nabla \cdot \mathbf{A})-\nabla^{2} \mathbf{A}$

### [[2d-Curl]]
