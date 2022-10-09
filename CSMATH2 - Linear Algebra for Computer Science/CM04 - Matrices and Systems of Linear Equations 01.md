<br><br>

##### Matrices and Systems of Linear Equations 1
---

##### | **Matrix Representation**
There are three different ways that a matrix can be represented.
| Standard Equation Form | Matrix Form | Augmented Matrix Form |
| :-: | :-: | :-: |
| $$\begin{cases} a_1x + b_1y = c_1 \\ a_2x + b_2y =c_2 \end{cases}$$ | $$\begin{bmatrix} a_1x + b_1y \\ a_2x + b_2y \end{bmatrix} = \begin{bmatrix} c_1 \\ c_2 \end{bmatrix}$$ | $$\begin{bmatrix} a_1 & b_1 & \bigm\| & c_1 \\ a_2 & b_2 & \bigm\| & c_2 \end{bmatrix}$$|

- Matrix $A$ is called the <u>coefficient matrix</u>.
- Matrix $B$ is called the column matrix of constants, or the <u>constant matrix</u>.
- Matrix $X$ is called the column matrix of unknowns, or the <u>variable matrix</u>.


##### | **Matrix Inversion Method**
1. Given a matrix in <u>standard equation form</u>, look for the coefficients. The left-side coefficients represent matrix $A$, while the coefficients from the right-side represent matrix $B$. The leftover variables represent a single column matrix $X$.
   --> Example: $$\begin{matrix}Given \ \begin{cases} \textcolor{Apricot}{2}\textcolor{LightGray}{x} + \textcolor{LightGray}{y} = \textcolor{Skyblue}{3} \\ \textcolor{Apricot}{9}\textcolor{LightGray}{x} + \textcolor{Apricot}{5}\textcolor{LightGray}{y} = \textcolor{Skyblue}{4} \end{cases} && \textcolor{Apricot}{A = \begin{bmatrix} 2 & 1 \\ 9 & 5 \end{bmatrix}},\ \ \textcolor{Skyblue}{B = \begin{bmatrix} 3 \\ 4 \end{bmatrix}},\ \ \textcolor{LightGray}{X = \begin{bmatrix} x \\ y \end{bmatrix}} \end{matrix}$$
2. Referencing the theorem, determine the <u>inverse</u> of the matrix $A$, by performing EROs to the augmented matrix and the identity. 
   --> Example: $$\begin{bmatrix} \textcolor{Apricot}{2} & \textcolor{Apricot}{1} & \bigm| & \textcolor{LightGray}{1} & \textcolor{LightGray}{0} \\ \textcolor{Apricot}{9} & \textcolor{Apricot}{5} & \bigm| & \textcolor{LightGray}{0} & \textcolor{LightGray}{1} \end{bmatrix} \longrightarrow \begin{bmatrix} \textcolor{LightGray}{1} & \textcolor{LightGray}{0} & \bigm| & \textcolor{Apricot}{5} & \textcolor{Apricot}{-1} \\ \textcolor{LightGray}{0} & \textcolor{LightGray}{1} & \bigm| & \textcolor{Apricot}{-9} & \textcolor{Apricot}{2} \end{bmatrix}$$
3. Referencing the theorem again, to find the values of the variable matrix, multiply the inverse of matrix $A$ with matrix $B$. This will result in a matrix with the same dimensions of the variable matrix, where $(a^{-1}b)_{ij} = x_{ij}$.
   --> Example: $$\textcolor{LightGray}{X} = \textcolor{Apricot}{A^{-1}}\textcolor{Skyblue}{B} = \textcolor{Apricot}{\begin{bmatrix} 5 & -1 \\ -9 & 2 \end{bmatrix}} \textcolor{Skyblue}{\begin{bmatrix} 3 \\ 4 \end{bmatrix}} = \begin{bmatrix} 15 -4 \\ -27 + 8 \end{bmatrix} = \textcolor{LightGray}{\begin{bmatrix} 11 \\ -19 \end{bmatrix}} = \textcolor{LightGray}{\begin{bmatrix} x \\ y \end{bmatrix}}$$
> Theorem: Finding the variable matrix.$$\begin{aligned} \ \textcolor{LightGray}{Default} \ \ &\longrightarrow \ \ AX = B \\ \textcolor{LightGray}{Multiply\  Inverse} \ \ &\longrightarrow \ \ A^{-1}(AX) = A^{-1}B \\ \textcolor{LightGray}{Associativity} \ \ &\longrightarrow \ \ (A^{-1}A)X = A^{-1}B \\ \textcolor{LightGray}{Reduce\ to\ Identity} \ \ &\longrightarrow \ \ IX = A^{-1}B \\ \textcolor{LightGray}{Dissolve\ Identity} \ \ &\longrightarrow \ \ X = A^{-1}B \end{aligned}$$The variable matrix is determined by multiplying the <u>inverse of the co-efficient matrix</u> with the <u>constant matrix</u>.



