`$$\def\R{\mathbb{R}}$$`


## Vector spaces, linear combinations

COMP1021 MCS: Linear algebra


## Previously

See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/eda722174a07eaee5df5579226749d5d755a7e76/concepts.mmd)

Things in pink we will look at today



## Vector space

- Is a mathematical structure: sets, operations, axioms
- Has two sets: scalars $F$ and vectors $V$
- $V$ forms a commutative group under addition
- $F$ forms a field (different kind of addition)
- Scalar multiplication $: F \times V \rightarrow V$


## Notation conventions

- Write vector variables in bold $\mathbf \in V$
- Alternatives are $\overline$
- Write scalars plain $a,b \in F$
- Vectors in $\R^3$ as column `$\Big(\begin \Big)$` or row $(1,-2,0)$




## Vector Space Axioms

See [wikipedia](https://en.wikipedia.org/wiki/Vector_space#Definition_and_basic_properties)

- $ a(b\mathbf$
- $1\mathbf$
- $a(\mathbf$
- $(a + b)\mathbf$
- [MML](https://mml-book.github.io/) 2.4.2 only talks about vectors over reals $\R$


## Examples of vector spaces



- $\R^3 = \R \times \R \times \R$ over $\R$ 
  - vectors in $\R^3$, scalars in $\R$
- $\Z_2^8$ over $\Z_2$
- polynomials over $\R$
- write down an example of scalar multiplication for each of these


## Linear combinations

Given vectors $\mathbf$ and scalars $a_1, \ldots ,a_n$

We can form a _linear combination_

$$ a_1\mathbf$$

Alternatively

$$ \sum_ $$



## Span

The set of all linear combinations of a set of vectors is called its _span_


- Describe (in words) the span of the set `$\$`
- N.B. If the field is infinite then the span will be infinite (for a non-empty set)



## Spanning set

A set of vectors $S$ is a _spanning set_ for a vector space $(F,V)$ if $span(S)=V$