# Think Deep, Not Just Long — Measuring LLM Reasoning Effort via Deep-Thinking Tokens

| 项目 | 内容 |
|------|------|
| **作者** | Wei-Lin Chen et al. |
| **发表** | arXiv 2026 |
| **链接** | [arXiv 2602.13517](https://arxiv.org/abs/2602.13517) |

---

## 动机
原始token长度不能可靠衡量推理质量。提出**深度思考token**概念。

## 核心贡献
1. 定义"深度思考token"——模型深层预测发生显著修正的token
2. 提出深度思考比率(deep-thinking ratio)作为推理努力度量
3. Think@n策略：优先选择高深度思考比率的样本，降低推理成本

## 实验结果
- 深度思考比率与准确率的正相关显著优于长度和置信度基线

## 局限性
1. 需要访问模型内部中间层表示

[← 返回目录](../README.md)
