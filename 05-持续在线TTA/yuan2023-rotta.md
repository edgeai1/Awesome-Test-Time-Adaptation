# RoTTA — Robust Test-Time Adaptation in Dynamic Scenarios

| 项目 | 内容 |
|------|------|
| **作者** | Longhui Yuan, Binhui Xie, Shuang Li |
| **发表** | CVPR 2023 |
| **链接** | [arXiv 2303.13899](https://arxiv.org/abs/2303.13899) |
| **代码** | [GitHub](https://github.com/BIT-DA/RoTTA) |

---

## 动机
综合解决持续TTA的三重挑战：(1) BN统计量不稳定；(2) 类别分布不均衡；(3) 测试数据时效性。

## 核心贡献
1. **鲁棒BN**：修正BN统计量估计
2. **类别平衡Memory**：保持类别平衡
3. **时间感知重加权**：近期样本权重更高
4. 师生模型框架增强稳定性

## 实验结果
- 三种挑战同时存在时比CoTTA高5%，比NOTE高3%

## 局限性
1. 三个组件各有超参数，调参复杂
2. 时间衰减策略假设域线性变化

[← 返回目录](README.md)
