---
publish: true
created: 2026-07-17T11:46:28.016Z
modified: 2026-09-08T15:37:24.712Z
---

> [!greenbox]+ **Lemma SH.1**: (Locally describing a subsheaf of a sheaf)
> Suppose $\SF$ is a sheaf on a topological space $X$.
>
> 1. $\set{U_i}$ is a cover for $X$ and we are given sheaves $\SG_i$ on $U_i$ such that each $\SG_i$ is a subsheaf of $\SF|_{U_i}$ and $\SG_i|_{U_i\cap U_j} = \SG_j|_{U_i\cap U_j}$, then there exists a unique subsheaf $\SG$ of $\SF$ such that $\SG|_{U_i} = \SG_i$
> 2. Given another collection $\set{(\SH_i, V_i)}$ with its gluing $\SH$ as above, $\SH = \SG \iff \SG_i|_{U_i\cap V_j} = \SH_j|_{U_i\cap V_j}$

^46a917

> [!proof]- _Proof:_ TBW

> [!greenbox]+ **Lemma SH.2**: (Finite skyscrapers)
> Let $X$ be a topological space and $\set{x_1,\dots,x_n} = S$ be a finite collection of closed points. Let $\SF$ be a sheaf supported only on points of $S$. By $\SF_i$ denote the skyscraper sheaf at $x_i$ with $\SF_{i,x_i} \simeq \SF_{x_i}$. Then
>
> $$
> \SF \simeq \bigoplus_{i=1}^n \SF_i
> $$

^e7b717

> [!proof]- _Proof_: TBW

> [!greenbox]+ **Corollary SH.3**:
> Let $\SF$ and $\SG$ be sheaves on $X$, supported on a finite collection of closed points $S$.
> Then $\SF \simeq \SG \iff \SF_x = \SG_x \fall x\in X \iff \SF_x = \SG_x \fall x\in S$

^2f3027

> [!proof]- _Proof_: Follows from [[#^e7b717|lemma]] SH.2

> [!greenbox]+ **Proposition SH.4**:
> Let $(X, \OX)$ be scheme, $\set{x_1,\dots,x_n}$ a finite collection of closed points of $X$ and $\SF = \bigoplus_{i = 1}^n \SO_{X,x_i}/\mathfrak a_i$, where $a_i$ is an ideal. We have a natural map $\pi: \OX \to \SF$ obtained by taking stalks in each component and the taking the quotient. Then given any $\OX$-module morphism $\varphi: \OX \to \SF$ we have $\ker \varphi = \ker \pi$.

^f8f57b

> [!proof]- _Proof_:
> We do this by obtaining an isomorphism $f: \SF \to \SF$ such that $f \circ \varphi = \pi$
> \
> For any $i$, we have a map $\SO_{X,x_i} \to \SF_x = \SO_{X,x_i}/\mathfrak a_i$ with $1 \mapsto \bar g_{x_i}$
> But since the map is surjective, $\bar g_{x_i}$ must be a unit in $\SO_{X,x_i}/\mathfrak a_i$
> Multiplication by $\bar g_{x_i}\inv$ induces an isomorphism $\SF_{x_i}\to \SF_{x_i}$. Patching these together, we get $f$.
> \
> For $f_{x_i}\circ \varphi_{x_i}$, $1 \mapsto \bar g_{x_i}\inv \to \bar 1$, which is same as $\pi_{x_i}$.
> Thus $f\circ \varphi = \pi$
