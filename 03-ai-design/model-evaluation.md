# Model Evaluation

## 1. Evaluation Objective｜测试目标

The evaluation focused on whether the model could generate communication that users could realistically send.  
测试重点是模型能否生成用户真正愿意发送的消息。

The evaluation prioritized communication quality and product-specific usability rather than general benchmark performance.  
评估重点是沟通质量和产品实际可用性，而不是通用 benchmark 表现。

| Dimension | Evaluation Focus |
|---|---|
| **Context Understanding** | Understand the user's actual communication problem |
| **Strategy Quality** | Generate meaningfully different communication strategies |
| **Naturalness** | Sound like real online communication |
| **Voice Preservation** | Match the user's communication style |
| **Relationship Sensitivity** | Adapt to relationship and power structure |
| **Reasoning Quality** | Explain why a message works |
| **Usability** | Produce messages users can realistically send |

---

## 2. Test Scenarios｜测试场景

Four representative scenarios were used to test different communication risks.  
选取四类具有代表性的沟通场景，覆盖不同类型的沟通风险。

| Scenario | Main Problem |
|---|---|
| **Family** | Refusal and face-saving |
| **Friend** | Topic boundaries |
| **Authority** | Hierarchy and fear of appearing rude |
| **Intimate / Crush** | Emotional uncertainty and restrained expression |

---

## 3. Prompt Iteration｜Prompt 迭代

| Stage | Problem Identified | Design Decision |
|---|---|---|
| **V0** | Three outputs mainly differed in wording and tone | Shift from **tone variation → strategy variation** |
| **V1** | Outputs were still too direct and generic | Introduce stronger **Persona constraints** |
| **Further iteration** | Different relationships required different communication approaches | Add **relationship / power-structure routing** |
| **Further iteration** | Generic explanations provided little value | Add **context-specific reasoning & verification** |

---

## 4. Key Findings｜核心发现

### 4.1 Strategy > Tone｜策略比语气重要

Different wording does not necessarily mean different communication strategies.  
不同措辞不等于不同沟通策略。

The model should first decide **how to approach the situation**, then generate the wording.  
模型应该先决定**如何处理这个沟通问题**，再生成具体措辞。

---

### 4.2 Persona Affects Strategy｜Persona 会影响策略

The model tended to assume a relatively confident and direct communicator.  
模型容易默认用户是比较自信、直接的沟通者。

For Murmur's target users, communication preferences such as conflict avoidance and low directness can fundamentally change the appropriate strategy.  
对于 Murmur 的目标用户，回避冲突、低直接性等沟通特征会直接影响什么策略才是合适的。

→ **Decision: Persona should influence strategy, not only surface style.**  
→ **决策：Persona 应该影响沟通策略，而不仅仅是表层措辞。**

---

### 4.3 Relationship Matters｜关系决定沟通方式

The same intention may require different strategies depending on the relationship and power structure.  
相同的沟通意图，在不同关系和权力结构下可能需要完全不同的处理方式。

→ **Decision: Introduce relationship and power-structure analysis before generation.**  
→ **决策：在生成前加入关系与权力结构分析。**

---

### 4.4 Reasoning Is Part of the Product｜理由本身就是产品价值

Users do not only need a generated message. They also need to understand why it is appropriate to send.  
用户需要的不只是生成结果，还需要知道为什么这样发是合适的。

→ **Decision: Add a verification layer explaining the communication logic and possible interpretation.**  
→ **决策：增加确认层，解释沟通逻辑和对方可能的理解方式。**

---

### 4.5 Naturalness Includes Message Format｜自然度不只是文字

Evaluation showed that sentence length, message segmentation, punctuation, and emojis can affect whether a message feels like something the user would actually send.  
测试发现，句子长度、消息分段、标点和表情等都会影响一条消息是否像用户本人会发送的内容。

→ **Decision: Treat communication format as part of Persona and Style.**  
→ **决策：将消息呈现方式纳入 Persona 与 Style。**

---

## 5. Evaluation → AI Design Decisions｜测试到 AI 设计决策

```text
Generic tone variants
        ↓
Strategy-based generation
        ↓
Persona-aware strategy
        ↓
Relationship-aware routing
        ↓
Reasoning & verification
```

The evaluation shifted Murmur from a **message generator** toward a **communication strategy system**.  
测试最终推动 Murmur 从一个**消息生成器**转向一个**沟通策略系统**。

These findings directly informed the final System Prompt and Persona Prompt architecture.  
这些发现直接影响了最终 System Prompt 与 Persona Prompt 的设计。