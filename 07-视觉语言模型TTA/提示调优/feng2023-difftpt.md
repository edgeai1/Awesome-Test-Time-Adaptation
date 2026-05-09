# DiffTPT — Diverse Data Augmentation with Diffusions for Test-time Prompt Tuning

| 项目 | 内容 |
|------|------|
| **作者** | Chun-Mei Feng et al. |
| **发表** | ICCV 2023 |
| **链接** | [arXiv 2308.06038](https://arxiv.org/abs/2308.06038) |

---

## 动机
TPT使用标准增强多样性有限。用**扩散模型**生成更多样化的增强视图。

## 核心贡献
1. 扩散模型生成**语义一致但风格多样**的增强视图
2. 余弦相似度过滤语义偏离的增强

## 实验结果
- ImageNet-A上比TPT高约3%

## 局限性
1. 扩散模型推理极慢
2. 需要额外大型模型

[← 返回目录](../README.md)
