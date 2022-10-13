$\gdef\V#1{\mathbf{#1}}$
`$\gdef\Vthree#1#2#3{\begin{pmatrix} #1 \\ #2 \\  #3 \end{pmatrix} }$`
`$\gdef\Vthrees#1#2#3{\Big(\begin{smallmatrix} #1 \\ #2 \\  #3 \end{smallmatrix} \Big)}$`

{{{PURPLESLIDE}}}

## Vector spaces, linear combinations

COMP1021 MCS: Linear algebra

---

## Previously

See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/eda722174a07eaee5df5579226749d5d755a7e76/concepts.mmd)

Things in pink we will look at today

---
{{{APPEAR}}}

## Vector space

- Is a mathematical structure: sets, operations, axioms
- Has two sets: scalars $F$ and vectors $V$
- $V$ forms a commutative group under addition
- $F$ forms a field (different kind of addition)
- Scalar multiplication $: F \times V \rightarrow V$

---

## Notation conventions

- Write vector variables in bold $\V{u},\V{v} \in V$
- Alternatives are $\overline{v}, \underline{v}, \overrightarrow{v}$
- Write scalars plain $a,b \in F$
- Vectors in $\R^3$ as column $\Vthree{1}{-2}{0}$ or row $(1,-2,0)$

---

{{{APPEAR}}}

## Vector Space Axioms

See [wikipedia](https://en.wikipedia.org/wiki/Vector_space#Definition_and_basic_properties)

- $ a(b\V{v}) = (ab)\V{v}$
- $1\V{v} = \V{v}$
- $a(\V{u} + \V{v}) = a\V{u} + a\V{v}$
- $(a + b)\V{v} = a\V{v} + b\V{v}$
- [MML](https://mml-book.github.io/) 2.4.2 only talks about vectors over reals $\R$

---

## Examples of vector spaces

{{{APPEAR}}}

- $\R^3 = \R \times \R \times \R$ over $\R$ 
  - vectors in $\R^3$, scalars in $\R$
- $\Z_2^6$ over $\Z_2$
- polynomials over $\R$
- write down an example of scalar multiplication for each of these

---

## Linear combinations

Given vectors $\V{v_1}, \ldots ,\V{v_n}$ and scalars $a_1, \ldots ,a_n$

We can form a _linear combination_

$$ a_1\V{v_1} + \ldots + a_n\V{v_n}$$

Alternatively

$$ \sum_{i=1}^n a_i\V{v_i} $$

---
{{{REVEAL}}}

## Span

The set of all linear combinations of a set of vectors is called its _span_


- _Describe (in words) the span of the set `$\{\Vthrees{0}{1}{0},\Vthrees{0}{1}{1}\}$`_
- N.B. If the field is infinite then the span will be infinite (for a non-empty set)


---

## Spanning set

A set of vectors $S$ is a _spanning set_ for a vector space $(F,V)$ if $span(S)=V$