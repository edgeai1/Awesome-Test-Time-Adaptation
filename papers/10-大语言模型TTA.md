# 🤖 大语言模型与NLP的TTA (LLM & NLP TTA)

> 将TTA思想应用于NLP和大语言模型领域，包括测试时缩放（Test-Time Scaling）这一2024-2025年的热门方向。

---

## 📚 NLP领域TTA

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 1 | Test-Time Learning for Large Language Models (TLM) | Hu et al. | ICML 2025 | [arXiv](https://arxiv.org/abs/2505.20633) | 通过LoRA进行输入困惑度最小化实现LLM测试时域适应 |
| 2 | TTA for LLM Agents via Environment Interaction | Authors | arXiv 2024 | [arXiv](https://arxiv.org/abs/2511.04847) | LLM智能体的TTA，解决新环境中的语法/语义误解 |
| 3 | TTT-NN: Test-Time Training with Nearest Neighbors | Hardt & Sun | ICLR 2024 | [链接](https://proceedings.iclr.cc/paper_files/paper/2024) | 基于最近邻的语言模型测试时训练 |
| 4 | SGEM: Sequential-Level Generalized Entropy Minimization for ASR | Kim et al. | INTERSPEECH 2023 (Oral) | [arXiv](https://arxiv.org/abs/2306.01981) | 序列级广义熵最小化用于ASR，平均WER降低15.6% |
| 5 | PADA: Example-based Prompt Learning for Domain Adaptation | Ben-David et al. | TACL 2022 | [链接](https://aclanthology.org) | 基于提示的NLP域适应 |
| 6 | Titans: Learning to Memorize at Test Time | Behrouz et al. | arXiv 2025 | [链接](https://arxiv.org) | 具有测试时学习能力的长上下文记忆架构 |
| 7 | You Only Need 4 Extra Tokens: Synergistic TTA for LLMs | Authors | arXiv 2025 | [arXiv](https://arxiv.org/abs/2510.10223) | 仅需4个额外token的轻量级LLM测试时适应 |

---

## 📈 测试时缩放 / 测试时计算 (Test-Time Scaling / Compute)

> 2024-2025年最热门的方向之一，核心思想是在推理时投入更多计算资源以提升性能。

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 8 | Scaling LLM Test-Time Compute Optimally | Snell et al. | NeurIPS 2024 | [arXiv](https://arxiv.org/abs/2408.03314) | 证明最优测试时计算缩放可比模型参数缩放更有效 |
| 9 | s1: Simple Test-Time Scaling | Muennighoff et al. | EMNLP 2025 | [arXiv](https://arxiv.org/abs/2501.19393) | 预算强制测试时缩放；s1-32B在数学上超越o1-preview 27% |
| 10 | What, How, Where, and How Well? A Survey on Test-Time Scaling in LLMs | Fan et al. | arXiv 2025 | [arXiv](https://arxiv.org/abs/2503.24235) | 全面综述TTS：what/how/where/how-well四维分析 |
| 11 | The Art of Scaling Test-Time Compute for LLMs | Beeching et al. | arXiv 2025 | [arXiv](https://arxiv.org/abs/2512.02008) | 大规模研究（30B+ tokens, 8个LLM），发现没有单一TTS策略普遍占优 |
| 12 | Inference Scaling Laws: An Empirical Analysis of Compute-Optimal Inference | Brown et al. | ICLR 2025 | [arXiv](https://arxiv.org/abs/2408.00724) | 小模型+高级推理算法提供帕累托最优的成本-性能权衡 |
| 13 | Revisiting the Test-Time Scaling of o1-like Models | Huang et al. | ACL 2025 | [arXiv](https://arxiv.org/abs/2502.12215) | 揭示R1和QwQ自修正能力有限，延长解答长度不总是有帮助 |
| 14 | TTRL: Test-Time Reinforcement Learning | PRIME-RL | NeurIPS 2025 | [arXiv](https://arxiv.org/abs/2504.16084) | 以多数投票为奖励信号在无标签测试数据上进行RL，Qwen提升211% |
| 15 | Inference-Aware Fine-Tuning for Best-of-N Sampling | Authors | ICLR 2025 | [arXiv](https://arxiv.org/abs/2412.15287) | 专门为Best-of-N采样优化LLM的模仿和RL方法 |
| 16 | Process Reward Models That Think | Authors | NeurIPS 2025 | [链接](https://openreview.net/forum?id=V727xqBYIW) | 步骤级推理验证的过程奖励模型，测试时缩放的关键组件 |
| 17 | Do NOT Think That Much for 2+3=? On the Overthinking of o1-Like LLMs | Authors | arXiv 2025 | [链接](https://github.com/Dereck0602/Awesome_Test_Time_LLMs) | 识别推理模型的过度思考问题，提出高效测试时计算分配 |

## 测试时缩放的核心框架

```
测试时缩放策略
├── 并行缩放 (Parallel)
│   ├── Best-of-N 采样
│   ├── 多数投票 (Majority Voting)
│   └── 奖励模型重排序
├── 顺序缩放 (Sequential)
│   ├── 链式思考 (Chain-of-Thought)
│   ├── 预算强制 (Budget Forcing) ── s1
│   └── 自修正 (Self-Correction)
└── 混合缩放 (Hybrid)
    ├── 蒙特卡洛树搜索 (MCTS)
    └── 过程奖励模型引导搜索
```
