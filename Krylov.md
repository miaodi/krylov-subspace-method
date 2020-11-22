---
description: A knowledge refresh material for PETSc study
---

# Krylov Subspace Method

## Basic definitions and projection

### Projection

Consider the linear system

$$
\mathbf{Ax}=\mathbf{b},
$$

where $$\mathbf{A}$$ is a $$n\times n$$ matrix \($$\mathbf{A}\colon \mathbb{R}^n\rightarrow\mathbb{R}^n$$\). Let $$ \mathcal{K} $$ and $$\mathcal{L}$$ be two $$m$$-dimensional subspaces of $$\mathbb{R}^n $$. A projection onto $$\mathcal{K}$$ and orthogonal to $$\mathcal{L}$$ is stated as:

> Find $$\tilde{\mathbf{x}}\in\mathcal{K}$$, such that $$\mathbf{b}-\mathbf{A}\tilde{\mathbf{x}}\perp\mathcal{L}$$, or $$\left( \mathbf{b}-\mathbf{A}\tilde{\mathbf{x}}, \mathbf{w} \right) =0,\forall\mathbf{w}\in\mathcal{L}$$.

If $$\mathcal{K}\neq \mathcal{L}$$ the projection is called _oblique_, otherwise, it is called _orothogonal_ projection.

### Matrix form


