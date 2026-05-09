# RL^V — Putting the Value Back in RL for Better Test-Time Scaling

| 项目 | 内容 |
|------|------|
| **作者** | Kusha Sareen et al. |
| **发表** | arXiv 2025 |
| **链接** | [arXiv 2505.04842](https://arxiv.org/abs/2505.04842) |

---

## 动机
主流RL方法（如GRPO）抛弃价值函数，测试时无法利用验证器扩展计算。

## 核心贡献
1. 在RL训练中联合训练LLM作为**推理器和生成式验证器**
2. 通过并行采样将MATH准确率提升超20%
3. 实现8-32倍高效测试时计算扩展

## 局限性
1. 验证器质量影响最终效果

[← 返回目录](../README.md)
