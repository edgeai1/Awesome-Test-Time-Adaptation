# ⚡ 参数高效TTA (Parameter-Efficient TTA)

> 使用适配器、提示、LoRA等参数高效方法进行测试时适应，降低计算和存储开销。

## 论文列表

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 1 | Time-Varying LoRA: Towards Effective Cross-Domain Fine-Tuning (Terra) | Authors | NeurIPS 2024 | [链接](https://proceedings.neurips.cc/paper_files/paper/2024/hash/8716aa6a02bcc3c8e69a3a42be192236) | 时变低秩适配器用于连续域流，通过插值域解决域偏移 |
| 2 | Customizing Language Models with Instance-wise LoRA | Authors | NeurIPS 2024 | [链接](https://proceedings.neurips.cc/paper_files/paper/2024) | 实例级LoRA适应实现每个输入的定制化LLM行为 |
| 3 | L-TTA: Lightweight Test-Time Adaptation Using a Versatile Stem Layer | Authors | NeurIPS 2024 | [链接](https://proceedings.neurips.cc/paper_files/paper/2024) | 轻量级干细胞层实现高效TTA，无需完整模型更新 |
| 4 | Hierarchical Knowledge Prompt Tuning for Multi-task TTA (HKPT) | Authors | CVPR 2025 | [链接](https://openaccess.thecvf.com/content/CVPR2025) | 任务特定双动态知识图 + 自适应任务分组用于多任务TTA |
| 5 | VICT: Test-Time Visual In-Context Tuning | Authors | CVPR 2025 | [链接](https://openaccess.thecvf.com/content/CVPR2025) | 测试时视觉上下文调优实现域适应 |
| 6 | TinyTTA: Test-Time Adaptation on Edge Devices | Jia et al. | NeurIPS 2024 | [链接](https://proceedings.neurips.cc/paper_files/paper/2024) | 专为资源受限边缘设备设计的高效TTA |
| 7 | FOA: Forward-Only Adaptation for Test-Time | Niu et al. | ICML 2024 | [链接](https://proceedings.mlr.press/v235/) | 仅前向传播（无需反向传播）的高效测试时适应方法 |

## 参数效率对比

| 方法类型 | 更新参数比例 | 内存开销 | 代表方法 |
|---------|:----------:|:-------:|---------|
| 全模型更新 | 100% | 高 | TTT |
| BN层适应 | <1% | 低 | Tent, EATA |
| 适配器 | 1-5% | 中 | L-TTA, Terra |
| 提示调优 | <0.1% | 极低 | TPT, HKPT |
| LoRA | 0.1-1% | 低 | TLM, Instance LoRA |
| 无参数 | 0% | 极低 | LAME, T3A, FOA |
