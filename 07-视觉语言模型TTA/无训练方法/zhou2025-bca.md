# BCA — Bayesian Test-Time Adaptation for Vision-Language Models

| 项目 | 内容 |
|------|------|
| **作者** | Zhou et al. |
| **发表** | CVPR 2025 |
| **链接** | [arXiv 2503.09248](https://arxiv.org/abs/2503.09248) |

---

## 动机
从贝叶斯视角看TTA：分类概率 = 似然 × 先验。现有方法大多只优化似然。

## 核心贡献
1. 同时更新类别嵌入（似然）和类别先验概率
2. 长序列测试中更稳定

## 实验结果
- 长序列（10000+样本）测试中比TPT稳定约5%

## 局限性
1. 先验更新依赖样本顺序

[← 返回目录](../README.md)
