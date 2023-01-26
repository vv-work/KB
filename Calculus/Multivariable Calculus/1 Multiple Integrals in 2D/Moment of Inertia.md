## Moment of Inertia
#MVC 
### Definition
Given a plate occupying a region $R$ of the plane, with density $\rho(x, y)$ per unit area, then the [[Moment of Inertia]] of the plate about an axis vertically through a point $\left(x_{0}, y_{0}\right)$ equals
$$
\iint_{R} \rho(x, y)\left(\left(x-x_{0}\right)^{2}+\left(y-y_{0}\right)^{2}\right) \mathrm{d} A.
$$

### Example 12
>Find the moment of inertia of a uniform rectangle, with sides of length a and $b$ and mass $m$ about a corner of the rectangle.

**Solution**. Note $m=\rho a b$. Without loss of generality, we can take the corner to be $(0,0)$ and then the moment of inertia equals
$$
\begin{aligned}
& \int_{x=0}^{a} \int_{y=0}^{b}\left(\frac{m}{a b}\right)\left((x-0)^{2}+(y-0)^{2}\right) \mathrm{d} y \mathrm{~d} x \\
=& \frac{m}{a b} \int_{x=0}^{a}\left[x^{2} y+\frac{y^{3}}{3}\right]_{0}^{b} \mathrm{~d} x \\
=& \frac{m}{a b} \int_{x=0}^{a}\left(x^{2} b+\frac{b^{3}}{3}\right) \mathrm{d} x \\
=& \frac{m}{a b}\left[\frac{x^{3} b}{3}+\frac{b^{3} x}{3}\right]_{0}^{a} \\
=& \frac{m}{a b}\left(\frac{a^{3} b}{3}+\frac{b^{3} a}{3}\right) \\
=& \frac{m}{3}\left(a^{2}+b^{2}\right) .
\end{aligned}
$$