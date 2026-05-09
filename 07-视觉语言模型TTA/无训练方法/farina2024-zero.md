# ZERO — Frustratingly Easy Test-Time Adaptation of VLMs

| 项目 | 内容 |
|------|------|
| **作者** | Matteo Farina et al. |
| **发表** | NeurIPS 2024 |

---

## 动机
TPT的多步优化真的必要吗？极简方法就能达到接近效果。

## 核心贡献
1. 可能是**最简单的VLM TTA方法**
2. Augment → Select most confident → Marginalize at zero temperature
3. 比TPT快约10倍，内存高约13倍效率

## 实验结果
- 多数数据集上与TPT相当或略高

## 局限性
1. 仍需N次前向传播
2. 不更新模型，适应能力有上限

[← 返回目录](../README.md)