Let $AX = B$ and $CX = D$ be two linear systems of $m$ equations in $n$ unknowns. If the augmented matrices $[A\ |\ B]$ and $[C\ |\ D]$ of these systems are <u>row equivalent</u>, then both linear systems have <u>exactly the same solutions</u>.

##### | **Gaussian Elimination
1. Given a matrix in standard equation form, convert it into an augmented matrix, and perform EROs to reduce the matrix into <u>REF</u>.
   --> Example: $$\begin{matrix} \begin{cases} \textcolor{Apricot}{2}\textcolor{LightGray}{x} - \textcolor{Apricot}{4}\textcolor{LightGray}{y} = \textcolor{Skyblue}{0} \\ \textcolor{Apricot}{3}\textcolor{LightGray}{x} + \textcolor{LightGray}{y} = \textcolor{Skyblue}{7} \end{cases} && \textcolor{Apricot}{A = \begin{bmatrix} 2 & -4 & \bigm| & 0 \\ 3 & 1 & \bigm| & 7 \end{bmatrix}} && \longrightarrow && \textcolor{Skyblue}{\begin{bmatrix} 1 & -2 & \bigm| & 0 \\ 0 & 1 & \bigm| & 1 \end{bmatrix}} \end{matrix}$$
2. Once reduced, convert it back to its standard equation form. Notice how each the last row reduces to a singular answer that determines the value of last variable.
   --> Example: $$\begin{matrix} \begin{cases} \textcolor{Apricot}{1}\textcolor{LightGray}{x} - \textcolor{Apricot}{2}\textcolor{LightGray}{y} = \textcolor{Skyblue}{0} \\ \textcolor{Apricot}{0}\textcolor{LightGray}{x} + \textcolor{Apricot}{1}\textcolor{LightGray}{y} = \textcolor{Skyblue}{1} \end{cases} && \textcolor{Apricot}{0}\textcolor{LightGray}{x} + \textcolor{Apricot}{1}\textcolor{LightGray}{y} = \textcolor{Skyblue}{1} && \longrightarrow &&  \textcolor{Skyblue}{y = 1} \end{matrix}$$
3. On the next row above, there exists a new variable added with the coefficient multiplied with the last value of the variable. Transpose the coefficient and variable to the other side, plug in the corresponding values, and it should return the value of the next variable.
   --> Example: $$\begin{matrix} \textcolor{LightGray}{y = 1} && \textcolor{Apricot}{1}\textcolor{LightGray}{x} - \textcolor{Apricot}{2}\textcolor{LightGray}{y} = \textcolor{Skyblue}{0} && \textcolor{Apricot}{x} = 2\textcolor{LightGray}{y} \longrightarrow \textcolor{Apricot}{x} = 2(\textcolor{LightGray}{1}) && \longrightarrow && \textcolor{Skyblue}{x = 2} \end{matrix}$$
4. Repeat this until you find all the values of the variables.


##### | **Gauss-Jordan**
1. Given a matrix in standard equation form, convert it into an augmented matrix, and perform EROs to reduce the matrix into <u>RREF</u>.
   --> Example: $$\begin{matrix} \begin{cases} \textcolor{Apricot}{2}\textcolor{LightGray}{x} - \textcolor{Apricot}{4}\textcolor{LightGray}{y} = \textcolor{Skyblue}{0} \\ \textcolor{Apricot}{3}\textcolor{LightGray}{x} + \textcolor{LightGray}{y} = \textcolor{Skyblue}{7} \end{cases} && \textcolor{Apricot}{A = \begin{bmatrix} 2 & -4 & \bigm| & 0 \\ 3 & 1 & \bigm| & 7 \end{bmatrix}} && \longrightarrow && \textcolor{Skyblue}{\begin{bmatrix} 1 & 0 & \bigm| & 2 \\ 0 & 1 & \bigm| & 1 \end{bmatrix}} \end{matrix}$$
2. Once reduced, convert it back to its standard equation form. Notice that since all entries except the leading entries of one are zero, each variable should have a corresponding value.
   --> Example: $$\begin{matrix} \begin{cases} \textcolor{Apricot}{1}\textcolor{LightGray}{x} - \textcolor{Apricot}{0}\textcolor{LightGray}{y} = \textcolor{Skyblue}{2} & \longrightarrow & \textcolor{Skyblue}{x = 2} \\ \textcolor{Apricot}{0}\textcolor{LightGray}{x} + \textcolor{Apricot}{1}\textcolor{LightGray}{y} = \textcolor{Skyblue}{1} & \longrightarrow & \textcolor{Skyblue}{y = 1} \end{cases} \end{matrix}$$
___

Continue to next: [[CM05 - Matrices and Systems of Linear Equations 02]]
Last updated: 10/09/2022

#core #Y2T1 