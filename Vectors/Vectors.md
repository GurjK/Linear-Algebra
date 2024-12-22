## Vectors

Vectors are a mathematical concept that represent both magnitude and direction. For example:

$$
\begin{bmatrix} 
4 \\ 
3 
\end{bmatrix}
$$

This matrix can be seen as an ordered array in $\mathbb{R}^2$, where it has an x-component of 4 and a y-component of 3 in 2-D. If there were 3 components, it would be in 3D, i.e., $\mathbb{R}^3$. The **magnitude** of this vector is defined as its length, which can also be referred to as the norm. The general formula for the length is:

$$
\text{length} = \sqrt{x_0^2 + x_1^2 + \dots + x_{n-1}^2}
$$

This length in this example is more formally known as the **2-norm** or **Euclidean length**.

## Operations

Multiple operations can be performed on vectors, such as addition, scaling, and subtraction. Division does not exist explicitly for vectors.

### **Addition**

- Addition can be seen as combining two vectors by placing the tail of one vector at the head of another vector. 
- Mathematically, this is adding the components of one vector to another vector. 

$$
\begin{bmatrix} 
x_0 \\ 
x_1 \\ 
x_2 
\end{bmatrix} + 
\begin{bmatrix} 
y_0 \\ 
y_1 \\ 
y_2 
\end{bmatrix} = 
\begin{bmatrix} 
x_0 + y_0 \\ 
x_1 + y_1 \\ 
x_2 + y_2 
\end{bmatrix}
$$

### **Scaling**

- Scaling stretches a vector by a certain factor as described by the scaling factor.
- Intuitively, this increases the vector's magnitude without changing its direction.

$$
\alpha \begin{bmatrix} 
x_0 \\ 
x_1 \\ 
x_2 
\end{bmatrix} = 
\begin{bmatrix} 
\alpha x_0 \\ 
\alpha x_1 \\ 
\alpha x_2 
\end{bmatrix}
$$

## Standard Basis Vectors

The standard basis vectors, also known as unit basis vectors, are vectors where all components are 0 except for one entry, which is 1. For example, in $\mathbb{R}^3$, there are three standard basis vectors:

$$
\begin{bmatrix} 
1 \\ 
0 \\ 
0 
\end{bmatrix}, \quad 
\begin{bmatrix} 
0 \\ 
1 \\ 
0 
\end{bmatrix}, \quad 
\begin{bmatrix} 
0 \\ 
0 \\ 
1 
\end{bmatrix}
$$

## Dot Product

The dot product can be viewed in multiple ways, depending on the perspective. In general, it tells us how much one vector points in the direction of another vector.

- From a geometric perspective, the formula is:

$$
x \cdot y = ||x|| \, ||y|| \cos \theta
$$

where $\theta$ is the angle between the two vectors.

- From an algebraic perspective, which is more commonly used in linear algebra:

$$
x \cdot y = x_0 y_0 + x_1 y_1 + \dots
$$

Key takeaways:
- When $\theta = 90^\circ$, the two vectors are **orthogonal** (perpendicular in 2D), or if their dot product equals 0, it also implies orthogonality.

## Transpose of a Vector

A vector can be represented in one of two ways: as a column vector ($n \times 1$) or as a row vector ($1 \times n$).

- **Column Vector**: An $n$-dimensional vector:

$$
v = \begin{bmatrix} 
v_1 \\ 
v_2 \\ 
\vdots \\ 
v_n 
\end{bmatrix}
$$

- **Row Vector**: Transposing the column vector results in a row vector:

$$
v^T = \begin{bmatrix} 
v_1 & v_2 & \dots & v_n 
\end{bmatrix}
$$

## Vector Multiplication

To multiply two vectors, the rows of one vector must equal the columns of the vector it multiplies with. The result is either a scalar or a matrix:

### **Row-Column Multiplication**

- Given a column vector ($\mathbf{v}$) and a row vector ($\mathbf{w}^T$):

$$
\mathbf{w} = 
\begin{bmatrix} 
w_1 \\ 
w_2 \\ 
w_3 
\end{bmatrix}, \quad 
\mathbf{w}^T = 
\begin{bmatrix} 
w_1 & w_2 & w_3 
\end{bmatrix}, \quad 
\mathbf{v} = 
\begin{bmatrix} 
v_1 \\ 
v_2 \\ 
v_3 
\end{bmatrix}
$$

- The result of $\mathbf{w}^T \mathbf{v}$:

$$
w^T v = \sum_{i=1}^n w_i v_i = w_1 v_1 + w_2 v_2 + w_3 v_3
$$

### **Column-Row Multiplication**

- The result of $\mathbf{v} \mathbf{w}^T$:

$$
\mathbf{v} \mathbf{w}^T = 
\begin{bmatrix} 
v_1 \\ 
v_2 \\ 
v_3 
\end{bmatrix} 
\begin{bmatrix} 
w_1 & w_2 & w_3 
\end{bmatrix} = 
\begin{bmatrix} 
v_1 w_1 & v_1 w_2 & v_1 w_3 \\ 
v_2 w_1 & v_2 w_2 & v_2 w_3 \\ 
v_3 w_1 & v_3 w_2 & v_3 w_3 
\end{bmatrix}
$$

## Norms

Norms map a vector in $\mathbb{R}^n$ to a non-negative number, representing its size or length.

### **The Euclidean Norm ($L2$)**

The **Euclidean norm** measures the straight-line distance from the origin to the point represented by the vector:

$$
||\mathbf{v}||_2 = \sqrt{v_1^2 + v_2^2}
$$

### **The Manhattan Norm ($L1$)**

The **Manhattan norm** is the sum of the absolute values of the vector's components:

$$
||\mathbf{v}||_1 = |v_1| + |v_2|
$$

### **The Infinity Norm ($L\infty$)**

The **Infinity norm** measures the largest absolute value among the components:

$$
||\mathbf{v}||_\infty = \max(|v_1|, |v_2|)
$$

### **The $p$-Norm**

The $p$-norm of a vector:

$$
\mathbf{v} = \begin{bmatrix} 
v_1 \\ 
v_2 \\ 
\vdots \\ 
v_n 
\end{bmatrix}
$$

is defined as:


$$
||\mathbf{v}||_p = \sqrt[p]{|v_1|^p + |v_2|^p + \dots + |v_n|^p}
$$




