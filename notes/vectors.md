---
created: 2025-03-16
confidence level: low
---
## What is a vector?
A vector can be defined in two ways. A vector can be defined as an arrow in  with a given length and a given direction. It could also be defined as an ordered list of numbers. How we choose to define a vector doesn't matter as much as the relationship between these two views and how we translate from one representation to another.

## More Context
#### Vectors as Arrows in Space

```tikz
\begin{document}
\begin{tikzpicture}[x=4mm,y=4mm,scale=1.5]
  % Manual grid (if TikZJax doesn't support `grid`)
  \foreach \x in {-2,-1,0,1,2} \draw[thin,gray!40] (\x,-2) -- (\x,2);
  \foreach \y in {-2,-1,0,1,2} \draw[thin,gray!40] (-2,\y) -- (2,\y);
  \draw[<->] (-2,0)--(2,0) node[right]{$x$};
  \draw[<->] (0,-2)--(0,2) node[above]{$y$};
  \draw[line width=1pt,-stealth](0,0)--(1,1) node[anchor=west]{$\mathbf{u}$};
  \draw[line width=1pt,-stealth](0,0)--(-2,2) node[anchor=east]{$\mathbf{v}$};
\end{tikzpicture}
\end{document}
```
#### Vectors as Matrices (List of Numbers)

$$
\large
\mathbf u = \begin{bmatrix} 1 \\ 1 \end{bmatrix},
\mathbf v = \begin{bmatrix} -2 \\ 2 \end{bmatrix}
$$
## Key Points
- Two fundamental operations are carried out on vectors: [[vector-additon|vector addition]] and [[vector-multplication|vector multiplication]].
- A linear combination of one or more vectors is an expression where each vector is multiplied by a scalar and then subbed together. Formally:
$$
\large
c \mathbf{u} + d \mathbf{v} + e\mathbf{w}
$$ where $\mathbf u, \mathbf v, \mathbf w$ are vectors and $c, d, e$ are scalars.

## Links
