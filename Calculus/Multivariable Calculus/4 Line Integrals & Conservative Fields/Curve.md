## Curve
#MVC 
### Definition
By a **curve** we shall mean a **piecewise smooth** function $\gamma: I \rightarrow \mathbb{R}^{3}$ defined on an interval $I$ of $\mathbb{R}$. Notice that order on $I$ also gives the curve $\gamma$ an **orientation**.

We shall also use the term curve to describe the images of such maps $\gamma$. Given such an image then it will be the image of more than one such map $\gamma$ and we will talk about parameterizations $\gamma_{1}$ and $\gamma_{2}$ of the curve. These parameterizations of the image come in two different possible orientations.

### Definition: Simple
We say a curve $\gamma:[a, b] \rightarrow \mathbb{R}^{3}$ is [[simple]] if $\gamma$ is $1-1$, with the one possible exception that $\gamma(a)=\gamma(b)$ may be true. This means that the curve does not cross itself except possibly by its endpoints meeting.
### Definition: Closed
We say a curve $\gamma:[a, b] \rightarrow \mathbb{R}^{3}$ is [[closed]] if $\gamma(a)=\gamma(b)$.

### Example 49: Lines
The line through points $\mathbf{p}$ and $\mathbf{q}$ can be parameterized as
$$
\gamma(t)=\mathbf{p}+t(\mathbf{q}-\mathbf{p})
$$
When $0<t<1$ then $\gamma(t)$ lies between $\mathbf{p}$ and $\mathbf{q}$, for $t>1$ beyond $\mathbf{q}$ and for $t<0$ before $\mathbf{p}$.
### Example 50
A curve of the form
$$
\gamma(t)=(a \cos t, a \sin t, c t)
$$
is known as a **circular helix**.

### Example 52
>Show that the plane with equation $A x+B y+C z=D$ intersects the unit sphere $x^{2}+y^{2}+z^{2}=1$ in a circle if and only if $A^{2}+B^{2}+C^{2}>D^{2} .$ Parameterize the intersection of $x+y+z=1$ with the unit sphere.

**Solution.** The plane $A x+B y+C z=D$ has normal $(A, B, C)$ and so the point closest to the origin is the point with position vector $\lambda(A, B, C)$ which lies on the plane; by substitution, we see $\lambda=D /\left(A^{2}+B^{2}+C^{2}\right)$. This point is within unit distance of the origin if and only if
$$
1>\left|\frac{D}{A^{2}+B^{2}+C^{2}}(A, B, C)\right|=\frac{|D| \sqrt{A^{2}+B^{2}+C^{2}}}{A^{2}+B^{2}+C^{2}}
$$
i.e. if and only if $A^{2}+B^{2}+C^{2}>D^{2}$. By this criterion the plane $x+y+z=1$ intersects with the unit sphere. The centre of the circle which makes the intersection is at
$$
\frac{1}{1^{2}+1^{2}+1^{2}}(1,1,1)=\frac{(1,1,1)}{3}
$$
By Pythagoras' Theorem the radius $r$ of the circle satisfies
$$
r^{2}+\left|\frac{(1,1,1)}{3}\right|^{2}=1 \Longrightarrow r=\sqrt{\frac{2}{3}} \text { . }
$$
As $\mathbf{e}_{1}=(1,-1,0) / \sqrt{2}$ and $\mathbf{e}_{2}=(1,1,-2) / \sqrt{6}$ are two orthonormal vectors parallel to the plane then every point of the circle can be written in the form $\gamma(t)$ for $0 \leqslant t<2 \pi$ where
$$
\begin{aligned}
\gamma(t) &=\frac{(1,1,1)}{3}+\mathbf{e}_{1} \sqrt{\frac{2}{3}} \cos t+\mathbf{e}_{2} \sqrt{\frac{2}{3}} \sin t \\
&=\left(\frac{1}{3}+\frac{1}{\sqrt{3}} \cos t+\frac{1}{3} \sin t, \frac{1}{3}-\frac{1}{\sqrt{3}} \cos t+\frac{1}{3} \sin t, \frac{1}{3}-\frac{2}{3} \sin t\right).
\end{aligned}
$$