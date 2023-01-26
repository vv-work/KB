## Plane Polar Coordinates
#MVC 
### Jacobian
Let $x=r \cos \theta$ and $y=r \sin \theta$ where $r$ and $\theta$ are polar co-ordinates. Then
$$
\begin{aligned}
\frac{\partial(x, y)}{\partial(r, \theta)} &=\operatorname{det}\left(\begin{array}{cc}
\frac{\partial x}{\partial r} & \frac{\partial x}{\partial \theta} \\
\frac{\partial y}{\partial r} & \frac{\partial y}{\partial \theta}
\end{array}\right) \\
&=\operatorname{det}\left(\begin{array}{cc}
\cos \theta & -r \sin \theta \\
\sin \theta & r \cos \theta
\end{array}\right) \\
&=r\left(\cos ^{2} \theta+\sin ^{2} \theta\right)=r .
\end{aligned}
$$

In reverse, $r=\sqrt{x^{2}+y^{2}}$ and $\theta=\tan ^{-1}(y / x)$ and
$$
\begin{aligned}
\frac{\partial(r, \theta)}{\partial(x, y)} &=\operatorname{det}\left(\begin{array}{cc}
\frac{\partial r}{\partial x} & \frac{\partial r}{\partial y} \\
\frac{\partial \theta}{\partial x} & \frac{\partial \theta}{\partial y}
\end{array}\right) \\
&=\operatorname{det}\left(\begin{array}{cc}
\frac{x}{\sqrt{x^{2}+y^{2}}} & \frac{y}{\sqrt{x^{2}+y^{2}}} \\
\frac{-y}{x^{2}+y^{2}} & \frac{x}{x^{2}+y^{2}}
\end{array}\right) \\
&=\frac{x^{2}+y^{2}}{\left(x^{2}+y^{2}\right)^{3 / 2}} \\
&=\frac{1}{\sqrt{x^{2}+y^{2}}}=\frac{1}{r}
\end{aligned}
$$
### Divergence
$$
\nabla \cdot \mathbf{F}=\frac{1}{r} \frac{\partial}{\partial r}\left(r F_{r}\right)+\frac{1}{r} \frac{\partial F_{\theta}}{\partial \theta} .
$$