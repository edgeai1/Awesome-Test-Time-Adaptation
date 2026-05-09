# LAME — Parameter-Free Online Test-Time Adaptation

| 项目 | 内容 |
|------|------|
| **作者** | Malik Boudiaf, Romain Mueller, Ismail Ben Ayed, Luca Bertinetto |
| **发表** | CVPR 2022 |
| **链接** | [arXiv 2201.05718](https://arxiv.org/abs/2201.05718) |

---

## 动机
质疑"更新模型参数"的必要性。不如**不更新参数，直接修正模型输出**。

## 核心贡献
1. **完全无参数更新**的TTA方法
2. 拉普拉斯调整最大似然估计直接修正输出logits
3. **永远不会比不适应更差**（无崩溃风险）

## 方法详解
- 构建测试batch中所有样本的特征相似性图（Laplacian图）
- 通过标签传播平滑和修正预测
- 不进行任何梯度计算

## 实验结果
- batch≥64时性能与Tent相当，batch=1时远优于Tent

## 局限性
1. 依赖批次中样本多样性
2. 适应能力上限受原始模型特征质量限制

[← 返回目录](../README.md)
