# OpenAI 面经合集

> OpenAI 面试经验整理，涵盖 Research、Engineering 等方向。

## 面试流程概述

OpenAI 面试通常包含：

1. ** Recruiter Screen**（30分钟）— 初步沟通，了解背景和意向
2. **Technical Screen**（45-60分钟）— 技术面试，含 coding 或 research discussion
3. **Onsite/ Virtual Onsite**（4-5轮，每轮45-60分钟）— 深度技术面 + 系统设计 + Research
4. **Team Matching** — 匹配合适团队
5. **Final Review** — Hiring Committee 审核

## 面经列表

| 日期 | 岗位 | 轮次 | 链接 |
| :--- | :--- | :--- | :--- |
| 待补充 | Member of Technical Staff | Technical Screen | - |
| 待补充 | Research Engineer | Onsite | - |
| 待补充 | Research Scientist | Onsite | - |

## 高频考点

### Engineering 方向
- 系统设计（大规模 ML serving、分布式训练）
- 编程能力（Python / C++，算法与数据结构）
- ML 基础（模型训练、推理优化、分布式系统）
- LLM 相关（训练 pipeline、推理加速、RAG 系统）

### Research 方向
- 深度学习理论（Transformer、扩散模型、RLHF）
- 论文讨论（近期顶会论文 reading）
- Research proposal / 开放性问题
- Coding 实现（从论文到代码复现）

## 面试经验

> 以下为真实面经整理，投稿请使用 [面经模板](../../templates/面经模板.md)。

### 样例面经：Member of Technical Staff — Technical Screen

**基本信息**
- 公司：OpenAI
- 岗位：Member of Technical Staff (Engineering)
- 轮次：Technical Screen
- 形式：视频面（Zoom）
- 时长：约 60 分钟

**面试流程**

1. Intro & background（5分钟）
2. Coding / System Design（40分钟）
3. Experience deep dive（10分钟）
4. Q&A（5分钟）

**Technical Questions**

1. **Q: Design a system to serve GPT models at scale. How would you handle batching, caching, and rate limiting?**
   - A: 讨论 continuous batching（Orca/vLLM），KV cache 管理（PagedAttention），prefix caching，以及 token-level rate limiting。

2. **Q: Implement a tokenizer from scratch (BPE algorithm).**
   - A: 从语料统计 pair frequency，合并最高频 pair，重复直到达到 vocab size。实现 merge 规则的编码和解码。

3. **Q: How does RLHF work? Walk through the pipeline.**
   - A: SFT → Reward Model 讌练 → PPO/RLHF optimization。讨论 reward hacking 问题 and DPO as alternative。

**经验总结**

- OpenAI 面试很注重 practical engineering 和 research 的结合
- Coding 不是纯 LeetCode 风格，更偏向 ML 系统实现
- 对 LLM 底层原理的理解很重要（tokenization、attention、sampling）
- 英文沟通能力是基本要求
- 建议读 recent papers 并能讨论细节

---

> 📌 欢迎投稿你的 OpenAI 面经！请使用 [面经模板](../../templates/面经模板.md) 提交 PR。
