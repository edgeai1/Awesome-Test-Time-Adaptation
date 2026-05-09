# Think-with-Me — Beyond Model Scaling: Test-Time Intervention for Efficient Deep Reasoning

| 项目 | 内容 |
|------|------|
| **作者** | Qianyue Wang et al. |
| **发表** | arXiv 2026 |
| **链接** | [arXiv 2601.11252](https://arxiv.org/abs/2601.11252) |

---

## 动机
大推理模型常遭受**过度思考**（overthinking）和**超调**（overshoot），推理效率低下。

## 核心贡献
1. 提出**测试时交互推理**范式
2. 将转接词（如"因此"、"但是"）作为干预点
3. 引入外部反馈自适应终止或延长推理过程

## 实验结果
- AIME24上比QwQ-32B准确率提升7.19%，推理长度减少81%

## 局限性
1. 干预时机的选择需要精心设计

[← 返回目录](../README.md)
