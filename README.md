<p align="center">
  <h1 align="center">🧠 TTA知识库</h1>
  <h3 align="center">Test-Time Adaptation 测试时适应 — 全面论文知识库</h3>
</p>

<p align="center">
  <a href="#-论文分类导航"><img src="https://img.shields.io/badge/论文总数-175+-blue?style=for-the-badge" alt="论文总数"></a>
  <a href="#-论文分类导航"><img src="https://img.shields.io/badge/分类数-18-green?style=for-the-badge" alt="分类数"></a>
  <a href="#-什么是tta"><img src="https://img.shields.io/badge/领域-TTA-red?style=for-the-badge" alt="领域"></a>
  <a href="#-相关资源"><img src="https://img.shields.io/badge/持续更新中-yellow?style=for-the-badge" alt="更新"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ICML-论文收录-5C5CFF?style=flat-square" alt="ICML">
  <img src="https://img.shields.io/badge/NeurIPS-论文收录-8B45A6?style=flat-square" alt="NeurIPS">
  <img src="https://img.shields.io/badge/CVPR-论文收录-2E8B57?style=flat-square" alt="CVPR">
  <img src="https://img.shields.io/badge/ICLR-论文收录-E07020?style=flat-square" alt="ICLR">
  <img src="https://img.shields.io/badge/ECCV-论文收录-FF4500?style=flat-square" alt="ECCV">
  <img src="https://img.shields.io/badge/AAAI-论文收录-1e90ff?style=flat-square" alt="AAAI">
  <img src="https://img.shields.io/badge/MICCAI-论文收录-DC143C?style=flat-square" alt="MICCAI">
</p>

---

## 📌 什么是TTA？

**测试时适应（Test-Time Adaptation, TTA）** 是指在模型部署后，利用未标注的测试数据对预训练模型进行在线适应的技术。当测试数据与训练数据存在分布偏移时，TTA能够在不访问源域训练数据的前提下提升模型的泛化能力。

```
┌──────────┐     ┌──────────────┐     ┌──────────────┐
│ 训练阶段   │ ──▶ │   部署模型     │ ──▶ │  测试时适应   │
│ (源域数据) │     │ (预训练权重)    │     │ (目标域数据)  │
└──────────┘     └──────────────┘     └──────────────┘
                                            │
                                      ┌─────┴─────┐
                                      │ 适应后模型  │
                                      │ (更好性能)  │
                                      └───────────┘
```

---

## 📚 论文分类导航

> 每个类别都是一个独立目录，每篇论文都有独立的详细解读文件。

### 🏗️ 基础与核心

| 类别 | 描述 | 进入目录 |
|:----:|------|:-------:|
| 📖 综述论文 | 领域全面综述，建立整体认知 | [→ 进入](01-综述论文/) |
| 🏛️ 奠基论文 | TTT、SHOT、Tent等开创性工作 | [→ 进入](02-奠基论文/) |
| 🔬 核心TTA方法 | 熵方法/增强/归一化/伪标签/特征对齐 | [→ 进入](03-核心TTA方法/) |
| 🧪 测试时训练 | TTT系列：训练时引入辅助任务 | [→ 进入](04-测试时训练/) |
| 🔄 持续在线TTA | CoTTA、RoTTA等处理连续域偏移 | [→ 进入](05-持续在线TTA/) |
| 🔓 无源域适应 | 不访问源数据的域适应方法 | [→ 进入](06-无源域适应/) |

### 🚀 前沿方向

| 类别 | 描述 | 进入目录 |
|:----:|------|:-------:|
| 🖼️ 视觉语言模型TTA | CLIP/VLM的提示调优和缓存TTA | [→ 进入](07-视觉语言模型TTA/) |
| 🌊 扩散模型TTA | 利用扩散模型辅助测试时适应 | [→ 进入](08-扩散模型TTA/) |
| 🤖 大语言模型TTA | LLM测试时学习 + 测试时缩放 | [→ 进入](10-大语言模型TTA/) |
| ⚡ 参数高效TTA | LoRA/适配器/提示的高效TTA | [→ 进入](17-参数高效TTA/) |

### 🏥 领域应用

| 类别 | 描述 | 进入目录 |
|:----:|------|:-------:|
| 🏥 医学影像TTA | 跨设备/跨模态医学分割适应 | [→ 进入](09-医学影像TTA/) |
| 🎯 目标检测与分割 | 密集预测任务的TTA | [→ 进入](11-目标检测与分割TTA/) |
| 🎬 视频动作识别 | 视频理解的时序TTA | [→ 进入](12-视频与动作识别TTA/) |
| 🧊 点云与3D | 3D理解与自动驾驶TTA | [→ 进入](13-点云与3D-TTA/) |
| 📐 深度估计与姿态 | 几何理解任务的TTA | [→ 进入](14-深度估计与姿态TTA/) |
| 🎙️ 语音与音频 | ASR/语音增强的TTA | [→ 进入](15-语音音频TTA/) |

