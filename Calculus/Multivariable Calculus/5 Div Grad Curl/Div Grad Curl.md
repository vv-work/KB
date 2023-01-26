#MVC 

### Definition: Grad
Let $\phi: \mathbb{R}^{3} \rightarrow \mathbb{R}$ be a scalar field. Then the [[gradient]] of $\phi$ written $\operatorname{grad} \phi$ or $\nabla \phi$ equals
$$
\operatorname{grad} \phi=\nabla \phi=\left(\frac{\partial \phi}{\partial x}, \frac{\partial \phi}{\partial y}, \frac{\partial \phi}{\partial z}\right)
$$

### Definition: Div
Let $\mathbf{F}: \mathbb{R}^{3} \rightarrow \mathbb{R}^{3}$ be a vector field with $\mathbf{F}=\left(F_{1}, F_{2}, F_{3}\right) .$ Then the [[divergence]] of $\mathbf{F}$ written $\operatorname{div} \mathbf{F}$ or $\nabla \cdot \mathbf{F}$ equals
$$
\operatorname{div} \mathbf{F}=\nabla \cdot \mathbf{F}=\frac{\partial F_{1}}{\partial x}+\frac{\partial F_{2}}{\partial y}+\frac{\partial F_{3}}{\partial z} .
$$

### Definition: Curl
Let $\mathbf{F}: \mathbb{R}^{3} \rightarrow \mathbb{R}^{3}$ be a vector field with $\mathbf{F}=\left(F_{1}, F_{2}, F_{3}\right) .$ Then the [[curl]] of $\mathbf{F}$ written curl $\mathbf{F}$ or $\nabla \wedge \mathbf{F}$ equals
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

### Definition: Del
The differential operator
$$
\nabla=\left(\frac{\partial}{\partial x}, \frac{\partial}{\partial y}, \frac{\partial}{\partial z}\right)
$$
is called **[[del]]** or **nabla**.
### Definition: Laplacian
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

---
### Proposition 81
>Let $\mathbf{e}_{1}, \mathbf{e}_{2}, \mathbf{e}_{3}$ be a right-handed [[orthonormal basis]] of $\mathbb{R}^{3}$ with associated coordinates $X, Y, Z$ defined by the identity
>$$
X \mathbf{e}_{1}+Y \mathbf{e}_{2}+Z \mathbf{e}_{3}=x \mathbf{i}+y \mathbf{j}+z \mathbf{k}
\quad\color{yellow}\text{(5.1)}
>$$
Then
>$$
\mathbf{e}_{1} \frac{\partial}{\partial X}+\mathbf{e}_{2} \frac{\partial}{\partial Y}+\mathbf{e}_{3} \frac{\partial}{\partial Z}=\mathbf{i} \frac{\partial}{\partial x}+\mathbf{j} \frac{\partial}{\partial y}+\mathbf{k} \frac{\partial}{\partial z}.
>$$

