<!-- .slide: data-background="#6A246D" -->

## Dimensions: relation and reduction

COMP1021 MCS: Linear algebra


<!-- .slide: class="fragmented-lists" -->

## Previously

- See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/b29c8bdfd14d123c8c054fd830490d13f3f9316a/concepts.mmd)

- Things in pink we covered last time i.e. everything

- Questions? Assignment?


<!-- .slide: class="fragmented-lists" -->

## Row rank = Column rank

- Discussed last time
- IMPORTANT RESULT
- Dimension of $f(X)$ is the rank of the matrix for $f$
- Can calculate rank by Gaussian elimination
  - Count non-zero rows in row-echelon form of non-augmented matrix
- Matrix has _full rank_ if the rank is as high as it can be (max \#rows, \#columns)


## Kernel of a linear map

- if $f:X \rightarrow Y$ is a linear map
- _kernel_  or _null space_ of $f$ is the set of vectors that map to $\mathbf{0}$ i.e. 

$$\{ \mathbf{x} \in X.f(\mathbf{x}) = \mathbf{0} \}$$

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
  - So any inverse cannot be unique because $f(\mathbf{x} + \mathbf{k}) = f(\mathbf{x})$ if $\mathbf{k}$ is in the kernel
  - No


## Rank-nullity theorem

Define nullity as the dimension of the kernel
- Given a linear map on vector spaces $T:V \rightarrow W$
- If $V$ has finite dimension then

$$Rank(T) + Nullity(T) = dim(V)$$

Note that $dim(W)$ is not in the formula

Proof hint: Extend a basis for the kernel to a basis for $V$


<!-- .slide: class="fragmented-lists" -->

## Reducing dimensionality (not needed for assignment)

Many good reasons

- [Visualisation](https://www.nature.com/articles/s42003-022-03628-x)
- [Compression](https://www.sciencedirect.com/science/article/pii/S1877050917311900) of images and audio
- Speeding up machine learning
- Reducing overfitting/eliminating noise


<!-- .slide: data-background="#a5c8d0" -->

## More

- [3B1B Chapter 7: Inverse matrices, column space and null space](https://www.youtube.com/watch?v=uQhTuRlWMxw)
- [3B1B Chapter 8: Nonsquare matrices as transformations between dimensions](https://www.youtube.com/watch?v=v8VSDg_WQlA)
- [MML book](https://mml-book.github.io/book/mml-book.pdf) section 2.2.2
<!-- .slide: data-background="#a5c8d0" -->


## Next time

Efficiency of operations: intro to matrix factorisations