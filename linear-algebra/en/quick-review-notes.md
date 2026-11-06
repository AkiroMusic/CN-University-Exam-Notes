# Linear Algebra Final-Exam Quick Review Notes

## Module 1: Computing Determinants

**1. Key exam point: special determinants and row/column operations**

- **Claw-shaped determinant / rank-1 update**: when the entries of a determinant other than the diagonal are highly symmetric (e.g. all identical), one usually applies the **global row-difference method** or **adds all columns into the first column** to factor out a common factor.
- **Core rule of row/column operations**: adding one row (column) multiplied by a constant to another row (column) does not change the value of the determinant.

**2. Past-exam question walkthrough (corresponding to Problem 1 of the original exam paper)**

*Note: since OCR recognition of the original problem truncated some characters, the standard solution below is given for the most classic isomorphic problem in linear algebra exams — the determinant whose "rows all have equal entry sums".*

Compute the determinant of order $n$:

$$
D=\begin{vmatrix}a_1+\lambda&a_2&a_3&\cdots&a_n\\a_1&a_2+\lambda&a_3&\cdots&a_n\\a_1&a_2&a_3+\lambda&\cdots&a_n\\\vdots&\vdots&\vdots&\ddots&\vdots\\a_1&a_2&a_3&\cdots&a_n+\lambda\end{vmatrix}
$$

**Solution steps:**

1. **Observe the structure**: the entries of every column are very similar; if all columns are added into the first column, each entry of the first column becomes $\lambda+\sum\limits_{i=1}^{n}a_i$.
2. **Column operation**: add columns $2, 3, ..., n$ all into column 1 ($C_1 \leftarrow C_1 + C_2 + \cdots + C_n$):

$$
D=\begin{vmatrix}\lambda+\sum a_i&a_2&a_3&\cdots&a_n\\\lambda+\sum a_i&a_2+\lambda&a_3&\cdots&a_n\\\vdots&\vdots&\vdots&\ddots&\vdots\\\lambda+\sum a_i&a_2&a_3&\cdots&a_n+\lambda\end{vmatrix}
$$

3. **Factor out the common factor**: factor the common factor of the first column out:

$$
D=\Bigl(\lambda+\sum_{i=1}^{n}a_i\Bigr)\begin{vmatrix}1&a_2&a_3&\cdots&a_n\\1&a_2+\lambda&a_3&\cdots&a_n\\\vdots&\vdots&\vdots&\ddots&\vdots\\1&a_2&a_3&\cdots&a_n+\lambda\end{vmatrix}
$$

4. **Row operations to upper triangular form**: subtract row 1 from each of rows $2, 3, ..., n$ ($R_i \leftarrow R_i - R_1$):

$$
D=\Bigl(\lambda+\sum_{i=1}^{n}a_i\Bigr)\begin{vmatrix}1&a_2&a_3&\cdots&a_n\\0&\lambda&0&\cdots&0\\\vdots&\vdots&\vdots&\ddots&\vdots\\0&0&0&\cdots&\lambda\end{vmatrix}
$$

5. **Conclude the result**: multiply the entries on the main diagonal:

$$D=\lambda^{n-1}\Bigl(\lambda+\sum_{i=1}^{n}a_i\Bigr)$$

## Module 2: Matrix Operations and Matrix Polynomials

**1. Key exam point: matrix multiplication and proofs of invertibility**

- **Inner and outer products of vectors**: the column vector $\alpha$ transposed times itself, $\alpha^T\alpha$, is a **scalar** (a number); itself times its transpose, $\alpha\alpha^T$, is a square matrix of **rank 1**.
- **Inverting via a matrix polynomial**: use the given polynomial to arrange the equation into the form $AB = E$; then $A^{-1} = B$. It is **absolutely forbidden** to treat matrices as ordinary numbers and perform division.

**2. Past-exam question walkthrough (corresponding to Problem 2 of the original exam paper)**

Given $\alpha = (1, 2, 1)^T$, perform the related operations.

**Solution steps:**

1. **Find $\alpha^T\alpha$ (a scalar)**:

$$\alpha^T\alpha=\begin{pmatrix}1&2&1\end{pmatrix}\begin{pmatrix}1\\2\\1\end{pmatrix}=1^2+2^2+1^2=6$$

2. **Find $\alpha\alpha^T$ (a matrix)**:

