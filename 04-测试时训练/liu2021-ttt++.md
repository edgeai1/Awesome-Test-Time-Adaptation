# TTT++ — When Does Self-Supervised Test-Time Training Fail or Thrive?

| 项目 | 内容 |
|------|------|
| **作者** | Yuejiang Liu et al. |
| **发表** | NeurIPS 2021 |
| **链接** | [GitHub](https://github.com/vita-epfl/ttt-plus-plus) |

---

## 动机
原始TTT的旋转预测任务太简单，与分类任务关联性有限。系统研究TTT成功/失败的条件。

## 核心贡献
1. 将**对比自监督学习**引入TTT，替代旋转预测
2. 提出**离线特征摘要**：预计算源域特征的均值和协方差，测试时矩匹配
3. 系统分析TTT的成败条件

## 方法详解
- 训练：主任务 + SimCLR风格对比任务，共享编码器
- 离线摘要：训练后计算源域特征统计量μ_src, Σ_src
- 测试：(1) 对比损失更新编码器；(2) 矩匹配损失约束特征分布

## 实验结果
- CIFAR-10-C上比TTT降低约15%错误率

## 局限性
1. 仍需修改训练流程
2. 矩匹配假设高斯分布

[← 返回目录](README.md)
