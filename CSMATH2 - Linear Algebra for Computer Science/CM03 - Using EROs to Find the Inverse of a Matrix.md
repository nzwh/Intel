<br><br>

##### Using EROs to Find the Inverse of a Matrix
---

##### | **Systematic Procedure for Solving System of Linear Equations
1. Interchange any two equations -- $eq_1 \longleftrightarrow eq_2$
2. Multiply an equation by a non-zero constant -- $k(eq_1)$
3. Rule 2, then adding to another equation -- $k(eq_1) + eq_2$

##### | **Elementary Row Operations**
1. ERO 1 - Interchange any two rows -- $row_i \longleftrightarrow row_j$
2. ERO 2 - Multiply a row by a non-zero constant -- $k(row_i)$
3. ERO 3 - ERO 2, then adding into another equation -- $k(row_i) + row_j$
Note: Only the $j$th row changes, while the $i$th is used as a <u>pivot</u> or a <u>reference</u>, and the $i$th row remains unchanged.

A matrix $A$ is <u>row-equivalent</u> to matrix $B$, denoted by $A \sim B$, if and only if matrix $B$ is obtained from matrix $A$ by performing a sequences of <u>EROs</u>.
$$A = \ \begin{matrix} 1/3 \\ \ \end{matrix} \ \begin{bmatrix} 3 & -6 \\ -2 & 5 \end{bmatrix} \sim \begin{bmatrix} 1 & -2 \\ -2 & 5 \end{bmatrix} = B$$

A matrix $A$ is in the <u>row echelon form</u> (REF) if:
1. The <u>non-zero rows</u> are found on <u>top of the matrix</u>.
2. The <u>leading entries</u> of all the non-zero rows are <u>equal to 1</u>. The leading entry of a row is the first non-zero entry in the row.
3. The <u>leading entries</u> of the rows move down to the right as it descends down into the matrix. 

If in addition, all the other entries of a column with a leading entry are equal to 0, then the matrix is said to be in its <u>reduced row echelon form</u>. To add, matrices in RREF are always in REF, but not all matrices in REF are RREF.


##### | **Gaussian Elimination (Reducing to REF)**
1. Look for the first non-zero column, with preferably a leading entry of 1 or close.  Then, perform ERO:I by interchanging that row, with the first row of the matrix
	--> Example: ERO:I $$\begin{bmatrix} \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & \textcolor{Apricot}{2} & \textcolor{Apricot}{1} \\ 0 & 2 & 3 & 2 & -1 \\ \textcolor{Skyblue}{0} & \textcolor{Skyblue}{2} & \textcolor{Skyblue}{0} & \textcolor{Skyblue}{2} & \textcolor{Skyblue}{4} \end{bmatrix} \longrightarrow  \begin{bmatrix} \textcolor{Skyblue}{0} & \textcolor{Skyblue}{2} & \textcolor{Skyblue}{0} & \textcolor{Skyblue}{2} & \textcolor{Skyblue}{4} \\ 0 & 2 & 3 & 2 & -1 \\ \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & \textcolor{Apricot}{2} & \textcolor{Apricot}{1} \end{bmatrix}$$
2. If the leading entry of that row is not equal to 1, perform ERO:II, by multiplying the row with the leading entry, with its reciprocal to reduce it into 1. Otherwise, let it remain.
   --> Example: ERO:II $$\begin{matrix} \textcolor{Apricot}{1/2} \\ \ \\ \ \end{matrix} \begin{bmatrix} \textcolor{Apricot}{0} & \textcolor{Apricot}{2} & \textcolor{Apricot}{0} & \textcolor{Apricot}{2} & \textcolor{Apricot}{4} \\ 0 & 2 & 3 & 2 & -1 \\ 0 & 0 & 0 & 2 & 1 \end{bmatrix} \longrightarrow \begin{bmatrix} \textcolor{Skyblue}{0} & \textcolor{Skyblue}{1} & \textcolor{Skyblue}{0} & \textcolor{Skyblue}{1} & \textcolor{Skyblue}{2} \\ 0 & 2 & 3 & 2 & -1 \\ 0 & 0 & 0 & 2 & 1 \end{bmatrix}$$
3. Now, determine the column where that leading entry of 1 is located. Turn all entries below that leading entry of 1 into 0, by performing ERO:III, where you would choose a pivot to multiply the negative of the target entry, to the row where the leading entry is 1, and then adding it to the target entry.
   --> Example: ERO:III $$\begin{matrix} \\ \textcolor{Apricot}{\times \rightarrow} \\ \textcolor{Apricot}{-2}  \\ \ \end{matrix} \begin{array} \ \begin{matrix} 0 & -2 & 0 & -2 & -4 \end{matrix} \\ \begin{bmatrix} \textcolor{LightGray}{0} & \textcolor{LightGray}{+1} & \textcolor{LightGray}{0} & \textcolor{LightGray}{+1} & \textcolor{LightGray}{+2} \\ 0 & \textcolor{Apricot}{2} & 3 & 2 & -1 \\ 0 & 0 & 0 & 2 & 1 \end{bmatrix} \end{array} \begin{matrix} \\ \textcolor{Skyblue}{\leftarrow +} \\ \ \end{matrix} \ \ \ \longrightarrow \begin{bmatrix} 0 & 1 & 0 & 1 & 2 \\ \textcolor{Skyblue}{0} & \textcolor{Skyblue}{0} & \textcolor{Skyblue}{3} & \textcolor{Skyblue}{0} & \textcolor{Skyblue}{-5} \\ 0 & 0 & 0 & 2 & 1 \end{bmatrix}$$
