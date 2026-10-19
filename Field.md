---
type: concept
maturity: seed
created:
modified:
term-week:
tags:
  - maths/algebra/abstract
project:
author:
  - "[[Ella Boulton]]"
---
# Concept: Field
***
## Overview / Definition
### Rough definition: 
A **field** is a [[Set]] equipped with the four standard operations of addition, multiplication, subtraction (inverse of addition) and division (inverse of multiplication).

### Formal definition
A **field** is a [[Ring|commutative ring]] in which $0 \neq 1$ and all non-zero elements are invertible under multiplication.

Or in more detail, a **field** is a set $k$ with two operations, addition ($+$) and multiplication $(\cdot)$, such that
- It is an (abelian) [[Group]] under addition, with identity element $0=0_k$.
- The nonzero elements $k^\times$ form an abelian group under multiplication, with identity element $1=1_k$.
- Multiplication distributes over addition, as $a \cdot (b + c) = (a \cdot b) + (a \cdot c)$.


## Core principles / Key Characteristics
%% What is important to remember? %%


## Examples
### Infinite fields
- Rational numbers $\mathbb{Q}$, the "prototypical" field
- Real numbers $\mathbb{R}$
- Complex numbers $\mathbb{C}$ 

### Finite (Galois) fields
For more details, see [[Finite Field]].
- $\mathbb{F}_p = \mathbb{Z}/p\mathbb{Z}$, sometimes denoted $GF(p)$, for a prime $p \in \mathbb{Z}$
- $\mathbb{F}_{p^n} = GF(p^n)$ 

### Non-examples
- **Infinite fields:** $\mathbb{Q}$ (rationals), $\mathbb{R}$ (reals), $\mathbb{C}$ (complex numbers).
- **Finite fields:** $\mathbb{F}_p$ or $\mathbb{Z}/p\mathbb{Z}$ for a prime $p$ (e.g., [[Finite Field]]).



## Related Concepts
### Upstream
%% Parent or prerequisite content. %%
[[Ring]]
### Downstream
%% Child content and applications. %%
#### Variants and types
[[Topological field]]
[[Ordered Field]]
[[Finite Field]]
#### Core constructions
[[Vector space]]
[[Field extension]]
[[Galois theory]]
### Similar
%% Similar concepts. %%
[[Division ring]]
[[Integral domain]]

### Contrast
%% Counter concepts or adjacent but not similar things.. %%

## References / source
%% Any lectures, books, notes that this information was sourced from. %%