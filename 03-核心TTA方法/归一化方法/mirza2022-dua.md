# DUA — Dynamic Unsupervised Domain Adaptation by Normalization

| 项目 | 内容 |
|------|------|
| **作者** | Muhammad Jehanzeb Mirza et al. |
| **发表** | CVPR 2022 |
| **链接** | [GitHub](https://github.com/jmiemirza/DUA) |

---

## 动机
如何在**极少量**（<1%）目标域数据到达时就完成BN统计量的在线适应。

## 核心贡献
1. 动态BN统计量更新策略：用EMA逐步更新
2. 仅需<1%目标数据即可实现有效适应
3. **不需要任何反向传播**

## 方法详解
- 用衰减因子α混合训练和测试统计量：μ_new = (1-α)μ_train + αμ_test
- α动态衰减，避免后续噪声影响

## 实验结果
- 仅约100个测试样本即可接近使用全部测试集的AdaptiveBN性能
- 推理速度与标准推理相同

## 局限性
1. 适应能力上限较低（只适应统计量不适应参数）
2. 不适用于无BN架构

[← 返回目录](../README.md)