#### Proof
From $(5.1)$ we have that
$$
\begin{aligned}
x &=\left(\mathbf{e}_{1} \cdot \mathbf{i}\right) X+\left(\mathbf{e}_{2} \cdot \mathbf{i}\right) Y+\left(\mathbf{e}_{3} \cdot \mathbf{i}\right) Z, \\
X &=\left(\mathbf{e}_{1} \cdot \mathbf{i}\right) x+\left(\mathbf{e}_{1} \cdot \mathbf{j}\right) y+\left(\mathbf{e}_{1} \cdot \mathbf{k}\right) z,
\end{aligned}
$$
and four other similar equations for $y, z, Y, Z$. It follows from the [[chain rule]] that
$$
\frac{\partial}{\partial X}=\frac{\partial x}{\partial X} \frac{\partial}{\partial x}+\frac{\partial y}{\partial X} \frac{\partial}{\partial y}+\frac{\partial z}{\partial X} \frac{\partial}{\partial z}=\left(\mathbf{e}_{1} \cdot \mathbf{i}\right) \frac{\partial}{\partial x}+\left(\mathbf{e}_{1} \cdot \mathbf{j}\right) \frac{\partial}{\partial y}+\left(\mathbf{e}_{1} \cdot \mathbf{k}\right) \frac{\partial}{\partial z}
$$
and hence
$$
\begin{aligned}
& \mathbf{e}_{1} \frac{\partial}{\partial X}+\mathbf{e}_{2} \frac{\partial}{\partial Y}+\mathbf{e}_{3} \frac{\partial}{\partial Z} \\
=& \mathbf{e}_{1}\left[\left(\mathbf{e}_{1} \cdot \mathbf{i}\right) \frac{\partial}{\partial x}+\left(\mathbf{e}_{1} \cdot \mathbf{j}\right) \frac{\partial}{\partial y}+\left(\mathbf{e}_{1} \cdot \mathbf{k}\right) \frac{\partial}{\partial z}\right]+\mathbf{e}_{2}[\ldots]+\mathbf{e}_{3}[\ldots] \\
=&\left[\mathbf{e}_{1}\left(\mathbf{e}_{1} \cdot \mathbf{i}\right)+\mathbf{e}_{2}\left(\mathbf{e}_{2} \cdot \mathbf{i}\right)+\mathbf{e}_{3}\left(\mathbf{e}_{3} \cdot \mathbf{i}\right)\right] \frac{\partial}{\partial x}+[\ldots] \frac{\partial}{\partial y}+[\ldots] \frac{\partial}{\partial z} \\
=& \mathbf{i} \frac{\partial}{\partial x}+\mathbf{j} \frac{\partial}{\partial y}+\mathbf{k} \frac{\partial}{\partial z}
\end{aligned}
$$
this last line follows from the orthonormality of the bases as
$$
\mathbf{i}=\alpha \mathbf{e}_{1}+\beta \mathbf{e}_{2}+\gamma \mathbf{e}_{3}
$$
leads to $\alpha=\mathbf{e}_{1} \cdot \mathbf{i}, \beta=\mathbf{e}_{2} \cdot \mathbf{i}, \gamma=\mathbf{e}_{3} \cdot \mathbf{i}$, by dotting the equation with $\mathbf{e}_{1}, \mathbf{e}_{2}, \mathbf{e}_{3}$ respectively.

### Corollary 82
>We calculate [grad](Gradient), [div](Divergence) and [[curl]] using the same formulae, irrespective of what right-handed orthonormal coordinate system we are using.

Let $\mathbf{f}: \mathbb{R}^{3} \rightarrow \mathbb{R}^{3}$ be a vector field given by $\mathbf{f}=\left(f_{1}, f_{2}, f_{3}\right)$, let $\phi: \mathbb{R}^{3} \rightarrow \mathbb{R}$ be a
scalar field and let $\mathbf{e}_{1}, \mathbf{e}_{2}, \mathbf{e}_{3}$ be a right-handed orthonormal basis of $\mathbb{R}^{3} .$ Suppose that
$$
\begin{aligned}
F_{1} \mathbf{e}_{1}+F_{2} \mathbf{e}_{2}+F_{3} \mathbf{e}_{3} &=f_{1} \mathbf{i}+f_{2} \mathbf{j}+f_{3} \mathbf{k} \\
\Phi(X, Y, Z) &=\phi(x, y, z)
\end{aligned}
$$
That is, $\mathbf{F}$ and $\Phi$ represent $\mathbf{f}$ and $\phi$ in the new co-ordinates $X, Y, Z$. Then
>$$
\begin{aligned}
\operatorname{grad} \phi &=\frac{\partial \Phi}{\partial X} \mathbf{e}_{1}+\frac{\partial \Phi}{\partial Y} \mathbf{e}_{2}+\frac{\partial \Phi}{\partial Z} \mathbf{e}_{3} ; \\
\operatorname{div} \mathbf{f} &=\frac{\partial F_{1}}{\partial X}+\frac{\partial F_{2}}{\partial Y}+\frac{\partial F_{3}}{\partial Z} \\
\operatorname{curl} \mathbf{f} &=\left|\begin{array}{ccc}
\mathbf{e}_{1} & \mathbf{e}_{2} & \mathbf{e}_{3} \\
\frac{\partial}{\partial X} & \frac{\partial}{\partial Y} & \frac{\partial}{\partial Z} \\
F_{1} & F_{2} & F_{3}
\end{array}\right|
\end{aligned}
>$$

