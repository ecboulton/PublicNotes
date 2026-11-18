---
type: concept
maturity: sapling
created: 2026-10-20T20:08
modified: 2026-10-20T20:31
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
# Concept: Presheaf
***
## Overview / Definition
%% 1-2 sentence simple definition of the concept. %%
A **presheaf** $\mathcal{F}$ of [[Set|sets]] (or [[abelian groups]]/[[Ring|rings]]) on a [[topological space]] $X$ is a data structure that assigns a set (or abelian group/ring) $\mathcal{F}(U)$ of "local sections" to every open set $U \subseteq X$, along with a family of restriction maps that allow these sections to scale down to smaller open subsets in a way that respects topological nesting.

## Core principles / Key Characteristics
%% What is important to remember? %%
A presheaf consists of two core components governed by **[[contravariant functoriality]]**:
- **Sections:** For each open set $U \subseteq X$, there is a set $\mathcal{F}(U)$. Elements $f \in \mathcal{F}(U)$ are called *sections* over $U$, and elements of $\mathcal{F}(X)$ are called *global sections*. 
- **Restriction Functions:** For every inclusion of open sets $V \subseteq U$, there is a restriction map $\text{res}^U_V: \mathcal{F}(U) \to \mathcal{F}(V)$, typically denoted as $\text{res}^U_V(f) = f|_V$. These assignments must satisfy two properties:
	1. **Identity Restriction:** Restricting a section to itself does nothing: $\text{res}^U_U = \text{id}_{\mathcal{F}(U)}$.
	2. **Composition Property (Diagram Commutativity):** For nested open sets $W \subseteq V \subseteq U$, restricting directly from $U$ to $W$ is identical to restricting step-by-step from $U$ to $V$, then $V$ to $W$: $(f|_V)|_W = f|_W$.

## Examples
- **[[Continuous functions]]:** Let $X$ be a topological space. The assignment $U \mapsto C(U)$ (the ring of continuous valued functions on $U$), again with standard domain restriction, forms a presheaf.
	- **Smooth/continuous real-valued functions:** Let $X=\mathbb{R}^n$. The assignment $U \mapsto C^\infty (U)$ (the ring of smooth real-valued functions on $U$), paired with the standard restriction of function domains, forms a presheaf.
- **Constant Presheaf:** Fix a set $S$. Assigning $\mathcal{F}(U) = S$ for all non-empty open sets $U$ with restriction being the identity on $S$ forms a presheaf.
- **Presheaf of Sections:** For a continuous map $\pi: Y \to X$, the assignment $U \mapsto \left\{ f: U \to Y \mid pi \circ f = \operatorname{id}_U \right\}$ forms a presheaf on $X$.





## Related Concepts
### Upstream
%% Parent or prerequisite content. %%
[[Topological Space]]

### Downstream
%% Child content and applications. %%
[[Sheaf]]
[[Sheafification]]
[[Sheaf Stalk]]
### Similar
%% Similar concepts. %%
[[Presheaf (Category Theory)]]
### Contrast
%% Counter concepts or adjacent but not similar things.. %%
[[Sheaf]]: a presheaf only handles passing information down to smaller subsets; unlike sheaves, it does not guarantee that this information is locally compatible or can be glued back together.
## References / source
%% Any lectures, books, notes that this information was sourced from. %%
The Geometry of Schemes (ANU, 2026) - Lecture 2: Details of sheaves and ringed spaces.