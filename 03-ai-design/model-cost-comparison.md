# Model Comparison

## 1. Models Compared｜模型比较

The main models considered during prototype development were gpt-oss-20b, gpt-oss-120b, Gemini 2.5 Flash, DeepSeek, and lightweight GPT models.  
原型开发阶段主要考虑了 gpt-oss-20b、gpt-oss-120b、Gemini 2.5 Flash、DeepSeek 以及轻量级 GPT 模型。

| Model | Relative Strength | Main Trade-off |
|---|---|---|
| **gpt-oss-20b** | Low cost, fast iteration | Weaker performance in complex communication |
| **gpt-oss-120b** | Stronger reasoning and contextual understanding | Higher cost and latency |
| **Gemini** | Natural and emotionally expressive | Not necessarily optimal for rule-sensitive tasks |
| **DeepSeek** | Balanced reasoning and emotional understanding | Model choice depends on task and cost |
| **Lightweight GPT** | Conservative and controllable | Less expressive in emotional conversations |

---

## 2. Demo-stage Decision｜Demo 阶段决策

For the current Demo, **Gemini 2.5 Flash** was selected as the primary model.  
当前 Demo 阶段最终选择 **Gemini 2.5 Flash** 作为主要模型。

The decision was based on the practical balance between output quality, naturalness, response speed, and cost.  
选择主要基于输出质量、自然度、响应速度和成本之间的实际平衡。

The total model testing cost was kept below **¥5**.  
整个模型测试阶段的成本控制在 **¥5 以内**。

**Demo model → Gemini 2.5 Flash**

---

## 3. Why Hybrid Models for Production?｜为什么正式产品采用混合模型

A single model does not need to handle every communication problem.  
一个模型没有必要承担所有类型的沟通问题。

Different communication scenarios emphasize different capabilities, such as emotional expression, contextual reasoning, or social-risk control.  
不同沟通场景对模型能力的要求不同，例如情绪表达、上下文推理和社交风险控制。

Therefore, the production architecture could route different tasks to different models according to their strengths.  
因此，正式产品阶段可以根据不同模型的优势，将不同任务路由给不同模型。

---

## 4. Proposed Hybrid Model Strategy｜混合模型策略

| Model Role | Model Candidate | Core Strength | Suitable Scenarios |
|---|---|---|---|
| **Emotion-oriented communicator** | Gemini | Natural, human-like expression | Intimate relationships, emotional reassurance |
| **Balanced reasoning model** | DeepSeek | Reasoning + emotional understanding | Complex context, strategy generation |
| **Social-rule executor** | Lightweight GPT | Conservative and controllable | Authority communication, boundary checks, high-risk wording |

These roles are capability-based rather than permanently tied to specific models.  
这些角色是根据模型能力定义的，并不意味着未来必须永久绑定某一个具体模型。

As model capabilities and API costs change, the routing strategy can be updated accordingly.  
随着模型能力和 API 成本变化，具体的模型路由也可以持续调整。

---

## 5. Model Routing｜模型路由

```text
User Input
    ↓
Scenario & Communication Risk Detection
    ↓
┌───────────────────────────────┐
│ Emotional / Intimate          │
│ → Emotion-oriented Model      │
│                               │
│ Complex / Ambiguous           │
│ → Balanced Reasoning Model    │
│                               │
│ Authority / High-risk         │
│ → Social-rule Executor        │
└───────────────────────────────┘
    ↓
Response Generation
    ↓
Verification
    ↓
User Decision
```

The goal is not to identify one universally “best” model, but to match model capabilities with different communication requirements.  
目标不是找到一个适用于所有场景的“最佳模型”，而是让不同模型的能力与不同沟通需求匹配。

---

## 6. Final Decision｜最终决策

| Product Stage | Model Strategy | Decision |
|---|---|---|
| **Demo** | Single primary model | **Gemini 2.5 Flash** |
| **Production** | Hybrid model architecture | **Scenario-based model routing** |

The Demo prioritizes fast validation of the core product experience.  
Demo 阶段优先验证核心产品体验。

The production direction is to use a hybrid architecture to balance **communication quality, safety, latency, and cost**.  
正式产品阶段则通过混合模型架构平衡**沟通质量、安全性、响应速度和成本**。
