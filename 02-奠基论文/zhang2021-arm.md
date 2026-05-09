# ARM — Adaptive Risk Minimization: Learning to Adapt to Domain Shift

| 项目 | 内容 |
|------|------|
| **作者** | Marvin Zhang, Henrik Marklund, Nikita Dhawan, Abhishek Gupta, Sergey Levine, Chelsea Finn |
| **发表** | NeurIPS 2021 |
| **链接** | [arXiv 2007.02931](https://arxiv.org/abs/2007.02931) |

---

## 研究背景
传统ERM训练的模型在测试时是固定的，无法根据测试数据调整。TTT/Tent等方法在测试时做适应，但适应策略是手动设计的。

## 动机 (Motivation)
能否让模型**在训练阶段就学习如何在测试时进行适应**？类似于MAML——训练一个"擅长快速适应"的模型初始化。

## 核心贡献
1. 提出将测试时适应能力纳入训练目标的**自适应风险最小化**框架
2. 设计了基于上下文网络的适应机制
3. 适应能力是"学出来"的，不需要手动设计

## 方法详解
- **训练框架**：MAML式双层优化——外层优化模型初始化，内层模拟测试时适应
- **上下文网络**：接收小批次测试样本，生成上下文向量调制模型特征

## 实验设置
- **数据集**：CIFAR-10-C、FMoW、Camelyon17

## 实验结果
- 在FMoW和Camelyon17上超越ERM和域泛化方法
- 学出的适应策略比手动设计的Tent策略更有效

## 局限性与不足
1. 训练成本高（元学习双层优化）
2. 需要训练时已知域划分
3. 不适用于已有预训练模型

[← 返回目录](README.md)