---
### In [[Cylindrical Polar Coordinates]]
#### Proposition 84
The formulae for grad, div, curl in terms of cylindrical polar co-ordinates of fields $\psi(r, \theta, z)$ and $\mathbf{F}=F_{r} \mathbf{e}_{r}+F_{\theta} \mathbf{e}_{\theta}+F_{z} \mathbf{e}_{z}$ are
$$
\begin{aligned}
\nabla \psi &=\frac{\partial \psi}{\partial r} \mathbf{e}_{r}+\frac{1}{r} \frac{\partial \psi}{\partial \theta} \mathbf{e}_{\theta}+\frac{\partial \psi}{\partial z} \mathbf{e}_{z} \\
\nabla \cdot \mathbf{F} &=\frac{1}{r} \frac{\partial}{\partial r}\left(r F_{r}\right)+\frac{1}{r} \frac{\partial F_{\theta}}{\partial \theta}+\frac{\partial F_{z}}{\partial z} ; \\
\nabla \wedge \mathbf{F} &=\frac{1}{r}\left|\begin{array}{ccc}
\mathbf{e}_{r} & r \mathbf{e}_{\theta} & \mathbf{e}_{z} \\
\frac{\partial}{\partial r} & \frac{\partial}{\partial \theta} & \frac{\partial}{\partial z} \\
F_{r} & r F_{\theta} & F_{z}
\end{array}\right|
\end{aligned}
$$
##### Proof
###### Grad
$$
\begin{array}{r}
x=r \cos \theta, \quad y=r \sin \theta, \quad z=z \\
\text { Say } \phi(x, y, z)=\psi(r, \theta, z) \text { . Then } \\
\qquad \begin{aligned}
\frac{\partial \psi}{\partial r}=\frac{\partial \phi}{\partial x} \frac{\partial x}{\partial r}+\frac{\partial \phi}{\partial y} \frac{\partial y}{\partial r}+\frac{\partial \phi}{\partial z} \frac{\partial z}{\partial r}=\frac{\partial \phi}{\partial x} \cos \theta+\frac{\partial \phi}{\partial y} \sin \theta \\
\frac{\partial \psi}{\partial \theta}=\frac{\partial \phi}{\partial x} \frac{\partial x}{\partial \theta}+\frac{\partial \phi}{\partial y} \frac{\partial y}{\partial \theta}+\frac{\partial \phi}{\partial z} \frac{\partial z}{\partial \theta}=-\frac{\partial \phi}{\partial x} r \sin \theta+\frac{\partial \phi}{\partial y} r \cos \theta \\
\frac{\partial \psi}{\partial z}=\frac{\partial \phi}{\partial z}
\end{aligned}
\end{array}
$$
Hence
$$
\begin{aligned}
& \frac{\partial \psi}{\partial r} \mathbf{e}_{r}+\frac{1}{r} \frac{\partial \psi}{\partial \theta} \mathbf{e}_{\theta}+\frac{\partial \psi}{\partial z} \mathbf{e}_{z} \\
=&\left(\frac{\partial \phi}{\partial x} \cos \theta+\frac{\partial \phi}{\partial y} \sin \theta\right)(\cos \theta, \sin \theta, 0)+\frac{1}{r}\left(-\frac{\partial \phi}{\partial x} r \sin \theta+\frac{\partial \phi}{\partial y} r \cos \theta\right)(-\sin \theta, \cos \theta, 0)+\frac{\partial \phi}{\partial z} \mathbf{k} \\
=&\left(\frac{\partial \phi}{\partial x} \cos ^{2} \theta+\frac{\partial \phi}{\partial x} \sin ^{2} \theta\right) \mathbf{i}+\left(\frac{\partial \phi}{\partial y} \sin ^{2} \theta+\frac{\partial \phi}{\partial y} \cos ^{2} \theta\right) \mathbf{j}+\frac{\partial \phi}{\partial z} \mathbf{k} \\
=& \nabla \phi .
\end{aligned}
$$
###### Div
###### Curl
#TODO 

