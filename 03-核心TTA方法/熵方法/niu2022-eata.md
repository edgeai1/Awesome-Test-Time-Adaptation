# EATA — Efficient Test-Time Model Adaptation without Forgetting

| 项目 | 内容 |
|------|------|
| **作者** | Shuaicheng Niu, Jiaxiang Wu, Yifan Zhang, Yaofo Chen, Shijian Zheng, Peilin Zhao, Mingkui Tan |
| **发表** | ICML 2022 |
| **链接** | [arXiv 2204.02610](https://arxiv.org/abs/2204.02610) |
| **代码** | [GitHub](https://github.com/mr-eggplant/EATA) |

---

## 研究背景
Tent对所有测试样本无差别地进行熵最小化，导致两个问题：(1) 高熵噪声样本引入有害梯度；(2) 持续更新导致模型遗忘源域知识。

## 动机 (Motivation)
让TTA既**高效**（只适应可靠样本）又**抗遗忘**（约束参数不偏离源模型太远）。

## 核心贡献
1. 提出**样本感知熵过滤**：只选择低熵可靠样本进行适应
2. 引入**Fisher信息矩阵抗遗忘正则化**：约束重要参数的更新幅度

## 方法详解
- **可靠样本选择**：设定熵阈值 E₀（根据均匀分布的熵自适应设定），仅对 H(x) < E₀ 的样本执行适应
- **Fisher正则化**：L = L_ent(x) + λ Σᵢ Fᵢ(θᵢ - θᵢˢʳᶜ)²，其中 Fᵢ 是Fisher信息矩阵对角项，衡量参数对源域任务的重要性
- 被过滤掉的样本不做反向传播，减少计算量

## 实验设置
- **数据集**：CIFAR-10/100-C、ImageNet-C
- **骨干网络**：ResNet-50、WideResNet-28

## 实验结果
- ImageNet-C上比Tent降低约4%错误率
- 持续适应场景下Tent在100轮后崩溃，EATA保持稳定
- 通过样本过滤减少约20-40%的反向传播次数

## 局限性与不足
1. 熵阈值虽自适应但仍是启发式的
2. Fisher信息矩阵计算需要源域数据或预存统计量
3. 极端分布偏移下大部分样本被过滤，适应信号不足

[← 返回目录](../README.md)
