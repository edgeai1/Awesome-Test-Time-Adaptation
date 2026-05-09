# 🏥 医学影像TTA (Medical Imaging TTA)

> 医学影像中普遍存在跨设备、跨机构的域偏移问题，TTA是解决这一问题的关键技术。

## 论文列表

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 1 | Test-Time Adaptable Neural Networks for Robust Medical Image Segmentation (TTA-DAE) | Karani et al. | Medical Image Analysis 2021 | [链接](https://www.sciencedirect.com/science/article/abs/pii/S1361841520302711) | 基于去噪自编码器辅助任务的医学分割测试时适应 |
| 2 | Self Domain Adapted Network (SDA-Net) | He et al. | MICCAI 2020 | [链接](https://link.springer.com/chapter) | 自监督域适应网络用于医学影像分析的测试时适应 |
| 3 | Each Test Image Deserves A Specific Prompt: Continual TTA for Medical Segmentation | Chen et al. | arXiv 2023 | [arXiv](https://arxiv.org/abs/2311.18363) | 实例特定提示用于医学图像分割的持续TTA |
| 4 | DG-TTA: Out-of-domain Medical Image Segmentation through DG and TTA | Weihsbach et al. | arXiv 2023 | [arXiv](https://arxiv.org/abs/2312.06275) | 结合域泛化训练与TTA实现鲁棒的域外医学分割 |
| 5 | Quest for Clone: Test-time Domain Adaptation for Medical Image Segmentation | Authors | MICCAI 2024 | [链接](https://papers.miccai.org/miccai-2024/635-Paper0297.html) | 在潜在空间中搜索最近克隆用于医学分割TTA |
| 6 | Cache-Driven Spatial TTA for Cross-Modality Medical Image Segmentation | Authors | MICCAI 2024 | [链接](https://papers.miccai.org/miccai-2024/113-Paper1458.html) | 整合3D体积切片间空间信息 + TTA实现跨模态分割 |
| 7 | SAM-aware Test-time Adaptation for Universal Medical Image Segmentation (SAM-TTA) | Authors | arXiv 2025 | [arXiv](https://arxiv.org/abs/2506.05221) | 适应SAM基础模型处理医学影像的通道和语义差异 |
| 8 | A Large Scale Benchmark for TTA Methods in Medical Image Segmentation | Authors | arXiv 2024 | [arXiv](https://arxiv.org/abs/2512.02497) | 全面基准测试比较多种医学影像模态下的TTA方法 |
| 9 | SicTTA: Single Image Continual TTA for Medical Image Segmentation | Authors | Medical Image Analysis 2025 | [链接](https://www.sciencedirect.com/science/article/abs/pii/S1361841525004050) | 单图像持续TTA，解决临床场景下小批量约束 |

## 医学影像TTA的特殊挑战

| 挑战 | 描述 | 代表方法 |
|------|------|---------|
| 🔬 模态差异 | CT/MRI/超声等不同成像模态间的偏移 | Cache-Driven Spatial TTA |
| 🏥 设备差异 | 不同厂商/型号设备产生的域偏移 | DG-TTA |
| 📊 标注稀缺 | 医学数据标注昂贵且专业性强 | SAM-TTA |
| 🔢 小批量 | 临床场景通常一次处理单个患者 | SicTTA |
| ⚠️ 安全性要求 | 适应不能导致严重的错误诊断 | TTA-DAE |
