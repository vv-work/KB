# MVC1
#ProblemSheet #MVC 
1. Let $a, b>0$. By swapping the order of double integrals of $e^{-x y}$ on the set $[0, \infty) \times[a, b]$ show that
$$
\int_{0}^{\infty} \frac{e^{-a x}-e^{-b x}}{x} \mathrm{~d} x=\ln \left(\frac{b}{a}\right).
$$
2. Show that
$$
\int_{y=0}^{y=1}\left(\int_{x=0}^{x=1} \frac{x-y}{(x+y)^{3}} \mathrm{~d} x\right) \mathrm{d} y=-\frac{1}{2} \neq \frac{1}{2}=\int_{x=0}^{x=1}\left(\int_{y=0}^{y=1} \frac{x-y}{(x+y)^{3}} \mathrm{~d} y\right) \mathrm{d} x .
$$
3. Show that
$$
\iint_{[0,1]^{2}}|x-y| \mathrm{d} A=\frac{1}{3} \text { . }
$$
Why does this integral represent the mean distance between two points chosen randomly and independently from the unit interval $[0,1]$ ?
4. (i) The [[moment of inertia]] of a uniform disc $D$ of radius $a$ and mass $m$ about an axis vertically through its centre equals
$$
I_{0}=\iint_{D} r^{2} \rho \mathrm{d} A
$$
where $\rho$ is the density of the disc. Determine $\rho$ in terms of $a$ and $m$. Use polar co-ordinates to show that $I_{0}$ equals $m a^{2} / 2$.
(ii) The vertical axis is moved from the centre of the disc to a point distance $R \leqslant a$ away. The moment of inertia now equals
$$
I_{R}=\iint_{D} d(r, \theta, R)^{2} \rho \mathrm{d} A
$$
where $d(r, \theta, R)$ is the distance of the point $(r, \theta)$ from the axis. Find $I_{R}$ and show that it is an increasing function of $R$ for $0 \leqslant R \leqslant a$
5. Let
$$
I=\iint_{[0,1]^{2}} \frac{\mathrm{d} x \mathrm{~d} y}{1-x y}
$$
(i) By applying the binomial theorem to the integrand, show that
$$
I=\sum_{n=1}^{\infty} \frac{1}{n^{2}}
$$
(ii) Set $x=u-v$ and $y=u+v$. Determine the Jacobian $\partial(x, y) / \partial(u, v)$. Show that
$$
I=4 \iint_{T} \frac{\mathrm{d} u \mathrm{~d} v}{1-u^{2}+v^{2}}
$$
where $T$ is the triangle with vertices $(0,0),(1,0)$ and $(1 / 2,1 / 2)$.
(iii) By splitting the interval $0 \leqslant u \leqslant 1$ into halves, and using trigonometric substitutions and identities, show that $I=\pi^{2} / 6$.
6. (Optional)
(i) Let $a \geqslant 0$. By applying the method of Exercise 1 to $e^{-y x} \sin x$, show that
$$
\int_{0}^{\infty}\left(1-e^{-a x}\right) \frac{\sin x}{x} \mathrm{~d} x=\tan ^{-1} a
$$
Deduce that $\int_{0}^{\infty} \frac{\sin x}{x} \mathrm{~d} x=\pi / 2$.
(ii) What is $\int_{0}^{\infty} \frac{\sin c x}{x} \mathrm{~d} x$ where $c$ is a real number?
(iii) Show that the integrals $\int_{0}^{n \pi}\left|\frac{\sin x}{x}\right| \mathrm{d} x$ increase without bound as $n$ becomes large.