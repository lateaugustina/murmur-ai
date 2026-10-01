# System Prompt Design

## 1. Prompt Architecture｜Prompt 分层架构

The prompt is structured into separate layers to distinguish stable user characteristics, current context, and task-specific instructions.  
Prompt 被拆分为不同层级，用于区分用户长期特征、当前情境和本次任务。

```text
User Input
    ↓
System Layer
    → Product role
    → Core rules
    → Output requirements
    ↓
Persona Layer
    → Stable communication characteristics
    → Contextual preferences
    → Relationship-specific preferences
    → Expression style
    → Recent memory
    ↓
Task Layer
    → Current relationship
    → Communication goal
    → Emotional concern
    → Rough thought / existing draft
    ↓
Scenario & Relationship Analysis
    ↓
Communication Strategy
    ↓
Response Generation
    ↓
Explanation & Verification
    ↓
User Decision
```

---

## 2. System Layer｜规则层

The System Layer defines the model's general behavior and output principles.  
System Layer 定义模型的基本行为和输出原则。

| Design Element | Instruction |
|---|---|
| **Role** | Act as a communication copilot rather than a generic writing assistant. |
| **Strategy** | Identify the communication problem before generating wording. |
| **Context** | Consider relationship, power structure, intimacy, and social risk. |
| **User Voice** | Preserve the user's natural communication style. |
| **Usability** | Generate messages that users could realistically send. |
| **Explanation** | Explain why a strategy works instead of giving generic reassurance. |
| **Decision** | Support the user's decision without making it for them. |
| **Quality** | Prefer sufficiently good and natural communication over overly polished wording. |

### Core Rule

**Strategy before wording.**  
**先确定沟通策略，再生成具体措辞。**

```text
User Intention
      ↓
Communication Problem
      ↓
Relationship / Risk Analysis
      ↓
Communication Strategy
      ↓
Wording
      ↓
Reasoning & Verification
```

---

## 3. Persona Layer｜人格层

The Persona Layer translates long-term user characteristics into communication preferences.  
Persona Layer 将用户长期稳定的特征转化为具体的沟通偏好。

### 3.1 Four-Layer Structure｜四层结构

| Layer | Purpose | Examples |
|---|---|---|
| **Core Persona** | Stable communication tendencies | Directness, conflict avoidance, sensitivity |
| **Context Layer** | Preferences under different contexts | Authority, family, friends, intimate relationships |
| **Relationship Layer** | Preferences toward specific people | Formality, intimacy, power structure |
| **Style Layer** | Observable expression habits | Sentence length, punctuation, emojis, particles, message segmentation |
| **Memory Layer** | Recent relevant behavior | Recent communication patterns or preferences |

> Memory Layer is treated as supporting context rather than a permanent personality trait.  
> Memory Layer 用于提供近期相关信息，而不是直接定义用户人格。

---

## 4. Decision Weighting｜决策权重

Persona information should be treated as weighted preferences rather than a flat list of traits.  
Persona 信息应该作为有权重的偏好，而不是简单的信息列表。

### Example

| Preference | Weight |
|---|---|
| Conflict Avoidance | High |
| Need for Social Safety | High |
| Directness | Low |
| Refusal Ability | High |
| Formality | Context-dependent |

### Priority Order

```text
User Intention
      >
Relationship & Power Structure
      >
Communication Risk
      >
Persona Preferences
      >
Surface Style
```

This prevents surface-level style preferences from overriding the user's actual communication goal.  
这样可以避免表层风格偏好覆盖用户真正的沟通目标。

---

## 5. Relationship Decision Tree｜关系决策

The same wording should not be applied uniformly across different relationships.  
同一种表达方式不应该被机械地应用于不同关系。

| Relationship | Default Strategy |
|---|---|
| **Authority** | Conservative, respectful, context-sensitive |
| **Friend** | Casual, natural, flexible |
| **Family** | Consider existing dynamics and face-saving |
| **Intimate / Crush** | Lower pressure, emotionally sensitive, avoid unnecessary directness |

Relationship should be interpreted together with power structure and emotional risk.  
关系类型需要与权力结构和情感风险结合判断。

