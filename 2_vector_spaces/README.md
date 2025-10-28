<!-- .slide: data-background="#6A246D" -->


# Linear algebra: vector spaces

COMP1021 Maths for Computer Science


## Concept map

See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/6b85f75219cb74afa662c8e9b7d978f25269e50a/concepts.mmd)

Things in pink we will look at today



## More reading/watching

- Videos one and two in the series [Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) by [3blue1brown](https://www.3blue1brown.com/)
- Chapter 1 and section 2.4 of [Maths for machine learning](https://mml-book.github.io/)


## Structures (equipped) with multiple operations

So far we have ignored multiplication
- A _field_ has two operations, usually written $+$ and $\\cdot$
- Call them 'addition' and 'multiplication'
- In programming we are used to $+$ meaning different things


## Field axioms

- Look at the [classic definition of a field](https://en.wikipedia.org/wiki/Field_(mathematics)#Classic_definition)
- What terms are used that we haven't seen yet?
- Is a field also a group?
- Can every group be turned into a field?
- Can a field be finite?


## Structures with multiple sets

- Vectors are different from numbers (scalars)
- We can add vectors
- We can scale vectors (multiply)
- We can add scalars
- Can we multiply vectors?


<!-- .slide: class="fragmented-lists" -->

## Vector space

- Is a mathematical structure: sets, operations, axioms
- Has two sets: scalars $F$ and vectors $V$
- $V$ forms a commutative group under addition $\\mathbf{u}+\\mathbf{v} = \\mathbf{v}+\\mathbf{u}$
- $F$ forms a field (different kind of addition)
- Scalar multiplication $: F \\times V \\rightarrow V$


## Examples of vector spaces

<!-- .slide: class="fragmented-lists" -->

- $\\Bbb{R}^3 = \\Bbb{R} \\times \\Bbb{R} \\times \\Bbb{R}$ over $\\Bbb{R}$ 
  - vectors in $\\Bbb{R}^3$, scalars in $\\Bbb{R}$
- $\\Bbb{Z}_2^8$ over $\\Bbb{Z}_2$
- polynomials over $\\Bbb{R}$
- write down an example of scalar multiplication for each of these


## Notation conventions

- Write vector variables in bold $\\mathbf{u},\\mathbf{v} \\in V$
- Alternatives are $\\overline{v}, \\underline{v}, \\overrightarrow{v}$
- Write scalars plain $a,b \\in F$
- Vectors in $\\Bbb{R}^3$ as row $(1,-2,0)$ or column 

$$\\begin{pmatrix} 1\\\\-2\\\\0\\end{pmatrix}$$


<!-- .slide: class="fragmented-lists" -->

## Vector Space Axioms

- (commutative group and field axioms for vectors and scalars)
- $a(b\\mathbf{v}) = (ab)\\mathbf{v}$
- $1\\mathbf{v} = \\mathbf{v}$
- $a(\\mathbf{u} + \\mathbf{v}) = a\\mathbf{u} + a\\mathbf{v}$
- $(a + b)\\mathbf{v} = a\\mathbf{v} + b\\mathbf{v}$
- [MML](https://mml-book.github.io/) 2.4.2 only talks about vectors over reals $\\Bbb{R}$

<!-- .slide: class="fragmented-lists" -->

## Summary

- Fields have one set and two operations, addition and multiplication, like the real numbers
- Vector space includes a group of vectors and a field of scalars, with axioms governing scalar multiplication

