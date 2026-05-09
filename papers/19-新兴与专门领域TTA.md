# 🌍 新兴与专门领域TTA (Emerging & Specialized Domain TTA)

> TTA在自动驾驶、遥感、强化学习、多模态、推荐系统、元学习、域泛化、机器人、恶劣天气、行人重识别、人脸反欺骗、光流估计等新兴/专门领域的应用。

---

## 🚗 自动驾驶 / 自驾TTA (Autonomous Driving TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 1 | MOS: Model Synergy for Test-Time Adaptation on LiDAR-Based 3D Object Detection | Huang et al. | ICLR 2025 | [OpenReview](https://openreview.net/forum?id=Y6aHdDNQYD) | 在线TTA框架，动态选择历史检查点集成处理LiDAR天气/传感器/跨腐蚀偏移 |
| 2 | HGL: Hierarchical Geometry Learning for Test-time Adaptation in 3D Point Cloud Segmentation | Zou et al. | ECCV 2024 (Oral) | [arXiv](https://arxiv.org/abs/2407.12387) | 层次化几何学习（局部-全局-时序）用于点云分割TTA，mIoU提升3%且适应时间减少80% |
| 3 | APCoTTA: Continual Test-Time Adaptation for Semantic Segmentation of Airborne LiDAR Point Clouds | Gao et al. | arXiv 2025 | [arXiv](https://arxiv.org/abs/2505.09971) | 机载激光扫描点云的持续TTA，含动态层选择/熵一致性/随机参数插值，mIoU提升9-14% |
| 4 | Test-time Adaptation for Geospatial Point Cloud Semantic Segmentation with Distinct Domain Shifts | Wang et al. | ISPRS 2025 | [ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0924271625003338) | 地理空间点云的TTA，处理摄影测量-机载-移动-合成多种域偏移 |
| 5 | Exploring Test-Time Adaptation for Object Detection in Continually Changing Environments | Authors | arXiv 2024 | [arXiv](https://arxiv.org/abs/2406.16439) | 持续变化环境下目标检测的TTA，解决伪标签阈值固定和随机参数恢复问题 |
| 6 | LD-BN-ADAPT: Real-time Fully Unsupervised Domain Adaptation for Lane Detection | Authors | Conference 2023 | [GitHub](https://github.com/ejjun92/Autonomous-Driving-Papers) | 实时无监督域适应用于车道检测，通过BN层适应 |

---

## 🛰️ 遥感 / 卫星影像TTA (Remote Sensing TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 7 | LSCD-TTA: Low Saturation Confidence Distribution-based Test-Time Adaptation for Cross-Domain Remote Sensing Image Classification | Authors | ISPRS J. 2025 | [arXiv](https://arxiv.org/abs/2408.16265) | 首个遥感图像分类TTA方法，含弱置信度熵损失/类别平衡损失/低饱和分布损失，ResNet-101上提升5.22% |
| 8 | Domain Adaptation for Satellite-Borne Multispectral Cloud Detection | Du et al. | Remote Sensing 2024 | [MDPI](https://www.mdpi.com/2072-4292/16/18/3469) | 卫星载多光谱云检测的域适应，在真实航天硬件上实现TTA更新CNN |
| 9 | Search-TTA: A Multimodal Test-Time Adaptation Framework for Visual Search in the Wild | Authors | arXiv 2025 | [arXiv](https://arxiv.org/abs/2505.11350) | 野外视觉搜索的多模态TTA框架 |

---

## 🎮 强化学习TTA (Reinforcement Learning TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 10 | TARL: Test-time Adapted Reinforcement Learning with Action Entropy Regularization | Authors | ICML 2025 | [OpenReview](https://openreview.net/forum?id=Xv1jY6U0pT) | 离线RL的TTA，最小化动作熵避免OOD状态-动作对，覆盖离散和连续控制 |
| 11 | Design from Policies: Conservative Test-Time Adaptation for Offline Policy Optimization | Authors | ICLR 2024 | [OpenReview](https://openreview.net/forum?id=jZYf1GxH1V) | 离线策略优化的保守测试时适应 |
| 12 | FeedTTA: Test-Time Adaptation for Online Vision-Language Navigation with Feedback-based RL | Authors | OpenReview 2024 | [OpenReview](https://openreview.net/forum?id=K4GaB4fdIq) | 基于反馈的RL进行在线VLN测试时适应，智能体接收二值成功/失败信号 |
| 13 | TT-VLA: On-the-Fly VLA Adaptation via Test-Time Reinforcement Learning | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2601.06748v1) | VLA模型的测试时RL适应，利用逐步任务进度信号细化动作策略 |
| 14 | EVOLVE-VLA: Test-Time Training from Environment Feedback for Vision-Language-Action Models | Bai, Gao & Shou | arXiv 2025 | [arXiv](https://arxiv.org/abs/2512.14666) | VLA的测试时训练框架，学习进度估计器提供密集反馈，长程任务+8.6%，1-shot+22.0% |
| 15 | Boosting ASR Robustness via Test-Time RL with Audio-Text Semantic Rewards | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2603.05231) | 使用音频-文本语义奖励的测试时RL增强ASR鲁棒性 |

---

## 🎭 多模态TTA (Multimodal TTA, beyond VLMs)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 16 | Audio-Visual Continual Test-Time Adaptation without Forgetting | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2602.18528v1) | 首个音频-视觉持续TTA研究，共享缓冲区存储/检索注意力参数处理单/双模态腐蚀 |
| 17 | BriMPR: Bridging Modalities via Progressive Re-alignment for Multimodal TTA | Authors | arXiv 2025 | [arXiv](https://www.arxiv.org/abs/2511.22862) | 渐进式重对齐处理跨模态不同程度的分布偏移耦合效应 |
| 18 | Test-Time Adaptation for Combating Missing Modalities in Egocentric Videos | Authors | AAAI 2025 | [OpenReview](https://openreview.net/forum?id=1L52bHEL5d) | 以太视频中缺失模态的TTA，超越其他TTA基线 |
| 19 | RobustTouch: Test-Time Adaptation for Tactile-Vision-Language Models | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2602.15873) | 触觉-视觉-语言模型的TTA框架，通过动态样本过滤和自适应多模态融合处理异步分布偏移 |
| 20 | Energy-Guided Test-Time Adaptation for Data Shifts in Multi-Modal Perception | Authors | The Visual Computer 2025 | [Springer](https://link.springer.com/article/10.1007/s00371-025-03952-3) | 能量引导的多模态感知TTA |

---

## 📊 推荐系统TTA (Recommendation System TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 21 | TTA-GREC: Test-Time Adaptation on Recommender System with Data-Centric Graph Transformation | Authors | IJCAI 2025 | [IJCAI](https://www.ijcai.org/proceedings/2025/510) | 图推荐系统的TTA，含伪标签引导UI图变换/知识图修正/采样自监督适应 |
| 22 | T2ARec: Test-Time Alignment for Tracking User Interest Shifts in Sequential Recommendation | Zhang et al. | arXiv 2025 | [arXiv](https://arxiv.org/html/2504.01489) | 利用状态空间模型进行TTT，对齐时间间隔与学习间隔捕捉用户兴趣偏移 |
| 23 | Retrieve-then-Adapt: Retrieval-Augmented Test-Time Adaptation for Sequential Recommendation | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2604.05379v1) | 检索增强TTA，基于历史相似行为序列检索相关项目增强测试时预测 |

---

## 🧠 元学习 + TTA (Meta-Learning TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 24 | MT3: Meta Test-Time Training for Self-Supervised Test-Time Adaptation | Bartler et al. | AISTATS 2022 | [arXiv](https://arxiv.org/abs/2103.16201) | 结合元学习+自监督+TTT，单张无标签图像即可适应元模型参数 |
| 25 | Test-Time Fast Adaptation for Dynamic Scene Deblurring via Meta-Auxiliary Learning | Chi et al. | CVPR 2021 | [CVF](https://openaccess.thecvf.com/content/CVPR2021/papers/Chi_Test-Time_Fast_Adaptation_for_Dynamic_Scene_Deblurring_via_Meta-Auxiliary_Learning_CVPR_2021_paper.pdf) | 元辅助学习实现动态场景去模糊的测试时快速适应 |
| 26 | MASS: Test-Time Meta-Adaptation with Self-Synthesis | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2603.03524) | LLM元学习框架，通过双层优化生成问题特定合成训练数据并自适应更新 |
| 27 | Test-Time Adaptation for Video Highlight Detection Using Meta-Auxiliary | Authors | arXiv 2025 | [arXiv](https://arxiv.org/pdf/2508.04924) | 元辅助学习用于视频高光检测的TTA |

---

## 🌐 测试时域泛化 (Test-Time Domain Generalization)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 28 | ITTA: Improved Test-Time Adaptation for Domain Generalization | Chen et al. | CVPR 2023 | [arXiv](https://arxiv.org/abs/2304.04494) | 可学习一致性损失+自适应参数，仅更新自适应参数 |
| 29 | TestDG: Test-time Domain Generalization for Continual Test-time Adaptation | Li et al. | arXiv 2025 | [arXiv](https://arxiv.org/abs/2504.04981) | 在线测试时域泛化框架，学习对当前和历史测试域不变的特征以泛化到未来域 |
| 30 | Test-Time Domain Generalization via Universe Learning: A Multi-Graph Matching Approach for Medical Image Segmentation | Lv et al. | CVPR 2025 | [arXiv](https://arxiv.org/abs/2503.13012) | 多图匹配+宇宙嵌入整合形态先验，医学图像分割的测试时域泛化 |
| 31 | Test-Time Domain Generalization for Face Anti-Spoofing | Zhou et al. | CVPR 2024 | [CVF](https://openaccess.thecvf.com/content/CVPR2024/papers/Zhou_Test-Time_Domain_Generalization_for_Face_Anti-Spoofing_CVPR_2024_paper.pdf) | 无需测试时模型更新的域泛化方法，可无缝集成CNN和ViT |

---

## 🔄 持续/终身学习 + TTA (Continual/Lifelong Learning TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 32 | FEATHER: Lifelong Test-Time Adaptation with Lightweight Adapters | Authors | OpenReview 2025 | [OpenReview](https://openreview.net/forum?id=6yJuDK1DsK) | 解耦源域/目标域知识的终身TTA，对抗长期错误累积 |
| 33 | When and Where to Reset Matters for Long-Term Test-Time Adaptation (ASR) | Authors | ICLR 2026 | [arXiv](https://arxiv.org/abs/2603.03796) | 自适应选择性重置，动态决定何时何处重置+重要性正则化恢复重置丢失的知识 |
| 34 | CPT4: Continual Prompted Transformer for Test Time Training | Authors | Information Sciences 2025 | [ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0020025524017559) | 持续提示Transformer用于测试时训练 |
| 35 | Decorate the Newcomers: Visual Domain Prompt for Continual TTA | Gan et al. | AAAI 2023 | [AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/25922) | 学习视觉域提示适应目标域，同时冻结源模型参数 |

---

## 🤖 机器人感知TTA (Robotic Perception TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 36 | Embodied Perception for Test-Time Grasping Detection Adaptation (ETA) | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2504.04795) | 具身TTA用于抓取检测，含知识检索/多视角主动探索/网络优化三模块 |
| 37 | SPA: Few-Shot Test-Time Adaptation for Surgical Phase Recognition | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2506.20254) | 少样本空间适应+时序适应+动态TTA用于跨机构手术工作流理解 |

---

## 🌧️ 恶劣天气TTA (Adverse Weather TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 38 | DiffTTA: Genuine Knowledge from Practice: Diffusion Test-Time Adaptation for Video Adverse Weather Removal | Yang et al. | CVPR 2024 | [arXiv](https://arxiv.org/abs/2403.07684) | 首个将TTA融入扩散逆过程的视频恶劣天气去除框架，扩散管状自校准代理任务 |
| 39 | Test-Time Adaptation for Real-World Video Adverse Weather Restoration with Meta Batch Normalization | Authors | IEEE T-CSVT 2025 | [IEEE](https://ieeexplore.ieee.org/document/10833729/) | 元学习+自监督分支的元BN框架，提升视频天气恢复适应性 |

---

## 👤 行人重识别TTA (Person Re-identification TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 40 | TEMP: Test-time Similarity Modification for Person Re-identification toward Temporal Distribution Shift | Authors | arXiv 2024 | [arXiv](https://arxiv.org/abs/2403.14114) | 首个Re-ID的TTA方法，提出Re-ID熵替代分类熵，处理时序分布偏移 |
| 41 | BNTA: Generalizable Person Re-identification via Self-Supervised Batch Norm Test-Time Adaptation | Authors | AAAI 2022 | [AAAI](https://aaai.org/papers/00817-generalizable-person-re-identification-via-self-supervised-batch-norm-test-time-adaption/) | 自监督策略更新BN参数，从无标签目标数据提取域感知信息 |

---

## 😎 人脸识别 / 反欺骗TTA (Face Recognition / Anti-Spoofing TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 42 | 3A-TTA: Test-Time Adaptation for Robust Face Anti-Spoofing | Huang & Hsu | BMVC 2023 | [BMVC](https://proceedings.bmvc2023.org/379/) | 激活伪标签+抗遗忘特征学习+非对称原型对比学习的FAS TTA框架 |
| 43 | Optimal Transport-Guided Source-Free Adaptation for Face Anti-Spoofing | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2503.22984) | 最优传输引导的无源域适应用于人脸反欺骗 |
| 44 | Style Selective Normalization with Meta Learning for Test-Time Adaptive Face Anti-Spoofing | Authors | Expert Systems with Applications 2023 | [ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0957417422021248) | 元学习+风格选择性归一化用于FAS的测试时适应 |

---

## 🔍 光流 / 深度完成TTA (Optical Flow & Depth Completion TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 45 | Test-Time Adaptation for Optical Flow Estimation Using Motion Vectors | Authors | IEEE T-CSVT 2023 | [IEEE](https://ieeexplore.ieee.org/document/10236979/) | 利用压缩视频格式中的运动向量设计自监督TTA任务用于光流估计 |
| 46 | ETA: Energy-based Test-time Adaptation for Depth Completion | Chung et al. | ICCV 2025 | [CVF](https://openaccess.thecvf.com/content/ICCV2025/papers/Chung_ETA_Energy-based_Test-time_Adaptation_for_Depth_Completion_ICCV_2025_paper.pdf) | 基于能量的无监督深度补全TTA |
| 47 | Depth Completion as Parameter-Efficient Test-Time Adaptation | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2602.14751) | 将深度补全建模为参数高效的测试时适应问题 |
| 48 | Globally Consistent Video Depth and Pose Estimation with Efficient Test-Time Training | Lee et al. | CVPR 2022 | [PDF](https://3dvar.com/Lee2022Globally.pdf) | 高效测试时训练实现全局一致的视频深度和位姿估计 |

---

## 📱 模型压缩/量化 + TTA (Model Compression / Quantization TTA)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 49 | ZOA: Test-Time Model Adaptation for Quantized Neural Networks | Deng et al. | ACM MM 2025 | [arXiv](https://arxiv.org/abs/2508.02180) | 零阶适应框架，仅需两次前向传播即可适应量化模型，无需梯度反向传播 |
| 50 | Benchmarking Test-Time DNN Adaptation at Edge with Compute-In-Memory | Authors | ACM JATS 2024 | [ACM](https://dl.acm.org/doi/10.1145/3665898) | 边缘CIM硬件上TTA的基准测试 |

---

## 🔗 联邦学习 + TTA (Federated Learning TTA, 补充)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 51 | Latte: Collaborative Test-Time Adaptation of Vision-Language Models in Federated Learning | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2507.21494) | 联邦学习中VLM的协作TTA，客户端维护本地+外部记忆存储嵌入/原型 |
| 52 | FedCTTA: A Collaborative Approach to Continual Test-Time Adaptation in Federated Learning | Authors | arXiv 2025 | [arXiv](https://arxiv.org/abs/2505.13643) | 隐私保护+计算高效的联邦持续TTA框架 |

---

## 🗣️ 语音/音频TTA (Speech/Audio TTA, 补充)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 53 | SLM-TTA: A Framework for Test-Time Adaptation of Generative Spoken Language Models | Authors | arXiv 2025 | [arXiv](https://arxiv.org/pdf/2512.24739) | 生成式口语语言模型的TTA框架，动态适应少量模型参数缓解声学偏移 |
| 54 | LI-TTA: Language Informed Test-Time Adaptation for ASR | Authors | arXiv 2024 | [arXiv](https://arxiv.org/pdf/2408.05769) | 语言信息引导的ASR TTA，整合外部指令调优语言模型的纠正 |
| 55 | Dynamic Model-bank Test-time Adaptation for Automatic Speech Recognition | Authors | EMNLP 2025 | [ACL](https://aclanthology.org/2025.emnlp-main.1107.pdf) | 动态模型库的ASR测试时适应 |
| 56 | An Investigation of Test-time Adaptation for Audio Classification under Background Noise | Authors | arXiv 2025 | [arXiv](https://arxiv.org/html/2507.15523v1) | 背景噪声下音频分类TTA的系统调查 |

---

## 🎬 视频理解TTA (Video Understanding TTA, 补充)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 57 | Modality-Collaborative Test-Time Adaptation for Action Recognition | Xiong et al. | CVPR 2024 | [CVF](https://openaccess.thecvf.com/content/CVPR2024/papers/Xiong_Modality-Collaborative_Test-Time_Adaptation_for_Action_Recognition_CVPR_2024_paper.pdf) | (已有条目补充说明) 减少多模态信息的域偏移 |

---

## 🔬 最新2025前沿论文 (Very Recent 2025 Preprints)

| # | 论文标题 | 作者 | 发表venue | 链接 | 核心贡献 |
|:-:|---------|------|-----------|------|---------|
| 58 | Test-Time Training Done Right | Authors | arXiv 2025 | [arXiv](https://arxiv.org/abs/2505.23884) | 改进TTT的GPU利用率(提升数量级)，支持扩展非线性状态至40%模型参数 |
| 59 | End-to-End Test-Time Training for Long Context | Authors | arXiv 2025 | [arXiv](https://arxiv.org/abs/2512.23675) | 端到端TTT用于长上下文建模，128K上下文推理延迟恒定，比全注意力快2.7倍 |
| 60 | In-Place Test-Time Training (In-Place TTT) | Authors | ICLR 2025 | [OpenReview](https://openreview.net/forum?id=dTWfCLSoyl) | 将MLP最后投影矩阵作为快速权重，LLM即插即用TTT增强 |
| 61 | SICL: Towards Reliable Test-Time Adaptation: Style Invariance as a Correctness Likelihood | Authors | arXiv 2025 | [arXiv](https://www.arxiv.org/abs/2512.07390) | 风格不变性作为正确性似然的即插即用校准模块 |
| 62 | FS-TTA: Enhancing Test Time Adaptation with Few-shot Guidance | Authors | arXiv 2025 | [arXiv](https://arxiv.org/abs/2409.01341) | 少样本支持集减少盲目探索的少样本TTA |
| 63 | CSA-TTA: Cross-Sample Augmented Test-Time Adaptation for Personalized Intraoperative Hypotension Prediction | Authors | arXiv 2025 | [arXiv](https://arxiv.org/abs/2512.15762) | 跨样本增强TTA用于个性化术中低血压预测 |
| 64 | VLOD-TTA: Test-Time Adaptation of Vision-Language Object Detectors | Authors | OpenReview 2025 | [OpenReview](https://openreview.net/forum?id=7W4Gusa9rY) | 视觉语言目标检测器的TTA |
| 65 | Test-Time Adaptation of Vision-Language Models for Open-Vocabulary Semantic Segmentation | Authors | NeurIPS 2025 | [arXiv](https://arxiv.org/abs/2505.21844) | 首次将TTA扩展到密集预测开放词汇语义分割 |
| 66 | Realistic Test-Time Adaptation of Vision-Language Models | Zanella et al. | CVPR 2025 | [CVF](https://openaccess.thecvf.com/content/CVPR2025/papers/Zanella_Realistic_Test-Time_Adaptation_of_Vision-Language_Models_CVPR_2025_paper.pdf) | 现实场景下VLM的TTA |
| 67 | Source-Free Domain Adaptation for YOLO Object Detection | Authors | ECCV 2024 Workshop | [ACM](https://dl.acm.org/doi/10.1007/978-3-031-91672-4_14) | YOLO目标检测的无源域适应 |
| 68 | Test-Time Adaptation for EEG-Based Driver Drowsiness Classification | Authors | Springer 2024 | [Springer](https://link.springer.com/chapter/10.1007/978-981-97-8702-9_28) | 基于EEG的驾驶员疲劳分类TTA，含原型学习和免校准方法 |

---

## 核心趋势总结

```
新兴TTA领域发展趋势 (2024-2025)
├── 自动驾驶/机器人
│   ├── LiDAR点云TTA (MOS, HGL, APCoTTA)
│   ├── VLA测试时训练 (EVOLVE-VLA, TT-VLA)
│   └── 恶劣天气适应 (DiffTTA, MetaBN)
├── 跨模态TTA
│   ├── 音频-视觉 (AV-CTTA)
│   ├── 触觉-视觉-语言 (RobustTouch)
│   └── 缺失模态处理
├── 应用领域拓展
│   ├── 推荐系统 (TTA-GREC, T2ARec)
│   ├── 遥感/卫星 (LSCD-TTA)
│   ├── 人脸反欺骗 (3A-TTA, TTDG)
│   └── 行人重识别 (TEMP, BNTA)
├── 高效/终身TTA
│   ├── 量化模型TTA (ZOA)
│   ├── 联邦协作TTA (CoLA, Latte)
│   └── 长期TTA防崩溃 (ASR, PeTTA)
└── 元学习驱动
    ├── 元测试时训练 (MT3)
    └── 自合成元适应 (MASS)
```
