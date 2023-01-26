## Arc Length
#MVC 
### Definition
If $C$ is a curve with parameterization $\gamma:[a, b] \rightarrow \mathbb{R}^{3}$ then the [[arc length]] of the curve is
$$
\int_{C} \mathrm{~d} s=\int_{a}^{b}\left|\gamma^{\prime}(t)\right| \mathrm{d} t.
$$
### Example
>Find the [[arc length]] of the circular helix $\mathbf{r}(t)=(\cos t, \sin t, t)$ where $0 \leqslant t \leqslant 2 \pi$.

**Solution**. We have
$$
s=\int_{0}^{2 \pi}|(-\sin t, \cos t, 1)| \mathrm{d} t=\int_{0}^{2 \pi} \sqrt{1+\sin ^{2} t+\cos ^{2} t} \mathrm{~d} t=\int_{0}^{2 \pi} \sqrt{2} \mathrm{~d} t=2 \sqrt{2} \pi .
$$