4. Repeat the same procedure to the submatrix, excluding the first row. Do this until you have a stair-like pattern of leading entries of 1. The resulting matrix should have leading entries of 1 for all rows, excluding zero rows, but not necessarily for all columns.
   --> Example: ERO:II -> ERO:II -> ERO:III $$ \begin{matrix} \ \\ \textcolor{Apricot}{\frac{1}{3}} \\ \ \end{matrix} \begin{bmatrix} 0 & 1 & 0 & 1 & 2 \\ \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & \textcolor{Apricot}{3} & \textcolor{Apricot}{0} & \textcolor{Apricot}{-5} \\ 0 & 0 & 0 & 2 & 1 \end{bmatrix} \longrightarrow \begin{matrix} \ \\ \ \\ \ \textcolor{Apricot}{\frac{1}{2}} \end{matrix} \begin{bmatrix} 0 & 1 & 0 & 1 & 2 \\ 0 & 0 & 1 & 0 & -\frac{5}{3} \\ \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & \textcolor{Apricot}{0} & \textcolor{Apricot}{2} & \textcolor{Apricot}{1} \end{bmatrix} \longrightarrow \begin{matrix} \textcolor{Apricot}{-1} \\ \ \\ \ \end{matrix} \begin{bmatrix} 0 & 1 & 0 & \textcolor{Apricot}{1} & 2 \\ 0 & 0 & 1 & 0 & -\frac{5}{3} \\ \textcolor{LightGray}{0} & \textcolor{LightGray}{0} & \textcolor{LightGray}{0} & \textcolor{LightGray}{1} & \textcolor{LightGray}{\frac{1}{2}} \end{bmatrix} \rightarrow \textcolor{LightGray}{\begin{bmatrix} 0 & 1 & 0 & 0 & \frac{3}{2} \\ 0 & 0 & 1 & 0 & -\frac{5}{3} \\ 0 & 0 & 0 & 1 & \frac{1}{2} \end{bmatrix}} $$
When reducing the matrix to RREF, instead turn all the entries of with a leading entry of 1 column to 0, above and below, excluding the leading entry. Note that there can be <u>different REFs</u> of a matrix, but there is only <u>one unique RREF</u> of a matrix.


##### | **Finding the Inverse using Gaussian Elimination**
1. Augment the matrix with its corresponding identity to the right of the matrix, separated with a long bar. Make sure the identity has the same order of the given matrix. Also note that this method <u>does not work for non-square matrices</u>.
   --> Example: $$\begin{bmatrix} 3 & -6 & \textcolor{Apricot}{\bigm|} & \textcolor{Apricot}{1} & \textcolor{Apricot}{0} \\ -2 & 5 & \textcolor{Apricot}{\bigm|} & \textcolor{Apricot}{0} & \textcolor{Apricot}{1} \end{bmatrix}$$
2. Apply EROs to each row, while simultaneously applying the same rules and operations into the augmented identity matrix.
   --> Example: $$\begin{matrix} \textcolor{Apricot}{\frac{1}{3}} \\ \ \end{matrix} \begin{bmatrix} \textcolor{Apricot}{3} & \textcolor{Apricot}{-6} & \bigm| & \textcolor{Apricot}{1} & \textcolor{Apricot}{0} \\ -2 & 5 & \bigm| & 0 & 1 \end{bmatrix} \longrightarrow \begin{matrix} \ \\ \textcolor{Apricot}{2} \end{matrix} \begin{bmatrix} \textcolor{LightGray}{1} & \textcolor{LightGray}{-2} &\bigm| & \textcolor{LightGray}{\frac{1}{3}} & \textcolor{LightGray}{0} \\ \textcolor{Apricot}{-2} & 5 & \bigm| & 0 & 1 \end{bmatrix} \longrightarrow \begin{matrix} \textcolor{Apricot}{2} \\ \ \end{matrix} \begin{bmatrix} 1 & \textcolor{Apricot}{-2} & \bigm| & \frac{1}{3} & 0 \\ \textcolor{LightGray}{0} & \textcolor{LightGray}{1} & \bigm| & \textcolor{LightGray}{\frac{2}{3}} & \textcolor{LightGray}{1} \end{bmatrix}$$
3. Once the main matrix has completely reduced to the identity, the augmented identity would have been completely transformed into the inverse of the main matrix.
   --> Example: $$\begin{bmatrix} \textcolor{Apricot}{1} & \textcolor{Apricot}{0} & \textcolor{Apricot}{\bigm|} & \textcolor{Skyblue}{\frac{5}{3}} & \textcolor{Skyblue}{2} \\ \textcolor{Apricot}{0} & \textcolor{Apricot}{1} & \textcolor{Apricot}{\bigm|} & \textcolor{Skyblue}{\frac{2}{3}} & \textcolor{Skyblue}{1} \end{bmatrix}$$
___

Continue to next: [[CSMATH2 - Linear Algebra for Computer Science/CM04 - Matrices and Systems of Linear Equations 01]]
Last updated: 10/09/2022

#core #Y2T1