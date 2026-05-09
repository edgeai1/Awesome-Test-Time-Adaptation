# TeSLA — Test-Time Self-Learning With Automatic Adversarial Augmentation

| 项目 | 内容 |
|------|------|
| **作者** | Devavrat Tomar et al. |
| **发表** | CVPR 2023 |
| **链接** | [arXiv 2303.09870](https://arxiv.org/abs/2303.09870) |

---

## 动机
现有TTA的增强策略过于"随机"。更好的做法是**自动学习最有挑战性的增强方式**，即对抗性增强。

## 核心贡献
1. 可学习的**对抗增强模块**
2. 在线知识蒸馏（EMA教师→学生）
3. 软伪标签精炼

## 方法详解
- 对抗增强：通过可微增强网络，用梯度上升找到使模型最不确定的增强参数
- 教师通过EMA更新，提供稳定软伪标签

## 实验结果
- ImageNet-C上比CoTTA高约3%，比EATA高约5%

## 局限性
1. 对抗增强的梯度计算增加计算开销
2. 增强网络本身需要在线训练

[← 返回目录](../README.md)
