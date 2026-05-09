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

**测试时适应（Test-Time Adaptation, TTA）** 是指在模型部署后，利用未标注的测试数据对预训练模型进行在线适应的技术。当测试数据与训练数据存在分布偏移（Distribution Shift）时，TTA能够在不访问源域训练数据的前提下提升模型的泛化能力。

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

### 核心特点

| 特性 | 描述 |
|------|------|
| 🚫 无需源数据 | 适应过程不需要访问原始训练数据 |
| 🏷️ 无需标注 | 仅使用未标注的测试数据 |
| ⚡ 在线适应 | 在推理过程中实时进行 |
| 🎯 处理偏移 | 应对训练-测试分布不匹配 |

---

## 🗺️ TTA研究领域全景图

```
                            ┌─────────────────────┐
                            │    Test-Time         │
                            │    Adaptation (TTA)  │
                            └─────────┬───────────┘
               ┌──────────────────────┼──────────────────────┐
               ▼                      ▼                      ▼
      ┌────────────────┐    ┌────────────────┐    ┌────────────────┐
      │   方法论研究     │    │   应用领域      │    │   分析与评估    │
      └───────┬────────┘    └───────┬────────┘    └───────┬────────┘
         ┌────┴────┐          ┌─────┴─────┐          ┌────┴────┐
         ▼         ▼          ▼           ▼          ▼         ▼
    ┌─────────┐ ┌──────┐ ┌───────┐  ┌────────┐ ┌───────┐ ┌───────┐
    │核心TTA  │ │持续   │ │医学    │  │LLM/NLP │ │鲁棒性  │ │基准   │
    │方法     │ │在线   │ │影像    │  │视觉语言 │ │分析    │ │测试   │
    └─────────┘ │TTA   │ └───────┘  └────────┘ └───────┘ └───────┘
                └──────┘
```

---

## 📚 论文分类导航

### 🏗️ 基础与核心

| 类别 | 论文数 | 文件 | 描述 |
|:----:|:-----:|:----:|------|
| 📖 综述论文 | 5 | [查看](papers/01-综述论文.md) | 领域全面综述，建立整体认知 |
| 🏛️ 奠基论文 | 6 | [查看](papers/02-奠基论文.md) | TTT、SHOT、Tent等开创性工作 |
| 🔬 核心TTA方法 | 18 | [查看](papers/03-核心TTA方法.md) | 熵方法/增强/归一化/伪标签/特征对齐 |
| 🧪 测试时训练 | 8 | [查看](papers/04-测试时训练.md) | TTT系列：训练时引入辅助任务 |
| 🔄 持续在线TTA | 13 | [查看](papers/05-持续在线TTA.md) | CoTTA、RoTTA等处理连续域偏移 |
| 🔓 无源域适应 | 4 | [查看](papers/06-无源域适应.md) | 不访问源数据的域适应方法 |

### 🚀 前沿方向

| 类别 | 论文数 | 文件 | 描述 |
|:----:|:-----:|:----:|------|
| 🖼️ 视觉语言模型TTA | 16 | [查看](papers/07-视觉语言模型TTA.md) | CLIP/VLM的提示调优和缓存TTA |
| 🌊 扩散模型TTA | 9 | [查看](papers/08-扩散模型TTA.md) | 利用扩散模型辅助测试时适应 |
| 🤖 大语言模型TTA | 17 | [查看](papers/10-大语言模型TTA.md) | LLM测试时学习 + 测试时缩放 |
| ⚡ 参数高效TTA | 7 | [查看](papers/17-参数高效TTA.md) | LoRA/适配器/提示的高效TTA |

### 🏥 领域应用

| 类别 | 论文数 | 文件 | 描述 |
|:----:|:-----:|:----:|------|
| 🏥 医学影像TTA | 9 | [查看](papers/09-医学影像TTA.md) | 跨设备/跨模态医学分割适应 |
| 🎯 目标检测与分割 | 6 | [查看](papers/11-目标检测与分割TTA.md) | 密集预测任务的TTA |
| 🎬 视频动作识别 | 4 | [查看](papers/12-视频与动作识别TTA.md) | 视频理解的时序TTA |
| 🧊 点云与3D | 5 | [查看](papers/13-点云与3D-TTA.md) | 3D理解与自动驾驶TTA |
| 📐 深度估计与姿态 | 6 | [查看](papers/14-深度估计与姿态TTA.md) | 几何理解任务的TTA |
| 🎙️ 语音与音频 | 7 | [查看](papers/15-语音音频TTA.md) | ASR/语音增强的TTA |

### 📊 分析与拓展

| 类别 | 论文数 | 文件 | 描述 |
|:----:|:-----:|:----:|------|
| 🛡️ 鲁棒性与可靠性 | 11 | [查看](papers/16-鲁棒性与可靠性.md) | TTA的陷阱、对抗风险与评估 |
| 🌐 特殊领域TTA | 26 | [查看](papers/18-特殊领域TTA.md) | 图/表格/联邦学习/EEG/底层视觉等 |

