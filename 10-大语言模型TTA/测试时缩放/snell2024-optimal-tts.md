# Scaling LLM Test-Time Compute Optimally

| 项目 | 内容 |
|------|------|
| **作者** | Charlie Snell, Jaehoon Lee, Kelvin Xu, Aviral Kumar |
| **发表** | NeurIPS 2024 |
| **链接** | [arXiv 2408.03314](https://arxiv.org/abs/2408.03314) |

---

## 动机
在固定模型大小的情况下，测试时投入更多计算能否超越增大模型的效果？

## 核心贡献
1. 提出**测试时计算的最优缩放**框架
2. 证明测试时缩放可比训练时缩放更高效
3. 提出"compute-optimal"测试时推理概念

## 关键结果
- 小模型(1B) + 最优测试时缩放 > 大模型(14B) + 标准推理

## 局限性
1. 需要高质量过程奖励模型
2. 最优分配需预知问题难度

[← 返回目录](../README.md)
