# CLIPTTA — Robust Contrastive Vision-Language Test-Time Adaptation

| 项目 | 内容 |
|------|------|
| **作者** | Marc Lafon et al. |
| **发表** | NeurIPS 2025 |
| **链接** | [arXiv 2507.14312](https://arxiv.org/abs/2507.14312) |

---

## 动机
传统TTA的熵最小化目标与CLIP的对比预训练目标根本不匹配，导致伪标签漂移和类塌缩。

## 核心贡献
1. 用**软对比损失**替代熵最小化，与CLIP预训练目标对齐
2. 通过离群对比曝光(OCE)扩展到开放集OOD检测
3. 在75个数据集上持续优于基于熵的TTA方法

## 局限性
1. 对比损失需要正负样本对的构造

[← 返回目录](../README.md)
