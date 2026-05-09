# DeYO — Entropy is not Enough for Test-Time Adaptation

| 项目 | 内容 |
|------|------|
| **作者** | Jonghyun Lee et al. |
| **发表** | ICLR 2024 (**Spotlight**) |
| **链接** | [GitHub](https://github.com/Jhyun17/DeYO) |

---

## 研究背景
现有TTA方法几乎全部依赖预测熵作为样本可靠性的唯一指标。

## 动机 (Motivation)
**低熵不等于正确**。有些样本虽然预测熵低（模型自信），但预测是错误的——模型的自信来自于对"捷径特征"（如背景纹理）的依赖，而非真正的物体语义特征。

## 核心贡献
1. 提出**PLPD**（Pseudo-Label Prediction Difference）指标：衡量模型预测对物体区域遮挡的敏感度
2. 结合熵和PLPD构建更可靠的样本选择标准
3. 证明了"熵不够"，需要语义层面的信号

## 方法详解
- 对输入图像进行patch遮挡，比较遮挡前后的预测变化
- PLPD高 = 预测依赖物体区域 = 可靠样本
- PLPD低 = 预测不依赖物体 = 不可靠样本
- 最终选择：低熵 AND 高PLPD的样本才进行适应

## 实验设置
- **数据集**：ImageNet-C/R、CIFAR-10/100-C

## 实验结果
- ImageNet-C上比SAR降低约2%错误率，比EATA降低约4%
- 噪声场景下优势更明显

## 局限性与不足
1. PLPD计算需要多次前向传播，增加约2-4倍计算量
2. 对全局图像级偏移（如色偏），PLPD区分能力有限

[← 返回目录](../README.md)
