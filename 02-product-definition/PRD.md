# # Murmur AI

**Product Requirements Document · v0.3**  
*你的沟通顾问，懂你，也懂分寸*

Research basis: 108 real-world communication samples + 4 user interviews  
研究基础：108 条真实沟通语料 + 4 次用户访谈

---

## 1. Product Overview｜产品概述

### 1.1 Product Positioning｜产品定位

Murmur helps users turn difficult-to-express thoughts into messages they genuinely want to send.

Murmur 帮助用户把难以表达的想法，转化成自己真正愿意发送的消息。

It is not designed to make users say what others want to hear. Its role is to reduce communication uncertainty while preserving the user's own judgment and voice.

它不是帮助用户说出“对方想听的话”，而是在保留用户判断和表达方式的前提下，降低沟通中的不确定感。

### 1.2 Core Value Proposition｜核心价值

| Value Proposition 核心价值 | Description 描述 |
|---|---|
| **Ask without disturbing anyone / 随时问，不打扰任何人** | Provide private communication support without requiring help from friends. / 在不打扰朋友的情况下获得私密的沟通支持。 |
| **Private by default / 私密沟通** | Users can process sensitive communication situations without exposing them to people they know. / 用户可以处理不方便向熟人透露的沟通情境。 |
| **Low-input communication / 粗糙输入也可以** | Users can provide incomplete or rough thoughts instead of organizing the entire situation first. / 用户无需先整理完整背景，可以直接输入粗糙想法。 |
| **Check before sending / 发出去之前先确认** | Help users evaluate whether an existing message is appropriate and explain why. / 在发送前帮助用户检查消息，并解释为什么可以发送。 |
| **Honest feedback / 不为了安慰而说假话** | Murmur should provide useful feedback rather than simply reassuring the user. / Murmur 应提供真实、有依据的反馈，而不是单纯迎合用户。 |

---

## 2. Problem Definition｜问题定义

### 2.1 Core Problem｜核心问题

Users are not necessarily unable to communicate. In high emotional-risk situations, they often lose confidence in their own judgment.

用户不一定不会沟通，而是在高情感风险的沟通场景中容易失去对自己判断力的信任。

The core problem is therefore not simply **“I don't know how to write this.”**, but often **“I don't know whether this is okay to send.”**

因此，核心问题不只是「我不知道怎么写」，而经常是「我不知道这样发到底行不行」。

### 2.2 Key Problems Identified in Research｜研究识别出的核心问题

| Problem 问题 | Evidence 证据 | Product Implication 产品影响 |
|---|---|---|
| **Pre-send anxiety / 发送前焦虑** | All four interviewees described concrete situations where they had difficulty sending a message despite knowing what they wanted to say. / 四位访谈对象均描述了真实的“知道怎么说却发不出去”的场景。 | Sending confirmation becomes a core product function. / 发送确认成为核心功能。 |
| **Social cost of asking friends / 找朋友的社交代价** | All four participants described situations where they did not want friends to know, be bothered, or see their vulnerable side. / 四人均提到隐私、麻烦朋友或暴露脆弱面的顾虑。 | Provide private, always-available support. / 提供私密且随时可用的支持。 |
| **Input cost as emotional cost / 输入成本即情绪成本** | One participant explicitly described re-explaining an emotional situation to AI as increasing internal stress. / 用户明确提到重新向 AI 描述痛苦情境会增加内耗。 | Reduce cognitive and emotional input burden. / 降低认知和情绪输入成本。 |
| **General AI solves generation but not confirmation / 通用 AI 解决生成但未必解决确认** | All four participants had experience using Doubao; one participant still required another person to confirm the final message. / 四人均使用过豆包，其中用户04生成完成后仍需要男友确认。 | Differentiate through verification, context, and communication-specific support. / 通过检查、上下文和专门化沟通支持形成差异化。 |
| **Authority communication pressure / 权威沟通压力** | Advisor, workplace, and parent communication repeatedly appeared as high-cost scenarios. / 导师、职场、家校等权威关系反复出现。 | Prioritize authority communication in MVP. / MVP 优先支持权威沟通。 |

---

## 3. Target Users｜目标用户

### 3.1 Core User Profiles｜核心用户画像

