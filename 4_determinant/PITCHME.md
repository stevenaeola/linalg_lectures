{{{PURPLESLIDE}}}

## Determinants

COMP1021 MCS: Linear algebra

---

## Previously

See the [concept diagram](https://github.com/stevenaeola/linalg_lectures/blob/7794af3b1bcf1fe50f97c7947652383e7b748776/concepts.mmd)

Things in pink we will look at today

---

## Pythagoras' Theorem

![Graphical proof of Pythagoras theorem](Pythagoras-proof-anim.svg)

William B. Faulk, [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0), via Wikimedia Commons

---

## Area of unit square image

The linear map $f: \Bbb{R}^2 \rightarrow \Bbb{R}^2$ is represented by

`$$\begin{pmatrix}a & b \\ c & d\end{pmatrix}$$`

Using a graphical argument, find the area covered by the quadrilateral whose corners are

- $f((0,0))$
- $f((1,0))$
- $f((1,1))$
- $f((0,1))$

---

## What is a determinant?

See [3blue1brown video on determinants](https://www.youtube.com/watch?v=Ip3X9LOh2dk&list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab&index=6)

---

## Determinant of a 2x2 matrix

Determinant of matrix $A$ is written as $det(A)$ or $|A|$

For a 2x2 matrix 

`$$det(\begin{pmatrix}a & b \\ c & d\end{pmatrix}) = \begin{vmatrix}a & b \\ c & d\end{vmatrix} = ad-bc$$`

The determinant is the signed area of the image of the unit square

---

## 2x2 examples

`$$\begin{vmatrix}1 & -2 \\ 3 & -4\end{vmatrix} = 1.(-4) - (-2).3 = 2$$`

`$$\begin{vmatrix}1 & -2 \\ -2 & 4\end{vmatrix} = 1.4 - (-2).(-2) = 0$$`

The determinant is 0 when the columns are linearly dependent

---

## Determinant of nxn matrix

(Not defined for non-square matrices)

We define the determinant in terms of its properties

If a matrix $A$ is made out of columns vectors $\mathbf{c}_1,\ldots,\mathbf{c}_n$ we can define the function on the columns

$det(A) = det(\mathbf{c}_1,\ldots,\mathbf{c}_n)$ 

---

## det() definition: 1 linearity

Linearity in each column so that 

`$$det(a\mathbf{c}_1,\ldots,\mathbf{c}_n) = a.det(\mathbf{c}_1,\ldots,\mathbf{c}_n)$$`

`$$det(\mathbf{c}_1,\ldots,a\mathbf{c}_n) = a.det(\mathbf{c}_1,\ldots,\mathbf{c}_n)$$`

`$$det(\mathbf{c}_1 + \mathbf{c'}_1,\ldots,\mathbf{c}_n) = det(\mathbf{c}_1,\ldots,\mathbf{c}_n) + det(\mathbf{c'}_1,\ldots,\mathbf{c}_n)$$`

Etc: applies to all columns

---

## det() definition: 2 alternating


If $\mathbf{c}_i = \mathbf{c}_j$ for some $i \neq j$ then $det(A)=0$

---

## det() definition: 3 identity

The determinant of the identity matrix $I_n$ is 1

---

{{{APPEAR}}}

## Rationale based on area/volume

- Doubling one of the vectors doubles the area/volume
- We can add together the area/volumes of rectangles/cuboids/hypercuboids
- If the image of two vectors is the same then the image space has collapsed e.g. from 3D to 2D
- The unit square/cuboid/hypercuboid has area/volume 1

---



## Properties of determinants (provable)

If a matrix $B$ is like $A$ but with two columns swapped then $det(B) = - det(A)$

- Consider $det(\mathbf{c}_1+\mathbf{c}_2, \mathbf{c}_1+\mathbf{c}_2, \mathbf{c}_3, \ldots , \mathbf{c}_n)$
- Remember repeated columns have determinant 0

---

{{{APPEAR}}}

- If a matrix $A$ has a column made up of zeros then $det(A)=0$

- If a scalar multiple of one column is added to another column the determinant is unchanged

- If a matrix $A$ has columns that are linearly dependent then $det(A)=0$

---

## det() of diagonal matrix

`$$\small{
\begin{align}\begin{vmatrix}2&0&0\\0&4&0\\0&0&-3\end{vmatrix} &= 
2.\begin{vmatrix}1&0&0\\0&4&0\\0&0&-3\end{vmatrix} \\
&= 2.4.\begin{vmatrix}1&0&0\\0&1&0\\0&0&-3\end{vmatrix} \\
&= 2.4.-3\begin{vmatrix}1&0&0\\0&1&0\\0&0&1\end{vmatrix} \\
&= -24
\end{align}}
$$`

---

## Alternative derivation of 2x2 determinant

- Use linearity on the first column to expand out
- Then expand out the second column
- Determinants of repeated columns are 0
- Determinants of others are $\pm1$

---

## Determinant of 3x3

- Expand out first column: three terms
- Expand out second column: each one has two non-zero terms
- Expand out third column: each one has one non-zero term

Want more detail: see Strang text book or [youtube 18](https://www.youtube.com/watch?v=srxexLishgY&list=PL221E2BBF13BECF6C&index=39) and [19](https://www.youtube.com/watch?v=23LLB9mNJvc&list=PL221E2BBF13BECF6C&index=41)

---

{{{APPEAR}}}

## Determinant of nxn

Expanding out indefinitely to matrices whose columns are _permutations_ of the identity

Based on this we can use the _Laplace expansion_ 

`$$det(C) = \sum_{j=1}^n (-1)^{i+j}c_{ij}M_{ij}$$`

Where $M_{ij}$ is the minor: the determinant of the matrix $C$ with row $i$ and column $j$ removed

This works for any $i$: usually people use $i=1$

---

## 3x3 example

Find the determinant

`$$
\begin{vmatrix}1&2&3\\ 3&1&2 \\ 0&0&1\end{vmatrix} =
$$`

`$$ 1\begin{vmatrix}1&2 \\ 0&1 \end{vmatrix} -2 \begin{vmatrix}3&2 \\ 0&1\end{vmatrix} + 3 \begin{vmatrix}3&1 \\ 0&0 \end{vmatrix}
$$`

Check your answer in [MML](https://mml-book.github.io/book/) example 4.3

---

## Combining matrices

`$$det(AB) = det(A).det(B)$$`

`$$det(A^{-1}) = \frac{1}{det(A)}$$`

---

{{{APPEAR}}}

## Uses of determinants

- Finding the area/volume of images
- Finding out whether a set of vectors is linearly dependent
- Finding out whether a matrix has an inverse $det(A)\neq 0$
- Finding the inverse of a matrix (see next time)
- Hence solving equations with matrices (after that)

---

##

Next time: inverses

