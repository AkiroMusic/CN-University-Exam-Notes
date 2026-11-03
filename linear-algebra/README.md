# Linear Algebra Solutions

This project collects and organizes detailed solutions to classic linear algebra exercises. It aims to help learners consolidate core knowledge points such as matrix theory, linear spaces, and eigenvalues through step-by-step breakdowns and logical analysis.

## Project Introduction
This repository contains solutions to common linear algebra problem types, covering the following core areas:
* Determinants
* Vector Spaces & Linear Independence
* Matrix Operations & Invertibility
* Linear Equations
* Eigenvalues & Eigenvectors

## Solution Preview
### Example: Problem 2 - Vector Outer Product Operation
Given $\alpha = [1, 2, 1]^T$, compute $(\alpha\alpha^T)^{100}$:
1. **Basic transformation**: Using associativity, $\alpha\alpha^T\alpha = \alpha(\alpha^T\alpha) = 6\alpha$.
2. **Power operation induction**: Let $B = \alpha\alpha^T$, then $B^2 = (\alpha\alpha^T)(\alpha\alpha^T) = \alpha(\alpha^T\alpha)\alpha^T = 6B$.
3. **Final conclusion**: $B^n = 6^{n-1}B$, i.e.:
   $(\alpha\alpha^T)^{100} = 6^{99}\begin{pmatrix}1&2&1\\ 2&4&2\\ 1&2&1\end{pmatrix}$

## Content Contribution
The solutions have been organized as follows:
- [x] Problem 1: $n$-order determinant calculation
- [x] Problem 2: Vector and its inner product, outer product operations
- [x] Problem 3: Proof of matrix invertibility
- [x] Problem 4: Classification discussion of linear equations
- [x] Problem 5: Proof of linear independence of vector sets
- [x] Problem 6: Matrix rank and maximal independent group
- [x] Problem 7: Eigenvalue and eigenvector calculation

## Study Suggestions
* This project is written in Markdown and supports MathJax/KaTeX rendering. For local reading, it is recommended to use the VS Code plugin "Markdown All in One".
* The solutions are for reference only; mathematics learning emphasizes logical derivation rather than memorizing conclusions. It is advisable to think independently first before consulting the steps.

## License
This project is open-sourced under the [MIT License](LICENSE).

---

# Linear Algebra Solutions (线性代数习题集解析)

本项目收集并整理了线性代数相关经典习题的详细解析。旨在通过步骤拆解和逻辑分析，帮助学习者巩固矩阵论、线性空间及特征值等核心知识点。

## 项目简介
本库包含对线性代数常见题型的解答，涵盖以下核心领域：
* 行列式计算 (Determinants)
* 向量空间与线性相关性 (Vector Spaces & Linear Independence)
* 矩阵运算与可逆性 (Matrix Operations)
* 线性方程组求解 (Linear Equations)
* 特征值与特征向量 (Eigenvalues & Eigenvectors)

## 解析预览
### 示例：第2题 - 向量外积运算
给定 $\alpha = [1, 2, 1]^T$，计算 $(\alpha\alpha^T)^{100}$：
1. **基础转换**：利用结合律，有 $\alpha\alpha^T\alpha = \alpha(\alpha^T\alpha) = 6\alpha$。
2. **幂运算归纳**：设 $B = \alpha\alpha^T$，则 $B^2 = (\alpha\alpha^T)(\alpha\alpha^T) = \alpha(\alpha^T\alpha)\alpha^T = 6B$。
3. **最终结论**：$B^n = 6^{n-1}B$，即：
   $$(\alpha\alpha^T)^{100} = 6^{99}\begin{pmatrix}1&2&1\\ 2&4&2\\ 1&2&1\end{pmatrix}$$

## 内容贡献
目前解析内容已整理如下：
- [x] 第1题：$n$ 阶行列式计算
- [x] 第2题：向量及其内积、外积运算
- [x] 第3题：矩阵可逆性证明
- [x] 第4题：线性方程组分类讨论
- [x] 第5题：向量组线性无关证明
- [x] 第6题：矩阵秩与最大无关组
- [x] 第7题：特征值与特征向量计算

## 学习建议
* 本项目采用 Markdown 编写，支持 MathJax/KaTeX 渲染。若在本地阅读，推荐使用 VS Code 插件 "Markdown All in One"。
* 解析过程仅供参考，数学学习重在逻辑推导而非记忆结论。建议先尝试独立思考，再参考步骤。

## 协议
本项目基于 [MIT License](LICENSE) 开源。
