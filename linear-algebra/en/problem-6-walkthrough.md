# Problem 6: Detailed Solution

## 1. Elementary row operations

Apply elementary row operations to the matrix $A$, first eliminating the entries below the pivot in column 1:

Row operations: $R_2 \leftarrow R_2 - 3R_1, \quad R_4 \leftarrow R_4 - 5R_1$

$$
A=\begin{pmatrix}1&1&1&1&1\\3&2&1&-3&a\\0&1&2&6&3\\5&4&3&-1&b\end{pmatrix}
\longrightarrow
\begin{pmatrix}1&1&1&1&1\\0&-1&-2&-6&a-3\\0&1&2&6&3\\0&-1&-2&-6&b-5\end{pmatrix}
$$

Then add row 3 to row 2 and to row 4 respectively, eliminating the nonzero entries of those rows:

Row operations: $R_2 \leftarrow R_2 + R_3, \quad R_4 \leftarrow R_4 + R_3$

$$
\longrightarrow
\begin{pmatrix}1&1&1&1&1\\0&0&0&0&a\\0&1&2&6&3\\0&0&0&0&b-2\end{pmatrix}
$$

Swap rows 2 and 3, and arrange into standard row echelon form:

Row operation: $R_2 \leftrightarrow R_3$

$$
\longrightarrow
\begin{pmatrix}1&1&1&1&1\\0&1&2&6&3\\0&0&0&0&a\\0&0&0&0&b-2\end{pmatrix}
$$

## 2. Determine the parameters $a, b$

The rank of the matrix is given as 2, and rows 1 and 2 are linearly independent, already forming the basis of rank 2.

For the matrix as a whole to have rank 2, rows 3 and 4 must be all-zero rows, so the constant terms at the end of these rows must be 0:

- Row 3: $a = 0$
- Row 4: $b - 2 = 0 \implies b = 2$

Final parameter values: $\boldsymbol{a=0,\ b=2}$

## 3. Find the maximal linearly independent subset of the set of column vectors

Substituting $a=0,\ b=2$, further reduce the row echelon form to reduced row echelon form:

Row operation: $R_1 \leftarrow R_1 - R_2$

$$
\longrightarrow
\begin{pmatrix}1&0&-1&-5&-2\\0&1&2&6&3\\0&0&0&0&0\\0&0&0&0&0\end{pmatrix}
$$

The pivots (leading nonzero entries) lie in columns 1 and 2, so **columns 1 and 2** (denoted $\boldsymbol{\alpha}_1, \boldsymbol{\alpha}_2$) form a maximal linearly independent subset of the set of column vectors.

## 4. Express the remaining vectors in terms of the maximal linearly independent subset

Reading the coefficients of the corresponding columns directly from the reduced row echelon matrix gives the linear expressions:

- Column 3: $\boldsymbol{\alpha}_3 = -\boldsymbol{\alpha}_1 + 2\boldsymbol{\alpha}_2$
- Column 4: $\boldsymbol{\alpha}_4 = -5\boldsymbol{\alpha}_1 + 6\boldsymbol{\alpha}_2$
- Column 5: $\boldsymbol{\alpha}_5 = -2\boldsymbol{\alpha}_1 + 3\boldsymbol{\alpha}_2$
