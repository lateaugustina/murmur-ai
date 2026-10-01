# User Insights Report

> Initial synthesis based on 108 real-world communication samples.  
> 基于 108 条真实沟通语料形成的初步研究综合。
>
> Version: V1.0 · Before User Interviews  
> 版本：V1.0 · 用户访谈前

## Core Insight｜核心洞察

Users are not necessarily unable to communicate. In high emotional-risk situations, they often lose confidence in their own judgment. What they need is not simply a writing tool, but an always-available source of communication confirmation.

用户不是不会沟通，而是在高情感风险时刻对自己的判断力失去信任。他们需要的不是单纯的写作工具，而是一个随时在线的「确认者」。

---

## 1. Core User Profiles｜核心用户画像

| Profile 画像 | Description 描述 | Core Need 核心需求 | Representative Scenarios 代表场景 |
|---|---|---|---|
| **A. High-Pressure Communicators / 高压表达者** | Communication anxiety in authority relationships such as advisors, managers, or teachers. They repeatedly check messages but still cannot press send. / 主要在导师、领导、老师等权威关系中产生沟通焦虑，反复检查消息却迟迟无法发送。 | Confirmation rather than repeated rewriting. / 确认，而不只是继续改稿。 | Sending progress updates to advisors, asking managers for leave, repairing inappropriate wording. / 给导师发进度、给领导请假、措辞不当后的补救。 |
| **B. Emotionally Sensitive Communicators / 情感高敏者** | Anxiety in crushes and intimate relationships. The more they care, the more they overinterpret messages and responses. / 主要在 crush 和亲密关系中产生焦虑，越在意越容易过度解读消息和回复。 | External confirmation before sending and emotional buffering after sending. / 发送前的外部确认，以及发送后的情绪缓冲。 | Initiating contact, waiting for replies, reconnecting after silence. / 主动联系、等待回复、断联后复联。 |
| **C. Socially Depleted Communicators / 精力枯竭者** | Replying itself becomes a burden. They value relationships but lack the energy to maintain conversations. / 回复本身已经成为负担，珍惜关系却没有足够精力维持沟通。 | Low-cost communication that helps maintain relationships. / 以最低成本维持关系。 | Receiving messages when exhausted, prolonged non-response, maintaining relationships during low-energy periods. / 精力耗尽时收到消息、长期不回复、低能量状态下维持关系。 |

---

## 2. User Boundaries｜用户边界

Murmur is not primarily designed for:

1. People who have lost interest in social interaction and do not want to communicate.  
   对社交本身失去兴趣、没有沟通动机的人。

2. People whose problem is “I do not want to contact them” rather than “I want to contact them but do not know how to say it.”  
   问题是「不想联系」，而不是「想联系但不知道怎么说」的人。

3. People requiring clinical psychological intervention for severe social anxiety.  
   需要临床心理干预的重度社交焦虑人群。

---

## 3. Psychological Mechanisms & Feature Priorities｜核心心理机制与功能优先级

| Priority 优先级 | Psychological Mechanism 心理机制 | Evidence / User Pattern 用户表现 | Feature Direction 功能方向 |
|---|---|---|---|
| **P0** | **Pre-Send Anxiety / 发送前焦虑 ★★★★★** | Users already have an idea or draft but cannot confidently send it. / 已经有想法甚至写好草稿，却无法确认自己是否可以发送。 | Draft checking + “This is okay to send because…” confirmation. / 审阅草稿 +「这样发可以，因为……」的确认。 |
| **P0** | **Authority Communication Pressure / 权威沟通压力 ★★★★★** | Strong concern about wording and evaluation when communicating with advisors, managers, or teachers. / 面对导师、领导、老师时高度关注措辞是否合适以及是否影响评价。 | Authority-context understanding + safe wording generation + confirmation. / 识别权威关系 + 安全表达生成 + 发送确认。 |
| **P0** | **Relationship Initiation Anxiety / 关系发起焦虑 ★★★★** | Users want to initiate or restart contact but become stuck on the first sentence. / 想主动联系或重新联系某人，却卡在第一句话。 | Context-aware opening generation + reassurance. / 结合关系背景生成自然开场 + 发送确认。 |
| **P1** | **Post-Send Anxiety / 发送后焦虑 ★★★★** | Waiting after sending can trigger repeated interpretation of silence and response timing. / 发送后的等待阶段容易反复解读沉默和回复速度。 | Expectation calibration + response interpretation + post-send support. / 预期校准 + 回复解读 + 发送后支持。 |
| **P1** | **Social Energy Depletion / 社交精力耗竭 ★★★** | Replying itself becomes an emotional and cognitive burden. / 回复本身成为情绪和认知负担。 | Minimum-effort relationship maintenance. / 最低成本的关系维护。 |

