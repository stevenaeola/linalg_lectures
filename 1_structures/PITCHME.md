#  COMP1021  Maths for computer science {data-background-color=#6A246D}

Linear algebra: mathematical structures

---

## Why be abstract?

::: incremental

- Abstraction allows generalisation
- E.g. 3D vectors can be used to model force, position, velocity, acceleration, momentum, spin
- E.g. a list can be implemented with an array or a linked list
- We can build structures with other structures e.g. queue from a list
- Layers of abstraction e.g. NAND gate, CPU component, machine code instruction, virtual machine instruction, prog lang instruction, OS instruction
- At each level we fix the interface: can change details
- Algebra = abstraction

:::

---

## What about maths

::: incremental
- In programming we have data structures and operations e.g. string and concatentate
- A mathematical structure typically defines set(s), operations and axioms
- Programming operations are related to one another e.g. add an element to a list, increase length by 1
- Axioms are the rules which define a mathematical structure
:::

---

## Groups
... have a set $G$, a _binary operation_ $\star$, and some axioms
::: incremental
- $\star$ is _closed_ on $G$ i.e. $\star : G\times\G \rightarrow G$
- $\star$ is _associative_ i.e. for all $a,b,c$ in $G$, $a \star (b \star c) = (a \star b) \star c
- $G$ has an _identity_ element $e$ i.e. $\forall a \in G.a \star e = e \star a = a$
- $\star$ has an _inverse operator_ i.e. $\forall a \in G.\exists a^{-1}.a \star a^{-1}= a^{-1} \star a = e$

---

## Examples of groups

- The real numbers with +
- The integers with +
- Modulo arithmetic with +
- Anything we can prove about groups in general we know about all these groups
- E.g. identity is unique

---

## Which of these are groups?

- Even numbers with addition
- Odd numbers with addition
- Rational numbers with multiplication
- Strings with concatenation

---

# Next time {data-background-color=#a5c8d0}

Linear combinations of vectors