```text
Relationship
    +
Power Structure
    +
Intimacy
    +
Social Risk
    ↓
Communication Strategy
```

---

## 6. Communication Strategy｜沟通策略

Early versions generated three outputs mainly by changing tone.  
早期版本主要通过改变语气生成三个版本。

This resulted in outputs that looked different but often used the same underlying strategy.  
这种方式导致三个版本看起来不同，但底层沟通策略往往没有真正变化。

The design was therefore changed from **tone variation** to **strategy variation**.

因此，设计从“语气差异”改为“沟通策略差异”。

| Strategy | Purpose |
|---|---|
| **Conservative** | Minimize social risk and preserve the relationship |
| **Natural / Balanced** | Balance authenticity and social appropriateness |
| **Restrained / Boundary-setting** | Express the user's position more clearly while remaining socially acceptable |

The three options should represent different ways of solving the communication problem, not merely different wording.  
三个选项应该代表不同的沟通解决方式，而不只是不同的措辞。

---

## 7. Verification Layer｜确认层

Generation alone does not fully address the user's uncertainty.  
单纯生成消息无法完全解决用户的沟通不确定感。

The model therefore needs to explain why the suggested message is appropriate.  
因此模型还需要解释为什么这条消息适合发送。

| Verification Question | Purpose |
|---|---|
| **Why does this work?** | Explain the communication strategy |
| **How might the recipient interpret it?** | Reduce uncertainty about the other person's possible interpretation |
| **What risk does it avoid?** | Explain the social trade-off |
| **Is there unnecessary wording?** | Prevent over-explaining or artificial language |

A useful output structure is:

```text
Message
    ↓
Why it works
    ↓
Possible interpretation
    ↓
Risk / ambiguity check
```

The explanation should be specific rather than generic reassurance.  
解释应该具体，而不是简单地说“这样发没问题”。

---

## 8. Few-shot Design｜Few-shot 设计

Few-shot examples are used to teach communication behavior and strategy, rather than only surface wording.  
Few-shot 示例用于教模型理解沟通行为和策略，而不仅仅是模仿语言表面形式。

| Scenario | Desired Behavior |
|---|---|
| **Authority** | Respect hierarchy while avoiding excessive deference |
| **Friend** | Maintain natural conversational flow and boundaries |
| **Family** | Consider face-saving and practical consequences |
| **Intimate / Crush** | Preserve emotional subtlety and reduce pressure |

Examples should demonstrate the difference between:

```text
What the user genuinely wants to say
                ≠
What the recipient wants to hear
```

Murmur should prioritize the user's genuine intention.  
Murmur 应优先保留用户真实想表达的内容。

---

## 9. Token Control｜Token 控制

The Persona Layer should contain only high-signal information.  
Persona Layer 只保留高信息量内容。

**Target range: 300–800 tokens**

| Risk | Why it matters |
|---|---|
| **Attention dilution** | Too much information reduces the relative importance of key preferences. |
| **Preference conflict** | Multiple characteristics may contradict each other. |
| **Style drift** | Excessive persona information can produce an artificial “average persona”. |

The goal is **high-signal personalization**, not maximum personalization.  
目标是**高信号密度的个性化**，而不是最大化个性化。

---

## 10. Prompt Iteration｜Prompt 迭代

The main iteration was a shift from **surface-level tone control** to **communication strategy modeling**.  
核心迭代是从“表层语气控制”转向“沟通策略建模”。

| Stage | Problem | Design Change |
|---|---|---|
| **V0** | Three outputs were mostly wording variations | Introduced explicit strategy differentiation |
| **V1** | Outputs still assumed a relatively confident user | Introduced stronger Persona constraints |
| **Later iteration** | Generic explanations provided little value | Added reasoning and verification |
| **Scenario refinement** | Different relationships required different strategies | Added relationship and power-structure routing |

### Resulting Architecture

```text
Scenario Understanding
        ↓
Persona & Relationship Analysis
        ↓
Communication Strategy
        ↓
Strategy-based Generation
        ↓
Explanation & Verification
        ↓
User Decision
```

This architecture became the basis for subsequent model evaluation.  
这一架构成为后续模型测试的基础。