---
### In [[Spherical Polar Coordinates]]
#### Proposition 86
The formulae for grad, div, curl in terms of spherical polar co-ordinates of fields $\psi(r, \phi, \theta)$ and $\mathbf{F}=F_{r} \mathbf{e}_{r}+F_{\phi} \mathbf{e}_{\phi}+F_{\theta} \mathbf{e}_{\theta}$ are
$$
\begin{aligned}
\nabla \psi &=\frac{\partial \psi}{\partial r} \mathbf{e}_{r}+\frac{1}{r} \frac{\partial \psi}{\partial \theta} \mathbf{e}_{\theta}+\frac{1}{r \sin \theta} \frac{\partial \psi}{\partial \phi} \mathbf{e}_{\phi} ; \\
\nabla \cdot \mathbf{F} &=\frac{1}{r^{2} \sin \theta}\left[\frac{\partial}{\partial r}\left(r^{2} \sin \theta F_{r}\right)+\frac{\partial}{\partial \theta}\left(r \sin \theta F_{\theta}\right)+\frac{\partial}{\partial \phi}\left(r F_{\phi}\right)\right] \\
\nabla \wedge \mathbf{F} &=\frac{1}{r^{2} \sin \theta}\left|\begin{array}{ccc}
\mathbf{e}_{r} & r \mathbf{e}_{\theta} & r \sin \theta \mathbf{e}_{\phi} \\
\frac{\partial}{\partial r} & \frac{\partial}{\partial \theta} & \frac{\partial}{\partial \phi} \\
F_{r} & r F_{\theta} & r \sin \theta F_{\phi}
\end{array}\right| .
\end{aligned}
$$
---
### Identities
#### Proposition 87
Let $\mathbf{F}$ be a vector field on $\mathbb{R}^{3}$ and $\phi$ be a scalar field on $\mathbb{R}^{3}$. Then
$\operatorname{curl} \operatorname{grad} \phi=\mathbf{0} ; \quad \operatorname{div} \operatorname{curl} \mathbf{F}=0 .$
##### Proof
With the notation $\nabla \phi=\left(\phi_{x}, \phi_{y}, \phi_{z}\right)$ where subscripts now denote partial differentiation, we have
$$
\operatorname{curl}(\nabla \phi)=\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
\phi_{x} & \phi_{y} & \phi_{z}
\end{array}\right|=\left(\phi_{z y}-\phi_{y z}, \phi_{x z}-\phi_{z x}, \phi_{y x}-\phi_{x y}\right)=\mathbf{0}
$$
Again with subscripts denoting partial differentiation, we also have
$$
\begin{aligned}
\operatorname{div}(\operatorname{curl} \mathbf{F}) &=\operatorname{div}\left(\frac{\partial F_{3}}{\partial y}-\frac{\partial F_{2}}{\partial z}, \frac{\partial F_{1}}{\partial z}-\frac{\partial F_{3}}{\partial x}, \frac{\partial F_{2}}{\partial x}-\frac{\partial F_{1}}{\partial y}\right) \\
&=\left[\left(F_{3}\right)_{y x}-\left(F_{2}\right)_{z x}\right]+\left[\left(F_{1}\right)_{z y}-\left(F_{3}\right)_{x y}\right]+\left[\left(F_{2}\right)_{x z}-\left(F_{1}\right)_{y z}\right]=0
\end{aligned}
$$

#### Proposition 89
>Product Rules for div and curl

