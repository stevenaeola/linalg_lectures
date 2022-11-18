<!-- .slide: data-background="#6A246D" -->

## Matrix inverse, rank, kernel

COMP1021 MCS: Linear algebra


## Previously

See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/a2f55831993da5e52848b86e57f004452bff43f4/concepts.mmd)

Things in pink we will look at today


## Reminder: row-echelon form

- All zero rows at the bottom
- Leading 1s in non-zero rows
- Leading 1s move right as you go down rows


<!-- .slide: class="fragmented-lists" -->

## Reminder: Gaussian elimination 

Gaussian elimination produces row-echelon form
  - Find pivot column, leftmost non-zero
  - Non-zero pivot element at top, swap rows if necessary
  - Multiply row to change pivot column to 1
  - Add multiples of top row to make other values in pivot column 0
  - Do GE on remaining rows


## Reminder: Gauss-Jordan elimination

- Produces reduced row-echeolon form
- Add suitable multiples of each row to create 0s above the leading 1s
- Can read off solutions directly
- Can find general solution to linear system


<!-- .slide: class="fragmented-lists" -->

## Definition of inverse

- The _inverse_ of a function $f$ undoes the operation of $f$ and is written $f^{-1}$

- Inverse has to be _unique_ for $f^{-1}$ to be a function (otherwise a relation)

- When $f:X \rightarrow Y$ then $g$ is an inverse function of $f$ if $\forall x \in X.g(f(x)) = x$ and $\forall y \in Y.f(g(y)) = y$


## Inverse of a 2x2 matrix

Suppose we want to find the inverse of 

`$$\begin{pmatrix}1&2\\3&4\end{pmatrix}$$`

Then we want

`$$\begin{pmatrix}w&x\\y&z\end{pmatrix}\begin{pmatrix}1&2\\3&4\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix}$$`


This gives the equations

`$$\begin{align}
w + 3x &= 1 \\
2w + 4x &= 0 \\
y + 3z &= 0\\
2y + 4z &= 1 
\end{align}
$$`

Solve these simultaneous equations for $w,x,y,z$


Answer is 

`$$\begin{pmatrix}-2&1\\ \frac{3}{2} & -\frac{1}{2}\end{pmatrix}$$`


## General form of 2x2 inverse

Using the same approach for the general matrix $A$

`$$\begin{pmatrix}w&x\\y&z\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix} = \begin{pmatrix}1&0\\0&1\end{pmatrix}$$`

We get 

`$$A^{-1} = \frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$$`

N.B. The inverse does not exist if the determinant is 0


## Inverse commutes

In general matrix multiplication is not commutative

But if $AB=I$ then

`$$ A = IA = (AB)A = A(BA)$$`

So $BA$ is also the identity and hence $AA^{-1} = A^{-1}A = I$

<!-- .slide: class="fragmented-lists" -->

## Inverse by Gauss-Jordan elimination


- Given $A$ we want to find $B$ so that $BA = I$
- Or, equivalently $AB = I$
- Could write down lots of equations and solve to find elements of $B$
- But we have a better way of solving systems of linear equations!
- Use Gauss-Jordan elimination on augmented matrix $A|I$


## Inverse of 2x2 example with Gauss-Jordan

Find inverse of 

`$$\begin{pmatrix}1&2\\3&4\end{pmatrix}$$`


`$$\begin{align}
\begin{pmatrix}1&2&1&0\\3&4&0&1\end{pmatrix} 
&\rightsquigarrow \begin{pmatrix}1&2&1&0\\0&-2&-3&1\end{pmatrix} \\
&\rightsquigarrow \begin{pmatrix}1&2&1&0\\0&1&\frac{3}{2}&-\frac{1}{2}\end{pmatrix} \\
&\rightsquigarrow \begin{pmatrix}1&0&-2&1\\0&1&\frac{3}{2}&-\frac{1}{2}\end{pmatrix} \\
\end{align}
$$`


<!-- .slide: class="fragmented-lists" -->

## Column space and column rank

- All vectors can be written as linear combinations of basis vectors
- Under a linear map $f: X \rightarrow Y, f(a\mathbf{x} + b \mathbf{y}) = a f(\mathbf{x}) + b f(\mathbf{y})$
- $f(X)$ is the span of of the columns, called the _column space_
- Define the _column rank_ as the dimension of the column space
- Column rank = \# linearly independent columns


## Row rank

- Define row space and row rank similarly
- Define _row space_ as the span of all the row vectors
- Define _row rank_ as the dimension of the row space
- Row rank = \# linearly independent rows 



<!-- .slide: class="fragmented-lists" -->
## Row rank=column rank

Define _rank_ of a matrix as the row/column rank

Proof (sketch)
- Each step of Gauss-Jordan elimination leaves column and row rank unchanged
- Reduced row echelon form is reached
- Can do more row/column operations to arrive at identity matrix surrounded by 0s
- In this form row rank=column rank



<!-- .slide: class="fragmented-lists" -->

## Implications


- IMPORTANT RESULT
- Dimension of $f(X)$ is the rank of the matrix for $f$
- Can calculate rank by Gaussian elimination
  - Count non-zero rows in row-echelon form of non-augmented matrix
- Matrix has _full rank_ if the rank is as high as it can be (max \#rows, \#columns)


## Kernel of a linear map

- if $f:X \rightarrow Y$ is a linear map
- _kernel_  or _null space_ of $f$ is the set of vectors that map to $\mathbf{0}$ i.e. 

`$$\{ \mathbf{x} \in X.f(\mathbf{x}) = \mathbf{0} \}$$`

- The kernel forms a vector space: all linear combinations of kernel elements are in the kernel


<!-- .slide: class="fragmented-lists" -->

## No inverse of non-square matrices

Assume $f:X \rightarrow Y$ is a linear map

Can an inverse exist if $dim(X) < dim(Y)$?
 - $dim(f(X)) \leq dim(X)$, so $dim(f(X)) < dim(Y)$
 - Some elements of $Y$ are not in $f(X)$
 - No


<!-- .slide: class="fragmented-lists" -->

Can an inverse exist if $dim(X) > dim(Y)$?
  - The columns of the matrix cannot be linearly independent
  - So there is a non-zero vector that maps to zero (kernel is non-trivial)
  - So any inverse cannot be unique because $f(\mathbf{x} + \mathbf{k}) = f(\mathbf{x})$ if $k$ is in the kernel
  - No


<!-- .slide: data-background="#a5c8d0" -->

## More

- [3B1B Chapter 7: Inverse matrices, column space and null space](https://www.youtube.com/watch?v=uQhTuRlWMxw)
- [3B1B Chapter 8: Nonsquare matrices as transformations between dimensions](https://www.youtube.com/watch?v=v8VSDg_WQlA)
- [MML book](https://mml-book.github.io/book/mml-book.pdf) section 2.2.2

Next time: Dot products and norms

Practicals: Gaussian elimination, Gauss-Jordan elimination, rank, relationship to determinant




