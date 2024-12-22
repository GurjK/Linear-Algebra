## Vectors

Vectors represent are a mathematical concept that represent a magnitude and direction. For example:  
$$
				\left[\begin{matrix} 4 \\ 3\end{matrix} \right]	
$$
This matrix can be see as a ordered array in $R^{2}$ where it has an x - component of 4 and y component of 3 in 2-D. If there were 3 components then it would be in 3D therefore in $R^{3}$. The **Magnitude** of this vector would be define as its length which can also be referred to as the norm or length of the vector. The general formula for the length is 
$$
length = \sqrt{x_{0}^{2}+x_{1}^{2}+...+x_{n-1}^{2}}
$$

This length in this example is more formally know as the **2 Norm** or **Euclidian Length**

## Operations 

Multiple operations can be performed on vector such as addition, scaling, subtraction. Division does not exist explicitly for vectors. 

**Addition** 
-  Can be seen as combining 2 vectors by placing the tail of one vector to the head of another vector. 
-  A more mathematical way of thinking about it is adding the components of one vector to another vector. 
$$
\left[\begin{matrix} x_{0} \\ x_{1} \\ x_{2}\end{matrix} \right] + \left[\begin{matrix} y_{0} \\ y_{1} \\ y_{2}\end{matrix} \right] = \left[\begin{matrix} x_{0} +y_{0} \\ x_{1} + y_{1} \\ x_{2} + y_{2}\end{matrix} \right]
$$

**Scaling**
- Scaling can be seen as stretching a vector by a certain factor as described by the scaling factor
- Intuitively this stretches or increases the vector without changing its direction
$$
\alpha\left[\begin{matrix} x_{0} \\ x_{1} \\ x_{2}\end{matrix} \right] = \left[\begin{matrix} \alpha * x_{0} \\ \alpha *x_{1} \\ \alpha *x_{2}\end{matrix} \right]
$$

## Standard Basis Vectors

The standard basis vectors also known as the unit basis vectors are vectors whose entire are all 0s except for one entry which is one. For example in $R^{3}$ there are only 3 standard basic vectors as follows: 

$$
\left[\begin{matrix} 1 \\ 0 \\ 0\end{matrix} \right], \left[\begin{matrix} 0 \\ 1 \\ 0\end{matrix} \right],\left[\begin{matrix} 0 \\ 0 \\ 1\end{matrix} \right]

$$

## Dot Product

The dot product can be viewed in multiple different ways depending on the type of lens that one wants to view this through. In general, it tells us how much one vector points in the direction of another vector. 
- From a geometric perspective: this is know by this formula where x and y are both vectors:
- Here $\theta$ is the angle in between the 2 vectors 
$$ x \cdot y = |x||y|\cos\theta $$
-From the algebraic sense which is the more regular used notion in linear algebra it is the 
$$
  x\cdot y = x_{0}y_{0} +x_{1}y_{1}+... 
$$
The important take aways from the dot product are as follows:
- When $\theta$ = 90 then it means that the 2 vectors are **orthogonal** to each other or if their dot product equal 0 it also implies orthogonality (perpendicular in the 2D sense)

## Transpose of a Vector

A vector be seen in one of 2 ways: A column vector with dimensions n x 1 or a row vector with dimensions 1 x n:

Column Vector: n dimensional vector than can be denoted as  $v=v_{i=1:n}$ - This would be an n x 1 vector

$$

v = \left[\begin{matrix} v_{1} \\ v_{2} \\ ... \\ v_{n}\end{matrix} \right]
$$
Now say that we wanted to convert this n x 1 vector into a 1 x n  vector. The way to do that would be to **transpose** the vector
- Create an empty 1 x n vector
- For each positions that was v1,v2 that would then be equal to v1,v2 in the new vector as well.
- The end result of this would be a **Row Vector** with dimensions 1xn

Row Vector :  n dimensional vector that if v was the Column vector then $v^{T}$ is the Row vector form of the same vector 
$$
v^{T} = \left[\begin{matrix} v_{0} & v_{1} & ... & v_{n}\end{matrix} \right]
$$
## Vector Multiplication

Now in order to multiply to vectors together they must follow the following rules:
- The rows of one vector have to equal the columns of the vector the it is multiplying against 
- The result will be either a scalar or a matrix consisting of a the columns of the first vector and the rows of the second vector
	- This is dependent on whether row - column vector multiplication is being performed or if column - row vector multiplication is being performed.

**Row Column Multiplication**
- v = column vector of size 3
- $w^{T}$ = row vector of size 3
$$
 \mathbf{w} = \begin{bmatrix} w_1 \\ w_2 \\ w_3 \end{bmatrix}, \quad \mathbf{w}^T = \begin{bmatrix} w_1 & w_2 & w_3 \end{bmatrix}, \quad \mathbf{v} = \begin{bmatrix} v_1 \\ v_2 \\ v_3 \end{bmatrix}
$$
- Compute $w^{T}v$
	- Since the dimensions of this problem is a 1 x n * n x 1 vector the result will be a 1 x 1 (scalar)
	- In this case it is the sum of the components so 
	
$$
w^{T}v = \sum_{n=0}^{n} {w_{i}v_{i}} =  \mathbf{w}^T \cdot \mathbf{v} = w_1v_1 + w_2v_2 + w_3v_3 
$$

**Column Row Multiplication**
- Same as above but now compute $vw^{T}$
	- Here this is a n x 1 * 1 x n problem where the result by the rules defined above would be a n x n **matrix** (expanded on in further sections)

$$ \mathbf{v} \mathbf{w}^T = \begin{bmatrix} v_1 \\ v_2 \\ v_3 \end{bmatrix} \begin{bmatrix} w_1 & w_2 & w_3 \end{bmatrix} = \begin{bmatrix} v_1w_1 & v_1w_2 & v_1w_3 \\ v_2w_1 & v_2w_2 & v_2w_3 \\ v_3w_1 & v_3w_2 & v_3w_3 \end{bmatrix} 
$$

## Norms

Norms mentioned above are a way to map a vector in $R^{n}$ to a non-negative number, representing it's size or length. There are many different norms some of the most basic ones are listed below: 

**The Euclidean Norm ( L2 )**
- The **Euclidean norm** (or \( L2 \)-norm) measures the straight-line distance from the origin to the point represented by the vector. For a vector 
$$
  \mathbf{v} = \begin{bmatrix} v_1 \\ v_2 \end{bmatrix} :  ||\mathbf{v}||_2 = \sqrt{v_1^2 + v_2^2} 
$$
**The Manhattan Norm ( L1 )** 
- The **Manhattan norm** (or \( L1 \)-norm) is the sum of the absolute values of the vector's components, representing the total distance traveled along each axis. 
$$ ||\mathbf{v}||_1 = |v_1| + |v_2|
$$
**The Infinity Norm ($( L\infty$))**

- The **Infinity norm** measures the largest absolute value among the components of the vector. It is also called the **max norm**. 
$$
 ||\mathbf{v}||_\infty = \max(|v_1|, |v_2|)
$$
**( p \)-Norm** 
- The \( p \)-norm of a vector $( \mathbf{v} = \begin{bmatrix} v_1 \\ v_2 \\ \dots \\ v_n \end{bmatrix} )$ is a generalized measure of the vector's size. It is defined as:
$$ ||\mathbf{v}||_p = \left( \sum_{i=1}^n |v_i|^p \right)^{1/p} 
$$
