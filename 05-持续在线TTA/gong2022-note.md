# NOTE — Robust Continual Test-time Adaptation Against Temporal Correlation

| 项目 | 内容 |
|------|------|
| **作者** | Taesik Gong et al. |
| **发表** | NeurIPS 2022 |
| **链接** | [GitHub](https://github.com/TaesikGong/NOTE) |

---

## 动机
测试数据往往有**时序相关性**（如自动驾驶连续帧同一场景）。当batch中都是同一类样本时，BN统计量严重偏向该类。

## 核心贡献
1. 首次解决**时序相关**测试数据流的TTA问题
2. 提出**实例感知BN（IABN）**：每个样本独立计算归一化统计量
3. **预测平衡Reservoir采样**：维护类别平衡的memory buffer

## 方法详解
- IABN：对每个样本独立计算均值/方差归一化（类似Instance Norm），但保留BN仿射参数
- Reservoir采样：固定大小buffer，保持类别平衡

## 实验结果
- 时序相关设置下Tent准确率降低20%以上，NOTE保持稳定
- i.i.d.设置下也与Tent相当

## 局限性
1. IABN增加约30%计算开销
2. 类别平衡采样依赖模型预测质量

[← 返回目录](README.md)
