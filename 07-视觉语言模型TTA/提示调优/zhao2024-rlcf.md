# RLCF — Test-Time Adaptation with CLIP Reward

| 项目 | 内容 |
|------|------|
| **作者** | Shuai Zhao et al. |
| **发表** | ICLR 2024 |
| **链接** | [arXiv 2305.18010](https://arxiv.org/abs/2305.18010) |

---

## 动机
CLIP的图文匹配分数本身就是天然的**奖励信号**。

## 核心贡献
1. 用CLIP作为**奖励模型**进行TTA
2. 不需要增强-过滤的复杂流程

## 实验结果
- 多个数据集上比TPT高1-3%

## 局限性
1. 依赖CLIP自身质量

[← 返回目录](../README.md)
