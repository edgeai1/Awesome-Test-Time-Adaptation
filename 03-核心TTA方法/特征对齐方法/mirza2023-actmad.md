# ActMAD — Activation Matching to Align Distributions for TTT

| 项目 | 内容 |
|------|------|
| **作者** | Muhammad Jehanzeb Mirza et al. |
| **发表** | CVPR 2023 |
| **链接** | [arXiv 2211.12870](https://arxiv.org/abs/2211.12870) |

---

## 动机
BN适应方法只对齐第一层统计量，但不同层的激活分布偏移可能各不相同。需要在**多个层**上对齐。

## 核心贡献
1. 跨多层的激活统计量匹配策略
2. 存储源域各层的激活统计量
3. 测试时优化模型使测试激活对齐到源域

## 方法详解
- 训练时记录各层激活分布（均值μ和方差σ²）
- 测试时优化：L = Σ_l (‖μ_l^test - μ_l^src‖² + ‖σ_l^test - σ_l^src‖²)

## 实验结果
- ImageNet-C上比Tent提升约3-5%

## 局限性
1. 需要预存源域统计量
2. 统计量对齐假设源域和目标域结构相似

[← 返回目录](../README.md)
