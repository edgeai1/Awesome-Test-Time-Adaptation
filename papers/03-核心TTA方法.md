# 🔬 核心完全测试时适应方法 (Core Fully TTA Methods)

> 提出关键TTA算法的核心论文，按技术路线分类。

---

## 🔥 基于熵的方法 (Entropy-Based)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 1 | EATA: Efficient Test-Time Model Adaptation without Forgetting | Niu et al. | ICML 2022 | [arXiv](https://arxiv.org/abs/2204.02610) | 样本高效熵最小化，引入抗遗忘正则化 |
| 2 | Towards Stable Test-Time Adaptation in Dynamic Wild World (SAR) | Niu et al. | ICLR 2023 (Oral) | [arXiv](https://arxiv.org/abs/2302.12400) | 锐度感知熵最小化，过滤大梯度噪声样本实现稳定TTA |
| 3 | DELTA: Degradation-Free Fully Test-Time Adaptation | Zhao et al. | ICLR 2023 | [arXiv](https://arxiv.org/abs/2301.13018) | 测试时批重归一化 + 动态在线重加权防止退化 |
| 4 | COME: Test-time Adaption by Conservatively Minimizing Entropy | Zhang et al. | ICLR 2025 | [arXiv](https://arxiv.org/abs/2410.10894) | 建模Dirichlet先验，保守熵最小化防止模型崩溃 |
| 5 | DeYO: Entropy is not Enough for TTA | Lee et al. | ICLR 2024 (Spotlight) | [GitHub](https://github.com/Jhyun17/DeYO) | 提出PLPD置信度度量，结合熵与物体形状影响进行样本选择 |

---

## 🎨 基于增强的方法 (Augmentation-Based)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 6 | MEMO: Test Time Robustness via Adaptation and Augmentation | Zhang et al. | NeurIPS 2022 | [arXiv](https://arxiv.org/abs/2110.09506) | 通过最小化单个测试样本多个增强视图的边际熵实现适应 |
| 7 | Better Aggregation in Test-Time Augmentation | Shanmugam et al. | ICCV 2021 | [链接](https://openaccess.thecvf.com/content/ICCV2021/html/Shanmugam_Better_Aggregation_in_Test-Time_Augmentation_ICCV_2021_paper.html) | 分析并改进测试时增强的预测聚合策略 |

---

## 📊 基于归一化的方法 (Normalization-Based)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 8 | Dynamic Unsupervised Domain Adaptation by Normalization (DUA) | Mirza et al. | CVPR 2022 | [GitHub](https://github.com/jmiemirza/DUA) | 仅在线适应BN统计量，需<1%目标数据，无需反向传播 |
| 9 | Unraveling Batch Normalization for Realistic TTA (TEMA) | Su et al. | AAAI 2024 | [arXiv](https://arxiv.org/abs/2312.09486) | 识别批次中类别多样性不足为关键问题，提出自适应数据范围EMA |
| 10 | TTN: A Domain-Shift Aware Batch Normalization in TTA | Lim et al. | ICLR 2023 | [链接](https://openreview.net/pdf?id=EQfeudmWLQ) | 域偏移感知的BN层用于测试时适应 |

---

## 🏷️ 自训练与伪标签方法 (Self-Training & Pseudo-Label)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 11 | Contrastive Test-Time Adaptation (AdaContrast) | Chen et al. | CVPR 2022 | [arXiv](https://arxiv.org/abs/2204.10377) | 结合对比学习与最近邻投票在线伪标签精炼 |
| 12 | Parameter-Free Online Test-Time Adaptation (LAME) | Boudiaf et al. | CVPR 2022 | [arXiv](https://arxiv.org/abs/2201.05718) | 拉普拉斯调整最大似然估计，适应模型输出而非参数 |
| 13 | Test-Time Classifier Adjustment Module (T3A) | Iwasawa & Matsuo | NeurIPS 2021 (Spotlight) | [GitHub](https://github.com/matsuolab/T3A) | 无需反向传播，通过伪原型表示调整分类器 |
| 14 | TeSLA: Test-Time Self-Learning With Automatic Adversarial Augmentation | Tomar et al. | CVPR 2023 | [arXiv](https://arxiv.org/abs/2303.09870) | 在线知识蒸馏 + 可学习对抗增强 + 软伪标签精炼 |
| 15 | Improved Self-Training for Test-Time Adaptation (IST) | Ma et al. | CVPR 2024 | [链接](https://openaccess.thecvf.com/content/CVPR2024/html/Ma_Improved_Self-Training_for_Test-Time_Adaptation_CVPR_2024_paper.html) | 基于图的伪标签校正 + 参数移动平均实现稳定适应 |
| 16 | Conjugate Pseudo-Labels for Source-Free Domain Adaptation | Goyal et al. | NeurIPS 2022 | [链接](https://proceedings.neurips.cc/paper_files/paper/2022) | 引入共轭伪标签用于更鲁棒的域偏移自训练 |

---

## 🎯 特征对齐方法 (Feature Alignment)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 17 | ActMAD: Activation Matching to Align Distributions for TTT | Mirza et al. | CVPR 2023 | [arXiv](https://arxiv.org/abs/2211.12870) | 跨多层对齐OOD测试数据与训练数据的激活统计量 |
| 18 | Ada-ReAlign: Adaptive Representation Alignment in Non-stationary Environments | Zhang et al. | NeurIPS 2024 | [链接](https://openreview.net/forum?id=0EfUYVMrLv) | 使用不同窗口大小的多基模型 + 元学习器实现自适应对齐 |

---

## 技术路线图

```
核心TTA方法
├── 基于熵 ─── Tent → EATA → SAR → DELTA → DeYO → COME
├── 基于增强 ─── MEMO, TTA聚合
├── 基于归一化 ─── AdaptiveBN → DUA → TTN → TEMA
├── 伪标签/自训练 ─── T3A → AdaContrast → LAME → TeSLA → IST
└── 特征对齐 ─── ActMAD → Ada-ReAlign
```
