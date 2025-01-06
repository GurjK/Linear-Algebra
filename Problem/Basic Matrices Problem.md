
1. Show that A has a rank = 3 for column and row where 

$$A = \begin{bmatrix} 
1 & -1 & 2 & 5 & 4 \\
3 & -2 & 1 & 4 & 2 \\
0 & 1 & 2 & -1 & 3 \\
-5 & 4 & 2 & -4 & 3 
\end{bmatrix}
$$

**Answer**

To show that this has $colrank =3$ we have show that the columns of A are not linearly independent because if they were then they would have a rank of 5. A key note is that since there are more columns then rows we would never get full rank so the columns would always be linearly dependent. 


For **colrank** we need to get the first entry in each column to be equal to 0. We do this through RREF method and the same applies to **rowrank**

For colrank we get

$$A = \begin{bmatrix} 
1 & 0 & 0 & 0 & 0 \\
3 & 1 & 0 & 0 & 0 \\
0 & 1 & 7 & 10 & 13 \\
-5 & -1 & 7 & 10 & 13 
\end{bmatrix}
$$

Looking at this we can determine the pivots by looking for the first non-zero entry in each below the previous one. From here we can see the pivots are 1,1, 7 so the colrank=3

For rowrank we get

$$A = \begin{bmatrix} 
1 & -1 & 2 & 5 & 4 \\
0 & 1 & -5 & -11 & -10 \\
0 & 0 & 7 & 10 & 13 \\
0 & 0 & 0 & 0 & 0 
\end{bmatrix}
$$

From here we can see the the pivots are the first entry in each row that isn't equal to zero and isn't in the same column as the previous row which gives us 1,1,7 so the rowrank=3 so in conclusion

$$
rowrank=colrank=Rank=3
$$
2. Let $$C= I +M = \begin{bmatrix} 
1 & 0 & 0 & 0 \\
3 & 1 & 0 & 0 \\
1 & -1 & 1 & 0 \\
-1 & 2 & 1 & 1  
\end{bmatrix}
$$
Compute $C^M$ where $m \geq 2$

**Answer**

Use the following if A,B are square matrices and AB=BA then $(A+B)^M = \sum_{j=0}^{m} \binom{m}{j} A^jB^{(m-j)}$ and $\binom{m}{j} = \frac{m!}{j!(m-j)!}$


First note the following for 

$$
M = \begin{bmatrix} 
0 & 0 & 0 & 0 \\
3 & 0 & 0 & 0 \\
1 & -1 & 0 & 0 \\
-1 & 2 & 1 & 0  
\end{bmatrix}
$$
$$
M^2 = \begin{bmatrix} 
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
-3 & 0 & 0 & 0 \\
7 & -1 & 0 & 0  
\end{bmatrix}
$$
$$
M^3 = \begin{bmatrix} 
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
-3 & 0 & 0 & 0  
\end{bmatrix}
$$
$$
M^4 = \begin{bmatrix} 
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0  
\end{bmatrix}
$$

If we let A = M and B=I and we know that after $M^3$ that the value is 0, then we can use the binomial formula and get:

$$
C^m = (M+I)^m = \sum_{j=0}^{3} \binom{m}{j} M^jI^{m-j} = \binom{m}{0}I + \binom{m}{1} M + \binom{m}{2} M^2 + \binom{m}{3} M^3
$$
where 
$$
\binom{m}{0} = 1; \binom{m}{1} = m; \binom{m}{2} =  \frac{m(m-1)}{2}; \binom{m}{3} =\frac{m(m-1)(m-2)}{6}
$$



