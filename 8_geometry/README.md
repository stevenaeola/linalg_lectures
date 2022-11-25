<!-- .slide: data-background="#6A246D" -->

## Geometry: Norms and dot product

COMP1021 MCS: Linear Algebra


## Definition and Etymology

> The branch of mathematics concerned with the properties and relations of points, lines, surfaces, and solids (originally one of the four subjects of the quadrivium). In later use also (from the 19th cent.): a generalization of this to spaces of more than three dimensions. 

([Oxford English Dictionary](https://www.oed.com/view/Entry/77794))

From land (geo-) survey/measure (metry)

We will think about lengths of vectors (norms) and angles between vectors


<!-- .slide: class="fragmented-lists" -->

## Euclidian norm

- How long is the vector $(x_1,x_2)$?
- By Pythagoras $l^2 = x_1^2 + x_2^2$
- In 3D $l^2 = x_1^2 + x_2^2 + x_3^2$


If $\mathbf{x} = (x_1,\ldots,x_n) \in \Bbb{R}^n$ then the _Euclidean norm_ is defined as

`$$\| \mathbf{x} \|_2 = \sqrt{\sum_{i=1}^n x_i^2}$$`

It is often shortened to 

`$$\| \mathbf{x} \|$$`

Euclidean is the 'default' norm


## Unit vectors

A unit vector has length (norm) 1

Any non-zero vector $\mathbf{x}$ can be used to define a unit vector in the direction of $\mathbf{x}$

`$$\mathbf{\hat{x}} = \mathbf{x}/ \| \mathbf{x} \|_2$$`


<!-- .slide: class="fragmented-lists" -->

## Generalised norms

Given a vector space $X$ a function $d:X \rightarrow \Bbb{R}$ is a _norm_ if it satisfies
- Triangle inequality. $d(\mathbf{x} + \mathbf{y}) \leq d(\mathbf{x}) + d(\mathbf{y})$ for all $\mathbf{x},\mathbf{y} \in X$
- Absolute homogeneity. $d(s\mathbf{x}) = |s|d(\mathbf{x})$ or all $\mathbf{x} \in X$ and scalars $s$
- Positive definite. If $d(\mathbf{x}) = 0$ then $\mathbf{x} = \mathbf{0}$


<!-- .slide: class="fragmented-lists" -->

## Provable properties of norms

- $d(\mathbf{0}) = 0$ 
- _Hint_ use absolute homogeneity
- Non-negative. $d(\mathbf{x}) \geq 0$ for all $\mathbf{x} \in X$ 
- _Hint_ consider $\mathbf{0} = \mathbf{x} - \mathbf{x}$


![Manhattan. Image by <a href="https://pixabay.com/users/wikiimages-1897/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=67474">WikiImages</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=67474">Pixabay</a>](manhattan.jpg)


## Manhattan norm

In Manhattan the streets are (mostly) laid out in a grid

To get anywhere you have to travel some distance north/south and some distance east/west

This gives rise to the Manhattan distance

`$$d_M((x_1, \ldots , x_n)) = \sum_{i = 1}^n |x_i|$$`

Is this a norm?


- Triangle inequality: yes
- Absolute homogeneity: yes
- Positive definite: yes


<!-- .slide: class="fragmented-lists" -->

## p-norms

Given $p \in \Bbb{R}^{+}$ we can define the _p-norm_ $\ell_p$ on $\Bbb{R}^n$ as

`$$\| \mathbf{x} \|_p = \sqrt[p]{\sum_{i=1}^n |x_i|^p}$$`

- $\ell_1$ is the Manhattan norm
- $\ell_2$ is the Euclidean norm

Different norms are often used in ML [regularisation](https://en.wikipedia.org/wiki/Regularization_(mathematics)) e.g. of [regression](https://en.wikipedia.org/wiki/Lasso_(statistics))

## p-norms to the limit

What happens if $p \rightarrow \infty$ 

Large terms dominate so $\ell_\infty$ is

`$$\| \mathbf{x} \|_{\infty} = max(|x_1|,\ldots,|x_n|)$$`

This is a norm (check properties)


What happens if $p \rightarrow 0$?

`$$\lim_{p\to 0} x^p = 1$$`

`$$\lim_{p\to 0} \| \mathbf{x} \| = \infty$$`

But (assuming $0^0=0$), can define $\ell_0$ as

`$$ \| (x_1,\ldots,x_n) = |x_0|^0 + \ldots + |x_n|^0 $$`

i.e. The number of locations in which $\mathbf{x} \neq 0$

Commonly used (Hamming distance), but not a norm. Why not?


## Other norms

Norms can be [combined](https://en.wikipedia.org/wiki/Norm_(mathematics)#Composite_norms)

Norms can be constructed relative to a point e.g. [railway metric](https://math.stackexchange.com/questions/3386031/show-that-the-railway-metric-is-a-metric)


## Non-Euclidean geometry

If we change the definition of 'parallel' we get [hyperbolic geometry](https://en.wikipedia.org/wiki/Hyperbolic_geometry)

E.g. hyperbolic [half-plane](https://en.wikipedia.org/wiki/Poincar%C3%A9_half-plane_model) or [disk](https://en.wikipedia.org/wiki/Poincar%C3%A9_disk_model)

These occur in [nature and art](https://web.colby.edu/thegeometricviewpoint/author/aredhunt/) and [crochet](https://pi.math.cornell.edu/~dwh/papers/crochet/crochet.html)


## Dot product

Given vectors $\mathbf{a}, \mathbf{b}$ define

`$$\mathbf{a} \cdot \mathbf{b} = \| \mathbf{a} \|_2 \| \mathbf{b} \|_2 \cos \theta$$`

Where $\theta$ is the angle between $\mathbf{a}$ and $\mathbf{b}$

Also referred to as inner product, scalar product



## Properties of dot product

- Finds projection of a vector in the direction of the other
- $\hat{\mathbf{a}} \cdot \hat{\mathbf{b}} = \hat{\mathbf{b}} \cdot \hat{\mathbf{a}} = \cos \theta$
- $(s \mathbf{a}) \cdot \\mathbf{b} = s(\mathbf{a} \cdot \mathbf{b})$
- $(\mathbf{a_1} + \mathbf{a_2})\cdot \mathbf{b} = \mathbf{a_1} \cdot \mathbf{b} + \mathbf{a_2} \cdot \mathbf{b}$
- $\mathbf{a} \cdot \mathbf{b} = 0$ if only if they are orthogonal or one is zero

`$$\mathbf{a} \cdot \mathbf{a} = \| \mathbf{a} \|_2^2$$`


## Calculating dot product

If $\mathbf{a} = (a_1,\ldots,a_n)$ and $\mathbf{b} = (b_1,\ldots,b_n)$

Then 

`$$\mathbf{a} \cdot \mathbf{b} = \sum_{i=1}^n a_ib_i$$`

Proof: write each vector as linear combination of standard basis vectors

## Cosine rule

Consider $\mathbf{a} = \mathbf{b} + \mathbf{c}$ and look at $\mathbf{c} \cdot \mathbf{c}$


<!-- .slide: class="fragmented-lists" -->

## Orthonormality

- Vectors are _orthogonal_ (at right angles) if their dot product is 0
- Vectors are _normal_ if their $\ell_2$ norm is 1
- A set of vectors is _orthonormal_ if they are all orthogonal and normal
- It is often useful to have an _orthonormal basis_ for a vector space

