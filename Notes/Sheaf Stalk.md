---
type: concept
maturity: seed
created: 2026-10-20T20:48
modified: 2026-10-20T21:50
term-week:
tags:
  - area/academic/courses/anu/schemes
  - maths/geotop/algebraic
  - maths/geotop/general-topology
project:
author:
aliases:
  - germ
  - stalk
---
%% Template for making a permanent note on a concept or idea. %%
# Concept: Sheaf Stalk
***
## Overview / Definition
%% 1-2 sentence simple definition of the concept. %%
Given a [[sheaf]] $(X,\mathcal{F})$, the **stalk** $\mathcal{F}_x$ at a point $x \in X$ captures the local behaviour of the sheaf in an arbitrarily small neighbourhood around $x$. 

It formalises what it means to look at a sheaf section infinitesimally close to a point without evaluating it strictly *at* that point (since sections are defined only on [[open sets]]), using a [[Categorical Colimit|direct limit]]:
$$\mathcal{F}_x = \varinjlim_{U \ni x} \mathcal{F}(U)$$
Elements of the stalk $\mathcal{F}_x$ are called **germs**, they are equivalence classes of pairs $(U,f)$ with $x \ni U$ and $f \in \mathcal{F}(U)$ where equivalence describes compatibility on intersections.


## Core principles / Key Characteristics
%% What is important to remember? %%
### Germ
Elements of the stalk $\mathcal{F}_x$ are called **germs**. They are equivalence classes of pairs $(U,f)$ where $U \ni x$ and $f \in \mathcal{F}(U)$, where $(U,f) \sim (V,g)$ if there is a smaller open neighbourhood $x \in W \subseteq U \cap V$ where $f$ and $g$ agree ($f|_W = g|_W$).
### Structure preservation
If $\mathcal{F}$ is a sheaf whose sections belong to a specific [[category]], then the stalk $\mathcal{F}_x$ inherits that same category, because restrictions are [[Morphism (Category Theory)|morphisms]].
### Local rings
In [[Scheme|scheme]] theory, the stalks of the structure sheaf $\mathcal{O}_{X,x}$ are always [[Local Ring|local rings]], because the structure sheaf is a [[Locally Ringed Space|locally ringed space]]. This means the stalks contain a unique maximal ideal.

## Examples
### Continuous functions on $\mathbb{R}$
Let $\mathcal{F}=C(\mathbb{R})$ be the sheaf of [[continuous functions]] on $\mathbb{R}$. The stalk $\mathcal{F}_0$ is a ring. It has the following (types of) germs (among others):
- **Constant germs:** every real number $c \in \mathbb{R}$ corresponds to a constant $c$-valued function, each of which has its own germ. So the constant germs form a subring of $\mathcal{F}_0$ which is isomorphic to $\mathbb{R}$.
- **Algebraic germs:** corresponding to [[rational functions]] (polynomials and ratios of polynomials). Two rational functions $\frac{P_1}{Q_1}$ and $\frac{P_2}{Q_2}$ (with $Q_i(0) \neq 0$) are equivalent (in the same germ) if and only if $P_1 Q_2 = P_2 Q_1$. 
	- That is, if there is a polynomial $S$ with $S(0)\neq 0$ such that $\frac{P_1}{Q_1} \sim \frac{P_2}{Q_2}$ in the [[localisation]] at $S$.
- **[[Analytic]] germs:** corresponding to [[power series]] with a non-zero [[radius of convergence]] centred at zero. For example, $\sin(x)$ and $e^x$
- **[[Smooth]]/[[differentiable]] germs:** corresponding to smooth/differentiable functions such as [[bump functions]].
- **Continuous germs:** things which are continuous but may not be differentiable at zero, e.g. $|x|$.
- **Not germs at all:** $\sqrt{x}$, since it is not defined on the negative side of any open neighbourhood.

The unique maximal ideal consists of all germs that vanish at the origin:
$$
\mathfrak{m}=\left\{ f \in \mathcal{F}_0 \mid f(0) = 0 \right\}
$$

### Structure sheaf stalk
For more details, see [[Structure Sheaf]].
For an [[affine scheme]] $X = \operatorname{spec}R$, the stalk of the structure sheaf $\mathcal{O}_X$ at a prime ideal $\mathfrak{p}$ is isomorphic to the local ring obtained by [[Ring Localisation|ring localisation]]: $\mathcal{O}_{X,\mathfrak{p}} \cong R_\mathfrak{p}$.


## Related Concepts
### Upstream
%% Parent or prerequisite content. %%
[[Direct Limit]]
[[Sheaf]]
[[Presheaf]]
[[Open Set]]
[[Locally Ringed Space]]
[[Ring Localisation]]
[[Structure Sheaf]]

### Downstream
%% Child content and applications. %%

### Similar
%% Similar concepts. %%
[[Categorical Colimit]]
### Contrast
%% Counter concepts or adjacent but not similar things.. %%
[[Global Section]]: a global section provides information about data across the entire topological space, whereas a germ in a stalk isolates the properties local to a point.
## References / source
%% Any lectures, books, notes that this information was sourced from. %%
The Geometry of Schemes (ANU, 2026) - Lecture 2