| Profile 画像 | Typical Situation 典型情况 | Core Need 核心需求 | Priority |
|---|---|---|---|
| **A. High-Pressure Communicators / 高压表达者** | They know what they want to say but repeatedly check messages and cannot confidently send them, especially in authority relationships. / 知道想说什么，却反复检查消息，在权威关系中尤其明显。 | Confirmation and contextual judgment rather than endless rewriting. / 确认和情境判断，而不是继续修改。 | **P0** |
| **B. Emotionally Sensitive Communicators / 情感高敏者** | The more they care about a relationship, the more they overinterpret messages and responses. / 越在意关系，越容易过度解读消息和回复。 | Support before and after emotionally risky communication. / 发送前支持与发送后缓冲。 | **P1 / Research priority** |
| **C. Socially Depleted Communicators / 精力枯竭者** | Maintaining communication becomes difficult when cognitive and emotional energy is low. / 精力不足时，维持沟通本身成为负担。 | Minimal-input communication support. / 最低输入成本的沟通支持。 | **P1** |

### 3.2 User Boundaries｜用户边界

| Not a Target User 不主要服务 | Reason 原因 |
|---|---|
| People who do not want to communicate at all / 对社交本身没有沟通意愿的人 | Murmur addresses “I want to communicate but I'm stuck,” not “I don't want to communicate.” / Murmur 解决的是“想沟通但卡住”，而不是“不想沟通”。 |
| People who are already fully satisfied with general AI / 通用 AI 已经完全满足需求的人 | A dedicated product only creates value when communication-specific support provides additional utility. / 独立产品需要在通用 AI 之外提供额外价值。 |
| Users requiring clinical psychological intervention / 需要临床心理干预的人群 | Psychological treatment is outside the product scope. / 心理治疗不属于产品服务范围。 |

---

## 4. Product Goals｜产品目标

### Primary Goal｜核心目标

Help users move from **“I know what I want to say but cannot send it”** to **“I understand why this is okay to send, and I can send it.”**

帮助用户从「我知道想说什么但发不出去」，走到「我知道为什么可以这样说，并且能够把它发出去」。

### Product Goals｜产品目标

| Goal 目标 | Definition 定义 |
|---|---|
| Reduce pre-send uncertainty / 降低发送前不确定感 | Help users evaluate their own draft and communication strategy. / 帮助用户判断自己的草稿和沟通策略。 |
| Reduce input burden / 降低输入负担 | Allow rough thoughts and scenario selections instead of requiring carefully structured prompts. / 支持粗糙想法和场景选择，而不是要求用户先整理复杂 Prompt。 |
| Preserve user agency / 保留用户自主权 | Support decisions without making interpersonal decisions for the user. / 提供判断支持，但不替用户决定是否发送。 |
| Provide communication-specific value / 提供沟通专属价值 | Offer relationship context, verification, and communication strategy beyond generic text generation. / 提供通用 AI 不一定具备的关系上下文、消息检查和沟通策略支持。 |

---

## 5. Product Scope｜产品范围

### 5.1 Core User Flow｜核心流程

