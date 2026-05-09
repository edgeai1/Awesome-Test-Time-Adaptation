# ADAPT — Backpropagation-Free TTA via Probabilistic Gaussian Alignment

| 项目 | 内容 |
|------|------|
| **作者** | Youjia Zhang et al. |
| **发表** | NeurIPS 2025 |
| **链接** | [arXiv 2508.15568](https://arxiv.org/abs/2508.15568) |

---

## 动机
将TTA重新建模为高斯概率推断任务，实现无梯度、闭式推断。

## 核心贡献
1. 通过逐步更新的类均值和共享协方差建模类条件似然
2. 闭式、无训练推断，由CLIP先验和知识库引导
3. 无需源数据、无需梯度更新

## 实验结果
- 支持在线和转导设置，性能优异

[← 返回目录](../README.md)
