# BATCLIP — Bimodal Online Test-Time Adaptation for CLIP

| 项目 | 内容 |
|------|------|
| **作者** | Sarthak Kumar Maharana et al. |
| **发表** | ICCV 2025 |
| **链接** | [arXiv 2412.02837](https://arxiv.org/abs/2412.02837) |

---

## 动机
现有TTA方法因单模态特性在适配CLIP时存在局限。BATCLIP提出**双模态在线TTA**，同时调整视觉和文本编码器。

## 核心贡献
1. 同时调整视觉和文本编码器的LayerNorm参数
2. 最大化类原型与文本特征的对齐，增强类原型可分离性
3. 在图像腐蚀和域泛化基准上取得在线TTA最优性能

## 局限性
1. 同时更新两个编码器增加不稳定性风险

[← 返回目录](../README.md)
