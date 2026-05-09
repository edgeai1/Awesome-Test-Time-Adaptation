# IMSE — Intrinsic Mixture of Spectral Experts Fine-tuning for TTA

| 项目 | 内容 |
|------|------|
| **作者** | Sunghyun Baek et al. |
| **发表** | ICLR 2026 |
| **链接** | [arXiv 2603.07926](https://arxiv.org/abs/2603.07926) |

---

## 动机
利用ViT中内在嵌入的频谱专家，通过SVD分解实现参数高效适应。

## 核心贡献
1. 将每个线性层分解为秩-1频谱专家，仅适应奇异值
2. 基于专家-输入对齐的多样性最大化损失
3. 域感知频谱代码检索机制

[← 返回目录](README.md)
