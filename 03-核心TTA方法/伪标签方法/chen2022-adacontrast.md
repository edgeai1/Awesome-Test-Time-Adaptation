# AdaContrast — Contrastive Test-Time Adaptation

| 项目 | 内容 |
|------|------|
| **作者** | Dian Chen, Dequan Wang, Trevor Darrell, Sayna Ebrahimi |
| **发表** | CVPR 2022 |
| **链接** | [arXiv 2204.10377](https://arxiv.org/abs/2204.10377) |

---

## 动机
用**对比学习**改善伪标签质量，用**最近邻投票**平滑伪标签噪声。

## 核心贡献
1. 将对比学习引入TTA
2. 最近邻投票机制精炼伪标签
3. 多样性正则化防止类别崩溃

## 方法详解
- 维护特征memory bank，对新样本计算对比损失
- 查找K个最近邻的预测做多数投票作为伪标签

## 实验结果
- VisDA-C上达85.3%准确率，比SHOT高约3%

## 局限性
1. Memory bank需要额外存储
2. 近邻搜索在大规模数据上开销大

[← 返回目录](../README.md)
