# Linear Algebra — Final-Exam Problems with Detailed Solutions (Integrated Version)

## Problem 1: Determinant Computation

**Problem**: Compute the $n$-order determinant:

$$D_{n}=\begin{vmatrix}a_{1}+\lambda & a_{2} & \cdots & a_{n} \\ a_{1} & a_{2}+\lambda & \cdots & a_{n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{1} & a_{2} & \cdots & a_{n}+\lambda\end{vmatrix}$$

**Solution**:

1.  **Column operation**: Add columns $2, 3, \dots, n$ all to column 1; every entry of column 1 becomes $\lambda + \sum_{i=1}^{n}a_{i}$.

2.  **Factor out the common factor**:

    $$D_{n}=(\lambda+\sum_{i=1}^{n}a_{i})\begin{vmatrix}1 & a_{2} & \dots & a_{n} \\ 1 & a_{2}+\lambda & \dots & a_{n} \\ \vdots & \vdots & \ddots & \vdots \\ 1 & a_{2} & \dots & a_{n}+\lambda\end{vmatrix}$$

3.  **Row operations**: subtract row 1 from row $i$ $(i=2, \dots, n)$, reducing the determinant to upper triangular form.

4.  **Result**: multiply the diagonal entries:

    $$D_{n}=\lambda^{n-1}(\lambda+a_{1}+a_{2}+\dots+a_{n})$$


## Problem 2: Vector Operations

**Problem**: Let $\alpha=\begin{pmatrix}1\\ 2\\ 1\end{pmatrix}$; compute $\alpha^{T}\alpha, \alpha\alpha^{T}, \alpha\alpha^{T}\alpha, (\alpha\alpha^{T})^{100}$.

**Solution**:

1.  **Scalar product**: $\alpha^{T}\alpha = 1^2 + 2^2 + 1^2 = 6$.

2.  **Matrix product**: $\alpha\alpha^{T} = \begin{pmatrix}1\\ 2\\ 1\end{pmatrix}\begin{pmatrix}1 & 2 & 1\end{pmatrix} = \begin{pmatrix}1 & 2 & 1\\ 2 & 4 & 2\\ 1 & 2 & 1\end{pmatrix}$.

3.  **Mixed product**: by associativity, $\alpha\alpha^{T}\alpha = \alpha(\alpha^{T}\alpha) = 6\alpha = \begin{pmatrix}6\\ 12\\ 6\end{pmatrix}$.

4.  **Power**: let $B = \alpha\alpha^{T}$; then $B^2 = 6B$, and by induction $B^n = 6^{n-1}B$.

    $$(\alpha\alpha^{T})^{100} = 6^{99}\begin{pmatrix}1 & 2 & 1\\ 2 & 4 & 2\\ 1 & 2 & 1\end{pmatrix}$$


## Problem 3: Proving Matrix Invertibility

**Problem**: Let $A$ be an $n$-order square matrix satisfying $A^{2}-5A+E=0$; prove that $A-E$ is invertible and find its inverse.

**Solution**:

1.  Rearrange the equation: $A^{2}-5A+E=0 \Rightarrow A^2-A-4A+4E=3E$.

2.  Factor: $(A-E)(A-4E)=3E$.

3.  Hence: $(A-E) \cdot \frac{1}{3}(A-4E) = E$.

4.  By definition, $A-E$ is invertible and $(A-E)^{-1} = \frac{1}{3}(A-4E)$.


## Problem 4: Discussion of a Linear System

**Problem**: Discuss the solutions of the system $\begin{cases}ax_{1}+x_{2}+x_{3}=0\\ x_{1}+ax_{2}+x_{3}=2\\ x_{1}+x_{2}+ax_{3}=a\end{cases}$.

**Solution**: the determinant of the coefficient matrix is $|A| = (a+2)(a-1)^2$.

1.  **Unique solution**: when $a \neq 1$ and $a \neq -2$, the system has a unique solution.

2.  **No solution**: when $a=1$, row reduction of the augmented matrix gives $r(A)=1 \neq r(\overline{A})=2$, so there is no solution.

3.  **Infinitely many solutions**: when $a=-2$, the equivalent system is $\begin{cases}x_{1}-2x_{2}+x_{3}=2\\ -3x_{2}+3x_{3}=4\end{cases}$; taking the free variable $x_3=c$, the general solution is $X=c\begin{pmatrix}1\\ 1\\ 1\end{pmatrix}+\begin{pmatrix}-2/3\\ -4/3\\ 0\end{pmatrix}$.


## Problem 5: Proof of Linear Independence

**Problem**: Given that $\alpha_{1}, \alpha_{2}, \alpha_{3}$ are linearly independent, and $\beta_{1}=\alpha_{1}+\alpha_{2}, \beta_{2}=\alpha_{2}+\alpha_{3}, \beta_{3}=\alpha_{3}+\alpha_{1}$, prove that $\beta_{1}, \beta_{2}, \beta_{3}$ are linearly independent.

**Solution**:

1.  Set $k_1\beta_1+k_2\beta_2+k_3\beta_3=0$; substituting and collecting terms gives $(k_1+k_3)\alpha_1 + (k_1+k_2)\alpha_2 + (k_2+k_3)\alpha_3=0$.

2.  Since the $\alpha_i$ are linearly independent, the determinant of the coefficient matrix is $\begin{vmatrix}1 & 0 & 1 \\ 1 & 1 & 0 \\ 0 & 1 & 1 \end{vmatrix} = 2 \neq 0$.

3.  The system has only the zero solution, so the $\beta_i$ are linearly independent.


## Problem 6: Determining Parameters and the Maximal Linearly Independent Subset

**Problem**: $A=\begin{pmatrix}1 & 1 & 1 & 1 \\ 3 & 2 & 1 & -3 & a \\ 0 & 1 & 2 & 6 & 3 \\ 5 & 4 & 3 & -1 & b \end{pmatrix}$ has rank 2; find $a, b$ and a maximal linearly independent subset of the columns.

**Solution**:

1.  **Row operations**: row reduction to echelon form shows rows 3 and 4 must be zero rows.

2.  **Parameters**: solving gives $a=0, b=2$.

3.  **Maximal linearly independent subset**: the pivots lie in columns 1 and 2, so $\{\alpha_1, \alpha_2\}$ is a maximal linearly independent subset.

4.  **Linear expressions**: the remaining columns are $\alpha_3=-\alpha_1+2\alpha_2, \alpha_4=-5\alpha_1+6\alpha_2, \alpha_5=-2\alpha_1+3\alpha_2$.


## Problem 7: Eigenvalues and Eigenvectors

**Problem**: Find the eigenvalues and eigenvectors of $A_1=\begin{pmatrix}1 & 1 & 0 \\ 1 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}$ and $A_2=\begin{pmatrix}1 & 1 \\ 1 & 1 \end{pmatrix}$.

**Solution**:

1.  **$A_1$**: the eigenvalues are $\lambda_1=0, \lambda_2=1, \lambda_3=2$.

    -   $\lambda_1=0 \to \xi_1=(-1, 1, 0)^T$

    -   $\lambda_2=1 \to \xi_2=(0, 0, 1)^T$

    -   $\lambda_3=2 \to \xi_3=(1, 1, 0)^T$

2.  **$A_2$**: the eigenvalues are $\lambda_1=0, \lambda_2=2$.

    -   $\lambda_1=0 \to \xi_1=(-1, 1)^T$

    -   $\lambda_2=2 \to \xi_2=(1, 1)^T$
