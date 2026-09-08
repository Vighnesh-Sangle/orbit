---
publish: true
created: 2026-09-03T15:59:00.065Z
modified: 2026-09-08T15:37:27.261Z
---

> [!yellowbox]+ **Definition**: (Constructible set)
> A subset $Z$ of a scheme $X$ is said to be constructible if it can written as a finite disjoint union of locally closed sets.

> [!orangebox]+ **Theorem**: (Chevalley's Theorem) (Hartshorne II Exercise 3.9)
> Let $f: X\to Y$ be a morphism of finite type of Noetherian schemes. Then the image of every constructible subset of $X$ is a constructible subset of $Y$.

^020957

> [!bluebox]+ **Lemma**: (Hartshorn I Exercise 1.6)
> Let $X$ be a topological space and $A$ irreducible subset, then $\bar A$ the closure of $A$ in $X$ is an irreducible closed subset of $X$.

> [!bluebox]+ **Lemma**: (Hartshorne I Exercise 1.10(a))
> If $Y$ is any subset of a topological space $X$, then $\Dim Y \leq \Dim X$

^9b4a24

> [!greenbox]+ **Proposition**:
> Let $f: X\to Y$ be a morphism of varieties. Then the closure of $f(X)$ in $Y$ has dimension at most the dimension of $X$.

^34e12f

> [!proof]- _Proof_:
> We proceed by induction.
> Induction hypothesis: if $X$ is dimension $n$ variety and $f: X\to Y$ a morphism of varieties, then closure of $f(X)$ in $Y$ is irreducible and has dimension $\leq n$
> \
> Base case, when $n = 0$
> $X$ is a point. $f(x)$ is a point, hence irreducible and has dimension $0$.
> \
> Now suppose the hypothesis holds upto $n-1$.
> Let $f: X\to Y$ a morphism of varieties and $X$ of dimension $n$.
> \
> First we will show that $f(X)$ as a topological space has dimension $\leq n$
> Note that since  $X$ is irreducible and $f$ continuous, $f(X)$ is irreducible. Let $C$ be an irreducible closed subset in $f(X)$. To show that $f(X)$ has dimension at most $n$, it is enough to show that $\Dim C < n$.
> \
> Since $C$ is proper closed subset of $f(X)$, $f\inv(C)$ is a proper closed subset of $X$. Write $f\inv(C) = \bigcup C_i$, where each $C_i$ is an irreducible component of $f\inv (C)$.
> $\therefore$ $C = \bigcup f(C_i)$. Since this is a finite union, we also get $\bar C = \bigcup \bar {f(C_i)}$, where closures are taken in $Y$.
> \
> Each $C_i$ being a proper closed subset of $X$ has dimension $\leq n-1$. Therefore, by induction hypothesis, $\bar {f(C_i)}$ has dimension $\leq n-1$.  And since $\bar C$ is finite union of these and also irreducible, we must have $\bar C$ has dimension at most $n-1$ and so $C$ has dimension at most $n-1$ by [[#^9b4a24|lemma]].
> This shows that $f(X)$ has dimension at most $n$.
> \
> Now to show that $f(X)$ closure in $Y$ has dimension at most $n$. Here we have to use [[#^020957|Chevalley's Theorem]]. Since $f$ is a morphism of varieties, it is automatically of finite type. Hence, using the theorem write $f(X) = \bigsqcup K_i$ where each $K_i$ is closed inside $U_i$ an open subset of $Y$.
> \
> Within each $U_i$, $K_i$ can be written as a finite union of irreducible closed subset $C_{ij}$. Since $C_{ij}$ is closed inside an open set, it is open inside its closure in $Y$. Since  $C_{ij}$ and  $\bar C_{ij}$ are both varieties, we must have $\Dim C_{ij} = \Dim \bar C_{ij}$. But $C_{ij}$ is a subset of $f(X)$ hence has dimension at most $n$.
> \
> But $\bar {f(X)} = \bigcup \bar {C_{ij}}$ where this is a finite union and each $\bar {C_{ij}}$ has dimension at most $n$, we have that $\bar {f(X)}$ has dimension at most $n$.
