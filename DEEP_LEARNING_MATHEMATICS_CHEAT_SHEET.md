# Deep Learning Mathematics Cheat Sheet

This cheat sheet provides a quick reference to the most important mathematical concepts used throughout deep learning, machine learning, and artificial intelligence.

---

# Linear Algebra

Linear algebra forms the foundation of deep learning because data, weights, activations, and gradients are represented using vectors, matrices, and tensors.

## Scalars

A scalar is a single numerical value.

Examples:

```text
5
-3.14
0.25
```

Notation:

```text
a, b, c
```

---

## Vectors

A vector is an ordered collection of numbers.

Example:

```text
x = [1, 2, 3]
```

Shape:

```text
(3,)
```

Applications:

- Feature vectors
- Word embeddings
- Input data

---

## Matrices

A matrix is a two-dimensional array of numbers.

Example:

```text
A =

[1 2]
[3 4]
```

Shape:

```text
(2 × 2)
```

Applications:

- Weight matrices
- Image representations
- Feature transformations

---

## Tensors

A tensor is a multi-dimensional array.

| Tensor Type | Dimensions |
|------------|------------|
| Scalar | 0D |
| Vector | 1D |
| Matrix | 2D |
| Tensor | 3D+ |

Examples:

```python
import torch

x = torch.tensor([1, 2, 3])
```

---

## Matrix Addition

Matrices must have identical dimensions.

Formula:

```text
C = A + B
```

Example:

```text
[1 2]   [3 4]   [4 6]
[3 4] + [5 6] = [8 10]
```

---

## Matrix Multiplication

Formula:

```text
C = AB
```

Requirements:

```text
(m × n) × (n × p)
```

Result:

```text
(m × p)
```

Applications:

- Neural network forward propagation
- Linear transformations

---

## Dot Product

Formula:

```text
a · b = Σ(aᵢbᵢ)
```

Example:

```text
[1,2,3] · [4,5,6]

= 1×4 + 2×5 + 3×6
= 32
```

Applications:

- Similarity measurement
- Neuron computation

---

## Matrix Transpose

Formula:

```text
Aᵀ
```

Example:

```text
[1 2 3]ᵀ

[1]
[2]
[3]
```

---

## Identity Matrix

Formula:

```text
I
```

Example:

```text
[1 0]
[0 1]
```

Property:

```text
AI = A
```

---

# Calculus

Calculus enables neural networks to learn by computing gradients and updating weights.

---

## Function

A function maps inputs to outputs.

Example:

```text
f(x) = x²
```

---

## Derivative

Measures the rate of change.

Formula:

```text
f'(x)
```

Example:

```text
f(x)=x²

f'(x)=2x
```

Applications:

- Gradient computation
- Optimization

---

## Partial Derivative

Used when functions have multiple variables.

Formula:

```text
∂f/∂x
```

Example:

```text
f(x,y)=x²+y²

∂f/∂x = 2x
∂f/∂y = 2y
```

---

## Gradient

Vector of partial derivatives.

Formula:

```text
∇f
```

Example:

```text
∇f = [∂f/∂x, ∂f/∂y]
```

Applications:

- Backpropagation
- Optimization

---

## Chain Rule

Core mathematical principle behind backpropagation.

Formula:

```text
dy/dx = (dy/du)(du/dx)
```

Applications:

- Deep neural networks
- Automatic differentiation

---

## Gradient Descent

Optimization algorithm used to train neural networks.

Formula:

```text
w = w − η∇L
```

Where:

| Symbol | Meaning |
|----------|----------|
| w | Weight |
| η | Learning rate |
| L | Loss function |

---

## Common Activation Function Derivatives

### Sigmoid

Function:

```text
σ(x)=1/(1+e⁻ˣ)
```

Derivative:

```text
σ'(x)=σ(x)(1−σ(x))
```

---

### Tanh

Function:

```text
tanh(x)
```

Derivative:

```text
1−tanh²(x)
```

---

### ReLU

Function:

```text
max(0,x)
```

Derivative:

```text
1 if x > 0
0 otherwise
```

---

# Probability and Statistics

Probability and statistics help deep learning models reason about uncertainty, randomness, and data distributions.

---

## Mean

Average value.

Formula:

```text
μ = Σx / n
```

Example:

```text
Data: 2,4,6

Mean = 4
```

---

## Variance

Measures data spread.

Formula:

```text
Var(X)=Σ(x−μ)² / n
```

Interpretation:

- Low variance → clustered values
- High variance → spread values

---

## Standard Deviation

Square root of variance.

Formula:

```text
σ = √Variance
```

Applications:

- Data normalization
- Statistical analysis

---

## Probability

Probability of an event.

Formula:

```text
P(A)
```

Range:

```text
0 ≤ P(A) ≤ 1
```

---

## Conditional Probability

Probability given another event.

Formula:

```text
P(A|B)
```

Example:

```text
Probability of rain
given cloudy weather
```

---

## Bayes' Theorem

Fundamental formula in probabilistic machine learning.

Formula:

```text
P(A|B)=P(B|A)P(A)/P(B)
```

Applications:

- Bayesian models
- Spam filtering
- Medical diagnosis

---

## Normal Distribution

Bell-shaped probability distribution.

Characteristics:

- Symmetric
- Mean at center
- Common in real-world datasets

Notation:

```text
N(μ,σ²)
```

---

## Z-Score

Measures how far a value is from the mean.

Formula:

```text
z=(x−μ)/σ
```

Interpretation:

| Z-Score | Meaning |
|----------|----------|
| 0 | Mean |
| +1 | One standard deviation above |
| -1 | One standard deviation below |

---

## Cross-Entropy Loss

Common loss function for classification.

Formula:

```text
L = −Σ y log(p)
```

Where:

| Symbol | Meaning |
|----------|----------|
| y | True label |
| p | Predicted probability |

Applications:

- Image classification
- NLP
- Deep neural networks

---

# Essential Deep Learning Formulas

| Concept | Formula |
|----------|----------|
| Linear Model | y = Wx + b |
| Sigmoid | 1/(1+e⁻ˣ) |
| ReLU | max(0,x) |
| Softmax | eˣ/Σeˣ |
| Mean Squared Error | (1/n)Σ(y−ŷ)² |
| Cross Entropy | −Σylog(p) |
| Gradient Descent | w = w − η∇L |
| Dot Product | Σ(aᵢbᵢ) |
| Variance | Σ(x−μ)²/n |
| Standard Deviation | √Variance |

---

# Key Takeaways

- Linear algebra powers tensors, vectors, and matrix operations.
- Calculus enables gradient computation and optimization.
- Probability and statistics help model uncertainty and evaluate performance.
- Understanding these mathematical foundations makes deep learning architectures easier to understand and implement.
- Most modern deep learning frameworks such as PyTorch and TensorFlow automatically perform many of these calculations, but understanding the underlying mathematics is essential for building effective models.
