# s1 — Simple Test-Time Scaling

| 项目 | 内容 |
|------|------|
| **作者** | Niklas Muennighoff et al. |
| **发表** | EMNLP 2025 |
| **链接** | [arXiv 2501.19393](https://arxiv.org/abs/2501.19393) |

---

## 动机
用**最简单的方法**复现o1的测试时缩放效果。

## 核心贡献
1. 提出**预算强制**（Budget Forcing）
2. 仅需1000条数据+Qwen2.5-32B即超越o1-preview
3. 开源模型和数据

## 方法详解
- 思考太短→在</think>处追加"Wait"迫使继续
- 思考太长→强制插入</think>截断
- 更多Wait = 更多自我验证和错误修正

## 关键结果
- s1-32B在MATH上比o1-preview高27%

## 局限性
1. 不区分问题难度
2. 长思考链增加延迟

[← 返回目录](../README.md)
