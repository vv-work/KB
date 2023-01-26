## Spherical Polar Coordinates
#MVC 
### Definition
In [[Spherical Polar Coordinates]] $r,\theta,\phi$ are defined by the identity $$\mathbf{r}=(x, y, z)=(r \sin \theta \cos \phi, r \sin \theta \sin \phi, r \cos \theta).$$ Such that
$x=r \sin \theta \cos \phi, \quad y=r \sin \theta \sin \phi, \quad z=r \cos \theta, \quad \theta \in[0, \pi], \quad \phi \in[0,2 \pi).$
### Basis
$$
\mathbf{e}_{r}=(\sin \theta \cos \phi, \sin \theta \sin \phi, \cos \theta), \quad \mathbf{e}_{\theta}=(\cos \theta \cos \phi, \cos \theta \sin \phi,-\sin \theta), \quad \mathbf{e}_{\phi}=(-\sin \phi, \cos \phi, 0)
$$
Note, for any values of $r, \theta, \phi$ the vectors $\mathbf{e}_{r}, \mathbf{e}_{\theta}, \mathbf{e}_{\phi}$, make a right-handed orthonormal basis.
### Grad, Div, Curl
then we may write
$$
\mathrm{d} \mathbf{r}=\mathbf{e}_{r} \mathrm{~d} r+r \mathbf{e}_{\theta} \mathrm{d} \theta+r \sin \theta \mathbf{e}_{\phi} \mathrm{d} \phi
$$
Then 
> [[Div Grad Curl#Proposition 86]]

$$\begin{aligned} \nabla \psi &=\frac{\partial \psi}{\partial r} \mathbf{e}_{r}+\frac{1}{r} \frac{\partial \psi}{\partial \theta} \mathbf{e}_{\theta}+\frac{1}{r \sin \theta} \frac{\partial \psi}{\partial \phi} \mathbf{e}_{\phi} ; \\ \nabla \cdot \mathbf{F} &=\frac{1}{r^{2} \sin \theta}\left[\frac{\partial}{\partial r}\left(r^{2} \sin \theta F_{r}\right)+\frac{\partial}{\partial \theta}\left(r \sin \theta F_{\theta}\right)+\frac{\partial}{\partial \phi}\left(r F_{\phi}\right)\right] \\ \nabla \wedge \mathbf{F} &=\frac{1}{r^{2} \sin \theta}\left|\begin{array}{ccc}\mathbf{e}_{r} & r \mathbf{e}_{\theta} & r \sin \theta \mathbf{e}_{\phi} \\ \frac{\partial}{\partial r} & \frac{\partial}{\partial \theta} & \frac{\partial}{\partial \phi} \\ F_{r} & r F_{\theta} & r \sin \theta F_{\phi}\end{array}\right| . \end{aligned}$$
### [[Jacobian]]
$$
\begin{aligned}
\frac{\partial(x, y, z)}{\partial(r, \phi, \theta)} &=\left|\begin{array}{ccc}
\frac{\partial x}{\partial r} & \frac{\partial x}{\partial \theta} & \frac{\partial x}{\partial \phi} \\
\frac{\partial y}{\partial r} & \frac{\partial y}{\partial \theta} & \frac{\partial y}{\partial \phi} \\
\frac{\partial z}{\partial r} & \frac{\partial z}{\partial \theta} & \frac{\partial z}{\partial \phi}
\end{array}\right| \\
&=\left|\begin{array}{ccc}
\sin \theta \cos \phi & r \cos \theta \cos \phi & -r \sin \theta \sin \phi \\
\sin \theta \sin \phi & r \cos \theta \sin \phi & r \sin \theta \cos \phi \\
\cos \theta & -r \sin \theta & 0
\end{array}\right| \\
&=\cos \theta\left|\begin{array}{cc}
r \cos \theta \cos \phi & -r \sin \theta \sin \phi \\
r \cos \theta \sin \phi & r \sin \theta \cos \phi
\end{array}\right|+r \sin \theta\left|\begin{array}{l}
\sin \theta \cos \phi \\
\sin \theta \sin \phi & -r \sin \theta \sin \phi \\
r \sin \theta \cos \phi
\end{array}\right| \\
&=r^{2} \cos \theta \sin \theta \cos \theta\left(\cos ^{2} \phi+\sin ^{2} \phi\right)+r^{2} \sin ^{3} \theta\left(\cos ^{2} \phi+\sin ^{2} \phi\right) \\
&=r^{2} \sin \theta\left(\cos ^{2} \theta+\sin ^{2} \theta\right) \\
&=r^{2} \sin \theta \geqslant 0 \text { for } 0 \leqslant \theta \leqslant \pi .
\end{aligned}
$$

---
### Volume
Thus, for spherical polar co-ordinates, we have
$$
\mathrm{d} V=\mathrm{d} x \mathrm{~d} y \mathrm{~d} z=r^{2} \sin \theta \mathrm{d} r \mathrm{~d} \theta \mathrm{d} \phi
$$