<br><br>

##### Matrices and Properties of Matrix Operations 
---

A <u>matrix</u> is a rectangular array of real numbers, where $a_{ij}$ are called <u>entries</u> or <u>elements</u> of the matrix. A capital letter is used to represent a matrix, and its corresponding lowercase letter is used to represent its entries.

$a_{ij}$ is known as the entry on the $i$th row (horizontal) and the $j$th column (vertical). The number of rows times the number of columns ($i*j$) of a matrix equal to the **order** or the **size** of the matrix.

In a square matrix, entries where the row and column are the same ($i=j$), are called the <u>main diagonal entries</u> of the matrix. Matrices with the same amount of rows and columns are called <u>square matrices</u>. A matrix with only one column ($2*1$) is called a <u>column matrix</u>. A matrix with only one row ($1*2$) however, is called a <u>row matrix</u>.

| Standard Matrix | Column Matrix | Row Matrix |
| :-: | :-: | :-: |
| $\begin{bmatrix} 1 & 0& -\frac{1}{2} \\ -3 & 2 & 5 \end{bmatrix}$ | $\begin{bmatrix} 1 \\ 2 \end{bmatrix}$ | $\begin{bmatrix} 1 & 2 \end{bmatrix}$ |


##### | **Equality between Matrices**
Two matrices of the same order are said to be <u>equal</u> if their corresponding entries are also equal. Given both matrices have the same order and the same composition of elements, then they should be equal.

E1: Find the corresponding $x$ and $y$ values. 
$$\begin{bmatrix} 1 & \textcolor{Apricot}{2x-1} \\ -5 & 0 \end{bmatrix} = \begin{bmatrix} 1 & 7 \\ \textcolor{Apricot}{y+5} & 0 \end{bmatrix} \ \ \rightarrow \ \ \begin{cases} \textcolor{Apricot}{2x-1}=\textcolor{Skyblue}{7},\ \ thus \ \textcolor{Apricot}x = \textcolor{Skyblue}4 \\ \textcolor{Apricot}{y+5} = \textcolor{Skyblue}{-5},\ \ thus \ \textcolor{Apricot}y = \textcolor{Skyblue}{-10} \end{cases}$$


##### | **Addition of Matrices**
- If the given two matrices have the same order and size, it can be added together normally, such that $a_{ij} + b_{ij}$. If they are not of the same size, they cannot be added together since the sum would be <u>undefined</u>.
$$\textcolor{Apricot}{\begin{bmatrix} 1 & 2 & 3 \\ -1 & 4 & 10 \end{bmatrix}} + \textcolor{Skyblue}{\begin{bmatrix} 0 & -4 & 8 \\ 5 & -9 & -4 \end{bmatrix}} = \begin{bmatrix} \textcolor{Apricot}{1} + \textcolor{Skyblue}{0} & \textcolor{Apricot}{2} + (\textcolor{Skyblue}{-4}) & \textcolor{Apricot}{3} + \textcolor{Skyblue}{8} \\ \textcolor{Apricot}{-1} + \textcolor{Skyblue}{5} & \textcolor{Apricot}{4} + (\textcolor{Skyblue}{-9}) & \textcolor{Apricot}{10} + (\textcolor{Skyblue}{-4}) \end{bmatrix} = \textcolor{LightGray}{\begin{bmatrix} 1 & -2 & 11 \\ 4 & -5 & 6 \end{bmatrix}}$$
- Addition is <u>commutative</u> -- $A + B = B + A$
- Addition is <u>associative</u> -- $(A + B) + C = A + (B + C)$
- Has an <u>additive identity</u> -- $A+O = A$
	--> For any given matrix, there exists a matrix $O$, where all entries of said matrix is zero. This is also called the <u>zero matrix</u>.
- Has an <u>additive inverse</u> -- $A + (-A) = O$
	--> For any given matrix, there exists a unique matrix $B$ = $-A$, such that $A+B = A+(-A) = O$. All entries are negated (or multiplied by -1). This is also called the <u>negative of A</u>.


##### | **Scalar Multiplication of Matrices**
- <u>Scalars</u> are constants that are usually applied to matrices. If $r$ is a scalar, and $A$ is an $n*m$ matrix, then the <u>scalar product</u> of $r$ with $A$, denoted by $rA$, is obtained by multiplying every entry of $A$ by $r$.
- $rA = [ra_{ij}]$ for all $i$ and $j$.
$$\textcolor{Apricot}{\begin{bmatrix} 1 & 2 & 3 \\ -1 & 4 & 10 \end{bmatrix}} \rightarrow \textcolor{Skyblue}{2} \textcolor{Apricot}{A} = \begin{bmatrix} \textcolor{Skyblue}{2}(\textcolor{Apricot}{1}) & \textcolor{Skyblue}{2}(\textcolor{Apricot}{2}) & \textcolor{Skyblue}{2} (\textcolor{Apricot}{3}) \\ \textcolor{Skyblue}{2} (\textcolor{Apricot}{-1}) & \textcolor{Skyblue}{2}(\textcolor{Apricot}{4}) & \textcolor{Skyblue}{2} (\textcolor{Apricot}{10}) \end{bmatrix} = \textcolor{LightGray}{\begin{bmatrix} 2 & 4 & 6 \\ -2 & 8 & 20\end{bmatrix}}$$
- Scalars are <u>distributive</u> -- $(r+s)A = rA + sA$, $r(A+B) = rA + rB$
- Scalars are <u>associative</u> -- $r(sA) = (rs)A$, $r(AB) = (rA)B$