$$\alpha\alpha^T=\begin{pmatrix}1\\2\\1\end{pmatrix}\begin{pmatrix}1&2&1\end{pmatrix}=\begin{pmatrix}1&2&1\\2&4&2\\1&2&1\end{pmatrix}$$

3. **Find $\alpha\alpha^T\alpha$**:

**Tip**: use the associative law of matrix multiplication; do not grind out the matrix product by brute force.

$$\alpha\alpha^T\alpha=\alpha(\alpha^T\alpha)=6\alpha=\begin{pmatrix}6\\12\\6\end{pmatrix}$$

4. **Find $(\alpha\alpha^T)^{100}$**:

**Tip**: for high powers of a rank-1 matrix, pull the scalar out toward the center.

$$(\alpha\alpha^T)^2=(\alpha\alpha^T)(\alpha\alpha^T)=\alpha(\alpha^T\alpha)\alpha^T=6\alpha\alpha^T$$

Recursing from this gives $(\alpha\alpha^T)^k=6^{k-1}\alpha\alpha^T$; therefore:

$$(\alpha\alpha^T)^{100}=6^{99}\begin{pmatrix}1&2&1\\2&4&2\\1&2&1\end{pmatrix}$$

**3. Past-exam question walkthrough (corresponding to Problem 3 of the original exam paper)**

Let A be a square matrix of order n satisfying $A^2-5A+E=0$; prove that $A-E$ is invertible, and find its inverse.

**Solution steps:**

1. **Target construction**: we need to extract $(A-E)$ as a factor from the original equation and build the form $(A-E)B=E$.
2. **Polynomial factoring and rearrangement**:

$$
\begin{aligned}
A^2-5A+E&=0\\
A^2-A-4A+E&=0\\
A(A-E)-4(A-E)-3E&=0
\end{aligned}
$$

3. **Factor out the common factor**:

$$(A-4E)(A-E)=3E$$

Divide both sides by the scalar 3:

$$(A-E)\biggl[\frac{1}{3}(A-4E)\biggr]=E$$

4. **Conclude**: by the definition of an invertible matrix, $A-E$ is invertible, and its inverse is:

$$(A-E)^{-1}=\frac{1}{3}(A-4E)$$

## Module 3: Structure of the Solutions of Systems of Linear Equations

**1. Key exam point: criteria for solutions**

Let the coefficient matrix of the system be $A$, the augmented matrix be $\overline{A}=(A|B)$, and the number of unknowns be $n$:

- **Unique solution**: rank $r(A)=r(\overline{A})=n$ (or $|A|\neq0$).
- **No solution**: rank $r(A)\neq r(\overline{A})$.
- **Infinitely many solutions**: rank $r(A)=r(\overline{A})<n$ (in which case $|A|=0$). The general solution has the structure: **a particular solution + a linear combination of the fundamental system of solutions of the homogeneous system**.

**2. Past-exam question walkthrough (corresponding to Problem 4 of the original exam paper)**

Discuss for which values of the parameter $a$ the system has a unique solution, no solution, or infinitely many solutions, and find the general solution when there are infinitely many:

$$\begin{cases}ax_1+x_2+x_3=0\\x_1+ax_2+x_3=2\\x_1+x_2+ax_3=a\end{cases}$$

**Solution steps:**

1. **Compute the determinant of the coefficient matrix**:

$$|A|=\begin{vmatrix}a&1&1\\1&a&1\\1&1&a\end{vmatrix}=(a+2)(a-1)^2$$

2. **Unique solution criterion**: when $|A|\neq0$, i.e. $a\neq1$ and $a\neq-2$, the system has a **unique solution**.
3. **Degenerate case** $(a=1)$:

Substituting $a=1$, the augmented matrix is:

$$\overline{A}=\begin{pmatrix}1&1&1&0\\1&1&1&2\\1&1&1&1\end{pmatrix}$$

Clearly rows 1 and 2 contradict each other (the coefficients on the left are identical while the constants on the right differ). Here $r(A)=1, r(\overline{A})=2$, so $r(A)\neq r(\overline{A})$: **no solution**.

4. **Degenerate case and solving** $(a=-2)$:

Substituting $a=-2$, apply elementary row operations to the augmented matrix:

