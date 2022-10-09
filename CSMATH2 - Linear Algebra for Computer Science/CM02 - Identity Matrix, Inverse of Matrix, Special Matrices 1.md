<br><br>

##### Identity Matrix, Inverse of Matrix, Special Matrices
---

Given an $n*m$ matrix $A$, there exists a square matrix $I$, such that $AI_m = I_nA = A$. The matrix $I$ is also known as the identity matrix. An <u>identity matrix</u> is defined as a matrix wherein all entries where $i=j$, or the <u>main diagonal entries</u>, are equal to 1, while the rest of the entries are 0.
$$\textcolor{Apricot}{A}\textcolor{Skyblue}{I} = \textcolor{Apricot}{\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}} * \textcolor{Skyblue}{\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}} = \begin{bmatrix} \textcolor{Apricot}{1}(\textcolor{Skyblue}{1}) + \textcolor{Apricot}{2}(\textcolor{Skyblue}{0}) & \textcolor{Apricot}{1}(\textcolor{Skyblue}{0}) + \textcolor{Apricot}{2}(\textcolor{Skyblue}{1}) \\ \textcolor{Apricot}{3}(\textcolor{Skyblue}{1}) + \textcolor{Apricot}{4}(\textcolor{Skyblue}{0}) & \textcolor{Apricot}{3}(\textcolor{Skyblue}{0}) + \textcolor{Apricot}{4}(\textcolor{Skyblue}{1}) \end{bmatrix} = \textcolor{Apricot}{\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}} = \textcolor{Apricot}{A}$$
The size of the identity of a non-square matrix should be determined by the its neighboring number when multiplied with the non-square matrix. Identity matrices are <u>usually square</u>. Hence, $_2A_3 \ _3I_3$ or $_2I_2 \ _2A_3$, depending on the arrangement.


##### | **Additional Properties of Matrix Multiplication**
- <u>Exponent rule</u> -- $A^P = A*A*A...A$
- <u>Exponent product rule</u> -- $A^P*A^Q = A^{P+Q}$ 
- <u>Power of a power rule</u> -- $(A^P)^Q = A^{P*Q}$ 
- <u>Not power of a product</u> -- $(AB)^Q \ne A^QB^Q$, since $AB \ne BA$

For $a, b \in R,\ \ ab = 0,\ \iff a = 0 \ or \ b = 0$, the <u>zero product property</u> does not hold for matrix multiplication. This means if the product of matrices $A$ and $B$ equal to zero, this does not mean either matrices $A$ or $B$ is a <u>zero matrix</u>.
$$\textcolor{Apricot}A\textcolor{Skyblue}{B} = \textcolor{Apricot}{\begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix}} * \textcolor{Skyblue}{\begin{bmatrix} 4 & -6 \\ -2 & 3 \end{bmatrix}} = \begin{bmatrix} 4 + (-4) & 6 + 6 \\ 8 + (-8) & -12 + 12 \end{bmatrix} = \textcolor{LightGray}{\begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}} = \textcolor{LightGray}{O}$$
Yet neither $A$ or $B$ are zero matrices $O$.

For $a, b, c \in R,\ \ ab = ac\ \ and \ \ a \ne 0 \ \ implies \ \ b = c$, the <u>cancellation law</u> does not apply for matrix multiplication. This means that when multiplying matrix $A$ with $B$, and multiplying matrix $A$ with $C$ yielding the same result, does not mean that matrix $B$ and $C$ are the <u>same matrix</u>.
$$\textcolor{Apricot}{A}\textcolor{Skyblue}{B} = \textcolor{Apricot}{\begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix}} \textcolor{Skyblue}{\begin{bmatrix} 2 & 1 \\ 3 & 2 \end{bmatrix}} = \textcolor{LightGray}{\begin{bmatrix} 8 & 5 \\ 16 & 10 \end{bmatrix}}, \ \ \ \textcolor{Apricot}{A}\textcolor{Lavender}{C} = \textcolor{Apricot}{\begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix}} \textcolor{Lavender}{\begin{bmatrix} -2 & 7 \\ 5 & -1 \end{bmatrix}} = \textcolor{LightGray}{\begin{bmatrix} 8 & 5 \\ 16 & 10 \end{bmatrix}}$$
$AB=AC$, yet $B$ and $C$ are not equal matrices.