### 📊 分析与拓展

| 类别 | 描述 | 进入目录 |
|:----:|------|:-------:|
| 🛡️ 鲁棒性与可靠性 | TTA的陷阱、对抗风险与评估 | [→ 进入](16-鲁棒性与可靠性/) |
| 🌐 特殊领域TTA | 图/表格/联邦学习/EEG/底层视觉等 | [→ 进入](18-特殊领域TTA/) |

---

## 🔥 必读论文 Top 10（含详细解读链接）

### 入门必读

| # | 论文 | 理由 | 详细解读 |
|:-:|------|------|:-------:|
| 1 | **Tent** (ICLR 2021) | TTA里程碑，定义问题范式 | [📄](02-奠基论文/wang2021-tent.md) |
| 2 | **TTT** (ICML 2020) | 测试时训练开山之作 | [📄](02-奠基论文/sun2020-ttt.md) |
| 3 | **SHOT** (ICML 2020) | 无源域适应先驱 | [📄](02-奠基论文/liang2020-shot.md) |
| 4 | **CoTTA** (CVPR 2022) | 持续TTA代表性工作 | [📄](05-持续在线TTA/wang2022-cotta.md) |
| 5 | **TPT** (NeurIPS 2022) | VLM测试时提示调优开创 | [📄](07-视觉语言模型TTA/提示调优/shu2022-tpt.md) |

### 进阶必读

| # | 论文 | 理由 | 详细解读 |
|:-:|------|------|:-------:|
| 6 | **SAR** (ICLR 2023 Oral) | 锐度感知的稳定TTA | [📄](03-核心TTA方法/熵方法/niu2023-sar.md) |
| 7 | **EATA** (ICML 2022) | 高效抗遗忘TTA | [📄](03-核心TTA方法/熵方法/niu2022-eata.md) |
| 8 | **MEMO** (NeurIPS 2022) | 单样本TTA解决方案 | [📄](03-核心TTA方法/增强方法/zhang2022-memo.md) |
| 9 | **LAME** (CVPR 2022) | 无参数更新TTA | [📄](03-核心TTA方法/伪标签方法/boudiaf2022-lame.md) |
| 10 | **s1** (EMNLP 2025) | 简单测试时缩放 | [📄](10-大语言模型TTA/测试时缩放/muennighoff2025-s1.md) |

---

## 📈 TTA发展时间线

```
2018  ZSSR ─────── 早期测试时内部学习

2020  TTT ──────── 开山之作：自监督辅助任务
      SHOT ─────── 无源域适应先驱
      AdaptiveBN ─ 测试时BN适应

2021  Tent ─────── 🔥 里程碑：定义完全TTA
      T3A ──────── 无需反向传播的分类器调整

2022  CoTTA ────── 持续TTA，随机权重恢复
      EATA ─────── 高效抗遗忘TTA
      MEMO ─────── 单样本多增强熵最小化
      TPT ──────── 🔥 VLM测试时提示调优

2023  SAR ──────── 🔥 锐度感知稳定TTA (ICLR Oral)
      RoTTA ────── 动态场景鲁棒TTA
      DDA ──────── 扩散驱动TTA

2024  DeYO ─────── 超越熵的样本选择 (ICLR Spotlight)
      TDA ──────── 无训练VLM适应
      TTS ──────── 🔥🔥 测试时缩放爆发

2025  s1 ─────────  简单测试时缩放
      TTRL ─────── 测试时强化学习
      StatA ────── 现实VLM TTA (CVPR Highlight)
```

---

## 📦 相关资源

| 资源 | 链接 | 描述 |
|------|------|------|
| 📁 完整资源列表 | [查看](resources/相关资源.md) | GitHub仓库、基准数据集、代码实现 |
| 🌟 Awesome TTA | [GitHub](https://github.com/tim-learn/awesome-test-time-adaptation) | 最全TTA论文列表 |
| 🌟 Awesome TT-LLMs | [GitHub](https://github.com/Dereck0602/Awesome_Test_Time_LLMs) | LLM测试时方法 |
| 🔧 torch-ttt | [GitHub](https://github.com/nikitadurasov/torch-ttt) | PyTorch TTT框架 |
| 📊 TTA Benchmark | [GitHub](https://github.com/mariodoebler/test-time-adaptation) | 统一TTA评估 |

---

## 🤝 贡献指南

1. **提交Issue** — 报告遗漏的论文或错误信息
2. **提交PR** — 添加新论文或改进内容
3. **Star** — 如果觉得有用，请给个Star支持

---

<p align="center">
  <b>如果这个知识库对你的研究有帮助，请给个 ⭐ Star！</b>
</p>
<p align="center"><i>最后更新：2025年5月</i></p>
