# 🔄 持续/在线测试时适应 (Continual / Online TTA)

> 处理持续变化的分布偏移，需要在不遗忘的前提下不断适应新域。这是TTA走向实际应用的关键挑战。

## 论文列表

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 1 | Continual Test-Time Domain Adaptation (CoTTA) | Wang et al. | CVPR 2022 | [arXiv](https://arxiv.org/abs/2203.13591) | 增强伪标签加权平均 + 随机权重恢复应对持续偏移 |
| 2 | NOTE: Robust Continual Test-time Adaptation Against Temporal Correlation | Gong et al. | NeurIPS 2022 | [GitHub](https://github.com/TaesikGong/NOTE) | 实例感知BN（IABN）处理非独立同分布时序相关测试流 |
| 3 | Robust Test-Time Adaptation in Dynamic Scenarios (RoTTA) | Yuan et al. | CVPR 2023 | [arXiv](https://arxiv.org/abs/2303.13899) | 鲁棒BN + 类别平衡采样 + 时间感知重加权的师生模型 |
| 4 | SoTTA: Robust Test-Time Adaptation on Noisy Data Streams | Gong et al. | NeurIPS 2023 | [arXiv](https://arxiv.org/abs/2310.10074) | 高置信度均匀类采样 + 熵-锐度最小化应对噪声流 |
| 5 | EcoTTA: Memory-Efficient Continual TTA via Self-Distilled Regularization | Song et al. | CVPR 2023 | [arXiv](https://arxiv.org/abs/2303.01904) | 轻量级元网络冻结原网络 + 自蒸馏，最小化内存占用 |
| 6 | ODS: Test-Time Adaptation in the Presence of Open-World Data Shift | Zhou et al. | ICML 2023 (Oral) | [链接](https://cs.nju.edu.cn/liyf/paper/ICML23-ods.pdf) | 同时处理变化的协变量和标签分布：分布追踪器 + 预测优化器 |
| 7 | TRIBE: Tri-Net Self-Training with Balanced Normalization | Su et al. | AAAI 2024 | [arXiv](https://arxiv.org/abs/2309.14949) | 平衡BN处理类不平衡流 + 三网络框架应对持续域偏移 |
| 8 | Persistent Test-time Adaptation in Recurring Testing Scenarios (PeTTA) | Hoang et al. | NeurIPS 2024 | [arXiv](https://arxiv.org/abs/2311.18193) | 检测模型向崩溃发散并动态调整适应策略，实现终身TTA |
| 9 | Universal TTA through Weight Ensembling and Prior Correction | Marsden et al. | WACV 2024 | [arXiv](https://arxiv.org/abs/2306.00650) | 定义覆盖所有实际场景的通用TTA + 自适应先验校正方案 |
| 10 | RMT: Robust Mean Teacher for Continual and Gradual TTA | Dobler et al. | CVPR 2023 | [链接](https://openaccess.thecvf.com/content/CVPR2023) | 对称交叉熵损失 + 鲁棒均值教师应对渐进域偏移 |
| 11 | PETAL: Prompt Enhanced Test-time Adaptation with Label Noise | Brahma & Rai | CVPR 2023 | [链接](https://openaccess.thecvf.com/content/CVPR2023) | 提示增强适应，处理持续TTA中的噪声伪标签 |
| 12 | MECTA: Memory-Efficient Continual TTA | Hong et al. | ICLR 2023 | [链接](https://openreview.net) | 通过高效优化策略降低持续TTA的内存占用 |
| 13 | BECoTTA: Input-dependent Balanced Expert Continual TTA | Lee et al. | ICML 2024 | [链接](https://proceedings.mlr.press/v235/) | 输入依赖的专家路由实现平衡的持续TTA（语义分割） |

## 持续TTA的核心挑战

```
┌─────────────────────────────────────────────────┐
│              持续TTA核心挑战                       │
├─────────────┬───────────────┬───────────────────┤
│  灾难性遗忘   │   错误累积     │   计算效率        │
│  (Forgetting) │ (Error Accum.) │  (Efficiency)    │
├─────────────┼───────────────┼───────────────────┤
│ CoTTA, RoTTA │ SoTTA, TRIBE  │ EcoTTA, MECTA    │
│ PeTTA       │ ODS           │ BECoTTA          │
└─────────────┴───────────────┴───────────────────┘
```
