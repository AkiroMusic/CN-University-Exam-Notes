# Linear Algebra Exam Answers (Concise Exam-Room Version)

## 1. Compute the determinant

$$
D_n=\begin{vmatrix}a_1+\lambda&a_2&\cdots&a_n\\a_1&a_2+\lambda&\cdots&a_n\\\vdots&\vdots&&\vdots\\a_1&a_2&\cdots&a_n+\lambda\end{vmatrix}
$$

**Solution:**

Add columns $2,3,\ldots,n$ all to column 1 and factor out the common factor $\lambda+\sum\limits_{i=1}^{n}a_i$:

$$
D_n=\biggl(\lambda+\sum_{i=1}^{n}a_i\biggr)
\begin{vmatrix}1&a_2&\cdots&a_n\\1&a_2+\lambda&\cdots&a_n\\\vdots&\vdots&&\vdots\\1&a_2&\cdots&a_n+\lambda\end{vmatrix}
$$

Subtract row 1 from row $i$ ($i=2,\ldots,n$), reducing to upper triangular form:

$$
D_n=\biggl(\lambda+\sum_{i=1}^{n}a_i\biggr)
\begin{vmatrix}1&a_2&\cdots&a_n\\0&\lambda&\cdots&0\\\vdots&\vdots&&\vdots\\0&0&\cdots&\lambda\end{vmatrix}
$$

$$\boldsymbol{D_n=\lambda^{n-1}(\lambda+a_1+a_2+\cdots+a_n)}$$

## 2. Vector operations

Given $\boldsymbol{\alpha}=\begin{pmatrix}1\\2\\1\end{pmatrix}$

**Solution:**

$$\text{1. }\alpha^T\alpha=\begin{pmatrix}1&2&1\end{pmatrix}\begin{pmatrix}1\\2\\1\end{pmatrix}=1+4+1=\mathbf{6}$$

$$\text{2. }\alpha\alpha^T=\begin{pmatrix}1\\2\\1\end{pmatrix}\begin{pmatrix}1&2&1\end{pmatrix}=\begin{pmatrix}1&2&1\\2&4&2\\1&2&1\end{pmatrix}$$

$$\text{3. By the associative law: }\alpha\alpha^T\alpha=\alpha(\alpha^T\alpha)=6\alpha=\begin{pmatrix}6\\12\\6\end{pmatrix}$$

## 3. Prove that $A-E$ is invertible and find its inverse

Given $A^2-5A+E=0$

**Proof:**

From $A^2-5A+E=0$, rearranging gives:

$$A^2-A-4A+4E=3E$$

$$(A-E)(A-4E)=3E$$

i.e.

$$(A-E)\cdot\frac{1}{3}(A-4E)=E$$

By the definition of invertibility, $A-E$ is invertible, and

$$\boldsymbol{(A-E)^{-1}=\frac{1}{3}(A-4E)}$$

## 4. Discussion of the solutions of the system of linear equations

$$\begin{cases}ax_1+x_2+x_3=0\\x_1+ax_2+x_3=2\\x_1+x_2+ax_3=a\end{cases}$$

**Solution:**

The determinant of the coefficient matrix

$$|A|=\begin{vmatrix}a&1&1\\1&a&1\\1&1&a\end{vmatrix}=(a+2)(a-1)^2$$

(1) **Unique solution**: when $|A|\neq0$, i.e. $\boldsymbol{a\neq1}$ and $\boldsymbol{a\neq-2}$, the system has a unique solution.

(2) **No solution**: when $a=1$, the augmented matrix

$$\overline{A}=\begin{pmatrix}1&1&1&0\\1&1&1&2\\1&1&1&1\end{pmatrix}\rightarrow\begin{pmatrix}1&1&1&0\\0&0&0&2\\0&0&0&1\end{pmatrix}$$

$r(A)=1\neq r(\overline{A})=2$, so there is no solution when $\boldsymbol{a=1}$.

(3) **Infinitely many solutions**: when $a=-2$,

$$\overline{A}=\begin{pmatrix}-2&1&1&0\\1&-2&1&2\\1&1&-2&-2\end{pmatrix}\rightarrow\begin{pmatrix}1&-2&1&2\\0&-3&3&4\\0&0&0&0\end{pmatrix}$$

$r(A)=r(\overline{A})=2<3$, so there are infinitely many solutions.

The equivalent system:

$$\begin{cases}x_1-2x_2+x_3=2\\-3x_2+3x_3=4\end{cases}$$

Let the free variable be $x_3=c$; solving gives $x_2=c-\frac{4}{3}$ and $x_1=c-\frac{2}{3}$.

The general solution:

$$\begin{pmatrix}x_1\\x_2\\x_3\end{pmatrix}=\boldsymbol{c}\begin{pmatrix}1\\1\\1\end{pmatrix}+\begin{pmatrix}-\dfrac{2}{3}\\[4pt]\dfrac{4}{3}\\[4pt]0\end{pmatrix}\quad(\boldsymbol{c}\in\mathbb{R})$$

