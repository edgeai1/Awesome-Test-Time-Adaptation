# AdaptiveBN — Improving Robustness against Common Corruptions by Covariate Shift Adaptation

| 项目 | 内容 |
|------|------|
| **作者** | Steffen Schneider, Evgenia Rusak, Luisa Eck, Oliver Bringmann, Wieland Brendel, Matthias Bethge |
| **发表** | NeurIPS 2020 |
| **链接** | [GitHub](https://github.com/bethgelab/robustness) |

---

## 研究背景
深度神经网络中的批归一化（BN）层在训练时会计算并存储训练数据的均值和方差统计量。推理时，这些固定的统计量被用来归一化特征。当测试数据的分布与训练数据不同时，这些统计量就会导致特征归一化不准确。

## 动机 (Motivation)
BN层的统计量本质上是对数据分布的"快照"。如果测试数据的分布偏移了，用训练分布的快照来归一化就不合理。最简单的想法：**用测试数据自己的统计量来替换**。

## 核心贡献
1. 揭示了BN统计量错配是模型对分布偏移敏感的关键原因
2. 提出极简方案：在测试时用目标域数据重新计算BN的均值和方差
3. 证明仅修改BN统计量（**无需任何梯度计算**）就能显著提升鲁棒性

## 方法详解
在测试时，将模型设为train模式让BN层重新计算当前批次测试数据的均值和方差。不修改任何可学习参数。

## 实验设置
- **数据集**：ImageNet-C（15种损坏 × 5级强度）
- **骨干网络**：多种ResNet变体、EfficientNet

## 实验结果
- 在ImageNet-C上平均减少约20-40%的错误率，且计算开销几乎为零

## 局限性与不足
1. 需要足够大的批次（通常≥32）
2. 批次内类别分布敏感
3. 不适应BN的仿射参数（γ和β）
4. 不适用于无BN的网络（如ViT）

[← 返回目录](README.md)
