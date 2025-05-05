# Day 1: Linear Algebra Basics

## Topics Covered

1. Vectors and Scalars
2. Matrix Definitions
3. Matrix Multiplication
4. Dot Product
5. Matrix Transpose and Identity
6. Reduced Row Echelon Form (RREF)
7. Unit Vectors
8. Parameterization of Lines
9. Linear Combinations & Span

---

## 1. Vectors and Scalars

* **Scalar**: A single numerical value (e.g. `5`, `-3.2`, `\pi`)
* **Vector**: An ordered list of numbers (1D array), can represent direction and magnitude.

Example:

```
v = [2, 3]       # 2D vector
u = [4, -1, 5]   # 3D vector
```

**Magnitude (Euclidean norm):**
$\|v\| = \sqrt{v_1^2 + v_2^2 + \dots + v_n^2}$

Example:
$\|v\| = \sqrt{2^2 + 3^2} = \sqrt{4 + 9} = \sqrt{13}$

---

## 2. Matrix Definitions

* **Matrix**: A 2D array of numbers arranged in rows and columns

$$
A = \begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
$$

* **Shape**: `(rows, columns)` → `A` above has shape `(2, 2)`

---

## 3. Matrix Multiplication

**Rule**: If `A` is (m × n) and `B` is (n × p), then `A × B = C` is (m × p)

Example:

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix},\quad
B = \begin{bmatrix} 2 & 0 \\ 1 & 3 \end{bmatrix}
$$

$$
C = A \times B = \begin{bmatrix}
(1\times2 + 2\times1) & (1\times0 + 2\times3) \\
(3\times2 + 4\times1) & (3\times0 + 4\times3)
\end{bmatrix} = \begin{bmatrix} 4 & 6 \\ 10 & 12 \end{bmatrix}
$$

---

## 4. Dot Product

Defined for vectors of the same size:
$\text{Dot}(u, v) = \sum u_i v_i$

Example:

$$
u = [2, 4],\quad v = [3, -1] \Rightarrow u \cdot v = (2\times3) + (4\times-1) = 6 - 4 = 2\]

Also:
\[ u \cdot v = \|u\|\|v\|\cos(\theta) \]
→ Used to find angles between vectors.

---

## 5. Matrix Transpose and Identity
**Transpose (A^T)**: Flip rows and columns.

\[
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \Rightarrow A^T = \begin{bmatrix} 1 & 3 \\ 2 & 4 \end{bmatrix}
$$

**Identity Matrix (Iₙ)**: Diagonal matrix with 1s on the diagonal.

$I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} \Rightarrow A \cdot I = A$

---

## 6. Reduced Row Echelon Form (RREF)

A matrix is in RREF if:

1. Each leading entry is 1.
2. Each leading 1 is the only nonzero entry in its column.
3. Rows with all 0s are at the bottom.

Example system:

$$
\begin{cases}
x + y + z = 6 \\
2y + 5z = -4 \\
2x + 5y + z = 27
\end{cases}
$$

Augmented matrix:

$$
\begin{bmatrix}
1 & 1 & 1 & | & 6 \\
0 & 2 & 5 & | & -4 \\
2 & 5 & 1 & | & 27
\end{bmatrix}
$$

RREF:

$$
\begin{bmatrix}
1 & 0 & 0 & | & 5 \\
0 & 1 & 0 & | & 3 \\
0 & 0 & 1 & | & -2
\end{bmatrix}
$$

→ Solution: `x = 5, y = 3, z = -2`

---

## 7. Unit Vectors

Vector with magnitude 1.

Formula:
$\hat{v} = \frac{v}{\|v\|}$

Example:
$v = [3, 4] \Rightarrow \|v\| = 5 \Rightarrow \hat{v} = [0.6, 0.8]$

---

## 8. Parameterization of Lines

Formula:
$\vec{r}(t) = \vec{p} + t\vec{d}$
Where:

* $\vec{p}$ is a point on the line
* $\vec{d}$ is a direction vector

Example:
$\vec{r}(t) = [1, 2] + t[3, -1] = [1 + 3t, 2 - t]$

---

## 9. Linear Combinations & Span

**Linear Combination**: A sum of scaled vectors.
$a\vec{v}_1 + b\vec{v}_2$

**Span**: The set of all linear combinations of a set of vectors.

Example:
$\vec{v}_1 = [1, 0],\ \vec{v}_2 = [0, 1] \Rightarrow \text{Span} = \mathbb{R}^2$

If $\vec{v}_2 = 2\vec{v}_1$ → span is a line, not a plane.

---

## ✅ Summary Table

| Concept               | Formula / Description                     | Example                                   |
| --------------------- | ----------------------------------------- | ----------------------------------------- |
| Vector magnitude      | $\|v\| = \sqrt{\sum v_i^2}$               | $\|[3,4]\| = 5$                           |
| Dot product           | $u \cdot v = \sum u_i v_i$                | $[1,2] \cdot [3,4] = 11$                  |
| Matrix multiplication | $AB$ where $A_{m\times n}, B_{n\times p}$ | See above for full example                |
| Transpose             | $A^T$ swaps rows/columns                  | $A^T = [[1,3],[2,4]]$                     |
| Identity matrix       | Diagonal of 1s: $I \cdot A = A$           | $I = [[1,0],[0,1]]$                       |
| Unit vector           | $\hat{v} = v / \|v\|$                     | $[3,4] \Rightarrow [0.6,0.8]$             |
| Parameterized line    | $r(t) = p + td$                           | $[1+3t, 2-t]$                             |
| Span                  | All linear combinations of vectors        | $\text{Span}([1,0],[0,1]) = \mathbb{R}^2$ |


