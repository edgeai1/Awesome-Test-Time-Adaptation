# COME — Test-time Adaption by Conservatively Minimizing Entropy

| 项目 | 内容 |
|------|------|
| **作者** | Yanming Zhang et al. |
| **发表** | ICLR 2025 |
| **链接** | [arXiv 2410.10894](https://arxiv.org/abs/2410.10894) |

---

## 研究背景
标准熵最小化容易导致模型过度自信，最终崩溃到将所有样本分为少数几个类。

## 动机 (Motivation)
应该**保守地**最小化熵，避免过度适应。从贝叶斯视角引入Dirichlet先验来约束预测分布。

## 核心贡献
1. 将模型预测视为Dirichlet分布的参数
2. 提出**保守熵最小化**：Dirichlet先验约束防止预测分布坍缩
3. 有效解决TTA中的模式崩溃问题

## 方法详解
- 保守熵 = 标准熵 - Dirichlet正则项
- 正则项阻止预测概率过度集中到某一类
- 集中度参数自适应调整：偏移小时更激进，偏移大时更保守

## 实验设置
- **数据集**：CIFAR-10/100-C、ImageNet-C

## 实验结果
- ImageNet-C上比SAR进一步降低约1-2%错误率
- 崩溃测试中，Tent在第50轮崩溃，COME保持稳定到第200轮以上

## 局限性与不足
1. Dirichlet建模增加数学复杂度
2. 简单偏移场景下相比标准熵最小化优势不大

[← 返回目录](../README.md)
