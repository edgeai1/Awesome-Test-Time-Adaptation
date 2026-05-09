# 🌐 特殊领域与应用TTA (Specialized Domain TTA)

> TTA在图数据、表格数据、底层视觉、联邦学习、EEG等特殊领域的应用。

---

## 📊 图数据与表格数据TTA

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 1 | GTRANS: Empowering GNNs with Test-Time Graph Transformation | Jin et al. | ICLR 2023 | [链接](https://openreview.net) | 测试时图变换用于GNN分布偏移适应 |
| 2 | TabLog: Test-Time Adaptation for Tabular Data Using Logic Rules | Authors | ICML 2024 | [链接](https://par.nsf.gov/biblio/10549097) | 离散化数值特征 + 对比损失建模依赖关系的表格TTA |
| 3 | FTAT: Fully Test-Time Adaptation for Tabular Data | Authors | AAAI 2025 | [链接](https://ojs.aaai.org) | 专为表格数据设计的完全测试时适应框架 |
| 4 | AdapTable: Test-Time Adaptation for Tabular Data via Shift-Aware Uncertainty Calibrator | Authors | AAAI 2025 | [链接](https://ojs.aaai.org) | 偏移感知的不确定性校准用于表格数据TTA |

---

## 🖼️ 底层视觉TTA

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 5 | ZSSR: "Zero-Shot" Super-Resolution Using Deep Internal Learning | Shocher et al. | CVPR 2018 | [链接](https://openaccess.thecvf.com/content_cvpr_2018) | 早期TTT用于图像超分辨率，从单图内部统计学习 |
| 6 | SRTTA: Test-Time Adaptation for Image Super-Resolution | Deng et al. | NeurIPS 2023 | [链接](https://proceedings.neurips.cc/paper_files/paper/2023) | 专为图像超分辨率设计的测试时适应框架 |
| 7 | Slot-TTA: Slot-Based Test-Time Adaptation | Prabhudesai et al. | ICML 2023 | [链接](https://proceedings.mlr.press/v202/) | 基于物体中心的槽表示学习用于组合式测试时适应 |

---

## 🔗 联邦学习TTA

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 8 | Enabling Collaborative TTA in Dynamic Environments via Federated Learning (TSA) | Authors | KDD 2024 | [链接](https://dl.acm.org/doi/10.1145/3637528.3671908) | 联邦TTA：客户端本地适应 + 上传服务器聚合 |
| 9 | Cross-Device Collaborative Test-Time Adaptation (CoLA) | Authors | NeurIPS 2024 | [链接](https://proceedings.neurips.cc/paper_files/paper/2024) | 利用多设备知识增强TTA性能和效率 |
| 10 | Adaptive Test-Time Personalization for Federated Learning (ATP) | Authors | NeurIPS 2024 | [arXiv](https://arxiv.org/abs/2310.18816) | 全局联邦模型在测试时的无监督本地适应 |
| 11 | PerAda: Parameter-Efficient Federated Learning Personalization | Xie et al. | CVPR 2024 | [链接](https://openaccess.thecvf.com/content/CVPR2024) | 参数高效联邦个性化 + 理论保证（通过适配器） |
| 12 | FedICON: Taming Heterogeneity to Handle Test-Time Shift in FL | Tan et al. | NeurIPS 2023 | [链接](https://proceedings.neurips.cc/paper_files/paper/2023) | 联合解决异质性和测试时偏移问题 |

---

## 🧠 EEG与其他专门领域

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 13 | Test-Time Adaptation for EEG Foundation Models | Authors | arXiv 2025 | [arXiv](https://arxiv.org/abs/2604.16926) | 真实世界分布偏移下EEG信号TTA方法的系统研究 |
| 14 | Temporal TTA with State-Space Models (STAD) | Authors | NeurIPS 2024 | [链接](https://openreview.net/forum?id=y4F2YZxN9T) | 概率状态空间模型用于渐进时序分布偏移下的TTA |
| 15 | Continual-MAE: Adaptive Distribution Masked Autoencoders for Continual TTA | Liu et al. | CVPR 2024 | [链接](https://openaccess.thecvf.com/content/CVPR2024) | 自适应分布MAE处理真实场景的持续域偏移 |
| 16 | Free on the Fly: Enhancing Flexibility in TTA with Online EM | Dai et al. | CVPR 2025 | [链接](https://openaccess.thecvf.com/content/CVPR2025) | 在线EM算法用于灵活的测试时适应，无需严格假设 |
| 17 | DocTTT: Document Test-Time Training for Handwritten Document Recognition | Gu et al. | WACV 2025 | [链接](https://openaccess.thecvf.com/content/WACV2025) | TTT应用于手写文档识别 |

---

## 🔬 主动学习与开放世界TTA

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 18 | Active Test-Time Adaptation: Theoretical Analyses and An Algorithm (SimATTA) | Gui et al. | ICLR 2024 | [链接](https://proceedings.iclr.cc/paper_files/paper/2024) | 将主动学习引入FTTA + 标签预算，B<300时超越所有TTA方法 |
| 19 | Open-World Test-Time Training: Self-Training with Contrast Learning (OWTTT) | Li et al. | ICCV 2023 | [arXiv](https://arxiv.org/abs/2409.09591) | 开放世界场景的测试时训练 + 对比学习 |

---

## 📏 理论分析

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 20 | Specialization after Generalization: Understanding TTT in Foundation Models | Authors | NeurIPS 2025 | [arXiv](https://arxiv.org/abs/2509.24510) | 证明TTT即使在全局欠参数化时也能泛化（线性表示假说） |
| 21 | Temporal Domain Regret Bound for TTA in Non-stationary Environments | Zhang et al. | NeurIPS 2024 | [链接](https://proceedings.neurips.cc/paper_files/paper/2024) | 在非平稳分布下实现O(T^{-1/3})平均遗憾界 |

---

## 📊 基准测试

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 22 | Benchmarking TTA against Distribution Shifts in Image Classification | Authors | TMLR 2024 | [arXiv](https://arxiv.org/abs/2307.03133) | 大规模系统基准比较不同分布偏移类型下的TTA方法 |
| 23 | A Versatile Framework for Continual TTA: Balancing Discriminability and Generalizability | Yang et al. | CVPR 2024 | [链接](https://openaccess.thecvf.com/content/CVPR2024) | 平衡持续TTA中的判别性和泛化性 |
| 24 | BoostAdapter: Improving TTA via Regional Bootstrapping | Zhang et al. | NeurIPS 2024 | [链接](https://proceedings.neurips.cc/paper_files/paper/2024) | 区域自举改进CLIP测试时适应 |
| 25 | SURGEON: Sharpness-Aware Minimization for TTA | Ma et al. | CVPR 2025 | [链接](https://openaccess.thecvf.com/content/CVPR2025) | 高级锐度感知方法实现更稳定的TTA |
| 26 | TCR: Test-time Contrastive Regularization | Sun et al. | ICLR 2025 | [链接](https://openreview.net) | 测试时对比正则化实现更鲁棒的适应 |
