<!-- .slide: data-background="#6A246D" -->

## Vector spaces, linear combinations

COMP1021 MCS: Linear algebra


## Previously

See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/eda722174a07eaee5df5579226749d5d755a7e76/concepts.mmd)

Things in pink we will look at today

<!-- .slide: class="fragmented-lists" -->

## Vector space

- Is a mathematical structure: sets, operations, axioms
- Has two sets: scalars $F$ and vectors $V$
- $V$ forms a commutative group under addition
- $F$ forms a field (different kind of addition)
- Scalar multiplication $: F \times V \rightarrow V$


<!-- .slide: class="fragmented-lists" -->

## Notation conventions

- Write vector variables in bold $\mathbf{u},\mathbf{v} \in V$
- Alternatives are $\overline{v}, \underline{v}, \overrightarrow{v}$
- Write scalars plain $a,b \in F$
- Vectors in $\Bbb{R}^3$ as column $(\begin{smallmatrix}1\\-2\\0\end{smallmatrix})$ or row $(1,-2,0)$


<!-- .slide: class="fragmented-lists" -->

## Vector Space Axioms

See [wikipedia](https://en.wikipedia.org/wiki/Vector_space#Definition_and_basic_properties)

- $a(b\mathbf{v}) = (ab)\mathbf{v}$
- $1\mathbf{v} = \mathbf{v}$
- $a(\mathbf{u} + \mathbf{v}) = a\mathbf{u} + a\mathbf{v}$
- $(a + b)\mathbf{v} = a\mathbf{v} + b\mathbf{v}$
- [MML](https://mml-book.github.io/) 2.4.2 only talks about vectors over reals $\Bbb{R}$


## Examples of vector spaces

<!-- .slide: class="fragmented-lists" -->

- $\Bbb{R}^3 = \Bbb{R} \times \Bbb{R} \times \Bbb{R}$ over $\Bbb{R}$ 
  - vectors in $\Bbb{R}^3$, scalars in $\Bbb{R}$
- $\Bbb{Z}_2^8$ over $\Bbb{Z}_2$
- polynomials over $\Bbb{R}$
- write down an example of scalar multiplication for each of these


## Linear combinations

Given vectors $\mathbf{v_1}, \ldots ,\mathbf{v_n}$ and scalars $a_1, \ldots ,a_n$

We can form a _linear combination_

$$ a_1\mathbf{v_1} + \ldots + a_n\mathbf{v_n}$$

Alternatively

$$ \sum_{i=1}^n a_i\mathbf{v_i} $$



## Span

The set of all linear combinations of a set of vectors is called its _span_


- Describe (in words) the span of the set $\lbrace(0,1,0),(0,1,2)\rbrace$
- N.B. If the field is infinite then the span will be infinite (for a non-empty set)



## Spanning set

A set of vectors $S$ is a _spanning set_ for a vector space $(F,V)$ if $span(S)=V$