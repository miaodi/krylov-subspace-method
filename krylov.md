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

where $$\mathbf{A}$$ is a $$n\times n$$ matrix \($$\mathbf{A}\colon \mathbb{R}^n\rightarrow\mathbb{R}^n$$\). Let $$\mathcal{K}$$ and $$\mathcal{L}$$ be two $$m$$-dimensional subspaces of $$\mathbb{R}^n$$. A projection onto $$\mathcal{K}$$ and orthogonal to $$\mathcal{L}$$ is stated as:

> Find $$\tilde{\mathbf{x}}\in\mathcal{K}$$, such that $$\mathbf{b}-\mathbf{A}\tilde{\mathbf{x}}\perp\mathcal{L}$$, or $$\left( \mathbf{b}-\mathbf{A}\tilde{\mathbf{x}}, \mathbf{w} \right) =0,\forall\mathbf{w}\in\mathcal{L}$$.

If $$\mathcal{K}\neq \mathcal{L}$$ the projection is called _oblique_, otherwise, it is called _orothogonal_ projection.

### Matrix form

Let $$\mathbf{V}=\begin{bmatrix} \mathbf{v}_1 &  \mathbf{v}_2 & \dots & \mathbf{v}_m\end{bmatrix} $$be a $$ n\times m$$matrix whose column-vectors form a basis of $$\mathcal{K} $$ and  $$\mathbf{W}=\begin{bmatrix} \mathbf{w}_1 &  \mathbf{w}_2 & \dots & \mathbf{w}_m\end{bmatrix} $$be a $$ n\times m$$matrix whose column-vectors form a basis of $$\mathcal{L} $$. A vector $$\mathbf{x}$$ in $$ \mathcal{K}$$ can be written as

$$
\mathbf{x}=\mathbf{V}\mathbf{y},
$$

The orthogonality condition leads to the following linear system for the vector $$\mathbf{y}$$

$$
\mathbf{W}^T\mathbf{A}\mathbf{V}\mathbf{y}=\mathbf{W}^T\mathbf{b}.
$$

If $$\mathbf{W}^T\mathbf{A}\mathbf{V}$$ is non-singular, the following expression for the approximate solution results,

$$
\mathbf{x}=\mathbf{V}\left(\mathbf{W}^T\mathbf{A}\mathbf{V}\right)^{-1}\mathbf{W}^T\mathbf{b}.
$$

The following result guarantees the non-singularity of $$\mathbf{W}^T\mathbf{A}\mathbf{V}$$:

> Let

