# TTT-MAE — Test-Time Training with Masked Autoencoders

| 项目 | 内容 |
|------|------|
| **作者** | Yossi Gandelsman, Yu Sun, Xinlei Chen, Alexei A. Efros |
| **发表** | NeurIPS 2022 |
| **链接** | [arXiv 2209.07522](https://arxiv.org/abs/2209.07522) |

---

## 动机
为ViT设计合适的TTT方法。MAE重建是ViT时代最成功的自监督方法，天然适合作为TTT辅助任务。

## 核心贡献
1. 将**MAE重建**作为TTT的自监督任务
2. 在损坏基准上大幅超越之前的TTT方法
3. MAE重建比旋转预测和对比学习更适合TTT

## 方法详解
- 训练：联合训练分类目标和MAE重建目标（遮掩75% patches → 重建）
- 测试：对测试样本随机遮掩多次，用MAE重建损失更新编码器

## 实验结果
- ImageNet-C上ViT-Large错误率从37.8%降到28.4%（相对提升25%）

## 局限性
1. MAE重建计算量大
2. 仅适用于ViT架构
3. 需要训练时引入MAE分支

[← 返回目录](README.md)