```text
Communication Difficulty
        ↓
Scenario Selection
        ↓
Input Rough Thought / Existing Draft
        ↓
┌──────────────────────────┐
│                          │
│   Help Me Write          │
│   帮我写                 │
│                          │
│   Help Me Check          │
│   帮我看                 │
│                          │
└──────────────────────────┘
        ↓
AI Analysis / Generation
        ↓
Reasoning & Confirmation
        ↓
User Decides
        ↓
Send


### 5.2 Product Intervention Point｜核心介入时机
Murmur should primarily intervene when users have calmed down enough to seek help, but are still uncertain whether or how to send the message.
Murmur 主要介入于用户已经从最强烈的情绪反应中稍微恢复、开始准备沟通，但仍然不确定是否以及如何发送的节点。
---
## 6. Functional Requirements｜功能需求
### 6.1 P0 — MVP｜第一版必须有
| Feature 功能 | User Story 用户故事 | Key Requirements 设计要求 | Research Basis 研究依据 |
|---|---|---|---|
| **Scenario-based Onboarding / 场景化 Onboarding** | I can tell Murmur what situations I commonly encounter without writing a long description. / 我可以通过简单选择告诉 Murmur 自己常遇到什么沟通问题。 | 3–4 questions; collect common scenarios, relationship types, and communication preferences. / 3–4 个问题；收集常见场景、关系类型和表达偏好。 | Interviews 03 & 04 |
| **Help Me Write / 帮我写** | I give Murmur a rough idea and it helps me turn it into a sendable message. / 我输入一个粗略想法，Murmur 帮我变成可以发送的消息。 | Scenario selection → communication type → minimal input → multiple versions. / 场景选择 → 沟通类型 → 最小输入 → 多版本生成。 | Corpus + all interviews |
| **Help Me Check / 帮我看** | I already wrote the message but need to know whether it is okay to send. / 我已经写好了消息，但需要确认这样发是否合适。 | Analyze from recipient perspective; identify ambiguity or unnecessary wording; explain why the message is okay to send. / 从接收者视角检查歧义和多余表达，并解释为什么可以发送。 | Interviews 03 & 04 |
| **Low-Input Interaction / 低输入交互** | I can provide rough thoughts without reconstructing the entire emotional context. / 我可以直接输入粗糙想法，不需要重新整理完整背景。 | Prefer selectable options and short input; accept raw material. / 优先选择题和短输入；允许直接输入原始材料。 | Interviews 03 & 04 |
| **Refusal Support / 拒绝支持** | I can refuse someone while understanding that my boundary is reasonable. / 我可以拒绝别人，同时确认自己的边界是合理的。 | Provide refusal wording plus reasoning that supports the user's own judgment. / 提供拒绝表达，同时帮助用户理解自己的拒绝为什么合理。 | Interview 03 + corpus |
| **Communication Profiles / 人物档案** | Murmur remembers how I communicate with recurring people. / Murmur 记住我与长期沟通对象之间的沟通方式。 | Store only fields that visibly affect output: style, formality, emoji habits, formatting preferences, previous communication patterns. / 只记录能够明显影响输出的字段：风格、正式程度、表情习惯、排版偏好、过去沟通方式。 | Interviews 01 & 04 |
### 6.2 P1 — Next Iteration｜第二阶段
| Feature 功能 | User Value 用户价值 | Key Requirements 核心要求 |
|---|---|---|
| **Post-Send Support / 发送后支持** | Reduce uncertainty while waiting for a response. / 降低发送后的等待焦虑。 | Calibrate likely responses and possible reasons for delayed replies. / 校准可能反应及未及时回复的可能原因。 |
| **Recipient Perspective / 对方视角** | Help users understand how the message may be interpreted. / 帮助用户理解对方可能如何理解消息。 | Explain possible interpretation rather than simply giving reassurance. / 解释可能的理解方式，而不是单纯安慰。 |
| **Format Suggestions / 格式建议** | Reduce anxiety about presentation, especially in authority communication. / 降低权威沟通中的格式焦虑。 | Suggest structure, message length, emoji use, and formatting when relevant. / 在必要时建议结构、长度、表情和排版。 |
| **Refusal Credibility Check / 拒绝理由检验** | Check whether a proposed reason is likely to invite further questions. / 检查拒绝理由是否容易引发追问。 | Identify potential inconsistencies and suggest more coherent alternatives. / 识别理由漏洞并提供更自洽的表达。 |
| **Reconnect Opening / 断联复联开场** | Reduce the barrier to restarting contact. / 降低重新建立联系的第一句话门槛。 | Generate context-aware openings based on relationship and silence duration. / 根据关系和断联时间生成自然开场。 |
| **Reply Interpretation / 回复解读** | Reduce uncertainty about received messages. / 降低对收到消息的过度解读。 | Explain possible interpretations without presenting speculation as fact. / 提供可能的理解方式，但不把猜测当作事实。 |
| **Communication Reflection / 沟通反思** | Help users gradually understand their own communication patterns. / 帮助用户逐渐理解自己的沟通规律。 | Summarize recurring patterns and provide reflective feedback. / 总结长期沟通规律并提供反思反馈。 |
---
## 7. Product Principles｜产品原则
| Principle 原则 | Requirement 要求 |
|---|---|
| **Preserve the user's voice / 保留用户表达** | If the user thinks “This is not something I would say,” the output has failed. / 如果用户觉得「这不是我会说的话」，则输出失败。 |
| **Good enough, not perfect / 够好而非完美** | Optimize for a message that can be sent, not endlessly polished wording. / 优先让用户能够发送，而不是无限追求完美措辞。 |
| **Explain, don't only judge / 解释而不是只下结论** | “Why it is okay to send” is more valuable than simply saying “Send it.” / 「为什么可以发」比单纯说「可以发」更有价值。 |
| **Support, don't decide / 支持而非代替决策** | Murmur provides analysis and options while leaving the final decision to the user. / Murmur 提供分析和选择，但最终决定权属于用户。 |
| **Honest feedback / 真实反馈** | Murmur should not reassure users by saying something it does not have sufficient reason to believe. / 不应为了安慰用户而给出缺乏依据的保证。 |
| **Communication-specific / 专注沟通** | Avoid becoming a general-purpose AI assistant. / 避免成为通用 AI 助手。 |
---
## 8. Out of Scope｜明确不做
| Feature 不做功能 | Reason 原因 |
|---|---|
| **Voice Input / 语音输入** | Interviews showed a consistent preference for text input; no sufficient demand signal yet. / 四位访谈对象均以文字输入为主，目前没有足够需求信号。 |
| **Hard Usage Limits / 硬性使用次数限制** | Could increase anxiety and encourage users to preprocess content with other AI tools. / 可能增加焦虑，并促使用户先用其他 AI 处理内容。 |
| **People-Pleasing Optimization / 迎合对方** | Murmur should help users express their genuine intention, not optimize for what the recipient wants to hear. / Murmur 帮助用户表达真实意图，而不是迎合接收者。 |
| **General AI Chat / 通用 AI 聊天** | Would weaken product specialization and differentiation. / 会削弱产品专一性和差异化。 |
| **Message Reminders / 消息提醒** | Notifications could become another source of communication pressure. / 提醒可能成为新的沟通压力来源。 |
| **Clinical Psychological Support / 临床心理支持** | Outside the product's intended scope. / 超出产品定位。 |
---
## 9. Core User Stories｜核心用户故事
| Scenario 场景 | User Situation 用户处境 | Murmur Flow Murmur 流程 | Expected Outcome 预期结果 |
|---|---|---|---|
| **Authority Communication / 权威沟通** | User wants to ask an advisor about delayed feedback but worries about sounding pushy. / 用户想询问导师论文进度，但担心显得催促。 | Authority → Help Me Write → Rough Input → Generate → Explain why it is okay to send. / 权威 → 帮我写 → 粗略输入 → 生成 → 解释为什么可以发送。 | User understands the communication strategy and sends the message. / 用户理解沟通策略并发送。 |
| **Help Me Check / 帮我看** | User already has a carefully edited message but still wants external confirmation. / 用户已经反复修改消息，但仍需要确认。 | Authority → Help Me Check → Paste Draft → Recipient Perspective → Confirmation. / 权威 → 帮我看 → 粘贴草稿 → 对方视角 → 确认。 | User can make the final decision without asking another person. / 用户无需再找别人确认即可做最终决定。 |
| **Refusal / 拒绝** | User wants to refuse a request but feels guilty and worries the reason may be challenged. / 用户想拒绝，但内疚并担心理由被追问。 | Family → Help Me Check → Paste Draft → Credibility Check → Boundary Support. / 家庭 → 帮我看 → 粘贴草稿 → 理由检验 → 边界支持。 | User can communicate a boundary without unnecessarily changing the decision. / 用户能够表达边界，而不是因为内耗再次妥协。 |
| **Reconnect / 断联复联** | User wants to reconnect after a long silence but cannot formulate the opening. / 用户想重新联系一个长期没联系的人，却不知道怎么开口。 | Friends → Reconnect → Relationship Context → Generate Opening → Confirmation. / 朋友 → 断联复联 → 关系背景 → 生成开场 → 确认。 | User obtains a natural opening and can initiate contact. / 用户获得自然开场并能够主动联系。 |
---
## 10. Success Metrics｜成功指标
### 10.1 North Star Metric｜北极星指标
| Metric 指标 | Definition 定义 | Why 为什么 |
|---|---|---|
| **Message Send Rate / 消息发出率** | Percentage of users who send a message after generating or checking it with Murmur. / 用户使用 Murmur 生成或检查消息后最终将消息发送出去的比例。 | Murmur's core value is helping users move from communication difficulty to action. / Murmur 的核心价值是帮助用户从沟通困难走向实际行动。 |
**MVP target:** ≥ 70%
### 10.2 Secondary Metrics｜次级指标
| Metric 指标 | Definition 定义 | MVP Target |
|---|---|---:|
| **Onboarding Completion Rate / Onboarding 完成率** | Percentage of first-time users completing onboarding. / 首次使用用户完成 Onboarding 的比例。 | ≥ 75% |
| **Help Me Check Usage / 「帮我看」使用占比** | Share of Help Me Check among core communication interactions. / 「帮我看」在核心沟通交互中的使用占比。 | ≥ 20% |
| **Profile Activation Rate / 档案激活率** | Percentage of users creating at least one communication profile. / 创建至少一个人物档案的用户比例。 | ≥ 50% |
| **Scenario Selection Rate / 场景选择率** | Percentage of users choosing a predefined scenario before input. / 用户在输入前选择预设场景的比例。 | ≥ 60% |
| **7-Day Retention / 7 日留存率** | Percentage of users returning within seven days. / 七天内再次使用产品的用户比例。 | ≥ 40% |
Targets are initial product hypotheses and should be recalibrated after real usage data is available.
以上目标均为早期产品假设，需在获得真实使用数据后重新校准。
---
## 11. Product Evolution｜产品成长路径
Murmur is designed to evolve from solving individual communication problems toward helping users understand their own communication patterns.
Murmur 的长期方向不是让用户永远依赖 AI，而是从解决单次沟通问题逐渐走向帮助用户理解自己的沟通模式。
| Stage 阶段 | Core Capability 核心能力 | User Value 用户价值 |
|---|---|---|
| **MVP — Help Me Write / 帮我写** | Scenario-based input + message generation + confirmation. / 场景化输入 + 消息生成 + 发送确认。 | Solve the immediate barrier to sending. / 解决单次消息发送障碍。 |
| **Next — Help Me Check / 帮我看** | Draft verification + recipient perspective + format analysis. / 草稿检查 + 对方视角 + 格式分析。 | Replace the external confirmation step users currently outsource to friends. / 替代用户目前依赖朋友完成的确认环节。 |
| **Long-term — Help Me Reflect / 帮我反思** | Communication pattern analysis + reflection + personalized feedback. / 沟通规律分析 + 反思 + 个性化反馈。 | Help users gradually internalize communication skills and reduce dependence on the tool. / 帮助用户逐渐内化沟通能力，并降低对工具的长期依赖。 |
---
## 12. Pricing Hypothesis｜定价假设
Four interviews produced an early qualitative willingness-to-pay range, but this should not be treated as validated market pricing.
四次访谈形成了初步的定性付费意愿区间，但目前不能视为经过市场验证的正式定价。
| Participant | Interview Signal |
|---|---:|
| User 01 | Up to ¥30/month |
| User 02 | Around ¥10/month |
| User 03 | ¥5–10/month currently; around ¥30/month after entering the workplace |
| User 04 | Up to ¥30/month |
**Initial pricing hypothesis:** ¥25–28/month for a future professional tier.
**Early product strategy:** validate product value and usage behavior before treating pricing as a confirmed business decision.
---
## 13. Validation Status｜验证状态
The following areas have been supported by the four interviews:
以下内容已得到四次访谈的支持：
| Validated Signal 已验证信号 | Current Interpretation 当前判断 |
|---|---|
| Communication difficulty is a real recurring problem. / 沟通困难是真实且反复出现的问题。 | Core problem confirmed. / 核心问题成立。 |
| Users may avoid asking friends because of privacy or social cost. / 用户可能因为隐私和社交成本而避免找朋友。 | Private AI support has a clear use case. / 私密 AI 支持具有明确使用场景。 |
| Text input is the natural interaction method for these users. / 文字是主要自然输入方式。 | Voice input is not an MVP priority. / 语音输入不是 MVP 优先级。 |
| General AI is already a real workaround. / 通用 AI 已经是现实替代方案。 | Murmur must differentiate beyond generation. / Murmur 必须在生成之外形成差异化。 |
| Help Me Check is a recurring need in Interviews 03 and 04. / 「帮我看」在用户03和04中重复出现。 | Promoted to P0. / 升级为 P0。 |
| Communication profiles show demand signals. / 人物档案出现明确需求信号。 | Included in P0, but implementation should remain lightweight. / 纳入 P0，但初期实现应保持轻量。 |
The following areas remain hypotheses:
以下内容仍属于待验证假设：
- Whether communication profiles provide greater value than simply using multiple general-AI conversations.
- Whether recipient-perspective post-send support produces measurable value.
- Whether onboarding choices improve actual first-use completion and retention.
- Whether refusal justification increases actual send rate.
- Whether crush-related scenarios become a sufficiently frequent product use case.
---
## 14. Document Status｜文档状态
**Version:** v0.3  
**Research basis:** 108 corpus samples + 4 user interviews  
**Stage:** Research completed → Demo development  
**Primary MVP focus:** Help Me Write + Help Me Check + Scenario-based Input + Communication Profiles