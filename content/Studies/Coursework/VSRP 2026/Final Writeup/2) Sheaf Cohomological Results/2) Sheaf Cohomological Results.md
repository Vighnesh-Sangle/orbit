---
publish: true
created: 2026-07-14T13:31:43.023Z
modified: 2026-09-08T15:38:03.931Z
---

### 2) Sheaf Cohomological Results

> [!yellowbox]+ **Definition 2.1**: (Sheaf Cohomology)
> For a sheaf $\SF$ on a topological space $X$, the sheaf cohomology groups $H^i(X,\SF)$ are the right derived functors to the global sections functor $\Gamma(X,\_)$

> [!orangebox]+ **Theorem 2.2**: (Harshorne III 2.7)
> Let $X$ be a Noetherian topological space of dimension $n$. Then for all $i > n$ and all sheaves of abelian groups $\SF$ on $X$, $H^i(X,\SF) = 0$

^720302

> [!orangebox]+ **Theorem 2.3**: (Hartshorne III 5.19)
> Let $k$ be a field, let $A$ be a finitely generated $k$-algebra, let $X$ be a projective scheme over $A$, and let $\SF$ be a coherent $\OX$-module. Then $\Gamma(X,\SF)$ is a finitely generated $A$-module. In particular, if $A = k$, $\Gamma(X,\SF)$ is a finite dimensional $k$-vector space.

^8f9d0b

> [!yellowbox]+ Notation: If $X$ is a projective variety, then $H^i(X,\SF)$ are finite dimensional $k$-vector spaces. Then $h^i(X,\SF)$ is used to denote $\Dims kH^i(X,\SF)$

> [!yellowbox]+ **Definition 2.4**: (Euler Characteristic $\chi(\SF)$)
> For a coherent sheaf $\SF$ on a projective variety, $\chi(\SF) := \Sigma(-1)^{i}h^i(X,\SF)$

The above definition makes sense since [[#^720302|Theorem]] 2.2 turns this into a finite sum and [[#^8f9d0b|Theorem]] 2.3 ensures all $H^i(X,\SF)$ are finite dimensional.

> [!greenbox]+ **Lemma 2.5**:
> Let $X$ be projective variety over $k$ and suppose we have an exact sequence of $\OX$-modules
>
> $$
> 0 \to \SF_1\to\SF_2\to\SF_3\to 0
> $$
>
> Then $\chi(\SF_2) = \chi(\SF_1)+\chi(\SF_3)$

^970f48

> [!proof]- _Proof:_
> We get a long exact sequence of cohomology groups:
>
> $$
> \dots\to H^{i-1}(X,\SF_3)\to H^i(X,\SF_1)\to H^i(X,\SF_2)\to H^i(X,\SF_3)\to H^{i+1}(X,\SF_1)\to\dots
> $$
>
> Since this is an exact sequence of vector sequence $V_j$, we get that $\Sigma(-1)^i\Dims k V_j = 0$
> $\implies \Sigma(-1)^{3k}h^k(X,\SF_1) +\Sigma(-1)^{3k+1}h^k(X,\SF_2) +\Sigma(-1)^{3k+2}h^k(X,\SF_3) = 0$
> $\implies \chi(\SF_2) = \chi(\SF_1)+\chi(\SF_3)$

> [!greenbox]+ **Lemma 2.6**:
> Let $X$ be a curve, i.e., a 1-dimesional variety and $\SF$ be a skyscraper sheaf at a closed point $x$. Then $H^i(X,\SF) =0 \fall i \geq 1$

^a21183

> [!proof]- _Proof_:
> For $i \geq 2$, $H^i(X,\SF) = 0$ follows from [[#^720302|Theorem]] 2.2
> \
> For $i = 1$, $H_i(X,\SF) = 0$ is equivalent to showing that, for all exact sequences
>
> $$
> 0 \to \SF \to \SG \to \SG' \to 0
> $$
>
> The sequence the following sequence is exact
>
> $$
> 0 \to \Gamma(X,\SF) \to\Gamma(X,\SG) \to \Gamma(X,\SG')\to 0
> $$
>
> Say the map $\SG\to \SG'$ is $\varphi$
> Since $\Gamma(X,\_)$ is left exact, we only need to show that the second map, is surjective.
> \
> Restriction to an open set is an exact functor. Hence, for $U = X-\set x$
>
> $$
> 0 \to \SF|_U \to \SG|_U \to \SG'|_U \to 0
> $$
>
> is exact. But $\SF|_U = 0$. Thus $\SG|_U \simeq \SG'|_U$
> \
> Further, taking stalks is also an exact functor, hence $\SG_x\to \SG'_x$ is also surjective.
> \
> Now, let $s \in \Gamma(X,\SG')$. Then $\texists <t_1,V>\ \in \SG_x$ such that $<t_1,V> = t_{1,x}\mapsto s_x$
> So there is an open neighborhood $V'$of $x$ such that $s|_{V'} = \varphi(t_1)|_{V'}$
> \
> Further, $\texists t_0 \in \Gamma(U,\SG)$ such that $\varphi(t_0) = s|_{U}$
> \
> Now look at $U\cap V'$.
> $\SG(U\cap V') \to  \SG'(U\cap  V')$ is an isomorphism and both $t_0|_{U\cap V'}$ and $t_1|_{U\cap V'}$ map to $s|_{U\cap V'}$. Thus $t_0|U\cap V' = t_1|_{U\cap V'}$ and they glue together to give $t\in \Gamma(X,\SG)$ such that $\varphi(t) = s$

> [!greenbox]+ **Corollary 2.7**:
> Let $X$ be a curve and $\SF$ a skyscraper sheaf at a closed point $x\in X$ such that $\SF_x$ is a finite dimensional $k$-vector space. Then $\chi(\SF) = \Dims k \SF_x$

^a50a53

> [!proof]- _Proof_:
> From [[#^a21183|lemma]] 2.6 it follows that $\chi(\SF) = h^0(X,\SF) = \Dims k \Gamma(X,\SF) = \Dims k \SF_x$

> [!orangebox]+ **Theorem 2.8**: (Serre Duality)
> Let $X$ be nonsingular variety of dimension $n$ over an algebraically closed field $k$ and $\omega_X$ the canonical bundle. Then for any locally free sheaf $\SF$ of finite rank,
>
> $$
> H^i(X,\SF) \simeq H^{n-i}(X,\SF^\vee\otimes\omega_X)
> $$

^634e0d

> [!orangebox]+ **Proposition 2.9**: (Hartshorne Exercise III 4.1)
> Let $f:X\to Y$ be an affine morphism of Noetherian separated schemes. For any quasi-coherent sheaf $\SF$ on $X$, there are natural isormorphisms for all $i\geq 0$
>
> $$
> H^i(X,\SF) \simeq H^i(Y, f_*\SF)
> $$

^def235
