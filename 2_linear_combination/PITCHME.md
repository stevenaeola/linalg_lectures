{{{PURPLESLIDE}}}

## Vector spaces, linear combinations

COMP1021 MCS: Linear algebra

---

## Previously

See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/c3cac59ea10b52ad14e8ca65e511f1ab6c652dee/concepts.mmd)

Things in pink we will look at today

---
{{{APPEAR}}}

## Vector space

- Is a mathematical structure: sets, operations, axioms
- Has two sets: scalars $F$ and vectors $V$
- $V$ forms a commutative group under addition $\mathbf{u}+\mathbf{v} = \mathbf{v}+\mathbf{u}$
- $F$ forms a field (different kind of addition)
- Scalar multiplication $: F \times V \rightarrow V$

---


## Notation conventions

- Write vector variables in bold $\mathbf{u},\mathbf{v} \in V$
- Alternatives are $\overline{v}, \underline{v}, \overrightarrow{v}$
- Write scalars plain $a,b \in F$
- Vectors in $\Bbb{R}^3$ as row $(1,-2,0)$ or column 

`$$\left( \begin{array}{c} 1\\-2\\0\end{array} \right)$$`

---

{{{APPEAR}}}

## Vector Space Axioms


- (commutative group and field axioms for vectors and scalars)
- $a(b\mathbf{v}) = (ab)\mathbf{v}$
- $1\mathbf{v} = \mathbf{v}$
- $a(\mathbf{u} + \mathbf{v}) = a\mathbf{u} + a\mathbf{v}$
- $(a + b)\mathbf{v} = a\mathbf{v} + b\mathbf{v}$
- [MML](https://mml-book.github.io/) 2.4.2 only talks about vectors over reals $\Bbb{R}$

---

## Examples of vector spaces

{{{APPEAR}}}

- $\Bbb{R}^3 = \Bbb{R} \times \Bbb{R} \times \Bbb{R}$ over $\Bbb{R}$ 
  - vectors in $\Bbb{R}^3$, scalars in $\Bbb{R}$
- $\Bbb{Z}_2^8$ over $\Bbb{Z}_2$
- polynomials over $\Bbb{R}$
- write down an example of scalar multiplication for each of these

---

## [3Blue1Brown](https://www.3blue1brown.com/)

[Essence of Linear Algebra](https://youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab&si=v4QBmXDAiy5LqX9D)

[Linear combination, span, and basis vectors](https://youtu.be/k7RM-ot2NWY?si=Ey2VR4H-qjlPk1fS)

---

## Linear combinations

__Defn__ Given vectors $\mathbf{v_1}, \ldots ,\mathbf{v_n}$ and scalars $a_1, \ldots ,a_n$

We can form a _linear combination_

$$ a_1\mathbf{v_1} + \ldots + a_n\mathbf{v_n}$$

Alternatively

$$ \sum_{i=1}^n a_i\mathbf{v_i} $$

---

{{{APPEAR}}}

## Span

__Defn__ The set of all linear combinations of a set of vectors is called its _span_


- Describe (in words) the span of the set $\lbrace(0,1,0),(0,1,2)\rbrace$
- N.B. If the field is infinite then the span will be infinite (for a non-empty set)


---

## Spanning set

__Defn__ A set of vectors $S$ is a _spanning set_ for a vector space $(F,V)$ if $span(S)=V$

We can equivalently say $S$ spans $V$

---

{{{APPEAR}}}

## Linear (in)dependence

- __Defn__ A set of vectors $S=\lbrace \mathbf{s_1},\ldots,\mathbf{s_n}\rbrace$ is _linearly dependent_ if there exists a linear combination

$$ \sum_{i=1}^n a_i\mathbf{s_i} = \mathbf{0} \text{ and } \exists i.a_i \neq 0$$

- In other words, we can write (at least) one of them as a linear combination of the others

- __Defn__ A set of vectors is _linearly independent_ if it is not linearly dependent

---

{{{APPEAR}}}

## Basis of a vector space

- __Defn__ A subset $S$ of vector space $V$ is a _basis_ for $V$ if $S$ spans $V$ and $S$ is linearly independent

- In other words $S$ is is the smallest spanning set we can find for $V$

- The standard/canonical basis for $\Bbb{R}^3$ is $\lbrace (1,0,0), (0,1,0), (0,0,1) \rbrace$

- Sometimes written $\lbrace \hat{\mathbf{i}}, \hat{\mathbf{j}}, \hat{\mathbf{k}}\rbrace$

---

{{{APPEAR}}}

## Dimension of a vector space

- __Defn__ The _dimension_ of a vector space is the cardinality (size) of its basis

- The dimension of $\Bbb{R}^3$ is 3

- We can prove that dimension is _well defined_ i.e. it is the same however you calculate

- I.e. all basis sets for a vector space are the same size

- Dimension can be infinite. Can you think of an example?

---

{{{APPEAR}}}

## Summary

- Vector space includes a group vectors and a field of scalars, with axioms governing scalar multiplication
- We can form linear combinations of vectors through scaling and adding
- All of the linear combinations of a set is called the span
- Vectors are linearly dependent if there is a non-zero linear combination of them that equals zero
- A basis is a linearly independent spanning set
- The dimension is the size of the basis

---

{{{BLUESLIDE}}}
Next time: linear maps and matrices