## 5. Prove that $\beta_1,\beta_2,\beta_3$ are linearly independent

Given that $\alpha_1,\alpha_2,\alpha_3$ are linearly independent, and $\beta_1=\alpha_1+\alpha_2$, $\beta_2=\alpha_2+\alpha_3$, $\beta_3=\alpha_3+\alpha_1$

**Proof:**

Set $k_1\beta_1+k_2\beta_2+k_3\beta_3=0$; substituting gives:

$$(k_1+k_3)\alpha_1+(k_1+k_2)\alpha_2+(k_2+k_3)\alpha_3=0$$

Since $\alpha_1,\alpha_2,\alpha_3$ are linearly independent,

$$\begin{cases}k_1+k_3=0\\k_1+k_2=0\\k_2+k_3=0\end{cases}$$

The determinant of the coefficients

$$\begin{vmatrix}1&0&1\\1&1&0\\0&1&1\end{vmatrix}=2\neq0$$

The system has only the zero solution $k_1=k_2=k_3=0$, so $\beta_1,\beta_2,\beta_3$ are linearly independent.

## 6. Determine the parameters and find the maximal linearly independent subset

$$A=\begin{pmatrix}1&1&1&1&1\\3&2&1&-3&a\\0&1&2&6&3\\5&4&3&-1&b\end{pmatrix}$$

**Solution:**

Apply elementary row operations to $A$:

$$A\rightarrow\begin{pmatrix}1&1&1&1&1\\0&-1&-2&-6&a-3\\0&0&0&0&a\\0&0&0&0&b-a-2\end{pmatrix}$$

From $r(A)=2$ we get $\begin{cases}a=0\\b-a-2=0\end{cases}$, i.e. $\boldsymbol{a=0,\ b=2}$.

The reduced row echelon form is then:

$$A\rightarrow\begin{pmatrix}1&0&-1&-5&-2\\0&1&2&6&3\\0&0&0&0&0\\0&0&0&0&0\end{pmatrix}$$

- A maximal linearly independent subset of the set of column vectors: $\boldsymbol{\alpha_1,\alpha_2}$
- Linear expressions of the remaining vectors:

$$\boldsymbol{\alpha_3}=-\boldsymbol{\alpha_1}+2\boldsymbol{\alpha_2},\quad \boldsymbol{\alpha_4}=-5\boldsymbol{\alpha_1}+6\boldsymbol{\alpha_2},\quad \boldsymbol{\alpha_5}=-2\boldsymbol{\alpha_1}+3\boldsymbol{\alpha_2}$$

## 7. Find the eigenvalues and eigenvectors

**(1)** $A=\begin{pmatrix}1&1&0\\1&1&0\\0&0&1\end{pmatrix}$

**Solution:**

The characteristic equation:

$$|\lambda E-A|=\begin{vmatrix}\lambda-1&-1&0\\-1&\lambda-1&0\\0&0&\lambda-1\end{vmatrix}=\lambda(\lambda-1)(\lambda-2)=0$$

The eigenvalues are $\boldsymbol{\lambda_1=0,\ \lambda_2=1,\ \lambda_3=2}$.

- $\lambda_1=0$: solve $-A\boldsymbol{x}=0$; the fundamental system of solutions is $\boldsymbol{\xi_1}=\begin{pmatrix}-1\\1\\0\end{pmatrix}$, and the eigenvectors are $k_1\xi_1$ $(k_1\neq0)$.
- $\lambda_2=1$: solve $(E-A)\boldsymbol{x}=0$; the fundamental system of solutions is $\boldsymbol{\xi_2}=\begin{pmatrix}0\\0\\1\end{pmatrix}$, and the eigenvectors are $k_2\xi_2$ $(k_2\neq0)$.
- $\lambda_3=2$: solve $(2E-A)\boldsymbol{x}=0$; the fundamental system of solutions is $\boldsymbol{\xi_3}=\begin{pmatrix}1\\1\\0\end{pmatrix}$, and the eigenvectors are $k_3\xi_3$ $(k_3\neq0)$.

**(2)** $A=\begin{pmatrix}1&1\\1&1\end{pmatrix}$

**Solution:**

The characteristic equation:

$$|\lambda E-A|=\begin{vmatrix}\lambda-1&-1\\-1&\lambda-1\end{vmatrix}=\lambda(\lambda-2)=0$$

The eigenvalues are $\boldsymbol{\lambda_1=0,\ \lambda_2=2}$.

- $\lambda_1=0$: solve $-A\boldsymbol{x}=0$; the fundamental system of solutions is $\boldsymbol{\xi_1}=\begin{pmatrix}-1\\1\end{pmatrix}$, and the eigenvectors are $k_1\xi_1$ $(k_1\neq0)$.
- $\lambda_2=2$: solve $(2E-A)\boldsymbol{x}=0$; the fundamental system of solutions is $\boldsymbol{\xi_2}=\begin{pmatrix}1\\1\end{pmatrix}$, and the eigenvectors are $k_2\xi_2$ $(k_2\neq0)$.