---

## 📈 TTA发展时间线

```
2018  ZSSR ─────── 早期测试时内部学习（超分辨率）

2020  TTT ──────── 开山之作：自监督辅助任务
      SHOT ─────── 无源域适应先驱
      AdaptiveBN ─ 测试时BN适应

2021  Tent ─────── 🔥 里程碑：定义完全TTA，熵最小化
      T3A ──────── 无需反向传播的分类器调整
      ARM ──────── 元学习TTA框架
      TTT++ ────── TTT + 对比学习

2022  CoTTA ────── 持续TTA，随机权重恢复
      EATA ─────── 高效抗遗忘TTA
      MEMO ─────── 单样本多增强熵最小化
      NOTE ─────── 时序相关流的鲁棒TTA
      TPT ──────── 🔥 VLM测试时提示调优
      TTT-MAE ──── MAE驱动的测试时训练
      AdaContrast ─ 对比学习+伪标签

2023  SAR ──────── 🔥 锐度感知稳定TTA (ICLR Oral)
      RoTTA ────── 动态场景鲁棒TTA
      CoTTA ────── 多种持续TTA方法涌现
      DDA ──────── 扩散驱动TTA
      Diffusion-TTA ── 生成反馈适应
      ViTTA ────── 视频TTA先驱

2024  DeYO ─────── 超越熵的样本选择 (ICLR Spotlight)
      RLCF ─────── CLIP奖励TTA
      TDA ──────── 无训练VLM适应
      PeTTA ────── 终身TTA
      TTS ──────── 🔥🔥 测试时缩放爆发
      多个领域特定TTA方法涌现

2025  COME ─────── 保守熵最小化
      TTT-Linear ─ TTT作为序列建模层
      s1 ─────────  简单测试时缩放
      TTRL ─────── 测试时强化学习
      多方向持续发展中...
```

---

## 🔥 必读论文推荐

### 入门必读 (Top 5)

| 序号 | 论文 | 理由 |
|:---:|------|------|
| 1 | **Tent** (Wang et al., ICLR 2021) | TTA领域里程碑，定义了问题范式 |
| 2 | **TTT** (Sun et al., ICML 2020) | 测试时训练的开山之作 |
| 3 | **Liang et al. Survey** (IJCV 2024) | 最全面的TTA综述 |
| 4 | **CoTTA** (Wang et al., CVPR 2022) | 持续TTA的代表性工作 |
| 5 | **TPT** (Shu et al., NeurIPS 2022) | VLM测试时提示调优的开创性工作 |

### 进阶必读 (Top 5)

| 序号 | 论文 | 理由 |
|:---:|------|------|
| 1 | **SAR** (Niu et al., ICLR 2023 Oral) | 锐度感知的稳定TTA |
| 2 | **EATA** (Niu et al., ICML 2022) | 高效抗遗忘TTA |
| 3 | **On Pitfalls of TTA** (Zhao et al., ICML 2023) | 理解TTA的局限性 |
| 4 | **Snell et al.** (NeurIPS 2024) | 测试时计算缩放的理论基础 |
| 5 | **Diffusion-TTA** (Prabhudesai et al., NeurIPS 2023) | 扩散模型驱动的TTA新范式 |

---

## 📦 相关资源

| 资源 | 链接 | 描述 |
|------|------|------|
| 📁 完整资源列表 | [查看](resources/相关资源.md) | GitHub仓库、基准数据集、代码实现 |
| 🌟 Awesome TTA | [GitHub](https://github.com/tim-learn/awesome-test-time-adaptation) | 最全TTA论文列表 |
| 🌟 Awesome TT-LLMs | [GitHub](https://github.com/Dereck0602/Awesome_Test_Time_LLMs) | LLM测试时方法 |
| 🔧 torch-ttt | [GitHub](https://github.com/nikitadurasov/torch-ttt) | PyTorch TTT框架 |
| 📊 TTA Benchmark | [GitHub](https://github.com/mariodoebler/test-time-adaptation) | 统一TTA评估 |
| 🎓 CVPR 2024 MAT Workshop | [Website](https://tta-cvpr2024.github.io/) | 第1届TTA研讨会 |
| 🎓 ICML 2025 PUT Workshop | [Website](https://icml.cc/virtual/2025/workshop/39974) | 第2届TTA研讨会 |

---

## 🤝 贡献指南

欢迎通过以下方式参与贡献：

1. **提交Issue** — 报告遗漏的论文或错误信息
2. **提交PR** — 添加新论文或改进内容
3. **Star** — 如果觉得有用，请给个Star支持

### 论文格式模板

```markdown
| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| N | Title Here | Author et al. | Venue Year | [arXiv](link) | 一句话描述核心贡献 |
```

---

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源协议。

---

<p align="center">
  <b>如果这个知识库对你的研究有帮助，请给个 ⭐ Star！</b>
</p>

<p align="center">
  <i>最后更新：2025年5月</i>
</p>
