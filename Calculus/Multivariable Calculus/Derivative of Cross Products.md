## Derivative of cross products 
#MVC
Two ways to find the derivative of the cross product of two vectors $\frac{d}{dt}[\vec{u(t)}\times \vec{v(t)}]$:

Direct calculation to differentiate the result.

Use the product rule: $$\frac{d}{dt}(\mathbf{u} \times \mathbf{v}) = \frac{d\mathbf{u}}{dt} \times \mathbf{v} + \mathbf{u} \times \frac{d\mathbf{v}}{dt}$$.
(The same process as how we deduce the product rule: $u(t+\delta)\wedge v(t+\delta)$)

Use the rule of differentiation of a determinant: $$ \frac{d}{d t}\left|\begin{array}{ccc}i & j & k \\ v_{x} & v_{y} & v_{z} \\ u_{x} & u_{y} & u_{z}\end{array}\right| =\left|\begin{array}{ccc}i & j & k \\ \frac{d v_{x}}{d t} & \frac{d v_{y}}{d t} & \frac{d v_{z}}{d t} \\ u_{x} & u_{y} & u_{z}\end{array}\right|+\left|\begin{array}{ccc}i & j & k \\ v_{x} & v_{y} & v_{z} \\ \frac{d u_{x}}{d t} & \frac{d u_{y}}{d t} & \frac{d u_{z}}{d t}\end{array}\right|$$
One useful application of it is in the proof of [Abel's identity](http://en.wikipedia.org/wiki/Abel%27s_identity)(which before Wikipedia was known to me as Ostrogradski-Liouville formula)
[Derivative of cross-product of two vectors](https://math.stackexchange.com/questions/149817/derivative-of-cross-product-of-two-vectors)
