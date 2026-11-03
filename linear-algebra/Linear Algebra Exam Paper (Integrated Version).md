# 线性代数期末习题与详细解析

## 第 1 题：行列式计算

**题目**：计算 $n$ 阶行列式：

$$D_{n}=\begin{vmatrix}a_{1}+\lambda & a_{2} & \cdots & a_{n} \\ a_{1} & a_{2}+\lambda & \cdots & a_{n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{1} & a_{2} & \cdots & a_{n}+\lambda\end{vmatrix}$$

**解析**：

1.  **列变换**：将第 $2, 3, \dots, n$ 列全部加到第 1 列，第 1 列每个元素均变为 $\lambda + \sum_{i=1}^{n}a_{i}$ 。
    
2.  **提取公因子**：
    
    $$D_{n}=(\lambda+\sum_{i=1}^{n}a_{i})\begin{vmatrix}1 & a_{2} & \dots & a_{n} \\ 1 & a_{2}+\lambda & \dots & a_{n} \\ \vdots & \vdots & \ddots & \vdots \\ 1 & a_{2} & \dots & a_{n}+\lambda\end{vmatrix}$$
    
3.  **行变换**：第 $i$ 行 $(i=2, \dots, n)$ 减去第 1 行，化为上三角矩阵 。
    
4.  **计算结果**：主对角线元素相乘 ：
    
    $$D_{n}=\lambda^{n-1}(\lambda+a_{1}+a_{2}+\dots+a_{n})$$
    

## 第 2 题：向量运算

**题目**：设 $\alpha=\begin{pmatrix}1\\ 2\\ 1\end{pmatrix}$，求 $\alpha^{T}\alpha, \alpha\alpha^{T}, \alpha\alpha^{T}\alpha, (\alpha\alpha^{T})^{100}$ 。

**解析**：

1.  **标量积**：$\alpha^{T}\alpha = 1^2 + 2^2 + 1^2 = 6$ 。
    
2.  **矩阵积**：$\alpha\alpha^{T} = \begin{pmatrix}1\\ 2\\ 1\end{pmatrix}\begin{pmatrix}1 & 2 & 1\end{pmatrix} = \begin{pmatrix}1 & 2 & 1\\ 2 & 4 & 2\\ 1 & 2 & 1\end{pmatrix}$ 。
    
3.  **混合积**：利用结合律，$\alpha\alpha^{T}\alpha = \alpha(\alpha^{T}\alpha) = 6\alpha = \begin{pmatrix}6\\ 12\\ 6\end{pmatrix}$ 。
    
4.  **幂运算**：设 $B = \alpha\alpha^{T}$，则 $B^2 = 6B$，归纳得 $B^n = 6^{n-1}B$ 。
    
    $$(\alpha\alpha^{T})^{100} = 6^{99}\begin{pmatrix}1 & 2 & 1\\ 2 & 4 & 2\\ 1 & 2 & 1\end{pmatrix}$$
    

## 第 3 题：矩阵可逆性证明

**题目**：设 $A$ 为 $n$ 阶方阵，满足 $A^{2}-5A+E=0$，证明 $A-E$ 可逆，并求其逆 。

**解析**：

1.  对等式变形：$A^{2}-5A+E=0 \Rightarrow A^2-A-4A+4E=3E$ 。
    
2.  提取公因式：$(A-E)(A-4E)=3E$ 。
    
3.  得到：$(A-E) \cdot \frac{1}{3}(A-4E) = E$ 。
    
4.  由定义知 $A-E$ 可逆，且 $(A-E)^{-1} = \frac{1}{3}(A-4E)$ 。
    

## 第 4 题：线性方程组讨论

**题目**：讨论方程组 $\begin{cases}ax_{1}+x_{2}+x_{3}=0\\ x_{1}+ax_{2}+x_{3}=2\\ x_{1}+x_{2}+ax_{3}=a\end{cases}$ 的解 。

**解析**： 系数矩阵行列式 $|A| [cite_start]= (a+2)(a-1)^2$ 。

1.  **唯一解**：$a \neq 1$ 且 $a \neq -2$ 时，方程组有唯一解 。
    
2.  **无解**：$a=1$ 时，增广矩阵初等变换后 $r(A)=1 \neq r(\overline{A})=2$，无解 。
    
3.  **无穷多解**：$a=-2$ 时，同解方程组为 $\begin{cases}x_{1}-2x_{2}+x_{3}=2\\ -3x_{2}+3x_{3}=4\end{cases}$，取自由变量 $x_3=c$，通解为 $X=c\begin{pmatrix}1\\ 1\\ 1\end{pmatrix}+\begin{pmatrix}-2/3\\ -4/3\\ 0\end{pmatrix}$ 。
    

## 第 5 题：线性无关证明

**题目**：已知 $\alpha_{1}, \alpha_{2}, \alpha_{3}$ 线性无关，$\beta_{1}=\alpha_{1}+\alpha_{2}, \beta_{2}=\alpha_{2}+\alpha_{3}, \beta_{3}=\alpha_{3}+\alpha_{1}$，证明 $\beta_{1}, \beta_{2}, \beta_{3}$ 线性无关 。

**解析**：

1.  设 $k_1\beta_1+k_2\beta_2+k_3\beta_3=0$，整理得 $(k_1+k_3)\alpha_1 + (k_1+k_2)\alpha_2 + (k_2+k_3)\alpha_3=0$ 。
    
2.  由于 $\alpha_i$ 线性无关，系数矩阵行列式为 $\begin{vmatrix}1 & 0 & 1 \\ 1 & 1 & 0 \\ 0 & 1 & 1 \end{vmatrix} = 2 \neq 0$ 。
    
3.  方程组只有零解，故 $\beta_i$ 线性无关 。
    

## 第 6 题：参数确定与最大无关组

**题目**：$A=\begin{pmatrix}1 & 1 & 1 & 1 \\ 3 & 2 & 1 & -3 & a \\ 0 & 1 & 2 & 6 & 3 \\ 5 & 4 & 3 & -1 & b \end{pmatrix}$，秩为 2，求 $a, b$ 及最大无关组 。

**解析**：

1.  **行变换**：经初等行变换化为行阶梯形，第 3、4 行须为 0 。
    
2.  **求参**：解得 $a=0, b=2$ 。
    
3.  **最大无关组**：主元位于第 1、2 列，故 $\{\alpha_1, \alpha_2\}$ 为最大无关组 。
    
4.  **线性表示**：其余向量为 $\alpha_3=-\alpha_1+2\alpha_2, \alpha_4=-5\alpha_1+6\alpha_2, \alpha_5=-2\alpha_1+3\alpha_2$ 。
    

## 第 7 题：特征值与特征向量

**题目**：求 $A_1=\begin{pmatrix}1 & 1 & 0 \\ 1 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}$ 和 $A_2=\begin{pmatrix}1 & 1 \\ 1 & 1 \end{pmatrix}$ 的特征值与特征向量 。

**解析**：

1.  **$A_1$**：特征值为 $\lambda_1=0, \lambda_2=1, \lambda_3=2$ 。
    
    -   $\lambda_1=0 \to \xi_1=(-1, 1, 0)^T$
        
    -   $\lambda_2=1 \to \xi_2=(0, 0, 1)^T$
        
    -   $\lambda_3=2 \to \xi_3=(1, 1, 0)^T$
        
2.  **$A_2$**：特征值为 $\lambda_1=0, \lambda_2=2$ 。
    
    -   $\lambda_1=0 \to \xi_1=(-1, 1)^T$
        
    -   $\lambda_2=2 \to \xi_2=(1, 1)^T$
