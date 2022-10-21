{{{PURPLESLIDE}}}

## Linear maps

COMP1021 MCS: Linear algebra

---

## Previously

See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/44dd15b4543fafc16fcbbd24464df16e6ac17e80/concepts.mmd)

Things in pink we will look at today

---
{{{APPEAR}}}

## Basis representation

- Remember: a set of vectors is a __basis__ for the vector space if it __spans__ the whole space and is __linearly independent__

- __Thm__ For a vector space $V$ the representation of any $v \in V$ as a linear combination of a given basis $S = \lbrace s_1,\ldots,s_n \rbrace$ is unique
- __Proof__ (sketch). Suppose not. Then subtract the two representations. This violates one of the properties of a basis. So we have a contradiction.

---

## Canonical (standard) basis

- This is kind of obvious for the _canonical basis_ for $\Bbb{R}^n$ 
$$\lbrace \mathbf{e}_i: i \leq 1 \leq n \rbrace$$
- Where $\mathbf{e}_i$ is the vector with a 1 in the ith position and 0 elsewhere
- In 3D sometimes referred to as $\mathbf{e}_x,\mathbf{e}_y,\mathbf{e}_z$ or $\mathbf{i},\mathbf{j},\mathbf{k}$



---

{{{APPEAR}}}

## Linear map

__Defn__ If we have a function $f:V \rightarrow W$ where $V$ and $W$ are vectors spaces over a field $F$ then $f$ is a _linear map_ if for any vectors $\mathbf{u}, \mathbf{v} \in V$ and $a \in F$
$$f(\mathbf{u} + \mathbf{v}) = f(\mathbf{u}) + f(\mathbf{v})$$
$$f(a \mathbf{v}) = a f(\mathbf{v}) $$

---

- This means that a linear map _respects_ linear combinations
- Linear maps are sometimes called _linear transformations_ or _vector space homomorphisms_
- If $V=W$ then $f$ is an _endomorphism_
- All linear maps preserve lines

---

{{{APPEAR}}}

## Examples of linear maps

- Scaling (on $\Bbb{R}^3$)
- Reflection
- Rotation
- Shearing 
- Projection
- Embedding
- Differentiation (on polynomials)

---

## Linear maps and basis vectors

- Every vector $\mathbf{v}$ can be represented as a linear combination of basis vectors $\mathbf{s}_i \in S$
- If we apply a linear map $f$ then
`$$f(v) = f(\sum_{i=1}^n a_i \mathbf{s}_i) = \sum_{i=1}^n a_i f(\mathbf{s}_i)$$`
- So a _linear map is characterised by its action on basis vectors_

---

{{{APPEAR}}}

## Images of basis vectors

For example, rotation by 90 degrees anti-clockwise in $\Bbb{R}^2$
- Q: What are the images of the canonical basis vectors $\mathbf{e}_1 (1,0)$ and $\mathbf{e}_2 (0,1)$?
- A: $(0,1)$ and $(-1,0)$ or $\mathbf{e}_2$ and $-1\mathbf{e}_1$
- Turn these into column vectors to get the  matrix representation

`$$\begin{pmatrix}0&-1 \\1 & 0 \end{pmatrix}$$`

---

## You try

Choose one of the linear map examples

Write down the images of the basis vectors in either $\Bbb{R}^2$ or $\Bbb{R}^3$

---

## Calculating from basis vector images

What happens when we rotate the vector $(2,3)$?

`$$\begin{aligned} rotate((2,3)) &= rotate(2\mathbf{e}_1 + 3\mathbf{e}_2) \\
&= 2.rotate(\mathbf{e}_1) + 3.rotate(\mathbf{e}_2)\\
&= 2\mathbf{e}_2 + 3.(-1.\mathbf{e}_1) \\
&= (-3,2)
\end{aligned}$$`

---

## Generalising basis images

Write basis vector images columns under f as a matrix

`$$\small{ A = \begin{pmatrix} a_{11} & a_{21} & \ldots & a_{1n}\\a_{21} & a_{21} & \ldots & a_{2n}\\
\vdots & \vdots & \ddots & \vdots \\a_{m1} & a_{m2} & \ldots & a_{mn}
\end{pmatrix}}$$`

$a_{ij}$ is ith component of f-image of jth basis vector

$$f(\mathbf{e_j}) = \sum_{i=1}^m a_{ij} \mathbf{e}_i$$

---

The image of the vector $A\mathbf{x} = A(x_1,\ldots,x_n)$ is

`$$\begin{aligned}
f(\sum_{j=1}^n x_j\mathbf{e}_j) &= \sum_{j=1}^n x_j f(\mathbf{e}_j) \\
&= \sum_{j=1}^n x_j \sum_{i=1}^m a_{ij} \mathbf{e}_i \\
&= \sum_{j=1}^n \sum_{i=1}^m a_{ij} x_j \mathbf{e}_i \\
\end{aligned}$$`

So the ith component of the image of $\mathbf{x}$ is $$\sum_{j=1}^m a_{ij} x_j$$

---

## Example

`$$\begin{pmatrix} 1 & -2 & 3 \\ -4 & 5 & -6 \end{pmatrix}
\begin{pmatrix} 9 \\ 8 \\7 \end{pmatrix}$$`
---

Matrix multiplication

Identity

{{{BLUESLIDE}}}
Next time: Determinants and inverses