##### | **Inverse of a Matrix**
If there exists a matrix $B$ such that, $AB = BA = I_n$, then $B$ is called the <u>inverse</u> of $A$, and it is denoted by $A^{-1}$. The <u>inverse of a matrix</u> may or may not exist. If it exists, then $A$ is a <u>non-singular matrix</u> or an <u>invertible matrix</u>. If not, $A$ will be a <u>singular matrix</u> or a <u>non-invertible matrix</u>. If $A^{-1}$ exists, then it is <u>unique</u>.
$$\textcolor{Apricot}{A} \textcolor{Skyblue}{A^{-1}} = \textcolor{Apricot}{\begin{bmatrix} 4 & -1 \\ 2 & 0 \end{bmatrix}} \textcolor{Skyblue}{\begin{bmatrix} 0 & \frac{1}{2} \\ -1 & 2 \end{bmatrix}} = \begin{bmatrix} 0 + 1 & 2 - 2 \\ 0 + 0 & 1 + 0 \end{bmatrix} = \textcolor{LightGray}{\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}} = \textcolor{LightGray}{I_n}$$
$$\textcolor{Skyblue}{A^{-1}} \textcolor{Apricot}{A} = \textcolor{Skyblue}{\begin{bmatrix} 0 & \frac{1}{2} \\ -1 & 2 \end{bmatrix}} \textcolor{Apricot}{\begin{bmatrix} 4 & -1 \\ 2 & 0 \end{bmatrix}} = \begin{bmatrix} 0 + 1 & 0 + 0 \\ -4 + 4 & 1 + 0 \end{bmatrix} = \textcolor{LightGray}{\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}} = \textcolor{LightGray}{I_n}$$
Properties of an Inverse of a Matrix
- If $A$ is a <u>non-singular</u> matrix, then $A^{-1}$ is <u>non-singular</u> -- $(A^{-1})^{-1} = A$
- If $A$ and $B$ are <u>non-singular</u> matrices, then $AB$ is <u>non-singular</u> --  $(AB)^{-1} = B^{-1} * A^{-1}$
- If $A_1,A_2,\ ...\ ,A_n$ are <u>non-singular</u> matrices, then $A_1,A_2,\ ...\ ,A_n$ is <u>non-singular</u> -- $(A_1A_2...A_n)^{-1} = A_n * A_{n-1} * ... * A_1$
- If $A$ is a <u>non-singular</u> matrix, then $A^T$ is <u>non-singular</u> -- $(A^T)^{-1} = (A^{-1})^T$


##### | **Special types of Square Matrices
1. A square matrix is a <u>symmetric</u> if and only if $A^T = A$, that is, $a_{ij} = a_{ji}$ for every $i$ and $j$. A prime example of this is the identity matrix.
   --> Example: $$\textcolor{Apricot}{A}^\textcolor{Skyblue}{T} = \textcolor{Apricot}{\begin{bmatrix} 1 & 4 & 7 \\ 4 & 2 & 5 \\ 7 & 5 & 3 \end{bmatrix}} \textcolor{Skyblue}{^T} = \textcolor{Skyblue}{\begin{bmatrix} 1 & 4 & 7 \\ 4 & 2 & 5 \\ 7 & 5 & 3 \end{bmatrix}} = \textcolor{Skyblue}{A}$$
2. A square matrix is <u>skew-symmetric</u> if and only if $A^T = -A$, that is, $a_{ij} = -a_{ji}$ for all $i \ne j$, and $a_{ij} = 0$ for $i = j$. 
   --> Example: $$\textcolor{Apricot}{A}\textcolor{Skyblue}{^T} = \textcolor{Apricot}{\begin{bmatrix} 0 & 1 & 3 \\ -1 & 0 & 2 \\ -3 & -2 & 0 \end{bmatrix}}\textcolor{Skyblue}{^T} = \textcolor{Skyblue}{\begin{bmatrix} 0 & -1 & -3 \\ 1 & 0 & -2 \\ 3 & 2 & 0 \end{bmatrix}} = \textcolor{Skyblue}{-A}$$
3. A square matrix is a <u>diagonal matrix</u> if all $a_{ij} = 0$ for all $i \ne j$. It still holds even if entries where $i=j$ are also zero (the zero matrix). 
   --> Example: $$\textcolor{LightGray}{A} = \begin{bmatrix} \textcolor{Skyblue}{2} & \textcolor{Apricot}{0} \\ \textcolor{Apricot}{0} & \textcolor{Skyblue}{3} \end{bmatrix},\ \ \ \textcolor{LightGray}{B} = \begin{bmatrix} \textcolor{Skyblue}{0} & \textcolor{Apricot}{0} \\ \textcolor{Apricot}{0} & \textcolor{Skyblue}{0} \end{bmatrix}$$
