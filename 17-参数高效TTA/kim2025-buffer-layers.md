# Buffer Layers for Test-Time Adaptation

| 项目 | 内容 |
|------|------|
| **作者** | Hyeongyu Kim et al. |
| **发表** | NeurIPS 2025 |
| **链接** | [arXiv 2510.21271](https://arxiv.org/abs/2510.21271) |

---

## 动机
现有TTA方法修改归一化层核心参数，存在根本性局限。

## 核心贡献
1. **Buffer Layer**作为模块化组件可无缝集成到几乎所有TTA框架
2. 保留预训练骨干网络的完整性
3. 从本质上缓解灾难性遗忘风险

## 局限性
1. Buffer Layer的设计需针对不同架构调整

[← 返回目录](README.md)
