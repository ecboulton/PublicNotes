---
type: concept
maturity: seed
created:
modified:
term-week:
tags:
  - maths/category
project:
author:
aliases:
---
%% Template for making a permanent note on a concept or idea. %%
# Theorem: Filtered colimits commute with finite products, fibre products and equalisers of sets.
***
Fix the category of sets.
## Theorem statement for limits.
*From [Stacks 4.19, Lemma 4.19.2](https://stacks.math.columbia.edu/tag/04AX).*
Let $I$ and $J$ be index sets, where $I$ is filtered ([[Directed Set|directed]]) and $J$ is finite. Let $M: I \times J \to \mathbf{Sets}$, $(i,j) \mapsto M_{i,j}$ be a diagram of diagrams (bifunctor) of sets. Then
$$
\varinjlim_{i \in I} \varprojlim_{j \in J} M_{i,j} = \varprojlim_{j \in J} \varinjlim_{i \in I} M_{i,j}
$$
### Proof
#### Bifunctor behaviour
The map $M: I \times J \to \mathbf{Sets}$ is a bifunctor, meaning a functor of two variables.

In the outer layer (fixed index $i \in I$), we have a functor $M_i: J \to \mathbf{Sets}$ taking $j \mapsto M_{i,j}$. 

In the inner layer (varying through $I$), we take a transition map in $I$, say $i \to i'$, and it produces a collection of functions that cleanly map the functor $M_i$ into the functor $M_{i'}$. 


#### Proof of isomorphism


An element of the LHS $\varinjlim_{i \in I} \varprojlim_{j \in J} M_{i,j}$ is represented by a pair $(i, (x_j)_{j \in J})$ where $i \in I$ and $(x_j)_{j \in J} \in \varprojlim_{j \in J} M_{i,j}$, meaning the $x_j \in M_{i,j}$ are compatible across the projective limit over $J$. We define a map:
$$
\begin{align*}
	\Phi: \varinjlim_{i \in I} \varprojlim_{j \in J} M_{i,j} & \to \varprojlim_{j \in J} \varinjlim_{i \in I} M_{i,j} \\
	[i, (x_j)_{j \in J}] & \mapsto ([i, x_j])_{j \in J}
\end{align*}
$$
##### Injectivity, using filtered property of $I$:
Suppose we have two elements of the LHS such that their image is the same:
$$
\Phi([i,(x_j)_{j \in J}]) = \Phi ([i', (y_j)_{j \in J}])
$$
Then for each $j \in J$, the components are equal in the colimit: $[i, x_j] = [i', y_j]$.

By definition of a filtered colimit, for each $j \in J$, there is an index $i_j \in I$ and morphisms $i \to i_j$ and $i' \to i_j$ mapping $x_j$ and $y_j$ to the same element of $M_{i,j}$. 

Since $J$ is finite and $I$ is filtered, we can find a single upper bound $n \in I$ which is greater than all $i_j \in I$, for all $j$. Thus, there exist common morphisms $\alpha: i \to n$ and $\beta: i' \to n$ such that for all $j \in J$, we have the equality $M(\alpha,j)(x_j) = M(\beta,j)(y_j)$ in $M_{n,j}$. So the tuples $(x_j)$ and $(y_j)$ become identical at index level $n$.

Thus, we have equality $[i,(x_j)_{j \in J}] = [i', (y_j)_{j \in J}]$ in the LHS colimit. So $\Phi$ is injective.

##### Surjectivity, using finiteness of $J$:
Let $(y_j)_{j \in J}$ be an element of the RHS limit $\varprojlim_{j \in J} \varinjlim_{i \in I} M_{i,j}$. 

Each $y_j$ is an equivalence class in the colimit, so $y_j = [i_j, x_j]$ for some $i_j \in I$ and $x_j \in M_{i_j, j}$. 

Since $J$ is finite and $I$ is filtered, there is a single index $n \in I$ that is greater than all $i_j$, and thus has maps $i_j \to n$. Thus we can assume (WLOG) that all elements share the index $n$. That is, $y_j = [n, x'_j]$ for all $j \in J$, where $x'_j \in M_{e,j}$. 

For any morphism $f: j \to j'$ in $J$, we know $y_j$ maps to $y_{j'}$. Thus, $[n, M(n,f)(x'_j)]=[n,x'_{j'}]$ are equal in the colimit. So for each morphism $f$, there is eventually an index $n_f \in I$ such that they are equal in $M_{n_f, j'}$. 

Since $J$ is finite, there are finitely many morphisms $f$ on $J$, so there are finitely many indices $n_f$ which equalise. Since $I$ is directed, there is a single index $n' \geq n_f$ and morphism $\omega: n \to n'$ in $I$ for all $f: j \to j'$ for any $j, j' \in J$, such that
$$
\begin{align*}
	M(\omega, j') \left( M(\operatorname{id}_n, f) (x'_j) \right) = M(\omega, j') (x'_{j'})
\end{align*}
$$
holds in $M_{n', j'}$. This index equalises the compatibility relations for all morphisms in $J$.

Pushing the tuple $(x'_j)$ forward to the index $n'$ produces an element of $\varprojlim_{j \in J} M_{n', j}$ which is compatible with everything. In the colimit, it represents the class $(y_j)_{j \in J}$, so $\Phi$ is surjective.


## Theorem statement for finite products

Let $(M_i)_{i \in I}$ and $(N_i)_{i \in I}$ be two directed systems of sets over a finite set $I$. Then the following are equivalent:
- The indexing set $I$ is a [[Directed Set|directed set]], i.e. the colimit is filtered.
- There is a bijection (set isomorphism):
$$
\varinjlim (M_i \times N_i) \cong \left( \varinjlim M_i \right) \times \left( \varinjlim N_i \right)
$$
- 
### Proof




## Theorem statement for finite fibre products.
### Proof

## Theorem statement for finite equalisers.


## Examples




## Related Concepts
### Upstream
%% Parent or prerequisite content. %%

### Downstream
%% Child content and applications. %%

### Similar
%% Similar concepts. %%

### Contrast
%% Counter concepts or adjacent but not similar things.. %%

## References / source
%% Any lectures, books, notes that this information was sourced from. %%
[Stacks project 4.19](https://stacks.math.columbia.edu/tag/04AX) 