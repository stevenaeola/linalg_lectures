{{{PURPLESLIDE}}}

## Matrix inverse

COMP1021 MCS: Linear algebra

---

## Previously

See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/tree/a2f55831993da5e52848b86e57f004452bff43f4)

Things in pink we will look at today

---

Questions? On determinants, row-echelon form, reduced row echelon form
Order of Steps of Gaussian elimination and Gauss-Jordan 
Given rref, write down solutions of equations

Rows of matrix as basis vector images

{{{APPEAR}}}

## Definition of inverse

- The _inverse_ of a function $f$ undoes the operation of $f$ and is written $f^{-1}$

- Inverse has to be _unique_ for $f^{-1}$ to be a function (otherwise a relation)

- When $f:X \rightarrow Y$ then $g$ is an inverse function of $f$ if $\forall x \in X.g(f(x)) = x$ and $\forall y \in Y.f(g(y)) = y$


---

## Inverse of a 2x2 matrix

Suppose we want to find the inverse of 

`$$\begin{pmatrix}1&2\\3&4\end{pmatrix}$$`

Then we want

`$$\begin{pmatrix}w&x\\y&z\end{pmatrix}\begin{pmatrix}1&2\\3&4\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix}$$`

Which gives the equations

`$$\begin{align}
w + 3x &= 1 \\
2w + 4x &= 0 \\
y + 3z &= 0\\
2y + 4z &= 1 
\end{align}
$$`

Solve these simultaneous equations for $w,x,y,z$

---

Answer is $\begin{pmatrix}-2&1\\ \frac{3}{2} & -\frac{1}{2}$


---

## General form of 2x2 inverse

Using the same approach for the general matrix $A$ write

`$$\begin{pmatrix}w&x\\y&z\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix}$$`

We get $A^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$

N.B. The inverse does not exist if the determinant is 0

---

## Inverse commutes

In general matrix multiplication is not commutative but if $AB=I$ then

`$$ A = IA = (AB)A = A(BA)$$`

So $BA$ is also the identity and hence $AA^{-1} = A^{-1}A = I$

---
{{{APPEAR}}}

## Finding inverse by Gauss-Jordan elimination


- Given $A$ we want to find $B$ so that $BA = I$
- Or, equivalently $AB = I$
- Could write down lots of equations and solve to find elements of $B$
- But we have a better way of solving systems of linear equations!
- Use Gauss-Jordan elimination on $A|I$

---

## Inverse of 2x2 example with Gauss-Jordan

Find inverse of $\begin{pmatrix}1&2\\3&4\end{pmatrix}$

`$$\begin{align}
\begin{pmatrix}1&2&1&0\\3&4&0&1\end{pmatrix} 
&\rightsquigarrow \begin{pmatrix}1&2&1&0\\0&-2&-3&1\end{pmatrix} \\
&\rightsquigarrow \begin{pmatrix}1&2&1&0\\0&1&\frac{3}{2}&-\frac{1}{2}\end{pmatrix} \\
&\rightsquigarrow \begin{pmatrix}1&0&-2&1\\0&1&\frac{3}{2}&-\frac{1}{2}\end{pmatrix} \\
\end{align}
$$`

---

{{{APPEAR}}}

## Column space and column rank

- Columns of a matrix are images of canonical basis vectors
- All vectors can be written as linear combinations of basis vectors
- Under a linear map $f: X \rightarrow Y, f(a\mathbf{x} + b \mathbf{y}) = a f(\mathbf{x}) + b f(\mathbf{y})$
- $f(X)$ is the span of of the columns, called the _column space_
- We define the _column rank_ to be the dimension of the column space
- The column rank is equal to the number of linearly independent columns in the matrix

---

## Row rank

- Define row space and row rank similarly
- Define _row space_ to be the span of all the row vectors
- Define _row rank_ is the dimension of the row space
- The row rank is equal to the number of linearly independent rows in the matrix

---



## Row rank=column rank

- Proof (sketch)
  - Each step of Gauss-Jordan elimination leaves column and row rank unchanged
  - Reduced row echelon form is reached
  - Can do more row/column operations to arrive at identity matrix surrounded by 0s
  - In this form row rank=column rank
- Define _rank_ of a matrix as the row/column rank

---

## Implications of Row rank=column rank

{{{APPEAR}}}

- IMPORTANT RESULT
- Dimension of $f(X)$ is the rank of the matrix for $f$
- Can calculate rank by Gaussian elimination
  - Count non-zero rows in row-echelon form of non-augmented matrix
- Matrix has _full rank_ if the rank is as high as it can be (max of number of rows, number of columns)

---

## Kernel of a linear map

- if $f:X \rightarrow Y$ is a linear map
- _kernel_  or _null space_ of $f$ is the set of vectors that map to $\mathbf{0}$ i.e. 

`$$\lbra \mathbf{x} \in X.f(\mathbf{x}) = \mathbf{0} \rbra$$`

- The kernel forms a vector space: all linear combinations of kernel elements are in the kernel

---

## No inverse of non-square matrices

Assume $X$ and $Y$ are vector spaces $f:X \rightarrow Y$ is a linear map

- Can an inverse exist if $dim(X) < dim(Y)$?
  - No: $dim(f(X)) \leq dim(X)$, so $dim(f(X)) < dim(Y)$
- Can an inverse exist if $dim(X) > dim(Y)$?
  - The columns of the matrix cannot be linearly independent
  - So there is a non-zero vector that maps to zero (kernel is non-trivial)
  - So any inverse cannot be unique because $f(\mathbf{x} + \mathbf{k}) = f(\mathbf{x})$ if $k$ is in the kernel

---

{{{BLUESLIDE}}}

## More

- [3B1B Chapter 7: Inverse matrices, column space and null space](https://www.youtube.com/watch?v=uQhTuRlWMxw) and [3B1B Chapter 8: Nonsquare matrices as transformations between dimensions](https://www.youtube.com/watch?v=v8VSDg_WQlA)

- [MML book](https://mml-book.github.io/book/mml-book.pdf) section 2.2.2

Next time: Dot products and norms

Practicals: Gaussian elimination, Gauss-Jordan elimination, rank, relationship to determinant




