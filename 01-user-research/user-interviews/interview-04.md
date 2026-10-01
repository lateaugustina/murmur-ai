# User Interview 04

## Participant｜访谈对象

| Field 字段 | Details 内容 |
|---|---|
| Age 年龄 | 23 |
| Role 身份 | Communication studies graduate student / 传播学研二 |
| Main Scenario 主要场景 | Advisor communication / 导师沟通 |
| Communication Issue 沟通问题 | Authority relationship anxiety / 权威关系沟通焦虑 |

## Concrete Events｜具体事件

### Event 01

The user submitted a paper to her advisor for revision but did not receive complete feedback for nearly a month. She wanted to ask about the progress but worried that doing so might seem rude or make the advisor feel pressured.

用户把论文交给导师修改后，近一个月没有收到完整反馈。她想询问进度，但担心主动询问会显得不礼貌，或者让导师觉得自己在催促。

She usually starts with a light topic and then naturally transitions to the main question. The advisor often understands the intention and explains the situation.

她通常会先从轻松的话题开始，再自然地转入正题。导师一般能够理解她的意图，并解释目前的情况。

## Existing Workarounds｜当前解决方式

- Draft messages in a memo or WPS / 在备忘录或 WPS 中起草
- Repeatedly edit wording, structure, particles, and emoji placement / 反复修改措辞、结构、语气词和表情的位置
- Use Doubao to generate an initial draft / 使用豆包生成初稿
- Ask her boyfriend to check the final version / 让男朋友检查最终版本

Her typical workflow is:

`Doubao generates → self-editing → boyfriend checks → send`

她目前比较典型的流程是：

`豆包生成 → 自己多轮修改 → 男朋友确认 → 发送`

## Product Concept Reaction｜产品概念反馈

The user was receptive to AI-assisted communication and wanted to provide raw material directly rather than carefully organizing the situation first.

用户接受 AI 辅助沟通，并希望能够直接把原始想法交给 AI，而不是先整理成完整的问题。

She considered persistent communication profiles useful, especially if the system could remember her advisor's communication style, common expressions, emoji habits, and previous interactions.

她认为长期沟通档案有价值，例如记录导师的沟通风格、常用表达、表情习惯和过去的沟通记录。

She also wanted the system to help her gradually understand and improve her own communication patterns rather than remain permanently dependent on it.

她还希望 AI 不只是长期替她解决单条消息，而是帮助她逐渐理解和改善自己的沟通方式。

## Hypothesis Validation｜假设验证

| Hypothesis 假设 | Result 结果 | Evidence 证据 |
|---|---|---|
| H1. Users may seek help in high-anxiety communication situations. / 用户会在高焦虑沟通场景寻求帮助 | Supported / 支持 | Complex situations involving authority relationships and uncertainty about the other person's attitude trigger repeated drafting and checking. / 涉及权威关系、且不确定对方态度的复杂场景会触发反复修改和确认 |
| H2. Lower input threshold may increase usage. / 更低的输入门槛可能提高使用意愿 | Revised / 修正 | The user prefers direct raw input, but may pre-process information when usage limits create friction. / 用户偏好直接输入原始信息，但如果存在使用限制，可能会先自行整理 |
| H3. Users may accept AI communication assistance. / 用户可能接受 AI 沟通辅助 | Supported / 支持 | The user already uses AI for drafting and is willing to use a dedicated communication tool. / 用户已经使用 AI 起草消息，也愿意使用专门的沟通工具 |
| H4. Post-send reassurance may be valuable. / 发送后的确认可能有价值 | Partially supported / 部分支持 | Concrete expectations about the other person's likely response may reduce uncertainty. / 对对方可能反应形成具体预期，有助于降低不确定感 |
| H5. Users may be willing to pay for dedicated communication support. / 用户可能愿意为专门的沟通支持付费 | Early signal only / 初步信号 | The user indicated a willingness to pay up to ¥30/month. / 用户表示最高约有30元/月的付费意愿 |

## Key Findings｜核心发现

1. **用户不仅需要“帮我写”，也需要“帮我确认”。**  
   The user already edits AI-generated messages herself but still seeks an external perspective before sending.

2. **个性化沟通档案有明确需求信号。**  
   Remembering relationship context and communication style may make AI assistance more useful.

3. **用户希望最终减少对 AI 的依赖。**  
   Communication support can potentially extend from solving individual messages to helping users reflect on their communication patterns.

4. **“对方视角”可能是降低不确定性的一个方向。**  
   Checking how a message may be interpreted could help users assess interpersonal risk before sending.

## Product Implications｜产品影响

- Explore personalized communication profiles for recurring relationships.  
  探索针对长期关系的个性化沟通档案。

- Support both **“帮我写”** and **“帮我看”** workflows.  
  同时支持 **“帮我写”** 和 **“帮我看”** 两种流程。

- Explore a longer-term **Write → Check → Reflect** experience.  
  探索长期的 **“写 → 看 → 反思”** 使用路径。

- Test whether recipient-perspective analysis consistently helps users handle communication uncertainty.  
  进一步验证接收者视角分析是否能够稳定降低用户的沟通不确定感。