##### | **Multiplication of Matrices**
- If $A$ is an $n*m$ matrix, and $B$ is an $m*p$ matrix, then multiplying the two should result in a matrix with the size of $n*p$. However, this is only possible if the column of matrix $A$ and the row of matrix $B$ are the same. Otherwise, it is <u>undefined</u>.
- Multiply $A$'s first element in the $i$th column with $B$'s first element in the $j$th row. Repeat until you have multiplied every element in $A$'s $i$th column and $B$'s $j$th row. The summation of all these products will be the element $c_{ij}$ in the output matrix.
- $_nA_m*_mB_p = _iC_j$ , and $c_{ij} = \sum^n_{k=1} a_{ik}*b_{kj}$ 
$$\textcolor{Apricot}{\begin{bmatrix} 1 & 2 \\ -2 & 3 \\ 4 & -1 \end{bmatrix}} \ * \ \textcolor{Skyblue}{\begin{bmatrix} 3 & 4 & -1 \\ 0 & 1 & 5 \end{bmatrix}} \ = \ \begin{bmatrix} \textcolor{Apricot}{1}(\textcolor{Skyblue}{3})+\textcolor{Apricot}{2}(\textcolor{Skyblue}{0}) & \textcolor{Apricot}{1}(\textcolor{Skyblue}{4})+\textcolor{Apricot}{2}(\textcolor{Skyblue}{1}) & \textcolor{Apricot}{1}(\textcolor{Skyblue}{-1})+\textcolor{Apricot}{2}(\textcolor{Skyblue}{5}) \\ \textcolor{Apricot}{-2}(\textcolor{Skyblue}{3})+\textcolor{Apricot}{3}(\textcolor{Skyblue}{0}) & \textcolor{Apricot}{-2}(\textcolor{Skyblue}{4})+\textcolor{Apricot}{3}(\textcolor{Skyblue}{1}) & \textcolor{Apricot}{-2}(\textcolor{Skyblue}{-1})+\textcolor{Apricot}{3}(\textcolor{Skyblue}{5}) \\ \textcolor{Apricot}{4}(\textcolor{Skyblue}{3})+\textcolor{Apricot}{-1}(\textcolor{Skyblue}{0}) & \textcolor{Apricot}{4}(\textcolor{Skyblue}{4})+\textcolor{Apricot}{-1}(1) & \textcolor{Apricot}{4}(\textcolor{Skyblue}{-1})+\textcolor{Apricot}{-1}(\textcolor{Skyblue}{5}) \end{bmatrix} = \textcolor{LightGray}{\begin{bmatrix} 3 & 6 & 9 \\ -6 & -5 & 17 \\ 12 & 15 & -9 \end{bmatrix}}$$
- Multiplication is <u>not commutative</u> -- $AB \ne BA$
- Multiplication is <u>associative</u> -- $A(BC) = (AB)C$
- Multiplication is <u>distributive</u> -- $A(B+C) - AB + AC$


##### | **Transposition of Matrices**
- If $A$ is an $n*m$ matrix, then the <u>transpose</u> of $A$, denoted by $A^T$, is an $m*n$ matrix obtained by interchanging each corresponding row with each corresponding column of the matrix. The first row becomes the first column, then second row becomes second column, and so on and so forth. To note, mind the order of the transposed matrix. It might not be compatible and return <u>undefined</u>.
- $A^T = [a_{ij} ^T] = a_{ji}$ for all $i$ and $j$.
$$\textcolor{Apricot}{A = \begin{bmatrix} 1 & 2 & 3 \\ -1 & -2 & 4 \end{bmatrix}} \rightarrow \textcolor{Apricot}{A}\textcolor{Skyblue}{^T} = \textcolor{Skyblue}{\begin{bmatrix} 1 & -1 \\ 2 & -2 \\ 3 & 4 \end{bmatrix}}, \ \ \ \ \textcolor{Apricot}{B = \begin{bmatrix} 2 & 1 \\ 1 & -1 \\ 1 & 0 \end{bmatrix}} \rightarrow \textcolor{Apricot}{B}\textcolor{Skyblue}{^T} = \textcolor{Skyblue}{\begin{bmatrix} 2 & 1 & 1 \\ 1 & -1 &  0\end{bmatrix}}$$
- Transposition of <u>transposition</u> -- $(A^T)^T = A$
- Transposition of <u>sum</u> -- $(A+B)^T = A^T + B^T$
- Transposition of <u>product</u> -- $(AB)^T = B^T * A^T$
- Transposition of <u>scalar multiple</u> -- $(rA)^T = rA^T$

___

Continue to next: [[CM02 - Identity Matrix, Inverse of Matrix, Special Matrices 1]]
Last updated: 10/06/2022

#core #Y2T1