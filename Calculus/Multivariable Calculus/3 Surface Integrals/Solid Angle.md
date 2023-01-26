## Solid Angle
#MVC 
### Definition
>The [[solid angle]] is the angle an object subtends at a point in three-dimensional space. More precisely, half-lines from a fixed point (or observer) will either intersect with the object in question or not; those lines of sight that are blocked by the object represent a subset of the unit sphere centred on the observer. The solid angle is the area of this subset. The unit of solid angle is the **steradian**. Given that the surface area of a sphere is $4 \pi(\text { radius })^{2}$ then a whole solid angle is $4 \pi .$

If $\Sigma^{*}$ is a [[surface]] and $\Sigma$ is the subset of $\Sigma^{*}$ facing the unit sphere, then the [[solid angle]] $\Omega$ subtended at $O$ by $\Sigma^{*}$ equals, by definition,
$$
\Omega=\iint_{\Sigma} \frac{\mathbf{e}_{r} \cdot \mathrm{d} \mathbf{S}}{r^{2}}=\iint_{\Sigma} \frac{\mathbf{r} \cdot \mathrm{d} \mathbf{S}}{r^{3}}.
$$

### Example 43
>Find the solid angle at the apex of a right pyramid with square base of side $2 d$ and height $h$.

**Solution.** Place the apex of the pyramid at the origin and orientate the axis of the pyramid along the positive $z$ -axis so that the square base of the pyramid has vertices $(\pm d, \pm d, h)$. By symmetry the solid angle at the apex is 4 times the solid angle subtended by the smaller square with vertices
$$
(0,0, h), \quad(0, d, h), \quad(d, d, h) \quad(0, d, h) \text { . }
$$
Hence the solid angle is
$$
\Omega=4 \int_{y=0}^{d} \int_{x=0}^{d} \frac{(x, y, h) \cdot \mathbf{k} \mathrm{d} x \mathrm{~d} y}{\left(x^{2}+y^{2}+h^{2}\right)^{3 / 2}}=4 h \int_{y=0}^{d} \int_{x=0}^{d} \frac{\mathrm{d} x \mathrm{~d} y}{\left(x^{2}+y^{2}+h^{2}\right)^{3 / 2}} .
$$
If we set $x=\sqrt{y^{2}+h^{2}} \tan t$ and $\tan \tau=d /\left(\sqrt{y^{2}+h^{2}}\right)$ then
$$
\begin{aligned}
\Omega &=4 h \int_{y=0}^{d} \int_{t=0}^{\tau} \frac{\sqrt{y^{2}+h^{2}} \sec ^{2} t \mathrm{~d} t \mathrm{~d} y}{\left(\left(y^{2}+h^{2}\right) \tan ^{2} t+y^{2}+h^{2}\right)^{3 / 2}} \\
&=4 h \int_{y=0}^{d} \int_{t=0}^{\tau} \frac{\sqrt{y^{2}+h^{2}} \sec ^{2} t \mathrm{~d} t \mathrm{~d} y}{\left(y^{2}+h^{2}\right)^{3 / 2}\left(\tan ^{2} t+1\right)^{3 / 2}} \\
&=4 h \int_{y=0}^{d} \int_{t=0}^{\tau} \frac{\cos t \mathrm{~d} t \mathrm{~d} y}{\left(y^{2}+h^{2}\right)}=4 h \int_{y=0}^{d} \frac{\sin \tau \mathrm{d} y}{\left(y^{2}+h^{2}\right)} \\
&=4 h d \int_{y=0}^{d} \frac{\mathrm{d} y}{\left(y^{2}+h^{2}\right) \sqrt{y^{2}+h^{2}+d^{2}}}
\end{aligned}
$$

as $\sin \tau=d\left(y^{2}+h^{2}+d^{2}\right)^{-1 / 2}.$
Making a similar substitution, namely $y=\sqrt{h^{2}+d^{2}} \tan \phi$ and $\tan \alpha=d / \sqrt{h^{2}+d^{2}}$, then
$$
\begin{aligned}
\Omega &=4 h d \int_{\phi=0}^{\alpha} \frac{\sqrt{h^{2}+d^{2}} \sec ^{2} \phi \mathrm{d} \phi}{\left(\left(h^{2}+d^{2}\right) \tan ^{2} \phi+h^{2}\right) \sqrt{h^{2}+d^{2}} \sec \phi} \\
&=4 h d \int_{\phi=0}^{\alpha} \frac{\cos \phi \mathrm{d} \phi}{\left(\left(h^{2}+d^{2}\right) \sin ^{2} \phi+h^{2} \cos ^{2} \phi\right)} \\
&=4 h d \int_{\phi=0}^{\alpha} \frac{\cos \phi \mathrm{d} \phi}{d^{2} \sin ^{2} \phi+h^{2}}
\end{aligned}
$$
Our final substitution is $u=\sin \phi$ so that $\sin \alpha=d / \sqrt{h^{2}+2 d^{2}}$ and
$$
\Omega=4 h d \int_{u=0}^{\sin \alpha} \frac{\mathrm{d} u}{d^{2} u^{2}+h^{2}}=\frac{4 h}{d}\left[\frac{d}{h} \tan ^{-1}\left(\frac{d u}{h}\right)\right]_{0}^{\sin \alpha}=4 \tan ^{-1}\left(\frac{d^{2}}{h \sqrt{h^{2}+2 d^{2}}}\right).
$$