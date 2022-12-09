{{{PURPLESLIDE}}}

## Sparse matrices: efficiency

COMP1021 MCS: Linear algebra

---

## Previously

- In the practical we found that matrix multiplication is $O(n^k)$
-  From [wikipedia](https://en.wikipedia.org/wiki/Matrix_multiplication_algorithm) we find $2.37188 \leq k \leq 3$

---

{{{APPEAR}}}

## Today

- Search engines using linear algebra
- Sparse matrices
- Santa using linear algebra (Markov chains)
- Diagonal matrices and eigenvectors

---

{{{APPEAR}}}

## [PageRank](https://en.wikipedia.org/wiki/PageRank)

- Invented by Larry Page and Sergey Brin (who founded google)
- (One of) the main non-content features of google until 2016
- Finds "importance" of a page by the number of pages that link to it
- But this can be gamed with link farms
- So want to consider the "importance" of pages of incoming links

---

{{{APPEAR}}}

## Basic idea of the algorithm

- Find all the links between web pages
- Construct the directed graph where nodes are pages and edges are links
- Make an initial assignment of PageRank values to each web page (node)
- Transfer the PageRank of each page to the pages it links to (follow edges)
- Weight the Rank according to the number of output links
- Repeat

---

## Solution in the simple case

`$$r(p) = \sum_{q \in I(p)}r(q)/l(q)$$`

Where 
- $r$ is the rank function
- $p$ and $q$ are pages
- $I(p)$ is the set of pages that link to $p$
- $l(q)$ is the number of links leaving $q$

---

## PageRank as a matrix equation

- Give all the pages a number $i=1 \ldots n$
- Find the [adjacency matrix](https://en.wikipedia.org/wiki/Adjacency_matrix) $A$
- Make $M$ the transposed modified adjacency matrix: scale so each column sums to 1
- Write the vector $\mathbf{r}$ as $(r_1,\ldots,r_n)$

`$$M\mathbf{r} = \mathbf{r}$$`

- More complex version includes _damping_

---

{{{APPEAR}}}
## How to solve the PageRank equation

- Currently [more than a billion web pages](https://siteefy.com/how-many-websites-are-there/)
- So solve a $10^9\times10^9$ matrix
- Good news: successive approximation gets close
- Bad news: just to store the matrix would take $8\times10^{18}$ bytes
- Good news: a lot of them are zeros (sparse)
- Bad news: multiplication in numpy is about $O(n^{2.85})$
- Good news: there are quicker ways of [multiplying sparse matrices](https://docs.scipy.org/doc/scipy/reference/sparse.html)

---

## Markov chains/processes

- Can think of the PageRank surfer as a Markov process
- Jumps randomly from state to state
- Probability of jumping depends only on current state
- PageRank is the steady state probability of being on a page

---

## Santa cares too

- Which reindeer should lead the sleigh?
- What is the [weather in Lapland](https://www.bbc.co.uk/weather/6296559)?
- A decent way to forecast the weather is "tomorrow will be the same as today"
- Could simplify to cloudy/snowy/clear

---

## [Weather as a Markov process](https://towardsdatascience.com/predicting-the-weather-with-markov-chains-a34735f0c4df)

- Look at the [history of weather in the place](https://www.timeanddate.com/weather/@830603/historic?month=12&year=2021)
- Work out transition probabilities between states
- Write transitions as a matrix $T$
- Write weather today as a (sparse) vector $\mathbf{w_0}$
- $\mathbf{w}_{i+1} = T \mathbf{w}_{i}$
- Then weather in $n$ days time is probably $\mathbf{w}_n = T^n \mathbf{w}_0$

---

{{{APPEAR}}}

## Steady state is an eigenvector

- Long range forecast is $\mathbf{w}_\infty$ 
- $T \mathbf{w}_\infty  = \mathbf{w}_\infty$
- This means that $\mathbf{w}_\infty$ is an _eigenvector_ with _eigenvalue_ 1
- In general if $A\mathbf{x} = \lambda \mathbf{x}$ then $\mathbf{x}$ is an _eigenvector_ of $A$ with _eigenvalue_ $\lambda$

---

## Basis of eigenvectors

If we can find a basis of eigenvectors then
- Matrix representation for that basis is diagonal
- Change of basis matrix $P$ is invertible
- Write $A = PDP^{-1}$ where $D$ is diagonal

---

## Advantages of diagonalisation

- Diagonal matrices are easy to store (sparse)
- Diagonal matrices are easy to multiply ($O(n)$)
- $A^n = (PDP^{-1})^n = PD^nP^{n-1}$
- Much quicker to find powers of matrices
- An example of _matrix factorisation_
- More in second term

---

{{{APPEAR}}}
## More on Markov processes

- Can be used to generate [musical chord sequences](https://towardsdatascience.com/markov-chain-for-music-generation-932ea8a88305)
- And also [words](https://sharecreative.com/news/can-we-use-ai-to-write-a-christmas-song/)
- Or [complete songs](https://yoloprogramming.com/post/2016/12/23/A-Very-Markov-Christmas)
- Have a Very Markov Christmas
- And may your matrices all be diagonal












