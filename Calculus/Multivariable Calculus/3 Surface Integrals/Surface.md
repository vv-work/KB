## Surface
#MVC 
### Definition
A *smooth parameterized [[surface]]* is a map $\mathbf{r}$, known as the **parameterization**
$$
\mathbf{r}: U \rightarrow \mathbb{R}^{3}, \quad(u, v) \mapsto(x(u, v), y(u, v), z(u, v))
$$
from an open subset $U \subseteq \mathbb{R}^{2}$ to $\mathbb{R}^{3}$, such that 
- $x, y, z$ have **continuous** partial derivatives with respect to $u$ and $v$ of all orders;
- $\mathbf{r}$ is a **bijection** between $U$ and $\mathbf{r}(U)$ with $\mathbf{r}^{-1}$ continuous and also possessing continuous partial derivatives of all orders;
- at each point the vectors $\frac{\partial \mathbf{r}}{\partial u}  \text { and }  \frac{\partial \mathbf{r}}{\partial v}$ are **[[linearly independent]]** (i.e. are not scalar multiples of one another). Equivalently,
$$
\frac{\partial \mathbf{r}}{\partial u} \wedge \frac{\partial \mathbf{r}}{\partial v} \neq \mathbf{0}
$$

We will not treat this definition with any generality. We shall simply parameterize some of the "standard" surfaces previously described.

### Example 33
>The quadrics are standard parameterized surfaces:
>- Sphere: $x^{2}+y^{2}+z^{2}=a^{2}$;
>- Ellipsoid: $x^{2} / a^{2}+y^{2} / b^{2}+z^{2} / c^{2}=1 ;$
>- Hyperboloid of One Sheet: $x^{2} / a^{2}+y^{2} / b^{2}-z^{2} / c^{2}=1 ;$
>- Hyperboloid of Two Sheets: $x^{2} / a^{2}-y^{2} / b^{2}-z^{2} / c^{2}=1$;
>- Paraboloid: $z=x^{2}+y^{2} ;$
>- Hyperbolic Paraboloid: $z=x^{2}-y^{2}$;
>- Cone: $x^{2}+y^{2}=z^{2} .$

### Definition 35
Let $\mathbf{r}: U \rightarrow \mathbb{R}^{3}$ be a smooth parameterized surface and let $\mathbf{p}$ be a point on the surface. The plane containing $\mathbf{p}$ and which is parallel to the vectors
$$
\frac{\partial \mathbf{r}}{\partial u}(\mathbf{p}) \quad \text { and } \quad \frac{\partial \mathbf{r}}{\partial v}(\mathbf{p})
$$
$\partial \mathbf{r} / \partial u$ and $\partial \mathbf{r} / \partial v$ is called the [[tangent plane]] to $\mathbf{r}(U)$ at $\mathbf{p}$. Because these vectors are independent the tangent plane is well-defined, and can also be shown to be independent of the choice of parameterization. 

Any vector in the direction
$$
\frac{\partial \mathbf{r}}{\partial u}(\mathbf{p}) \wedge \frac{\partial \mathbf{r}}{\partial v}(\mathbf{p})
$$
is said to be **normal** to the surface at $\mathbf{p}$. There are two unit normals of length one and we will write $\mathbf{n}$ or $\mathbf{n}(\mathbf{p})$ for a choice of unit normal; having made that choice the other unit normal is $-\mathbf{n}$.