$$\overline{A}=\begin{pmatrix}-2&1&1&0\\1&-2&1&2\\1&1&-2&-2\end{pmatrix}\xrightarrow{R_1\leftrightarrow R_2}\begin{pmatrix}1&-2&1&2\\-2&1&1&0\\1&1&-2&-2\end{pmatrix}$$

$$\xrightarrow{\substack{R_2+2R_1\\R_3-R_1}}\begin{pmatrix}1&-2&1&2\\0&-3&3&4\\0&3&-3&-4\end{pmatrix}\xrightarrow{R_3+R_2}\begin{pmatrix}1&-2&1&2\\0&-3&3&4\\0&0&0&0\end{pmatrix}$$

Simplifying gives the equivalent reduced system:

$$\begin{cases}x_1-2x_2+x_3=2\\-3x_2+3x_3=4\end{cases}$$

Here $r(A)=r(\overline{A})=2<3$: there are **infinitely many solutions**.

Taking the free variable $x_3=0$ gives the particular solution: $x_2=-4/3, x_1=-2/3$.

Taking the free variable $x_3=1$ and substituting into the corresponding homogeneous system $x_1-2x_2+x_3=0, -3x_2+3x_3=0$ gives the fundamental system of solutions: $x_2=1, x_1=1$.

**The general solution is:**

$$X=\begin{pmatrix}-2/3\\-4/3\\0\end{pmatrix}+k\begin{pmatrix}1\\1\\1\end{pmatrix}\quad(k\ \text{is an arbitrary constant})$$

## Module 4: Linear Dependence and Rank of Sets of Vectors

**1. Key exam point: linear combinations and maximal linearly independent subsets**

- **Definition of linear independence**: if $k_1\alpha_1+k_2\alpha_2+\cdots+k_n\alpha_n=0$ can only yield $k_1=k_2=\cdots=k_n=0$, then the set of vectors is linearly independent.
- **Method for finding a maximal linearly independent subset**: assemble the column vectors into a matrix and apply **elementary row operations** to bring it to echelon form; the columns where the echelon pivots stand form the maximal linearly independent subset.

**2. Past-exam question walkthrough (corresponding to Problem 5 of the original exam paper)**

Let $\alpha_1, \alpha_2, \alpha_3$ be linearly independent; prove that $\beta_1=\alpha_1+\alpha_2, \beta_2=\alpha_2+\alpha_3, \beta_3=\alpha_3+\alpha_1$ are linearly independent.

**Solution steps:**

1. **Set the linear combination equal to the zero vector**: suppose there exist constants $k_1, k_2, k_3$ such that

$$k_1\beta_1+k_2\beta_2+k_3\beta_3=0$$

2. **Substitute the original vectors and regroup**:

$$
\begin{aligned}
k_1(\alpha_1+\alpha_2)+k_2(\alpha_2+\alpha_3)+k_3(\alpha_3+\alpha_1)&=0\\
(k_1+k_3)\alpha_1+(k_1+k_2)\alpha_2+(k_2+k_3)\alpha_3&=0
\end{aligned}
$$

3. **Use the given condition**: since $\alpha_1, \alpha_2, \alpha_3$ are linearly independent, their coefficients must all be 0:

$$\begin{cases}k_1+k_3=0\\k_1+k_2=0\\k_2+k_3=0\end{cases}$$

4. **Solve for the coefficients**: the determinant of the coefficients of this homogeneous system is $\begin{vmatrix}1&0&1\\1&1&0\\0&1&1\end{vmatrix}=2\neq0$. By Cramer's rule, the system has only the zero solution, i.e. $k_1=k_2=k_3=0$.
5. **Conclusion**: therefore $\beta_1, \beta_2, \beta_3$ are linearly independent.

**3. Past-exam question walkthrough (corresponding to Problem 6 of the original exam paper)**

Determine the parameters $a, b$ such that the matrix $A$ has rank 2; find a maximal linearly independent subset of the column vectors and express the remaining vectors in terms of it. (The missing parameter in the first row is reconstructed from the problem statement and by closing the logical loop.)

$$A=\begin{pmatrix}1&1&1&1&a\\3&2&1&-3&8\\0&1&2&6&3\\5&4&3&-1&b\end{pmatrix}$$

**Solution steps:**

1. **Elementary row operations**:

$R_2\leftarrow R_2-3R_1,\ R_4\leftarrow R_4-5R_1$:

