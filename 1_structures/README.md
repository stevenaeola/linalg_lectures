#  COMP1021  Maths for Computer Science 

Linear algebra: mathematical structures


## Why be abstract?


- Abstraction allows generalisation
- E.g. a list can be implemented with an array or a linked list
- We can build structures with other structures e.g. queue from a list
- Layers of abstraction e.g. assembly instruction, virtual machine instruction, prog lang instruction
- At each level we fix the interface: can change details e.g. integers and real numbers on computer
- Algebra = abstraction



## What about maths?

- E.g. 3D vectors can be used to model force, position, spin etc
- In programming we have data structures and operations e.g. string and concatentate
- A mathematical structure typically defines set(s), operations and axioms
- Programming operations are related to one another e.g. add an element to a list, increase length by 1
- Axioms are the rules which define a mathematical structure
- Now not just the elements are abstract $x$, but also the operations


## Groups
... have a set $G$, a _binary operation_ $\star$, and some axioms
- $\star$ is _closed_ on $G$ i.e. $\star : G \times G \rightarrow G$
- $\star$ is _associative_ i.e. for all $a,b,c$ in $G$, $a \star (b \star c) = (a \star b) \star c$
- There exists an _identity_ element $e \in G$ i.e. $\forall a \in G.a \star e = e \star a = a$
- $\star$ has an _inverse operator_ i.e. $\forall a \in G.\exists b \in G . a \star b = b \star a = e$


## Examples of groups

- The real numbers with +
- The integers with +
- [Symmetries](https://en.wikipedia.org/wiki/Symmetry_group)
- Anything we can prove about groups in general we know about all these groups
- E.g. identity is unique


## Which of these are groups?

- Even numbers with addition
- Odd numbers with addition
- Rational numbers with multiplication
- Strings with concatenation


## Finite groups

- Most the examples have had infinite sets (which one hasn't?)
- Very common in CS to study finite sets e.g. bits
- In general we can study $Z_n$ modulo (clock) arithmetic


## Structures (equipped) with multiple operations

So far we have ignored multiplication
- A _field_ has two operations, usually written $+$ and $\cdot$
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


## More reading/watching

- Videos one and two in the series [Essence of Linear Algebra(https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) by [3blue1brown](https://www.3blue1brown.com/)
- Chapter 1 and section 2.4 of [Maths for machine learning](https://mml-book.github.io/)


# Next time 

Linear combinations of vectors, vector spaces