### Underlying Mechanisms｜底层机制

These mechanisms help explain user behavior but are not treated as independent feature directions.

以下机制主要用于理解用户行为，不直接对应独立功能方向。

- **Group Visibility Anxiety / 群体可见性焦虑** — Fear of being evaluated when speaking in group-visible situations.  
  在群聊或多人可见场景中发言时产生的被审判感。

- **Self-Presentation Pressure / 自我呈现压力** — Treating communication as a performance that may be judged by others.  
  将沟通视为一种可能被他人评价的自我呈现。

---

## 4. Core Use Cases｜核心使用场景

| Priority | Scenario 场景 | User Situation 用户处境 | Murmur Intervention Murmur 介入 |
|---|---|---|---|
| **P0** | Authority message cannot be sent / 权威消息发不出去 | User has written the message but cannot press send. / 已经写好消息，却无法按下发送键。 | Check the draft and explain why it is okay to send. / 审阅草稿并解释为什么可以发送。 |
| **P0** | First message after a long silence / 断联后复联第一句 | User wants to reconnect but is stuck on the opening. / 想复联，却卡在第一句话。 | Generate a natural opening with contextual reassurance. / 生成自然开场并提供发送确认。 |
| **P0** | Replying to an authority figure / 收到权威回复不知道怎么回 | User receives a message from an advisor or manager and does not know how to respond. / 收到导师或领导消息，不知道怎么回复。 | Interpret the message and generate a reply. / 解读对方消息并生成回复。 |
| **P1** | Refusing someone / 需要拒绝但不敢打开聊天框 | User wants to refuse but avoids opening the conversation. / 想拒绝，却连聊天框都不敢打开。 | Prepare the refusal before opening the conversation. / 先准备好拒绝消息，再去发送。 |
| **P1** | Repairing an inappropriate message / 说错话需要补救 | User worries that a word or expression was inappropriate after sending. / 发出后发现措辞不合适并产生焦虑。 | Generate a repair message and explain the strategy. / 生成补救消息并解释处理方式。 |

---

## 5. Competitors & User Workarounds｜竞品与用户 Workaround

| Current Solution 用户现在怎么做 | Limitation 局限 | Murmur Opportunity Murmur 机会 |
|---|---|---|
| **Xiaohongshu / Reddit guides / 小红书、Reddit 攻略** | Not personalized; users still need to adapt the answer. / 不够个性化，仍需自己修改。 | Generate directly from the user's situation. / 根据具体情境直接生成。 |
| **Friends / 找朋友审稿、代看、代回** | Not always available; privacy and social cost. / 不一定随时在线，存在隐私和社交成本。 | Private and always available. / 私密、随时可用。 |
| **ChatGPT / DeepSeek** | Users need to organize and explain the situation first. / 用户需要先整理并描述自己的问题。 | Accept rough thoughts and incomplete input. / 接受粗糙想法和不完整输入。 |
| **Notes / 备忘录** | No intelligent support. / 只有空白文档，没有智能支持。 | Combine drafting with AI support. / 在起草基础上提供 AI 支持。 |
| **Force-send / 硬撑发出** | Anxiety may remain after sending. / 发送后的焦虑仍然存在。 | Confirmation before sending. / 发送前提供确认。 |
| **Delayed or late-night replies / 延迟或半夜回复** | Treats the symptom rather than the communication problem. / 治标不治本。 | Generate low-cost, complete responses. / 生成低成本但完整的回复。 |

### Key Competitive Insight｜关键竞品洞见

General AI has already entered users' communication workflows. However, anxious users may struggle to clearly explain their situation and needs to AI in the first place.

通用 AI 已经进入用户的沟通辅助工作流，但焦虑状态下的用户可能连「如何把自己的问题讲清楚」都存在困难。

