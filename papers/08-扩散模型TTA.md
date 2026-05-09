# 🌊 扩散模型TTA (Diffusion-Based TTA)

> 利用扩散模型强大的生成能力辅助测试时适应，是TTA领域的新兴方向。

## 论文列表

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 1 | Back to the Source: Diffusion-Driven Adaptation to Test-Time Corruption (DDA) | Gao et al. | CVPR 2023 | [arXiv](https://arxiv.org/abs/2207.03442) | 用生成扩散模型将测试输入投射回源域 + 分类器自集成 |
| 2 | Diffusion-TTA: Test-time Adaptation via Generative Feedback | Prabhudesai et al. | NeurIPS 2023 | [arXiv](https://arxiv.org/abs/2311.16102) | 通过扩散模型生成反馈最大化图像似然来适应分类器/分割器 |
| 3 | CloudFixer: Test-Time Adaptation for 3D Point Clouds via Diffusion | Shim et al. | ECCV 2024 | [链接](https://www.ecva.net/papers/eccv_2024) | 基于扩散的几何变换用于3D点云测试时适应 |
| 4 | Everything to the Synthetic: Diffusion-driven TTA via Synthetic-Domain Alignment (SDA) | Guo et al. | CVPR 2025 | [链接](https://openaccess.thecvf.com/content/CVPR2025) | 将源模型和目标数据对齐到扩散模型的合成域 |
| 5 | GDA: Generalized Diffusion for Robust Test-time Adaptation | Tsai et al. | CVPR 2024 | [arXiv](https://arxiv.org/abs/2404.00095) | 扩散引导的反向采样 + 边际熵 + 风格/内容保留损失 |
| 6 | Diffusion-Enhanced TTA with Text and Image Augmentation (IT3A) | Feng et al. | IJCV 2025 | [链接](https://link.springer.com/article/10.1007/s11263-025-02412-8) | DiffTPT扩展版，同时用文本和图像增强通过预训练扩散模型 |
| 7 | SteeringTTA: Guiding Diffusion Trajectories for Robust TTA | Authors | ICLR 2025 | [链接](https://openreview.net/forum?id=iV0WBCDGcx) | Feynman-Kac引导扩散轨迹 + 伪标签奖励实现输入适应 |
| 8 | FOCUS: Frequency-Optimized Conditioning for Mitigating Catastrophic Forgetting during TTA | Authors | MVA 2026 | [链接](https://link.springer.com/article/10.1007/s00138-026-01786-0) | 频域条件化防止扩散TTA中的灾难性遗忘 |
| 9 | DiffCTA: Leveraging Diffusion Models for Continual TTA in Fundus Image Classification | Authors | MICCAI 2025 | [链接](https://papers.miccai.org/miccai-2025/0494-Paper1304.html) | 用扩散模型将测试样本与医学影像源分布对齐 |

## 扩散TTA的技术路线

```
扩散模型TTA
├── 输入适应型 ──── DDA: 将测试输入投射回源域
│                  ├── GDA: 通用化扩散反向采样
│                  └── SteeringTTA: 引导扩散轨迹
├── 生成反馈型 ──── Diffusion-TTA: 用生成似然适应判别模型
├── 增强型 ──────── DiffTPT/IT3A: 用扩散模型生成多样增强
├── 域对齐型 ────── SDA: 合成域对齐
└── 领域特定型 ──── CloudFixer (3D), DiffCTA (医学), FOCUS (抗遗忘)
```
