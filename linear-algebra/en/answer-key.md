# Linear Algebra Final Exam Standard Answer Key (Complete and Error-Free Version)

## Problem 1: Compute the determinant of order $n$

$$
D_n=\begin{vmatrix}a_1+\lambda&a_2&\cdots&a_n\\a_1&a_2+\lambda&\cdots&a_n\\\vdots&\vdots&\ddots&\vdots\\a_1&a_2&\cdots&a_n+\lambda\end{vmatrix}
$$

**Column operations**: add columns $2,3,\ldots,n$ all to column 1; every entry of column 1 becomes $\lambda+\sum\limits_{i=1}^{n}a_i$. Factor out the common factor:

$$
D_n=\Bigl(\lambda+\sum_{i=1}^{n}a_i\Bigr)
\begin{vmatrix}1&a_2&\cdots&a_n\\1&a_2+\lambda&\cdots&a_n\\\vdots&\vdots&\ddots&\vdots\\1&a_2&\cdots&a_n+\lambda\end{vmatrix}
$$

**Row operations**: subtract row 1 from row $i$ ($i=2,\ldots,n$), reducing to upper triangular form:

$$
D_n=\Bigl(\lambda+\sum_{i=1}^{n}a_i\Bigr)
\begin{vmatrix}1&a_2&\cdots&a_n\\0&\lambda&\cdots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\cdots&\lambda\end{vmatrix}
$$

**Multiply the entries on the main diagonal**:

$$\boxed{D_n=\lambda^{n-1}\Bigl(\lambda+a_1+a_2+\cdots+a_n\Bigr)}$$

## Problem 2: Vector operations

Let $\alpha=\begin{pmatrix}1\\2\\1\end{pmatrix}$; find $\alpha^T\alpha,\ \alpha\alpha^T,\ \alpha\alpha^T\alpha,\ (\alpha\alpha^T)^{100}$.

(1) $\alpha^T\alpha$ (a scalar):

$$\alpha^T\alpha=1^2+2^2+1^2=\mathbf{6}$$

(2) $\alpha\alpha^T$ (a $3\times3$ matrix):

$$\alpha\alpha^T=\begin{pmatrix}1\\2\\1\end{pmatrix}\begin{pmatrix}1&2&1\end{pmatrix}=\begin{pmatrix}1&2&1\\2&4&2\\1&2&1\end{pmatrix}$$

(3) $\alpha\alpha^T\alpha$: use the associative law of matrix multiplication

$$\alpha\alpha^T\alpha=\alpha\cdot(\alpha^T\alpha)=6\alpha=\begin{pmatrix}6\\12\\6\end{pmatrix}$$

(4) $(\alpha\alpha^T)^{100}$: let $B=\alpha\alpha^T$. Note that

$$B^2=(\alpha\alpha^T)(\alpha\alpha^T)=\alpha(\alpha^T\alpha)\alpha^T=6\alpha\alpha^T=6B$$

Induction gives $B^n=6^{n-1}B$ ($n\geq1$), hence

$$\boxed{(\alpha\alpha^T)^{100}=6^{99}\alpha\alpha^T=6^{99}\begin{pmatrix}1&2&1\\2&4&2\\1&2&1\end{pmatrix}}$$

## Problem 3: Prove that $A-E$ is invertible and find its inverse

We are given that the square matrix $A$ of order $n$ satisfies $A^2-5A+E=0$.

**Proof**: apply algebraic rearrangement to the given equation:

$$
\begin{aligned}
A^2-5A+E&=0\\
A^2-A-4A+4E&=3E\\
(A-E)(A-4E)&=3E\\
(A-E)\cdot\frac{1}{3}(A-4E)&=E
\end{aligned}
$$

By the definition of an invertible matrix, $A-E$ is invertible, and

$$\boxed{(A-E)^{-1}=\frac{1}{3}(A-4E)}$$

$\blacksquare$

## Problem 4: Discuss the solutions of the system of linear equations

$$\begin{cases}ax_1+x_2+x_3=0\\x_1+ax_2+x_3=2\\x_1+x_2+ax_3=a\end{cases}$$

Compute the determinant of the coefficient matrix:

$$|A|=\begin{vmatrix}a&1&1\\1&a&1\\1&1&a\end{vmatrix}=(a+2)(a-1)^2$$

(1) **Unique solution**: when $|A|\neq0$, i.e. $a\neq1$ and $a\neq-2$, the system has a unique solution.

