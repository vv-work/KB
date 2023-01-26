## 2D-Curl
#MVC 

![ | 350](https://cdn.kastatic.org/ka-perseus-images/80c78d0b5e74ff5ca5192950d28afc0795ce08f5.png)
### Capturing two-dimensional rotation with a formula
One of the simplest examples of a vector field which describes a rotating fluid is
$$\overrightarrow{\mathbf{v}}(x, y)=\left[\begin{array}{c}-y \\ x\end{array}\right]=-y \hat{\mathbf{i}}+x \hat{\mathbf{j}} .$$
>Here's what it looks like.![Rotational vector field | 300](https://cdn.kastatic.org/ka-perseus-images/2f87e8cc62d997a79f6ca66680eafc0a1673fc6c.png)
all the fluid particles just go in circles.

#### The $\mathbf{\hat i}$-component
The $-y\mathbf{\hat i}$-component suggests a **anticlockwise** rotation. Consider a small twig sitting in the fluid, oriented parallel to y-axis, one end at $(0,0)$ and the other at $(0,2)$.
The $-y\mathbf{\hat i}$ component of the vector field implies a anticlockwise rotation - *the vector point becomes more to the **left*** as we move up the vector field - i.e. the $\bf \hat i$-component of a vector attached to a point $(x_0,y_0)$ decreases as $y_0$ increases.
$$\frac{\partial}{\partial y}(-y)=-1<0$$

For a general vector field $$\overrightarrow{\mathbf{v}}(x, y)=v_{1}(x, y) \hat{\mathbf{i}}+v_{2}(x, y) \hat{\mathbf{j}}$$
Therefore, 
$$\frac{\partial v_{1}}{\partial y}\left(x_{0}, y_{0}\right)$$ suggests an anticlockwise rotation if it is negative.

#### The $\bf \hat j$-component
Similarly, $$\frac{\partial v_{2}}{\partial x}$$ suggests an anticlockwise rotation if it is positive.
#### Combining Together
Putting these two components together, the **rotation** of a fluid flowing along a
vector field $\overrightarrow{\mathbf{v}}$ near a point $\left(x_{0}, y_{0}\right)$ can be measured by:
$$\frac{\partial v_{2}}{\partial x}\left(x_{0}, y_{0}\right)-\frac{\partial v_{1}}{\partial y}\left(x_{0}, y_{0}\right)$$

- a **positive** number will indicate a general tendency to rotate **anticlockwise** around $(x_0,y_0)$,
- a **negative** indicates the opposite: **clockwise** rotation.

- If it equals $0$, there is no rotation in the fluid around $(x_0,y_0)$.
- The formula gives precisely twice the angular velocity of the fluid near $(x_0,y_0)$.

Hence we could, informally, define a $\operatorname{2d-curl}$:
$$
\operatorname{2d-curl}\overrightarrow{\mathbf{v}}=
\frac{\partial v_{2}}{\partial x}-\frac{\partial v_{1}}{\partial y}.
$$

### Example: Analyzing Rotation in a 2D Vector Field Using Curl
>
Considered the vector field defined by the function $\overrightarrow{\mathbf{v}}(x, y)=\left[\begin{array}{c}\cos (x+y) \\ \sin (x y)\end{array}\right]$
![2d-curl Example | 300](https://cdn.kastatic.org/ka-perseus-images/b31b47a0befb37e4dc89c063b4fc370817de3ef8.png)
Determine whether a fluid flowing according to this vector field has clockwise or counterclockwise rotation at the point $(0,{\pi\over2})$.

#### Solution
- Compute the [[2D-Curl]]: $$\operatorname{2d-curl}\overrightarrow{\mathbf{v}}=y\cos(xy)+\sin(x+y).$$
- So at point $(0,{\pi\over2})$ the [[2D-Curl]] equals ${\pi\over2}+1$.
- The sign indicates an **anticlockwise** rotation.


> Original: [Curl warmup, fluid rotation in two dimensions](https://www.khanacademy.org/math/multivariable-calculus/multivariable-derivatives/divergence-and-curl-articles/a/curl-warmup)