Let $\mathbf{F}$ be a vector field on $\mathbb{R}^{3}$ and $\phi, \psi$ be scalar fields on $\mathbb{R}^{3}$. Then
$$
\begin{aligned}
\operatorname{div}(\phi \mathbf{F}) &=\nabla \phi \cdot \mathbf{F}+\phi \operatorname{div} \mathbf{F} ; \\
\operatorname{curl}(\phi \mathbf{F}) &=\phi \operatorname{curl} \mathbf{F}+\nabla \phi \wedge \mathbf{F} .
\end{aligned}
$$
##### Proof
(i) With subscripts denoting partial differentiation we have
$$
\begin{aligned}
\operatorname{div}(\phi \mathbf{F}) &=\left(\phi F_{1}\right)_{x}+\left(\phi F_{2}\right)_{y}+\left(\phi F_{3}\right)_{z} \\
&=\phi\left(F_{1}\right)_{x}+\phi_{x} F_{1}+\phi\left(F_{2}\right)_{y}+\phi_{y} F_{2}+\phi\left(F_{3}\right)_{z}+\phi_{z} F_{3} \\
&=\phi\left[\left(F_{1}\right)_{x}+\left(F_{2}\right)_{y}+\left(F_{3}\right)_{z}\right]+\left(\phi_{x}, \phi_{y}, \phi_{z}\right) \cdot\left(F_{1}, F_{2}, F_{3}\right) \\
&=\phi \operatorname{div} \mathbf{F}+(\nabla \phi) \cdot \mathbf{F}
\end{aligned}
$$
(ii) $\operatorname{curl}(\phi \mathbf{F})$ equals
$$
\begin{aligned}
&\left(\frac{\partial\left(\phi F_{3}\right)}{\partial y}-\frac{\partial\left(\phi F_{2}\right)}{\partial z}, \frac{\partial\left(\phi F_{1}\right)}{\partial z}-\frac{\partial\left(\phi F_{3}\right)}{\partial x}, \frac{\partial\left(\phi F_{2}\right)}{\partial x}-\frac{\partial\left(\phi F_{1}\right)}{\partial y}\right) \\
=& \phi\left(\frac{\partial F_{3}}{\partial y}-\frac{\partial F_{2}}{\partial z}, \frac{\partial F_{1}}{\partial z}-\frac{\partial F_{3}}{\partial x}, \frac{\partial F_{2}}{\partial x}-\frac{\partial F_{1}}{\partial y}\right)+\left(\phi_{y} F_{3}-\phi_{z} F_{2}, \phi_{z} F_{1}-\phi_{x} F_{3}, \phi_{x} F_{2}-\phi_{y} F_{1}\right) \\
=& \phi \operatorname{curl} \mathbf{F}+\left|\begin{array}{ccc}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\phi_{x} & \phi_{y} & \phi_{z} \\
F_{1} & F_{2} & F_{3}
\end{array}\right| \\
=& \phi \operatorname{curl} \mathbf{F}+(\nabla \phi) \wedge \mathbf{F} .
\end{aligned}
$$