(2) **No solution ($a=1$)**: the augmented matrix

$$\bar{A}=\begin{pmatrix}1&1&1&0\\1&1&1&2\\1&1&1&1\end{pmatrix}\rightarrow\begin{pmatrix}1&1&1&0\\0&0&0&2\\0&0&0&1\end{pmatrix}$$

$r(A)=1\neq r(\bar{A})=2$, so there is no solution when $\mathbf{a=1}$.

(3) **Infinitely many solutions ($a=-2$)**: apply row operations to the augmented matrix:

$$\bar{A}=\begin{pmatrix}-2&1&1&0\\1&-2&1&2\\1&1&-2&-2\end{pmatrix}
\xrightarrow{R_1\leftrightarrow R_2}
\begin{pmatrix}1&-2&1&2\\-2&1&1&0\\1&1&-2&-2\end{pmatrix}
\xrightarrow{R_2+2R_1,\ R_3-R_1}
\begin{pmatrix}1&-2&1&2\\0&-3&3&4\\0&3&-3&-4\end{pmatrix}
\xrightarrow{R_3+R_2}
\begin{pmatrix}1&-2&1&2\\0&-3&3&4\\0&0&0&0\end{pmatrix}$$

$r(A)=r(\bar{A})=2<3$, so the system has infinitely many solutions. The equivalent system is:

$$\begin{cases}x_1-2x_2+x_3=2\\-3x_2+3x_3=4\end{cases}$$

Let the free variable be $x_3=c$; then

$$x_2=c-\frac{4}{3},\quad x_1=c-\frac{2}{3}$$

$$\boxed{\text{General solution:}\quad X=c\begin{pmatrix}1\\1\\1\end{pmatrix}+\begin{pmatrix}-\dfrac{2}{3}\\[2pt]-\dfrac{4}{3}\\[2pt]0\end{pmatrix},\quad c\in\mathbb{R}}$$

## Problem 5: Prove that $\beta_1,\beta_2,\beta_3$ are linearly independent

Given that $\alpha_1,\alpha_2,\alpha_3$ are linearly independent, and $\beta_1=\alpha_1+\alpha_2$, $\beta_2=\alpha_2+\alpha_3$, $\beta_3=\alpha_3+\alpha_1$.

**Proof**: set $k_1\beta_1+k_2\beta_2+k_3\beta_3=0$; substitute the expressions of the $\beta_i$ and collect terms:

$$(k_1+k_3)\alpha_1+(k_1+k_2)\alpha_2+(k_2+k_3)\alpha_3=0$$

Since $\alpha_1,\alpha_2,\alpha_3$ are linearly independent, every coefficient must be zero:

$$\begin{cases}k_1+k_3=0\\k_1+k_2=0\\k_2+k_3=0\end{cases}$$

The determinant of the coefficients of this homogeneous system is

$$\begin{vmatrix}1&0&1\\1&1&0\\0&1&1\end{vmatrix}=1\cdot(1-0)-0+1\cdot(1-0)=2\neq0$$

Hence the system has only the zero solution $k_1=k_2=k_3=0$, and therefore $\beta_1,\beta_2,\beta_3$ are linearly independent.

$\blacksquare$

## Problem 6: Determine the parameters and find the maximal linearly independent subset

$$A=\begin{pmatrix}1&1&1&1&1\\3&2&1&-3&a\\0&1&2&6&3\\5&4&3&-1&b\end{pmatrix}$$

**Elementary row operations** ($R_2-3R_1,\ R_4-5R_1$):

$$\rightarrow\begin{pmatrix}1&1&1&1&1\\0&-1&-2&-6&a-3\\0&1&2&6&3\\0&-1&-2&-6&b-5\end{pmatrix}$$

**Continue** ($R_2+R_3,\ R_4+R_3$):

$$\rightarrow\begin{pmatrix}1&1&1&1&1\\0&0&0&0&a\\0&1&2&6&3\\0&0&0&0&b-2\end{pmatrix}$$

**Swap** ($R_2\leftrightarrow R_3$) and arrange into row echelon form:

$$\rightarrow\begin{pmatrix}1&1&1&1&1\\0&1&2&6&3\\0&0&0&0&a\\0&0&0&0&b-2\end{pmatrix}$$

**Determine the parameters**: for $r(A)=2$, rows 3 and 4 must be all-zero rows, hence

$$a=0,\quad b-2=0\implies\mathbf{a=0,\ b=2}$$

