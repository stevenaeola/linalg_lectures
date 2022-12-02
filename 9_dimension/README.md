<!-- .slide: data-background="#6A246D" -->

## Dimensions: relation and reduction

COMP1021 MCS: Linear algebra


<!-- .slide: class="fragmented-lists" -->

## Previously

- See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/a2f55831993da5e52848b86e57f004452bff43f4/concepts.mmd)

- Things in pink we covered last time i.e. everything

- Any questions?

- Assignment 4)e)iii)


<!-- .slide: class="fragmented-lists" -->

## Reminder: rank

- The number of linearly independent columns of a matrix
- Equals the number of linearly independent columns rows of a matrix
- Equals the dimension of the image space
- Can be found by Gaussian elimination


<!-- .slide: class="fragmented-lists" -->

## Reminder: Kernel

- The set of all vectors that map to $\mathbf{0}$
- If kernel is non-trivial then the matrix is not invertible


## Rank-nullity theorem

Define nullity as the dimension of the kernel
- Given a linear map on vector spaces $T:V \rightarrow W$
- If $V$ has finite dimension then

`$$Rank(T) + Nullity(T) = dim(V)$$`

Note that $dim(W)$ is not in the formula

Proof hint: Extend a basis for the kernel to a basis for $V$


<!-- .slide: class="fragmented-lists" -->

## Reducing dimensionality

Many good reasons

- [Visualisation](https://towardsdatascience.com/dimensionality-reduction-for-data-visualization-pca-vs-tsne-vs-umap-be4aa7b1cb29)
- [Compression](https://towardsdatascience.com/image-compression-using-principal-component-analysis-pca-253f26740a9f) of images and audio
- Speeding up machine learning
- Reducing overfitting/eliminating noise

<!-- .slide: data-background="#a5c8d0" -->

## Next time

Efficiency of operations: intro to matrix factorisations