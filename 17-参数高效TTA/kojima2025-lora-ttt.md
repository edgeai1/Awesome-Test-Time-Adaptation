# LoRA-TTT — Low-Rank Test-Time Training for Vision-Language Models

| 项目 | 内容 |
|------|------|
| **作者** | Yuto Kojima et al. |
| **发表** | arXiv 2025 |
| **链接** | [arXiv 2502.02069](https://arxiv.org/abs/2502.02069) |

---

## 动机
对VLM图像编码器应用低秩适应（LoRA）进行测试时训练，在参数高效的同时保持适应能力。

## 核心贡献
1. 仅更新LoRA参数进行测试时训练
2. 引入高效重建损失函数
3. 在15个数据集上平均提高CLIP零样本准确率5.79%

## 局限性
1. LoRA秩的选择影响性能

[← 返回目录](README.md)