**Find the maximal linearly independent subset** (substitute $a=0,\ b=2$ and continue simplifying with $R_1-R_2$):

$$A\rightarrow\begin{pmatrix}1&0&-1&-5&-2\\0&1&2&6&3\\0&0&0&0&0\\0&0&0&0&0\end{pmatrix}$$

The pivots lie in columns 1 and 2, so a **maximal linearly independent subset** of the set of column vectors is $\{\alpha_1,\alpha_2\}$.

$$\boxed{\text{Linear expressions of the remaining column vectors (read off directly from the corresponding columns of the reduced row echelon matrix)}:\quad
\alpha_3=-\alpha_1+2\alpha_2,\quad \alpha_4=-5\alpha_1+6\alpha_2,\quad \alpha_5=-2\alpha_1+3\alpha_2}$$

## Problem 7: Find the eigenvalues and eigenvectors

(1) $A=\begin{pmatrix}1&1&0\\1&1&0\\0&0&1\end{pmatrix}$

**Characteristic equation**:

$$|\lambda E-A|=\begin{vmatrix}\lambda-1&-1&0\\-1&\lambda-1&0\\0&0&\lambda-1\end{vmatrix}=(\lambda-1)\bigl[(\lambda-1)^2-1\bigr]=\lambda(\lambda-1)(\lambda-2)=0$$

**Eigenvalues**: $\lambda_1=0,\ \lambda_2=1,\ \lambda_3=2$

$\lambda_1=0$: solve $-Ax=0$

$$(-A)=\begin{pmatrix}-1&-1&0\\-1&-1&0\\0&0&-1\end{pmatrix}\rightarrow\begin{pmatrix}1&1&0\\0&0&0\\0&0&1\end{pmatrix}\implies x_1+x_2=0,\ x_3=0$$

Taking $x_2=1$ gives the fundamental system of solutions $\xi_1=(-1,\,1,\,0)^T$, and the corresponding eigenvector is $k_1\xi_1$ ($k_1\neq0$).

$\lambda_2=1$: solve $(E-A)x=0$

$$E-A=\begin{pmatrix}0&-1&0\\-1&0&0\\0&0&0\end{pmatrix}\rightarrow\begin{pmatrix}1&0&0\\0&1&0\\0&0&0\end{pmatrix}\implies x_1=0,\ x_2=0$$

Taking $x_3=1$ gives the fundamental system of solutions $\xi_2=(0,\,0,\,1)^T$, and the corresponding eigenvector is $k_2\xi_2$ ($k_2\neq0$).

$\lambda_3=2$: solve $(2E-A)x=0$

$$2E-A=\begin{pmatrix}1&-1&0\\-1&1&0\\0&0&1\end{pmatrix}\rightarrow\begin{pmatrix}1&-1&0\\0&0&0\\0&0&1\end{pmatrix}\implies x_1-x_2=0,\ x_3=0$$

Taking $x_1=1$ gives the fundamental system of solutions $\xi_3=(1,\,1,\,0)^T$, and the corresponding eigenvector is $k_3\xi_3$ ($k_3\neq0$).

(2) $A=\begin{pmatrix}1&1\\1&1\end{pmatrix}$

**Characteristic equation**:

$$|\lambda E-A|=\begin{vmatrix}\lambda-1&-1\\-1&\lambda-1\end{vmatrix}=(\lambda-1)^2-1=\lambda(\lambda-2)=0$$

**Eigenvalues**: $\lambda_1=0,\ \lambda_2=2$

$\lambda_1=0$: solve $-Ax=0$

$$-A=\begin{pmatrix}-1&-1\\-1&-1\end{pmatrix}\rightarrow\begin{pmatrix}1&1\\0&0\end{pmatrix}\implies x_1+x_2=0$$

Taking $x_2=1$ gives the fundamental system of solutions $\xi_1=(-1,\,1)^T$, and the corresponding eigenvector is $k_1\xi_1$ ($k_1\neq0$).

$\lambda_2=2$: solve $(2E-A)x=0$

$$2E-A=\begin{pmatrix}1&-1\\-1&1\end{pmatrix}\rightarrow\begin{pmatrix}1&-1\\0&0\end{pmatrix}\implies x_1-x_2=0$$

Taking $x_2=1$ gives the fundamental system of solutions $\xi_2=(1,\,1)^T$, and the corresponding eigenvector is $k_2\xi_2$ ($k_2\neq0$).
