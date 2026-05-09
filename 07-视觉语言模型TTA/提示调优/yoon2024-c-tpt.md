# C-TPT — Calibrated Test-Time Prompt Tuning via Text Feature Dispersion

| 项目 | 内容 |
|------|------|
| **作者** | Jinhyeok Yoon et al. |
| **发表** | ICLR 2024 |
| **链接** | [arXiv 2403.14119](https://arxiv.org/abs/2403.14119) |

---

## 动机
TPT的熵最小化可能导致**校准失真**。发现文本特征的离散度与校准性密切相关。

## 核心贡献
1. 提出**ATFD**指标（Average Text Feature Dispersion）
2. 在TPT基础上增加ATFD最大化目标

## 实验结果
- 准确率与TPT相当，ECE降低约30-50%

## 局限性
1. 类别数多时ATFD计算开销大

[← 返回目录](../README.md)
