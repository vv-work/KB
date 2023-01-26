## Cylindrical Polar Coordinates
#MVC 
Cylindrical polar coordinates are $(r, \theta, z) .$ The relationship between cylindrical polars and cartesians $(x, y, z)$ is given by (Figure 11$)$
$$
x=r \cos \theta, \quad y=r \sin \theta, \quad z=z
$$
The position vector is given by
$$
\mathbf{r}=r \mathbf{e}_{r}+z \mathbf{e}_{z}
$$
where $\mathbf{e}_{z}=\mathbf{k}$ is the unit vector in the direction of increasing $z$.
![Figure 11 | 400](Dynamics_46.png)

### [[Jacobian]]
$\frac{\partial(x, y, z)}{\partial(r, \theta, z)}=\left|\begin{array}{ccc}\frac{\partial x}{\partial r} & \frac{\partial x}{\partial \theta} & \frac{\partial x}{\partial z} \\ \frac{\partial y}{\partial r} & \frac{\partial y}{\partial \theta} & \frac{\partial y}{\partial z} \\ \frac{\partial z}{\partial r} & \frac{\partial z}{\partial \theta} & \frac{\partial z}{\partial r}\end{array}\right|=\left|\begin{array}{ccc}\cos \theta & -r \sin \theta & 0 \\ \sin \theta & r \cos \theta & 0 \\ 0 & 0 & 1\end{array}\right|=\left|\begin{array}{cc}\cos \theta & -r \sin \theta \\ \sin \theta & r \cos \theta\end{array}\right|=r$
### Div, Grad and Curl
If we note
$$
\mathrm{d} \mathbf{r}=(\cos \theta, \sin \theta, 0) \mathrm{d} r+(-r \sin \theta, r \cos \theta, 0) \mathrm{d} \theta+(0,0,1) \mathrm{d} z
$$
then we may write
$$
\mathrm{d} \mathbf{r}=\mathbf{e}_{r} \mathrm{~d} r+r \mathbf{e}_{\theta} \mathrm{d} \theta+\mathbf{e}_{z} \mathrm{~d} z
$$
where
$$
\mathbf{e}_{r}=(\cos \theta, \sin \theta, 0), \quad \mathbf{e}_{\theta}=(-\sin \theta, \cos \theta, 0), \quad \mathbf{e}_{z}=(0,0,1) .
$$
Note, for any values of $r, \theta, z$, the vectors $\mathbf{e}_{r}, \mathbf{e}_{\theta}, \mathbf{e}_{z}$ make a right-handed orthonormal basis of $\mathbb{R}^{3} .$
#### [[Gradient]], [[Divergence]], [[Curl]], [[Laplacian]] in [[Cylindrical Polar Coordinates]]
>[[Div Grad Curl#Proposition 84]]

The formulae for grad, div, curl in terms of cylindrical polar co-ordinates of fields $\psi(r, \theta, z)$ and $\mathbf{F}=F_{r} \mathbf{e}_{r}+F_{\theta} \mathbf{e}_{\theta}+F_{z} \mathbf{e}_{z}$ are
$$
\begin{aligned}
\nabla \psi &=\frac{\partial \psi}{\partial r} \mathbf{e}_{r}+\frac{1}{r} \frac{\partial \psi}{\partial \theta} \mathbf{e}_{\theta}+\frac{\partial \psi}{\partial z} \mathbf{e}_{z} \\
\nabla \cdot \mathbf{F} &=\frac{1}{r} \frac{\partial}{\partial r}\left(r F_{r}\right)+\frac{1}{r} \frac{\partial F_{\theta}}{\partial \theta}+\frac{\partial F_{z}}{\partial z} ; \\
\nabla \wedge \mathbf{F} &=\frac{1}{r}\left|\begin{array}{ccc}
\mathbf{e}_{r} & r \mathbf{e}_{\theta} & \mathbf{e}_{z} \\
\frac{\partial}{\partial r} & \frac{\partial}{\partial \theta} & \frac{\partial}{\partial z} \\
F_{r} & r F_{\theta} & F_{z}
\end{array}\right| \\
\nabla^{2} \psi &= \frac{1}{r} \frac{\partial}{\partial r}\left(r \frac{\partial \psi}{\partial r}\right)+\frac{1}{r^{2}} \frac{\partial^{2} \psi}{\partial \theta^{2}}+\frac{\partial^{2} \psi}{\partial z^{2}}=0
\end{aligned}
$$

---
#Dynamics 
### Velocity
Note that now $|\mathbf{r}| \neq r$. By Pythagoras' theorem we have instead $|\mathbf{r}|=\left(r^{2}+z^{2}\right)^{1 / 2}$. The particle's velocity is
$$
\dot{\mathbf{r}}=\dot{r} \mathbf{e}_{r}+r \dot{\theta} \mathbf{e}_{\theta}+\dot{z} \mathbf{e}_{z}
$$
### Acceleration
The acceleration is
$$
\ddot{\mathbf{r}}=\left(\ddot{r}-r \dot{\theta}^{2}\right) \mathbf{e}_{r}+\frac{1}{r} \frac{\mathrm{d}}{\mathrm{d} t}\left(r^{2} \dot{\theta}\right) \mathbf{e}_{\theta}+\ddot{z} \mathbf{e}_{z}
$$
These are the same as in plane polar coordinates but with the simple Cartesian terms relating to $z$ as $\mathbf{e}_{z}$ does not vary in space.
### Volume Element
The volume element $d V$ is given by
$$
\mathrm{d} V=\mathrm{d} x \mathrm{~d} y \mathrm{~d} z=r \mathrm{~d} r \mathrm{~d} \theta \mathrm{d} z
$$
### Gradient in Cylindrical Polar Coordinates
$\nabla f=\frac{\partial f}{\partial r} \mathbf{e}_{r}+\frac{1}{r} \frac{\partial f}{\partial \theta} \mathbf{e}_{\theta}+\frac{\partial f}{\partial z} \mathbf{e}_{z}$

### Laplacian in Cylindrical Polar Coordinates
$$
\nabla^{2} \psi=\frac{1}{r} \frac{\partial}{\partial r}\left(r \frac{\partial \psi}{\partial r}\right)+\frac{1}{r^{2}} \frac{\partial^{2} \psi}{\partial \theta^{2}}+\frac{\partial^{2} \psi}{\partial z^{2}}=0
$$
