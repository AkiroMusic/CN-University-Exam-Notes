# Data Structure Final Review Notes (Modern C++ Refactored)

## Project Overview

This repository contains two complete final exam review handouts for college Data Structure courses, fully refactored with modern C++ standards. All core algorithms, theoretical formulas, and exam high-frequency test points are sorted systematically for undergraduate midterm & final review.

### Documents

1. **Volume 1**: Full version of core review handout (Modern C++ Refactored Edition)
2. **Volume 2**: Extended volume with extra exercises, multiple-choice summaries & detailed problem-solving walkthroughs

All raw C-style `malloc/free`, outdated macro definitions and misspelled variables are removed; standard `new/delete` object-oriented C++ implementations are adopted, compliant with C++11 and above.

## Key Content Coverage

### 1. Fundamental Concepts & Algorithm Complexity

- Definition hierarchy: Data / Data Element / Data Object / Data Structure
- Logical structures: Set / Linear / Tree / Graph
- Physical storage: Sequential / Linked / Index / Hash
- Algorithm 5 core characteristics & evaluation criteria
- Time & space complexity ranking, Big-O notation rules

### 2. Linear Tables

- Sequence table: Random access, element movement calculation, memory addressing
- Singly linked list (with/without head node): Empty judgment, insertion & deletion
- Doubly linked list core logic
- Array & sparse matrix compression: Triple table, Orthogonal Linked List

### 3. Stack & Queue

- LIFO stack & FIFO queue core properties
- Sequence stack, linked stack implementation
- Circular queue false overflow solution
- Linked queue with head node encapsulation

### 4. String, Generalized List

### 5. Tree & Binary Tree

- Binary tree mathematical properties (leaf formula n0 = n2 + 1)
- Pre-order / In-order / Post-order traversal
- Huffman Tree & Huffman coding, WPL calculation

### 6. Graph Theory

- Adjacency matrix & adjacency list comparison
- DFS / BFS traversal
- MST: Prim (dense) & Kruskal (sparse)
- Shortest path: Dijkstra (single source) & Floyd (all pairs)

### 7. Search Algorithms

- Binary search, BST, AVL balanced tree rotation (LL/RR/LR/RL)
- Average Search Length (ASL) calculation

### 8. Internal Sorting

- Complete comparison table of all sorting algorithms
- Direct Insertion / Shell / Bubble / Quick / Selection / Heap / Merge Sort

## Repository Features

1. **Exam-Oriented Summary** — highlights common mistakes
2. **Standard Modern C++ Code**
3. **Clear Formula & Derivation**
4. **Distinction of Textbook & Modern Standard**
5. **Clear Error Correction**

## Usage Guide

### For Students

- Personal review, print or split chapters for targeted recitation
- All code snippets can be copied for homework and algorithm practice
- Highlighted exam pitfalls help avoid common mistakes

### For Contributors

- Free for personal learning & classroom auxiliary teaching
- Commercial use, secondary packaging and unauthorized reprint are prohibited

## Language Note

When handwriting code on paper exams, professors generally accept raw pointers and reference `&`; avoid `std::shared_ptr` / `auto` which may be judged incorrect.

## License

© Akiro. Personal learning use only. No commercial redistribution without authorization.

---

# 数据结构期末复习笔记（Modern C++ 重构版）

## 项目概述

本仓库包含两份完整的高校数据结构期末复习讲义，使用 Modern C++ 标准全面重构。所有核心算法、理论公式和考试高频考点均经过系统整理，适用于本科期中期末复习。

### 文档列表

1. **卷一**：核心复习讲义完整版（Modern C++ 重构版）
2. **卷二**：扩展卷，含练习题、选择题总结和详细解题思路

所有 C 风格的 `malloc/free`、过时的宏定义和拼写错误的变量均已被移除；所有代码示例均采用标准的 `new/delete` 面向对象 C++ 实现，兼容 C++11 及以上标准。

## 核心内容

### 1. 基础概念与算法复杂度

- 定义层次：数据 / 数据元素 / 数据对象 / 数据结构
- 逻辑结构：集合 / 线性 / 树形 / 图状
- 物理存储：顺序 / 链式 / 索引 / 散列
- 算法五大核心特性与评价标准
- 时间与空间复杂度排序、大 O 记法规则

### 2. 线性表

- 顺序表：随机存取、元素移动次数计算、内存寻址
- 单链表（带头结点 / 不带头结点）：判空、插入与删除
- 双向链表核心逻辑
- 数组与稀疏矩阵压缩：三元组、十字链表

### 3. 栈与队列

- 后进先出栈与先进先出队列的核心性质
- 顺序栈、链栈实现
- 循环队列假溢出问题的解决
- 带头结点的链式队列封装

### 4. 串与广义表

### 5. 树与二叉树

- 二叉树数学性质（叶子公式 n0 = n2 + 1）
- 先序 / 中序 / 后序遍历
- 哈夫曼树与哈夫曼编码、WPL 计算

### 6. 图论

- 邻接矩阵与邻接表对比
- DFS / BFS 遍历
- 最小生成树：Prim（稠密图）与 Kruskal（稀疏图）
- 最短路：Dijkstra（单源）与 Floyd（多源）

### 7. 查找算法

- 二分查找、二叉排序树、AVL 平衡树旋转（LL/RR/LR/RL）
- 平均查找长度（ASL）计算

### 8. 内部排序

- 全部排序算法完整对比表
- 直接插入 / 希尔 / 冒泡 / 快速 / 选择 / 堆 / 归并排序

## 仓库特点

1. **面向考试** — 标注易错点
2. **标准 Modern C++ 代码**
3. **清晰的公式与推导**
4. **区分教材经典写法与现代标准**
5. **明确的错误修正**

## 使用指南

### 对学生

- 个人复习，可打印或按章节拆分进行针对性背诵
- 所有代码片段可复制用于作业与算法练习
- 标注的考试易错点有助于避免常见错误

### 对贡献者

- 免费用于个人学习与课堂辅助教学
- 禁止商业使用、二次包装与未经授权转载

## 笔试语言说明

笔试手写代码时，老师一般接受原始指针和引用 `&`；应避免使用 `std::shared_ptr` / `auto`，可能被判为错误。

## 许可

© Akiro。仅限个人学习使用，未经授权禁止商业再分发。