#### Proposition 90 
For vector fields $\mathbf{F}, \mathbf{G}$ :
$$
\begin{aligned}
\nabla(\mathbf{F} \cdot \mathbf{G}) &=(\mathbf{F} \cdot \nabla) \mathbf{G}+(\mathbf{G} \cdot \nabla) \mathbf{F}+\mathbf{F} \wedge(\nabla \wedge \mathbf{G})+\mathbf{G} \wedge(\nabla \wedge \mathbf{F}) \\
\nabla \cdot(\mathbf{F} \wedge \mathbf{G}) &=\mathbf{G} \cdot(\nabla \wedge \mathbf{F})-\mathbf{F} \cdot(\nabla \wedge \mathbf{G}) \\
\nabla \wedge(\mathbf{F} \wedge \mathbf{G}) &=\mathbf{F}(\nabla \cdot \mathbf{G})-\mathbf{G}(\nabla \cdot \mathbf{F})+(\mathbf{G} \cdot \nabla) \mathbf{F}-(\mathbf{F} \cdot \nabla) \mathbf{G} \\
\nabla \wedge(\nabla \wedge \mathbf{F}) &=\nabla(\nabla \cdot \mathbf{F})-\nabla^{2} \mathbf{F}
\end{aligned}
$$
##### Proof
###### (1)
Recall that $\mathbf{u} \wedge(\mathbf{v} \wedge \mathbf{w})=(\mathbf{u} \cdot \mathbf{w}) \mathbf{v}-(\mathbf{u} \cdot \mathbf{v}) \mathbf{w}$ and hence
$$
\begin{aligned}
&(\mathbf{F} \cdot \nabla) \mathbf{G}+(\mathbf{G} \cdot \nabla) \mathbf{F}+\mathbf{F} \wedge(\nabla \wedge \mathbf{G})+\mathbf{G} \wedge(\nabla \wedge \mathbf{F}) \\
=& \sum_{i}\left(\mathbf{F} \cdot \mathbf{e}_{i}\right) \frac{\partial \mathbf{G}}{\partial x_{i}}+\sum_{i}\left(\mathbf{G} \cdot \mathbf{e}_{i}\right) \frac{\partial \mathbf{F}}{\partial x_{i}}+\mathbf{F} \wedge\left(\sum_{i} \mathbf{e}_{i} \wedge \frac{\partial \mathbf{G}}{\partial x_{i}}\right)+\mathbf{G} \wedge\left(\sum_{i} \mathbf{e}_{i} \wedge \frac{\partial \mathbf{F}}{\partial x_{i}}\right) \\
=& \sum_{i}\left(\mathbf{F} \cdot \mathbf{e}_{i}\right) \frac{\partial \mathbf{G}}{\partial x_{i}}+\sum_{i}\left(\mathbf{G} \cdot \mathbf{e}_{i}\right) \frac{\partial \mathbf{F}}{\partial x_{i}}+\sum_{i} \mathbf{F} \wedge\left(\mathbf{e}_{i} \wedge \frac{\partial \mathbf{G}}{\partial x_{i}}\right)+\sum_{i} \mathbf{G} \wedge\left(\mathbf{e}_{i} \wedge \frac{\partial \mathbf{F}}{\partial x_{i}}\right) \\
=& \sum_{i}\left\{\left(\mathbf{F} \cdot \mathbf{e}_{i}\right) \frac{\partial \mathbf{G}}{\partial x_{i}}+\left(\mathbf{G} \cdot \mathbf{e}_{i}\right) \frac{\partial \mathbf{F}}{\partial x_{i}}+\left[\left(\mathbf{F} \cdot \frac{\partial \mathbf{G}}{\partial x_{i}}\right) \mathbf{e}_{i}-\left(\mathbf{F} \cdot \mathbf{e}_{i}\right) \frac{\partial \mathbf{G}}{\partial x_{i}}\right]+\left[\left(\mathbf{G} \cdot \frac{\partial \mathbf{F}}{\partial x_{i}}\right) \mathbf{e}_{i}-\left(\mathbf{G} \cdot \mathbf{e}_{i}\right) \frac{\partial \mathbf{F}}{\partial x_{i}}\right]\right\} \\
=& \sum_{i} \mathbf{e}_{i}\left(\mathbf{F} \cdot \frac{\partial \mathbf{G}}{\partial x_{i}}+\mathbf{G} \cdot \frac{\partial \mathbf{F}}{\partial x_{i}}\right) \\
=& \sum_{i} \mathbf{e}_{i} \frac{\partial}{\partial x_{i}}(\mathbf{F} \cdot \mathbf{G})=\nabla(\mathbf{F} \cdot \mathbf{G})
\end{aligned}
$$
###### (2)
#TODO 
###### (3)
#TODO 
###### (4)
Recall again that $\mathbf{u} \wedge(\mathbf{v} \wedge \mathbf{w})=(\mathbf{u} \cdot \mathbf{w}) \mathbf{v}-(\mathbf{u} \cdot \mathbf{v}) \mathbf{w}$ and then
$$
\begin{aligned}
\nabla \wedge(\nabla \wedge \mathbf{F}) &=\sum_{i} \mathbf{e}_{i} \wedge \frac{\partial}{\partial x_{i}}\left(\sum_{j} \mathbf{e}_{j} \wedge \frac{\partial \mathbf{F}}{\partial x_{j}}\right) \\
&=\sum_{i} \sum_{j} \mathbf{e}_{i} \wedge\left(\mathbf{e}_{j} \wedge \frac{\partial^{2} \mathbf{F}}{\partial x_{i} \partial x_{j}}\right) \\
&=\sum_{i} \sum_{j}\left[\left(\mathbf{e}_{i} \cdot \frac{\partial^{2} \mathbf{F}}{\partial x_{i} \partial x_{j}}\right) \mathbf{e}_{j}\right]-\sum_{i} \sum_{j}\left[\left(\mathbf{e}_{i} \cdot \mathbf{e}_{j}\right) \frac{\partial^{2} \mathbf{F}}{\partial x_{i} \partial x_{j}}\right] \\
&=\sum_{j} \mathbf{e}_{j} \frac{\partial}{\partial x_{j}}\left[\sum_{i} \mathbf{e}_{i} \cdot \frac{\partial \mathbf{F}}{\partial x_{i}}\right]-\sum_{i} \sum_{j}\left[\boldsymbol{\delta}_{i j} \frac{\partial^{2} \mathbf{F}}{\partial x_{i} \partial x_{j}}\right]\\
&=\sum_{j} \mathbf{e}_{j} \frac{\partial}{\partial x_{j}}\left[\sum_{i} \mathbf{e}_{i} \cdot \frac{\partial \mathbf{F}}{\partial x_{i}}\right]-\sum_{i} \frac{\partial^{2} \mathbf{F}}{\partial x_{i}^{2}}=\nabla(\nabla \cdot \mathbf{F})-\nabla^{2} \mathbf{F}
\end{aligned}
$$

