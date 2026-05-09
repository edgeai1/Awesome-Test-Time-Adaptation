# SAR — Towards Stable Test-Time Adaptation in Dynamic Wild World

| 项目 | 内容 |
|------|------|
| **作者** | Shuaicheng Niu, Jiaxiang Wu, Yifan Zhang, Zhiquan Wen, Yaofo Chen, Peilin Zhao, Mingkui Tan |
| **发表** | ICLR 2023 (**Oral**) |
| **链接** | [arXiv 2302.12400](https://arxiv.org/abs/2302.12400) |
| **代码** | [GitHub](https://github.com/mr-eggplant/SAR) |

---

## 研究背景
现实世界的测试数据远比实验室复杂：偏移类型和强度持续变化、批次中可能包含不同分布样本、类别分布严重不均衡。Tent和EATA在这些"动态野外"场景中仍然不够稳定。

## 动机 (Motivation)
SAR发现不稳定的主要原因是**大梯度噪声样本**——这些样本的梯度范数很大但方向有害。通过在损失面的**平坦区域**优化（锐度感知），可以提高对噪声梯度的鲁棒性。

## 核心贡献
1. 系统定义现实TTA的挑战：混合偏移、小批次、类不平衡、持续适应
2. 提出**锐度感知熵最小化**（Sharpness-Aware Entropy Minimization）
3. 提出可靠样本过滤 + 模型恢复机制

## 方法详解
- **锐度感知最小化（SAM for TTA）**：先找邻域内熵最大的点（对抗扰动），然后在该方向上做梯度下降，使模型收敛到更平坦的区域
- **样本过滤**：移除梯度范数异常大的样本
- **模型恢复**：监控熵均值，检测到崩溃信号时恢复到最近稳定状态

## 实验设置
- **数据集**：ImageNet-C（标准和混合偏移）、自定义野外TTA基准
- **基线对比**：Tent、EATA、CoTTA、MEMO等11种方法

## 实验结果
- 混合偏移场景下比Tent低约10%错误率，比EATA低约5%
- 标准ImageNet-C上也取得SOTA
- batch=1时仍然稳定

## 局限性与不足
1. SAM优化需要两次前向+一次反向，计算成本是Tent的约2倍
2. 模型恢复机制的阈值需要调整
3. 对标签偏移类型没有明显优势

[← 返回目录](../README.md)
