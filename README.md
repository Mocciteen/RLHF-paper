### RLHF paper

---

#### RLHF

**综述**

**A Survey of Reinforcement Learning from Human Feedback** 202404 [paper](https://arxiv.org/pdf/2312.14925)

最先提出这一概念的相关文章：

**Deep Reinforcement Learning from Human Preferences** NIPS2017 [paper](https://arxiv.org/pdf/1706.03741)

**Fine-Tuning Language Models from Human Preferences** OPENAI2019 [paper](https://arxiv.org/pdf/1909.08593):将自然语言处理的模型预训练与人类偏好学习相结合，是 RLHF 的雏形方案

**Learning to summarize from human feedback** NeurIPS2020 [paper](https://arxiv.org/pdf/2009.01325):初步在摘要任务中引入人类反馈和强化学习

**Training language models to follow instructions with human feedback** NeurIPS2022 [paper](https://arxiv.org/pdf/2203.02155):使用RLHF微调GPT3，得到InstructGPT

**Training a Helpful and Harmless Assistant with Reinforcement Learning from Human Feedback** 202204 [paper](https://arxiv.org/pdf/2204.05862)
 
---

**理论：**

**Is RLHF More Difficult than Standard RL? A Theoretical Perspective** NeurIPS2023 [paper](https://arxiv.org/pdf/2306.14111)

**Exploration-Driven Policy Optimization in RLHF: Theoretical Insights on Efficient Data Utilization** ICML2024 [paper](https://arxiv.org/pdf/2402.10342):基于轨迹的比较反馈来推断奖励函数,使用基于策略优化的 RLHF 算法并且分析该算法的复杂度边界

**Iterative Preference Learning from Human Feedback: Bridging Theory and Practice for RLHF under KL-constraint**ICLR2024 [paper](https://arxiv.org/pdf/2312.11456):研究LLM与RLHF对齐过程，理解 RLHF 的数学原理

**RLHF Deciphered: A Critical Analysis of Reinforcement Learning from Human Feedback for LLMs** 202404 [paper](https://arxiv.org/pdf/2404.08555)

**Understanding the Learning Dynamics of Alignment with Human Feedback** ICML2024 [paper](https://arxiv.org/pdf/2403.18742)

---

RLHF基础上进行相关改进

**Confronting Reward Model Overoptimization with Constrained RLHF** ICLR2024 [paper](https://arxiv.org/pdf/2310.04373):RM的不稳定性可能导致过度优化问题，引入带约束的强化学习，保证每个 RM 都保持在其作为有效代理的范围内

**Iterative Data Smoothing: Mitigating Reward Overfitting and Overoptimization in RLHF** ICML2024 [paper](https://arxiv.org/pdf/2401.16335):在模型训练中不断更新数据的标签作为新的数据集，从而优化奖励模型学习效果

**Principled Penalty-based Methods for Bilevel Reinforcement Learning and RLHF** ICML2024 [paper](https://openreview.net/pdf?id=Xb3IXEBYuw)

**RLAIF vs. RLHF: Scaling Reinforcement Learning from Human Feedback with AI Feedback** ICML2024 [paper](https://arxiv.org/pdf/2309.00267)

**Balancing Individual Preferences and Shared Objectives in Multiagent Reinforcement Learning** IJCAI2020 [paper](https://www.ijcai.org/proceedings/2020/0347.pdf)

**MaxMin-RLHF: Alignment with Diverse Human Preference** ICML2024 [paper](https://openreview.net/attachment?id=8tzjEMF0Vq&name=pdf)

**Mapping Social Choice Theory to RLHF** ICLR2024 [paper](https://arxiv.org/pdf/2404.13038)

**PERSONALIZED SOUPS: PERSONALIZED LARGE LANGUAGE MODEL ALIGNMENT VIA POST-HOC PARAMETER MERGING** 202310 [paper](https://arxiv.org/pdf/2310.11564):将偏好分解为多个维度来实现个性化对齐

**RLHF Can Speak Many Languages: Unlocking Multilingual Preference Optimization for LLMs** [paper](https://arxiv.org/pdf/2407.02552)

**Reinforcement Learning from Human Feedback with Active Queries** 202402 [paper](https://arxiv.org/pdf/2402.09401):引入主动学习，主动选择可以给予较大信息量的数据对，作为训练策略的数据集

---

一种高效且经典的改进方法:**DPO**

绕开奖励函数的设置直接优化，降低复杂度

**Direct Preference Optimization: Your Language Model is Secretly a Reward Model** NeurIPS2023 [paper](https://arxiv.org/pdf/2305.18290)
:
**Reward Model Learning vs. Direct Policy Optimization: A Comparative Analysis of Learning from Human Preferences** ICML2024 [paper](https://arxiv.org/pdf/2403.01857):系统地比较 RLHF 与 DPO 范式

**Contrastive Preference Optimization: Pushing the Boundaries of LLM Performance in Machine Translation** ICML2024 [paper](https://arxiv.org/pdf/2401.08417):对数据的偏好可以视作一种对比学习，简化了损失函数的计算

**Generalized Preference Optimization: A Unified Approach to Offline Alignment** ICML2024 [paper](https://arxiv.org/pdf/2402.05749):给出偏好优化的广义视图，将DPO、IPO等情况包含其中

**Provably Robust DPO: Aligning Language Models with Noisy Feedback** ICML2024 [paper](https://arxiv.org/pdf/2403.00409):改善DPO中的损失函数，消除噪声影响的偏差

**Token-level Direct Preference Optimization** ICML2024 [paper](https://arxiv.org/pdf/2404.11999):将KL散度对齐为tokens级别，加入正向 KL 发散约束，从而提高了对齐和多样性

---

#### human preference

采取其他方法实现对人类偏好的学习

**Position: Social Choice Should Guide AI Alignment in Dealing with Diverse Human Feedback**

**Linear Alignment: A Closed-form Solution for Aligning Human Preferences without Tuning and Feedback**

**Human Alignment of Large Language Models through Online Preference Optimisation**

**Rewards-in-Context: Multi-objective Alignment of Foundation Models with Dynamic Preference Adjustment**

**Coactive Learning for Large Language Models using Implicit User Feedback**

**Pragmatic Feature Preferences: Learning Reward-Relevant Preferences from Human Input**

**Active Preference Learning for Large Language Models**

**CONTRASTIVE PREFERENCE LEARNING: LEARNING FROM HUMAN FEEDBACK WITHOUT RL** ICLR2024 [paper](https://openreview.net/pdf?id=iX1RjVQODj)

**Quality Diversity through Human Feedback: Towards Open-Ended Diversity-Driven Optimization**

**A State Augmentation based approach to Reinforcement Learning from Human Preferences**

**Dueling RL: Reinforcement Learning with Trajectory Preferences**

**Balancing Individual Preferences and Shared Objectives in Multiagent Reinforcement Learning**

**LaMP: When Large Language Models Meet Personalization**

**Aligning LLM Agents by Learning Latent Preference from User Edits**