#### Remark 91
All vector calculus can be proven by simply grinding out the calculations. But there are neater ways to write out the formula for , grad and curl as given below:
$$
\nabla \phi=\sum_{i} \frac{\partial \phi}{\partial x_{i}} \mathbf{e}_{i}, \quad \nabla \cdot \mathbf{F}=\sum_{i} \mathbf{e}_{i} \cdot \frac{\partial \mathbf{F}}{\partial x_{i}}, \quad \nabla \wedge \mathbf{F}=\sum_{i} \mathbf{e}_{i} \wedge \frac{\partial \mathbf{F}}{\partial x_{i}}, \quad \mathbf{F} \cdot \nabla=\sum_{i}\left(\mathbf{F} \cdot \mathbf{e}_{i}\right) \frac{\partial}{\partial x_{i}}
$$
where the dummy variable i ranges over $1,2,3$ in each case and $\mathbf{e}_{1}, \mathbf{e}_{2}, \mathbf{e}_{3}$ is any right-handed
orthonormal basis. For example
$$
\begin{aligned}
\sum_{i} \mathbf{e}_{i} \wedge \frac{\partial \mathbf{F}}{\partial x_{i}} &=\mathbf{e}_{1} \wedge \frac{\partial \mathbf{F}}{\partial x_{1}}+\mathbf{e}_{2} \wedge \frac{\partial \mathbf{F}}{\partial x_{2}}+\mathbf{e}_{3} \wedge \frac{\partial \mathbf{F}}{\partial x_{3}} \\
&=\left|\begin{array}{ccc}
\mathbf{e}_{1} & \mathbf{e}_{2} & \mathbf{e}_{3} \\
1 & 0 & 0 \\
\frac{\partial F_{1}}{\partial x_{1}} & \frac{\partial F_{2}}{\partial x_{1}} & \frac{\partial F_{3}}{\partial x_{1}}
\end{array}\right|+\left|\begin{array}{ccc}
\mathbf{e}_{1} & \mathbf{e}_{2} & \mathbf{e}_{3} \\
0 & 1 & 0 \\
\frac{\partial F_{1}}{\partial x_{2}} & \frac{\partial F_{2}}{\partial x_{2}} & \frac{\partial F_{3}}{\partial x_{2}}
\end{array}\right|+\left|\begin{array}{ccc}
\mathbf{e}_{1} & \mathbf{e}_{2} & \mathbf{e}_{3} \\
0 & 0 & 1 \\
\frac{\partial F_{1}}{\partial x_{3}} & \frac{\partial F_{2}}{\partial x_{3}} & \frac{\partial F_{3}}{\partial x_{3}}
\end{array}\right| \\
&=-\mathbf{e}_{2} \frac{\partial F_{3}}{\partial x_{1}}+\mathbf{e}_{3} \frac{\partial F_{2}}{\partial x_{1}}+\mathbf{e}_{1} \frac{\partial F_{3}}{\partial x_{2}}-\mathbf{e}_{3} \frac{\partial F_{1}}{\partial x_{2}}-\mathbf{e}_{1} \frac{\partial F_{2}}{\partial x_{3}}+\mathbf{e}_{2} \frac{\partial F_{1}}{\partial x_{3}} \\
&=\nabla \wedge \mathbf{F} .
\end{aligned}
$$
With these formulae the proofs of identities involving, grad and curl are much shorter; on the other hand the formulae need to be applied with much more care and attention to detail than was previously the case.

