## Laplacian
#MVC 
### Definition
For any scalar field $\phi$ we have
$$
\operatorname{div}(\operatorname{grad} \phi)=\frac{\partial}{\partial x}\left(\frac{\partial \phi}{\partial x}\right)+\frac{\partial}{\partial y}\left(\frac{\partial \phi}{\partial y}\right)+\frac{\partial}{\partial z}\left(\frac{\partial \phi}{\partial z}\right)=\frac{\partial^{2} \phi}{\partial x^{2}}+\frac{\partial^{2} \phi}{\partial y^{2}}+\frac{\partial^{2} \phi}{\partial z^{2}},
$$
which is the [[Laplacian]]. As
$$
\text { div grad }=\nabla \cdot \nabla
$$
then we often write
$$
\nabla^{2} \phi=\frac{\partial^{2} \phi}{\partial x^{2}}+\frac{\partial^{2} \phi}{\partial y^{2}}+\frac{\partial^{2} \phi}{\partial z^{2}}
$$
Also, for vector fields $\mathbf{F}=\left(F_{1}, F_{2}, F_{3}\right)$ with respect to a Cartesian coordinate system, it is common to write
$$
\nabla^{2} \mathbf{F}=\left(\nabla^{2} F_{1}, \nabla^{2} F_{2}, \nabla^{2} F_{3}\right)
$$
Thus the [[Laplacian]] can both take scalar fields to scalar fields and vector fields to vector fields.
### Identities
$$
\begin{aligned}
\nabla^2 (\phi \psi) &=\nabla \cdot(\phi \nabla \psi)+\nabla \cdot(\psi \nabla \phi) \\
&=\nabla \phi \nabla \psi+\phi \nabla^{2} \psi+\nabla \psi D \phi+\psi \nabla^{2} \phi \\
&=2 \nabla \phi \nabla \psi+\phi \nabla^{2} \psi+\psi \nabla^{2} \phi .
\end{aligned}
$$

### Scalar Laplacian in Different Coordinate Systems
#### [[Cylindrical Polar Coordinates]] $(\rho,\varphi,z)$
$$
\nabla ^2 f = \frac{1}{\rho} \frac{\partial}{\partial \rho}\left(\rho \frac{\partial f}{\partial \rho}\right)+\frac{1}{\rho^{2}} \frac{\partial^{2} f}{\partial \varphi^{2}}+\frac{\partial^{2} f}{\partial z^{2}}
$$
#### [[Spherical Polar Coordinates]] $(r,\theta,\varphi)$ 
$$
\nabla ^2 f = \frac{1}{r^{2}} \frac{\partial}{\partial r}\left(r^{2} \frac{\partial f}{\partial r}\right)+\frac{1}{r^{2} \sin \theta} \frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial f}{\partial \theta}\right)+\frac{1}{r^{2} \sin ^{2} \theta} \frac{\partial^{2} f}{\partial \varphi^{2}}
$$