# User Interview 03

## Participant｜访谈对象

| Field 字段 | Details 内容 |
|---|---|
| Age 年龄 | 24 |
| Role 身份 | New graduate / 应届毕业生 |
| Main Scenario 主要场景 | Family & boundary setting / 家庭与边界表达 |
| Communication Issue 沟通问题 | Refusal and guilt / 拒绝与内疚 |

## Concrete Events｜具体事件

### Event 01

The user's aunt frequently brought food or other items with only 15–30 minutes' notice. The user wanted to refuse, but felt guilty, exhausted, and worried about appearing rude.

用户的姨妈经常只提前 15–30 分钟送东西或送饭。用户其实想拒绝，但会感到内疚、疲惫，也担心显得不礼貌。

After struggling with the situation for about a month, the user eventually said that she was dieting and did not eat dinner. After sending the message, she felt both relieved and guilty, and worried that the lie might eventually be discovered.

这种情况持续了大约一个月后，用户最终以“最近在减肥、不吃晚饭”为理由拒绝。发送后她既感到松了一口气，又因为说谎产生内疚，并担心以后被发现。

## Existing Workarounds｜当前解决方式

- Ask specific friends with relevant experience to review messages / 找熟悉家庭关系、HR 或社交沟通的朋友帮忙看
- Use GPT for longer or formal messages / 使用 GPT 处理较长或正式的沟通
- Delay replying or avoid the conversation / 延迟回复或暂时回避
- Send the message anyway and discuss the anxiety with a friend afterward / 硬着头皮发送，再向朋友倾诉

The user also described that explaining the entire situation to GPT can itself increase emotional burden.

用户提到，如果需要重新向 GPT 解释整个事情，有时反而会再次加重自己的内耗。

## Product Concept Reaction｜产品概念反馈

The user recognized the value of Murmur, especially for refusal, boundary-setting, and privacy-sensitive communication.

用户认可 Murmur 的价值，尤其是在拒绝、边界表达和隐私敏感的沟通场景中。

She emphasized that the input process should not be more burdensome than using GPT. She preferred scenario-specific choices and the ability to provide a rough idea without repeatedly explaining the whole situation.

她特别强调，输入过程不能比使用 GPT 更麻烦。她更喜欢场景化选择，并希望可以直接输入一个粗略想法，而不用反复重新解释完整背景。

She also independently suggested a verification mode: instead of only generating a message, AI could check how the recipient might interpret the draft.

她还主动提出了“帮我看”的模式：AI 不只是帮忙生成消息，还可以从接收者视角检查现有表达可能产生的理解偏差。

## Hypothesis Validation｜假设验证

| Hypothesis 假设 | Result 结果 | Evidence 证据 |
|---|---|---|
| H1. Users may seek help in high-anxiety communication situations. / 用户会在高焦虑沟通场景寻求帮助 | Partially supported / 部分支持 | The user experiences strong communication difficulty, but may seek help after calming down rather than at the peak of anxiety. / 用户存在明显沟通困难，但可能在情绪稍微平复后才寻求帮助 |
| H2. Lower input threshold may increase usage. / 更低的输入门槛可能提高使用意愿 | Revised / 修正 | Input burden is not only about the number of steps; re-explaining an emotional situation can itself create additional burden. / 输入成本不仅是操作步骤，重新描述痛苦情境本身也可能增加负担 |
| H3. Users may accept AI communication assistance. / 用户可能接受 AI 沟通辅助 | Supported / 支持 | The user already uses GPT and is comfortable with AI-assisted communication. / 用户已经使用 GPT，并接受 AI 辅助沟通 |
| H4. Post-send reassurance may be valuable. / 发送后的确认可能有价值 | Partially supported / 部分支持 | The user worries about whether a refusal is believable and whether she will be exposed later. / 用户会担心拒绝理由是否站得住脚，以及之后是否会被看穿 |
| H5. Users may be willing to pay for dedicated communication support. / 用户可能愿意为专门的沟通支持付费 | Early signal only / 初步信号 | The user mentioned ¥5–10/month under the current product gap, with a higher willingness in more frequent work communication. / 在当前产品差异化程度下，用户提到约5–10元/月；在工作沟通需求增加后可能接受更高价格 |

## Key Findings｜核心发现

1. **“帮我看”与“帮我写”是两种不同需求。**  
   Users may already have a draft but still need another perspective before sending.

2. **输入成本是核心设计问题。**  
   Re-explaining an emotionally difficult situation can increase communication anxiety.

3. **AI 的使用场景具有明显差异。**  
   Users may use general AI for formal or long messages while avoiding it for short but emotionally difficult conversations.

4. **用户希望 AI 提供判断支持，而不是替自己做决定。**  
   The user wants AI to check possible interpretations while retaining control over the final decision.

## Product Implications｜产品影响

- Consider a dedicated **“帮我看” / verification mode** alongside message generation.  
  在消息生成之外，考虑加入独立的 **“帮我看” / verification mode**。

- Minimize the need to repeatedly reconstruct emotionally difficult contexts.  
  尽量减少用户重复描述痛苦沟通背景的成本。

- Explore scenario-based input and selectable options to reduce cognitive load.  
  探索场景化输入和选项式交互，降低认知负担。

- Test whether recipient-perspective checking can reduce uncertainty before sending.  
  进一步验证从接收者视角检查消息，是否能降低发送前的不确定感。