### Identities
#### Second Derivative
$\nabla \cdot(\nabla \times \mathbf{A})=0$
$\nabla \times(\nabla \psi)=\mathbf{0}$
$\nabla \cdot(\nabla \psi)=\nabla^{2} \psi$ (scalar Laplacian)
$\nabla(\nabla \cdot \mathbf{A})-\nabla \times(\nabla \times \mathbf{A})=\nabla^{2} \mathbf{A}$ (vector Laplacian)
$\nabla \cdot(\phi \nabla \psi)=\phi \nabla^{2} \psi+\nabla \phi \cdot \nabla \psi$
$\psi \nabla^{2} \phi-\phi \nabla^{2} \psi=\nabla \cdot(\psi \nabla \phi-\phi \nabla \psi)$
$\nabla^{2}(\phi \psi)=\phi \nabla^{2} \psi+2(\nabla \phi) \cdot(\nabla \psi)+\left(\nabla^{2} \phi\right) \psi$
$\nabla^{2}(\psi \mathbf{A})=\mathbf{A} \nabla^{2} \psi+2(\nabla \psi \cdot \nabla) \mathbf{A}+\psi \nabla^{2} \mathbf{A}$
$\nabla^{2}(\mathbf{A} \cdot \mathbf{B})=\mathbf{A} \cdot \nabla^{2} \mathbf{B}-\mathbf{B} \cdot \nabla^{2} \mathbf{A}+2 \nabla \cdot((\mathbf{B} \cdot \nabla) \mathbf{A}+\mathbf{B} \times(\nabla \times \mathbf{A}))$ (Green's vector identity)
$\nabla^{2}(\nabla \psi) =\nabla(\nabla \cdot(\nabla \psi))=\nabla\left(\nabla^{2} \psi\right)$
#### Third Derivative
$\nabla^{2}(\nabla \cdot \mathbf{A}) =\nabla \cdot(\nabla(\nabla \cdot \mathbf{A}))=\nabla \cdot\left(\nabla^{2} \mathbf{A}\right)$
$\nabla^{2}(\nabla \times \mathbf{A}) =-\nabla \times(\nabla \times(\nabla \times \mathbf{A}))=\nabla \times\left(\nabla^{2} \mathbf{A}\right)$
#### Integration
>In the following surface–volume integral theorems, $V$ denotes a three-dimensional volume with a corresponding two-dimensional boundary $S = \partial V$ (a closed surface).

$\iint_{\partial V} \mathbf{A} \cdot d \mathbf{S}=\iiint_{V}(\nabla \cdot \mathbf{A}) d V$ ([[divergence theorem]])
$\iint_{\partial V} \psi d \mathbf{S}=\iiint_{V} \nabla \psi d V$
$\iint_{\partial V} \mathbf{A} \times d \mathbf{S}=-\iiint_{V} \nabla \times \mathbf{A} d V$
$\iint_{\partial V} \psi \nabla \varphi \cdot d \mathbf{S}=\iiint_{V}\left(\psi \nabla^{2} \varphi+\nabla \varphi \cdot \nabla \psi\right) d V$ (Green's first identity)
$\iint_{\partial V}(\psi \nabla \varphi-\varphi \nabla \psi) \cdot d \mathbf{S}=\iint_{\partial V}\left(\psi \frac{\partial \varphi}{\partial n}-\varphi \frac{\partial \psi}{\partial n}\right) d S=\iiint_{V}\left(\psi \nabla^{2} \varphi-\varphi \nabla^{2} \psi\right) d V$ (Green's second identity)
$\iiint_{V} \mathbf{A} \cdot \nabla \psi d V=\iint_{\partial V} \psi \mathbf{A} \cdot d \mathbf{S}-\iiint_{V} \psi \nabla \cdot \mathbf{A} d V$ (integration by parts)
$\iiint_{V} \psi \nabla \cdot \mathbf{A} d V=\iint_{\partial V} \psi \mathbf{A} \cdot d \mathbf{S}-\iiint_{V} \nabla \psi \cdot \mathbf{A} d V$ (integration by parts)
$\int_{\partial S} \mathbf{A} \cdot d \boldsymbol{\ell}=\iint_{S}(\nabla \times \mathbf{A}) \cdot d \mathbf{S}$ (Stokes' theorem)
$\int_{\partial S} \psi d \boldsymbol{\ell}=-\iint_{S} \nabla \psi \times d \mathbf{S}$