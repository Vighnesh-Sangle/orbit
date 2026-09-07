---
publish: true
created: 2026-09-07T11:32:42.300Z
modified: 2026-09-07T16:48:14.807Z
---

### 3) Divisors on Curves

#### Some facts about Curves

> [!bluebox] **Proposition 3.1**: (Hartshorne I 6.8)
> Let $X$ be a non-singular curve, $Y$ a projective variety
> Let $P \in X$ and $\varphi: X - P \to Y$ a morphism.
> Then there exists a unique morphism $\bar\varphi: X\to Y$ extending $\varphi$

^33f750

> [!bluebox] **Corollary 3.2**:
> If two complete non-singular curves are birational, then they are isomorphic

^e05fb7

> [!orangebox]+ **Proposition 3.3**: (Hartshorne II 6.8)
> Let $X$ be complete non-singular curve, $Y$ any curve over $k$ and $f: X\to Y$ a morphism. If $f$ is non-constant, then $f(X) = Y$, $[K(X):K(Y)]$ is finite, $f$ is a finite map and $Y$  is also complete.

^be3f40

#### Divisors on Curves

From [[#^be3f40|Proposition]] 3.3, any non-constant map between complete non-singular curves is finite dominant. Hence $f^*: \Div Y \to \Div X$, as in [[Studies/Coursework/VSRP 2026/Final Writeup/1) Setup/1.5) Behavior of Divisors under Finite Dominant Maps#^64368c|Definition]] 1.5.2 makes sense.

Further, since curves are one-dimensional, the prime divisor and their generic points are the same. So, there is a simpler description of $f^*$

> [!yellowbox]+ **Definition 3.4**: ($f^*: \Div Y \to \Div X$ for curves)
> Let $f: X\to Y$ be a morphism of non-singular curves. Prime divisor are points. Let $s$ be a local parameter for a point $P \in Y$. Then $f^*P = \Sigma_{f(Q) = P} \ \nu_Q(s)Q$

Further, for finite dominant morphism of curves, the relative degree, as in [[Studies/Coursework/VSRP 2026/Final Writeup/1) Setup/1.5) Behavior of Divisors under Finite Dominant Maps#^bff06b|Definition]] 1.5.5 also becomes simple.

Suppose $f(Q) = P$. $\textnormal{deg}_f(Q) = [\kk(Q):\kk(P)]$ but since both $P$ and $Q$ are closed points, and $k$ is algebraically closed, this is $1$.

So, for curves, [[Studies/Coursework/VSRP 2026/Final Writeup/1) Setup/1.5) Behavior of Divisors under Finite Dominant Maps#^a5ce59|Proposition]] 1.5.6 simplifies to the following

> [!greenbox]+ **Proposition 3.5**: (Hartshorne II 6.9)
> Let $f: X\to Y$ be a morphism of non-singular curves and $D\in \Div Y$. Then
>
> $$
> \deg f^*D = \deg f \cdot \deg D
> $$

> [!proof]- _Proof_:
> This follows from [[Studies/Coursework/VSRP 2026/Final Writeup/1) Setup/1.5) Behavior of Divisors under Finite Dominant Maps#^a5ce59|Proposition]] 1.5.6 since $\textnormal{deg}_f = \deg$

#### Maps from curves to $\PP^1$

> [!greenbox]+ **Lemma 3.6**:
> If $X$ is non-singular curve and $f \in K(X)$, at any point, either $f$ or $\frac 1 f$ is regular and there exists a map $\tilde(f): X\to \PP^1$ which is sends $x \to (f(x):1)$ or $(1: \frac 1 f (x))$ depending on which of those is defined.

^2f3d23

> [!proof]- _Proof_:
> Since $X$ is non-singular curve, all local rings are DVRs, so for any $x \in X$ given any $f \in K(X)$, either $f$ or $\frac 1 f$ is in $\OXx$.
> \
> Using this with [[Studies/Coursework/VSRP 2026/Final Writeup/1) Setup/1.4) Maps to Projective Spaces and Linear Systems#^dacdae|Lemma]] 1.4.13 we are done.

> [!greenbox]+ **Lemma 3.7**: (Harthorne II 6.10)
> Let $X$ be a complete non-singular curve and $f \in K(X)^\times$.
> Then $\deg (f) = 0$ and thus we get a well defined degree map $\Cl X\to \ZZ$

^7453ae

> [!proof]- _Proof_:
> Consider the map $\tilde f : X\to\PP^1$. If $f$ is a constant function, then $(f) = 0$ and we have nothing to prove. So, assume $f$ is not constant, hence $\tilde f$ is a finite dominant map.
> \
> Consider the divisors $(0:1)$ and $(1:0)$ on $\PP^1$.
> $f^*((0:1) - (1:0)) = \Sigma_{f(P) = 0} \ \nu_P(\varphi(\frac {x_0} {x_1})P - \Sigma_{\frac 1 f (P) = 0} \ \nu_P(\varphi(\frac {x_1} {x_0})P$
> But $\varphi(\frac {x_0} {x_1}) = f$. So, this is same as $\Sigma_{\nu_P(f)\neq 0)} \ \nu(f)P = (f)$
> \
> Therefore, $\deg (f) = \deg f^*((0:1)- (1:0)) = \deg f \cdot 0 = 0$.
> Since all principal divisors are in the kernel of $\textnormal{deg} : \Div X \to \ZZ$, it induces the degree map $\Cl X\to \ZZ$

> [!greenbox]+ **Lemma 3.8**: (Hartshorne II 6.10.1)
> Let $X$ be a complete non-singular curve. Then
> $X$ is rational, i.e. $X\simeq \PP^1$ $\iff \texists P,Q \in X$, distinct closed points, such the as divisors $P \sim Q$

^71aa25

> [!proof]- _Proof_:
> If $X \simeq \PP^1$, $P \leftrightarrow (a:b), Q \leftrightarrow (c:d)$, then the rational function $\frac {bx_0 - ax_1} {dx_0 - cx_1}$ gives the divisor $P - Q$ and thus $P\sim Q$
> \
> Now the converse.
> If $P \sim Q$, then $P - Q = (f)$ for some $f \in K(X)$.
> Consider the morphism $\tilde f$ defined using [[#^2f3d23|lemma]] 3.6.
> $\tilde f(P) = (0:1)$ and $\tilde f (Q) = (1:0)$. Hence this is a non-constant map.
> \
> And $\tilde f^*(0:1) = P$, since a local parameter at $(0:1)$ is $\frac {x_0} {x_1}$ which maps to $f$. So $\tilde f$ must be a map of degree $1$. Therefore $\tilde f$ is a birational, and by [[#^e05fb7|Corollary]] 3.2 it must be an isomorphism.
