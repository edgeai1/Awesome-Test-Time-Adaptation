# 🖼️ 视觉语言模型TTA (VLM / CLIP-Based TTA)

> 将TTA技术应用于CLIP等视觉语言大模型，是2022年以来TTA领域最活跃的方向之一。

---

## 📝 基于提示调优的TTA (Prompt-Based)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 1 | Test-Time Prompt Tuning for Zero-Shot Generalization (TPT) | Shu et al. | NeurIPS 2022 | [arXiv](https://arxiv.org/abs/2209.07511) | 通过置信度选择最小化熵，在线学习每个测试样本的自适应提示 |
| 2 | Diverse Data Augmentation with Diffusions for Test-time Prompt Tuning (DiffTPT) | Feng et al. | ICCV 2023 | [arXiv](https://arxiv.org/abs/2308.06038) | 用稳定扩散进行多样化增强 + 余弦相似度过滤用于测试时提示调优 |
| 3 | C-TPT: Calibrated Test-Time Prompt Tuning for VLMs | Yoon et al. | ICLR 2024 | [arXiv](https://arxiv.org/abs/2403.14119) | 引入平均文本特征离散度指标，校准感知的提示优化 |
| 4 | Test-Time Adaptation with CLIP Reward (RLCF) | Zhao et al. | ICLR 2024 | [arXiv](https://arxiv.org/abs/2305.18010) | 用CLIP作为奖励模型进行TTA，最大化输入与VLM输出分布间的奖励 |
| 5 | SwapPrompt: Test-Time Prompt Adaptation for VLMs | Ma et al. | NeurIPS 2023 | [链接](https://openreview.net/pdf?id=EhdNQiOWgQ) | 双提示范式 + EMA提示 + 自监督对比学习 |
| 6 | DynaPrompt: Dynamic Test-Time Prompt Tuning | Xiao et al. | ICLR 2025 | [链接](https://openreview.net) | 动态提示调优方法用于VLM测试时适应 |

---

## 💾 基于缓存/无训练的TTA (Cache / Training-Free)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 7 | Efficient Test-Time Adaptation of VLMs (TDA) | Karmanov et al. | CVPR 2024 | [arXiv](https://arxiv.org/abs/2403.18293) | 无训练动态适配器，用高置信度样本缓存实现VLM适应 |
| 8 | Frustratingly Easy Test-Time Adaptation of VLMs (ZERO) | Farina et al. | NeurIPS 2024 | [链接](https://proceedings.neurips.cc/paper_files/paper/2024) | 增强N次 → 保留最高置信度预测 → 零温度边际化；比TPT快10倍 |
| 9 | WATT: Weight Average Test-Time Adaptation of CLIP | Osowiechi et al. | NeurIPS 2024 | [GitHub](https://github.com/Mehrdad-Noori/WATT) | 多样文本提示模板 + 伪标签模型更新 + 权重平均的CLIP TTA |
| 10 | Dual Prototype Evolving for Test-Time Generalization of VLMs (DPE) | Zhang et al. | NeurIPS 2024 | [arXiv](https://arxiv.org/abs/2410.12790) | 从文本和视觉两种模态演化原型，比TPT提升3.5%+ |
| 11 | CLIPArTT: Adaptation of CLIP to New Domains at Test Time | Dastmalchi et al. | arXiv 2024 | [arXiv](https://arxiv.org/abs/2405.00754) | 轻量BN微调 + 自动文本提示构建作为伪标签 |
| 12 | MTA: Multimodal Test-time Adaptation | Zanella & Ayed | CVPR 2024 | [链接](https://openaccess.thecvf.com/content/CVPR2024) | 同时利用视觉和文本特征的多模态TTA方法 |

---

## 🔍 VLM分割TTA (Open-Vocabulary Segmentation)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 13 | TTA of VLMs for Open-Vocabulary Semantic Segmentation (MLMP) | Authors | NeurIPS 2025 | [arXiv](https://arxiv.org/abs/2505.21844) | 多级多提示熵最小化；即插即用适用于任何分割网络 |
| 14 | Realistic Test-Time Adaptation of Vision-Language Models | Zanella et al. | CVPR 2025 | [链接](https://openaccess.thecvf.com/content/CVPR2025) | 提出两种现实TTA评估设置：可变有效类别 + 非独立同分布批次 |
| 15 | RA-TTA: Retrieval-Augmented Test-Time Adaptation for VLMs | Authors | ICLR 2025 | [链接](https://openreview.net/forum?id=V3zobHnS61) | 检索增强方法用于测试时适应VLM |
| 16 | PromptAlign: Test-Time Prompting with Distribution Alignment | Samadh et al. | NeurIPS 2023 | [arXiv](https://arxiv.org/abs/2311.01459) | 通过提示调优将图像token嵌入的均值/方差与源统计量对齐 |