$$\begin{pmatrix}1&1&1&1&a\\0&-1&-2&-6&8-3a\\0&1&2&6&3\\0&-1&-2&-6&b-5a\end{pmatrix}$$

Add row 3 to row 2 and to row 4 respectively $(R_2\leftarrow R_2+R_3,\ R_4\leftarrow R_4+R_3)$:

$$\begin{pmatrix}1&1&1&1&a\\0&0&0&0&11-3a\\0&1&2&6&3\\0&0&0&0&b-5a+3\end{pmatrix}$$

2. **Determine the parameters**: the rank of the matrix is given as 2, and rows 1 and 3 are clearly linearly independent (forming the basis of rank 2), so the all-zero rows must occur in rows 2 and 4.

Set $11-3a=0\implies a=11/3$

Set $b-5a+3=0\implies b=5(11/3)-3=46/3$

3. **Find the maximal linearly independent subset**: now further reduce the echelon form to reduced row echelon form $(R_1\leftarrow R_1-R_3)$ and substitute $a$:

$$\begin{pmatrix}1&0&-1&-5&2/3\\0&1&2&6&3\\0&0&0&0&0\\0&0&0&0&0\end{pmatrix}$$

The pivot positions correspond to the first two columns of the original matrix, so **columns 1 and 2 $(c_1, c_2)$ form a maximal linearly independent subset**.

4. **Express the remaining vectors**: read the coefficients of the corresponding columns directly from the reduced row echelon matrix.

$$
\begin{aligned}
c_3&=-c_1+2c_2\\
c_4&=-5c_1+6c_2\\
c_5&=\frac{2}{3}c_1+3c_2
\end{aligned}
$$

## Module 5: Eigenvalues and Eigenvectors

**1. Key exam point: procedure for computing eigenvalues**

- **Solving for the eigenvalues**: the core logic is to solve the characteristic equation $|\lambda E-A|=0$ to find all the $\lambda$.
- **Solving for the eigenvectors**: substitute each $\lambda_i$ into the system $(\lambda_iE-A)x=0$; the fundamental system of solutions obtained is the eigenvectors.

**2. Past-exam question walkthrough (corresponding to Problem 7 of the original exam paper)**

Find the eigenvalues and eigenvectors of the matrix $A=\begin{pmatrix}1&1&0\\1&1&0\\0&0&1\end{pmatrix}$.

**Solution steps:**

1. **Write down the characteristic equation**:

$$|\lambda E-A|=\begin{vmatrix}\lambda-1&-1&0\\-1&\lambda-1&0\\0&0&\lambda-1\end{vmatrix}$$

Expanding:

$$=(\lambda-1)\bigl[(\lambda-1)^2-1\bigr]=(\lambda-1)(\lambda^2-2\lambda)=\lambda(\lambda-1)(\lambda-2)=0$$

2. **The eigenvalues obtained**:

$\lambda_1=0, \lambda_2=1, \lambda_3=2$

3. **Solve for the eigenvectors one by one**:

- For $\lambda_1=0$, solve $(-A)x=0$:

$$\begin{pmatrix}-1&-1&0\\-1&-1&0\\0&0&-1\end{pmatrix}\begin{pmatrix}x_1\\x_2\\x_3\end{pmatrix}=0\implies\begin{cases}x_1+x_2=0\\x_3=0\end{cases}$$

Taking $x_1=1$ gives the corresponding eigenvector $p_1=(1,-1,0)^T$.

- For $\lambda_2=1$, solve $(E-A)x=0$:

$$\begin{pmatrix}0&-1&0\\-1&0&0\\0&0&0\end{pmatrix}\begin{pmatrix}x_1\\x_2\\x_3\end{pmatrix}=0\implies\begin{cases}x_1=0\\x_2=0\end{cases}$$

Taking $x_3=1$ gives the corresponding eigenvector $p_2=(0,0,1)^T$.

- For $\lambda_3=2$, solve $(2E-A)x=0$:

$$\begin{pmatrix}1&-1&0\\-1&1&0\\0&0&1\end{pmatrix}\begin{pmatrix}x_1\\x_2\\x_3\end{pmatrix}=0\implies\begin{cases}x_1-x_2=0\\x_3=0\end{cases}$$

Taking $x_1=1$ gives the corresponding eigenvector $p_3=(1,1,0)^T$.
