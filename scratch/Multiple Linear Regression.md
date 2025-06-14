---
created: 2025-04-14
confidence level: low
review count: 0
---
## Intro
With regular linear regression there is a single input, $x$ used to predict a single output, $y$. With _multiple linear regression_, multiple inputs, $\mathbf x$ are used to predict $y$. Here are some additional notations:
+ $x_j$: $j^{th}$ feature
+ $n$: number of features
+ $\mathbf x^{(i)}$: features of $i^{th}$ training example
+ $x_j^{(i)}$: value of feature $j$ in $i^{th}$ training example

Model definition for multiple linear regression:

$$f_{\mathbf w,b}(\mathbf x) = \mathbf w_1 \cdot \mathbf x_1 + \mathbf w_2 \cdot \mathbf x_2 + \cdots + \mathbf w_n \cdot \mathbf x_n + b$$
$$or$$
$$f_{\mathbf w,b}(\mathbf x)=\mathbf w \cdot \mathbf x + b$$
## Vectorization
Writing vectorized code allows you to take advantage of modern hardware to perform operations in parallel. It makes use of SIMD (Simple Instruction Multiple Data) which is a parallel processing technique that allows you to perform a single instruction on multiple data points simultaneously. Vectorized code is faster and more efficient.

# Loss
The cost/loss function remains the same as in univariate linear regression.

# Gradient Descent
The calculations involved in gradient descent change slightly:
$$ \mathbf w = \mathbf w - \alpha\cdot\frac{\partial}{\partial{\mathbf w_j}}J(\mathbf w,b) \; for \; j = 0,1,...,n $$
$$ b = b - \alpha\cdot\frac{\partial}{\partial b}J(\mathbf w,b) $$
$\mathbf w$ is a vector here rather than a scalar as in univariate regression.

## Further Reading
+ [[Vectorized Dot Product in C]]