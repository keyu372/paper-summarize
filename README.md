# 轻量-VLA/WAM-Project


---


TKY License · Last commit: [2026.3.21] · PRs Welcome · Stars [666]  

---

- 正在探索 [如具身智能 VLA/轻量化VLA/轻量WAM]  
  

---

## 目录

- [简介](#简介)
- [论文分类](#论文分类)
  - [VLA](#VLA)
  - [WAM](#WAM)
- [数据集与工具](#数据集与工具)
- [贡献指南](#贡献指南)
- [引用](#引用)
- [许可](#许可)

---

## 简介

本仓库提供了一份全面且持续更新的 [VLA/轻量VLA/轻量WAM] 论文与资源列表，旨在帮助研究人员快速了解该方向的核心进展与前沿动态。

---

## 论文分类

### VLA
| 论文标题 | 会议/期刊 | 年份 | 核心 |
|---------|---------|------|------|
| Beyond Attention Magnitude: Leveraging Inter-layer Rank Consistency for Efficient Vision-Language-Action Models( https://arxiv.org/abs/2603.24941) | arXiv Preprint | 2025 | 挑战高注意力 token 更重要的默认假设，用层间秩一致性 (Kendall τ) 动态判断何时该信任注意力，实现 78% token 削减的同时性能反升 6%。  |
| SP-VLA: A  JOINT MODEL SCHEDULING AND TOKEN PRUNING APPROACH FOR VLA  MODEL  ACCELERATION(https://arxiv.org/abs/2506.12723) | ICLR | 2025 | 引入轻量级生成器，通过协同模型调度实现频率自适应执行；空间-语义双感知标记剪枝方法，将标记划分为空间型和语义型，并根据其双感知重要性进行剪枝以加速VLA推理 |
| Sparse ActionGen: Accelerating Diffusion Policy with Real-time Pruning(https://icml.cc/virtual/2026/poster/65503) | ICML | 2026 | SAG提出了一种动态适应的、参数化的、“全包含复用”的实时扩散剪枝器 |
| Token Expand-Merge: Training-Free Token Compression for Vision-Language-Action Models(https://ieeexplore.ieee.org/abstract/document/11560913) | IEEE Robotics and Automation Letters   |  2026  |   TEAM-VLA通过相似度驱动的令牌扩展将稀疏视觉-语言线索重建为密集前景区域，提升上下文的完整性。再以动作引导的软二分法合并压缩深层令牌，有效降低冗余度。全程无需训练、无需跨帧缓存，且语言与动作令牌完整保留  |
| ACTION-AWARE DYNAMIC PRUNING FOR EFFICIENT VISION-LANGUAGE-ACTION MANIPULATION( https://iclr.cc/virtual/2026/poster/10008304) |   ICLR   |  2026     |  VLA-ADP是一种即插即用的剪枝框架，它将基于文本的预测性剪枝与动作感知动态策略相结合，在保持可靠性的前提下加速VLA推理。|
| Realtime-VLA FLASH: Speculative Inference Framework for Diffusion-based VLAs(https://arxiv.org/abs/2605.13778) |  arXiv Preprint     |    2026    |   提出了一种推测性推理框架：通过引入轻量级草稿生成模型并借助主模型的动作专家模块进行并行验证，同时配备相位感知回退机制（必要时可切换至完整推理流程），该框架的动作规划相比于完整推理，所需的计算量大大减少    |
| LA4VLA: Learning to Act without Seeing via Language-Action Pretraining(https://arxiv.org/abs/2606.27295) |    arXiv Preprint   |  2026    |     LA4VLA 框架，通过从现有演示数据中构建不依赖视觉的原子指令-动作数据集 LA-33K 进行语言-动作预训练，使模型建立了语言与动作的关联，提升了 VLA 模型在模拟与真实场景中的性能、跨架构迁移能力和视觉鲁棒性。   |
| Environment-Aware Adaptive Pruning with Interleaved Inference Orchestration for Vision-Language-Action Models( https://arxiv.org/abs/2602.00780) | ICML | 2026 |   Eco-VLA根据环境变化动态剪枝模型参数，并通过在动作生成的同时并行调度剪枝策略的方法，确保剪枝策略对延迟的影响可忽略不计。  |
| EfficientVLA: Training-Free Acceleration and Compression for Vision-Language-Action Models(https://proceedings.neurips.cc/) |   NeurIPS  |  2025     |      |
| The Better You Learn, The Smarter You Prune: Towards Efficient Vision-language-action Models via Differentiable Token Pruning(https://arxiv.org/abs/2509.12345) |  arXiv Preprint |   2025  |  |
### WAM
| 论文标题 | 会议/期刊 | 年份 | 链接 |
|---------|---------|------|------|
| Fast-WAM: Do World Action Models Need Test-time Future Imagination?(https://arxiv.org/abs/2603.16666) | arXiv Preprint | 2026 | WAM的核心能力来源可能并不是future video prediction在推理阶段为action expert 提供指导，而是在训练阶段发挥proxy task 的作用，提供更丰富的监督信号，帮助 backbone 学到更好的表征。 |
| Efficient-WAM: A 1B-Parameter World-Action Model with Low-Cost Future Imagination(https://arxiv.org/abs/2606.12345) | arXiv Preprint  |  2026  |  Efficient-WAM的核心是“以行动为中心”，模型不需要生成逼真的视频，只需提取未来场景中与任务相关的几何结构、运动趋势和接触线索，作为引导动作生成的紧凑信号即可。  |

---

## 数据集与工具

- [数据集名称](链接) - 简短描述
- [工具库名称](链接) - 简短描述

---

## 贡献指南

我们非常欢迎你的贡献！请通过 Pull Request 提交新的论文或资源，并确保遵循以下格式：

- 论文按会议/年份排序
- 提供论文标题、作者、链接、代码（如有）
- 新增内容请放入对应分类中

感谢你的支持！

---

## 引用

如果你在研究中使用了本仓库，欢迎引用：

```bibtex
@misc{your-project-name,
  author = {Your Name},
  title = {Awesome Your Project Name},
  year = {2025},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/your-repo-link}}
}