Murmur's potential differentiation therefore lies not only in output quality, but also in reducing the input threshold.

因此，Murmur 的潜在差异化不只是生成质量，也在于降低用户的输入门槛。

---

## 6. Product Philosophy｜产品哲学

### Murmur Is｜Murmur 是

A communication support tool that helps users express what they genuinely want to say more clearly, appropriately, and confidently.

帮助用户把自己真正想说的话表达得更清晰、更合适、更有信心的沟通支撑工具。

### Murmur Is Not｜Murmur 不是

- A people-pleasing or performance tool / 帮用户说对方想听的话的表演工具
- A communication decision-maker / 替用户做沟通决策的代理人
- A psychological treatment tool / 解决依恋类型或自我价值问题的心理工具
- A reminder tool / 催用户回消息的提醒工具
- A communication training platform / 让用户成为「沟通高手」的训练平台

### Product Test｜产品检验标准

If the generated message makes the user think “This is not something I would say,” the feature is wrong.

如果生成的消息让用户觉得「这不是我会说的话」，这个功能就是错的。

The desired reaction is:

> “Yes, this is what I wanted to say. I just couldn't say it myself.”

> 「对，这就是我想说的，只是我自己说不出来。」

---

## 7. Five Core Hypotheses｜五个核心假设

These hypotheses were derived from the corpus and became the basis for the subsequent user interviews.

以下假设均来自前期语料分析，并作为后续用户访谈的主要验证方向。

| Hypothesis 假设 | What We Need to Validate 需要验证什么 | Validation Method 验证方法 |
|---|---|---|
| **H1. Usage Timing / 使用时机** | Users will think of opening an independent communication tool rather than first asking friends or searching online. / 用户是否会想到打开独立工具，而不是第一反应去问朋友或搜索攻略。 | Ask: “What was the first thing you did the last time this happened?” / 问：「上次遇到这种情况，你第一个动作是什么？」 |
| **H2. Input Threshold / 输入门槛** | Low input friction may matter more than output quality. / 低输入门槛是否比高输出质量更重要。 | Ask users to describe a recent real communication difficulty and observe how they naturally express it. / 让用户描述真实沟通困境，观察其自然表达方式。 |
| **H3. AI Resistance / AI 抵触度** | Users may have limited psychological resistance to AI-assisted message writing. / 用户对 AI 帮写消息的心理抵触是否较低。 | Ask: “If someone knew you used AI to help write a message, would you mind?” / 问：「如果别人知道你用 AI 帮你写消息，你会介意吗？」 |
| **H4. Post-Send Reassurance / 发送后安抚价值** | Post-send reassurance may provide meaningful value rather than being an optional add-on. / 发送后的安抚是否具有真实价值，而不只是附加功能。 | Ask: “How do you usually feel after sending a difficult message, and how long does it last?” / 问：「发完一条困难的消息之后，你通常是什么感觉？这种感觉会持续多久？」 |
| **H5. Willingness to Pay / 付费意愿** | Users may be willing to pay for dedicated communication support. / 用户是否愿意为专门的沟通支持付费。 | Ask: “If this tool existed, what price would feel reasonable to you?” / 问：「如果这个工具存在，你觉得什么价格是合理的？」 |

---

## From Corpus to Interviews｜从语料到访谈

The five hypotheses above defined what needed to be validated through real user interviews.

以上五个假设明确了下一阶段需要通过真实用户访谈验证的问题。

[View Interview Overview](./user-interviews/overview.md)

---

## Key Numbers｜关键数字

| Metric 指标 | Result 结果 |
|---|---|
| Total samples / 语料总量 | 108 |
| Source distribution / 来源分布 | Xiaohongshu ~60%; Reddit ~35%; Weibo/Jike ~5% |
| Language / 语言 | Mainly Chinese; ~25 English samples / 中文为主，约25条英文语料 |
| S-level samples / S级语料 | ~28 |
| A-level samples / A级语料 | ~45 |
| Psychological mechanisms / 心理机制 | 7 |
| Communication scenarios / 沟通场景 | 11 |
| Main age range / 主要年龄 | 18–28 |

---

## Version

V1.0 · Corpus Research Stage · Before User Interviews

V1.0 · 语料研究阶段 · 用户访谈前