4. A scalar matrix is a <u>diagonal matrix</u> similar to a standard square matrix, but all $a_ij = c$, where $c$ is a constant. It still holds on the zero matrix. 
   --> Example: $$\textcolor{LightGray}{A} = \begin{bmatrix} \textcolor{Skyblue}{4} & \textcolor{Apricot}{0} \\ \textcolor{Apricot}{0} & \textcolor{Skyblue}{4} \end{bmatrix},\ \ \ \textcolor{LightGray}{B} = \begin{bmatrix} \textcolor{Skyblue}{0} & \textcolor{Apricot}{0} \\ \textcolor{Apricot}{0} & \textcolor{Skyblue}{0} \end{bmatrix}$$
5. A square matrix is an <u>upper-triangular matrix</u> if $a_ij = 0$ for all $i > j$. All entries below the main diagonal line are zeros. However, it is called a <u>strictly upper triangular matrix</u> if in addition, $a_{ij} = 0$ for all $i=j$. Identity matrices hold, but zero matrices count as strict.
   --> Example: $$\textcolor{LightGray}{A} = \begin{bmatrix} 1 & 4 & 5 \\ \textcolor{Apricot}{0} & 2 & -1 \\ \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & 3 \end{bmatrix},\ \ \ \textcolor{LightGray}{B} = \begin{bmatrix} -2 & 0 & -3 \\ \textcolor{Apricot}{0} & 2 & 0 \\ \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & 4 \end{bmatrix},\ \ \ \textcolor{LightGray}{O} = \begin{bmatrix} \textcolor{Skyblue}{0} & 0 & 0 \\ \textcolor{Apricot}{0} & \textcolor{Skyblue}{0} & 0 \\ \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & \textcolor{Skyblue}{0} \end{bmatrix}$$
6. A square matrix is a <u>lower-triangular matrix</u> if $a_ij = 0$ for all $i < j$. All entries above the main diagonal line are zeros. However, it is called a <u>strictly lower triangular matrix</u> if in addition, $a_{ij} = 0$ for all $i=j$. Identity matrices hold, but zero matrices count as strict.
   --> Example: $$\textcolor{LightGray}{A} = \begin{bmatrix} 1 & \textcolor{Apricot}{0} & \textcolor{Apricot}{0} \\ 4 & 2 & \textcolor{Apricot}{0} \\ -5 & 0 & 3 \end{bmatrix}, \ \ \ \textcolor{LightGray}{B} = \begin{bmatrix} -2 & \textcolor{Apricot}{0} & \textcolor{Apricot}{0} \\ 0 & 2 & \textcolor{Apricot}{0} \\ 1 & 0 & 4 \end{bmatrix}, \ \ \ \textcolor{LightGray}{O} = \begin{bmatrix} \textcolor{Skyblue}{0} & \textcolor{Apricot}{0} & \textcolor{Apricot}{0} \\ 0 & \textcolor{Skyblue}{0} & \textcolor{Apricot}{0} \\ 0 & 0 & \textcolor{Skyblue}{0} \end{bmatrix}$$

> **Theorem:** Every square matrix $A$ can be uniquely expressed as $A=S+K$, where $S$ is a <u>symmetric matrix</u>, and $K$ is a <u>skew-symmetric matrix</u>. $$\begin{gather} A=S+K \rightarrow (1) \\ \\ A^T = (S+K)^T = S^T+K^T =S-K \rightarrow (2) \\ \\ (1)+(2) \Rightarrow A+A^T = 2S \Rightarrow S=\frac{1}{2}(A+A^T) \\ (1)-(2) \Rightarrow A-A^T = 2K \Rightarrow K=\frac{1}{2}(A-A^T) \\ S+K=\frac{1}{2}(A+A^T)+\frac{1}{2}(A-A^T)=A \\ S+K=\frac{1}{2}(A+A^T+A-A^T)=\frac{1}{2}(2A)=A \end{gather}$$Note: $S^T = S$ and $K^T = -K$.

___

Continue to next: [[CSMATH2 - Linear Algebra for Computer Science/CM03 - Using EROs to Find the Inverse of a Matrix]]
Last updated: 10/07/2022

#core #Y2T1