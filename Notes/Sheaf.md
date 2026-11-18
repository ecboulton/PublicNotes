---
type: concept
maturity: sapling
created: 2026-10-20T20:31
modified: 2026-10-20T20:33
term-week:
tags:
  - area/academic/courses/anu/schemes
  - maths/geotop/algebraic
  - maths/geotop/general-topology
project:
author:
aliases:
---
%% Template for making a permanent note on a concept or idea. %%
# Concept: Sheaf
***
## Overview / Definition
%% 1-2 sentence simple definition of the concept. %%
A **sheaf** $\mathcal{F}$ on a [[topological space]] $X$ is a [[presheaf]] whose sections are completely determined by their local behaviour. It adds two key constraints - **locality** and **gluing** - ensuring that data defined locally on an open cover can be uniquely pieced together into a well-defined global section.

## Core principles / Key Characteristics
%% What is important to remember? %%
### Definition
For a [[presheaf]] $\mathcal{F}$ to be upgraded to a sheaf, it must satisfy the following compatibility conditions for every open subset $U \subseteq X$ and every open covering $\{U_i\}_{i \in I}$ of $U$:
1. **Locality (Identity Axiom):** If two sections $f, g \in \mathcal{F}(U)$ agree on every piece of the open cover (i.e., $f|_{U_i} = g|_{U_i}$ for all $i \in I$), then they are globally equal on $U$ (i.e., $f = g$). In short: ***sections are equal if they are locally equal*.**
2. **Gluing (Gluing Axiom):** If you are given a collection of local sections $f_i \in \mathcal{F}(U_i)$ that match perfectly on all overlaps (i.e., $f_i|_{U_i \cap U_j} = f_j|_{U_i \cap U_j}$ for all $i, j \in I$), then there exists a section $f \in \mathcal{F}(U)$ such that $f|_{U_i} = f_i$ for all $i \in I$.

### Key properties
- **Uniqueness:** While the gluing axiom only dictates the *existence* of a glued section, this section is guaranteed to be unique by locality.
- **Empty set behaviour:** The section over the [[empty set]] (which is open) must collapse to a single point: $\mathcal{F}(\varnothing) = \left\{ * \right\}$.

## Examples
- **[[Continuous functions]]:** Let $X$ be a topological space. The assignment $U \mapsto C(U)$ (the ring of continuous valued functions on $U$), again with standard domain restriction, forms a sheaf.
	- **Smooth/continuous real-valued functions:** Let $X=\mathbb{R}^n$. The assignment $U \mapsto C^\infty (U)$ (the ring of smooth real-valued functions on $U$), paired with the standard restriction of function domains, forms a sheaf.
- **[[Structure Sheaf]]**:  a 
### Non-example
- **Constant Presheaf:** Fix a set $S$ which contains more than one element. Assigning $\mathcal{F}(U) = S$ for all non-empty open sets $U$ with restriction being the identity on $S$ forms a presheaf. But it fails the empty set condition since $\mathcal{F}(\varnothing)=S\neq \left\{ * \right\}$, so cannot be a sheaf.




## Related Concepts
### Upstream
%% Parent or prerequisite content. %%
[[Presheaf]]
[[Open Cover]]
### Downstream
%% Child content and applications. %%
[[Structure Sheaf]]
[[Ringed Space]]
[[Sheaf Stalk]]
[[Sheaf on a Base]]
### Similar
%% Similar concepts. %%
[[Sheafification]]
[[Sheaf (Category Theory)]]

### Contrast
%% Counter concepts or adjacent but not similar things.. %%
[[Presheaf]]: every sheaf is built from a presheaf, but presheaves themselves lack the gluing mechanism.
## References / source
%% Any lectures, books, notes that this information was sourced from. %%