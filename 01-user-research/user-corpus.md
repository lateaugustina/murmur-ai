# User Corpus

## Overview

This corpus contains 108 real-world communication samples collected from Xiaohongshu, Reddit, Weibo, and Jike.
本语料库包含 108 条真实沟通语料，来自小红书、Reddit、微博和即刻。

The corpus was built to explore how people experience and respond to communication difficulties in real-world situations.
建立语料库的目的是探索用户在真实沟通情境中如何经历和应对沟通困难。

It was used as an exploratory research input rather than a statistically representative sample.
该语料库用于探索性研究，不具有统计代表性。

## Key Numbers

Metric	Result
Total samples	108
Source distribution	Xiaohongshu ~60%; Reddit ~35%; Weibo/Jike ~5%
Language	Mainly Chinese; ~25 English samples
S-level samples	~28
A-level samples	~45
Psychological mechanisms covered	7
Communication scenarios covered	11
Main age range	18–28
Mature working users	A smaller group aged 25–45

## Data Collection

The samples were manually collected from public user-generated content on Xiaohongshu, Reddit, Weibo, and Jike.
语料由我从小红书、Reddit、微博和即刻的公开用户内容中手动收集。

The source distribution was approximately 60% Xiaohongshu, 35% Reddit, and 5% Weibo/Jike.
来源分布约为小红书 60%、Reddit 35%、微博/即刻 5%。

Most samples were in Chinese, with approximately 25 English samples.
语料以中文为主，约 25 条为英文语料。

I selected samples that contained concrete communication situations, triggers, emotional reactions, behaviors, coping methods, or communication difficulties.
筛选标准主要包括具体的沟通情境、触发事件、情绪反应、用户行为、应对方式或沟通困难。

The selected samples were manually entered into a Notion database for structured analysis.
筛选后的语料被手动录入 Notion 数据库，进行后续结构化分析。

## Corpus Structure

Each sample was organized into the following fields:

| 序号 ID | 一句话总结 One-line Summary | 价值评级 Value Rating | 原始内容 Raw Content | 来源平台 Source Platform | 沟通场景 Communication Context | 触发事件 Trigger Event | 用户情绪 Emotion | 用户行为 Behavior | 心理机制 Psychological Mechanism | 当前解决方式 Current Coping Strategy | 核心痛点 Core Pain Point | 产品机会点 Product Opportunity |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The corpus therefore preserves both the original user expression and the structured interpretation of each sample.
因此，语料库同时保留了用户的原始表达，以及对每条语料进行结构化分析后的信息。

### Example Samples

The following examples show how individual raw samples were transformed into structured research data and product insights.
以下示例展示了单条原始语料如何被转化为结构化研究数据，并进一步形成产品洞察。

#### Sample 11
| Field 字段 | Analysis 分析 |
| --- | --- |
| **序号 ID** | 11 |
| **一句话总结 One-line Summary** | 过度分析对方发消息的时间、语气和一致性，不信任自己的判断力，甚至自己动手做了一个工具来帮自己拆解情境、停止 spiral。<br>Overanalyzes message timing, tone, and consistency, loses trust in their own judgment, and eventually builds a tool to analyze situations and stop spiraling. |
| **价值评级 Value Rating** | S |
| **原始内容 Raw Content** | I keep overthinking texts and i don't know if i'm the problem or not<br><br>I feel like I'm losing my mind over something that should be simple.<br><br>Whenever someone texts me, I overanalyze everything:<br>- how long they took to reply<br>- how their tone changed<br>- if they're being dry or just busy<br><br>And it's worse when they're inconsistent. Like one day they're super into you, next day it feels like they don't care at all.<br><br>I keep asking friends what things mean but honestly I feel like I already know the answer most of the time... I just don't trust my own judgment.<br><br>At some point it got so annoying I even tried building a small thing for myself just to break down situations more clearly and stop spiraling.<br><br>But idk if the issue is actually me overthinking or if people really do act like this and I should take it as a sign.<br><br>What would you do in this situation? |
| **来源平台 Source Platform** | Reddit |
| **沟通场景 Communication Context** | Crush / 亲密关系 / 泛社交<br>Crush / intimate relationship / general social communication |
| **触发事件 Trigger Event** | 对方发消息行为不一致，一致性缺失触发无法停止的过度分析循环。<br>Inconsistent messaging behavior from the other person triggers an ongoing overanalysis loop. |
| **用户情绪 Emotion** | 焦虑；自我怀疑；不确定；烦躁；无力感（人工标签）<br>Anxiety; self-doubt; uncertainty; irritation; helplessness (manually tagged) |
| **用户行为 Behavior** | 过度分析消息；找人审稿；灾难化解读<br>Overanalyzing messages; asking others for interpretation; catastrophic interpretation |
| **心理机制 Psychological Mechanism** | 发送后焦虑；自我呈现压力<br>Post-send anxiety; self-presentation pressure |
| **当前解决方式 Current Coping Strategy** | 向他人倾诉；自建工具<br>Seeking reassurance from others; building a personal tool |
| **核心痛点 Core Pain Point** | 用户知道自己在过度分析但停不下来。核心是对自己判断力的不信任——问了朋友也觉得自己其实知道答案，但就是无法相信自己。<br>The user recognizes that they may be overanalyzing, but cannot stop. The deeper problem is distrust in their own judgment: even after asking friends, they often feel they already know the answer but cannot trust themselves. |
| **产品机会点 Product Opportunity** | 这条语料是 Murmur「对话解读」功能最直接的需求来源：用户描述对话情境，Murmur 给出客观分析，帮助用户停止 spiral。用户自己动手做工具，是未满足需求的强信号。<br>A direct signal for Murmur's conversation interpretation feature: users can describe a conversation context, and Murmur helps interpret the situation objectively and interrupt the spiraling loop. The user's attempt to build their own tool is a particularly strong signal of unmet demand. |

Tagging note: Emotion tags were manually assigned by the researcher. AI-assisted tagging was used during structured analysis, but human judgment was retained for emotion labels because emotional interpretation was not consistently accurate enough to rely on automation alone.
标签说明： 情绪标签由研究者人工判断。结构化分析过程中使用了 AI 辅助，但由于 AI 对人类情绪的识别并不总是足够准确，因此最终情绪标签保留人工判断。
Collection period: All samples were collected from public content published within the past year.
所有语料均来自收集时过去一年内发布的公开用户内容。

## Structured Analysis

Each raw sample was individually analyzed with Claude using the same field structure.
每条原始语料都单独交由 Claude 按统一字段进行分析。

The analysis did not only identify what users said. It also separated:

* what happened in the communication situation;
* what triggered the difficulty;
* how the user felt;
* what the user did;
* what psychological mechanism might explain the reaction;
* how the user currently tried to solve the problem;
* what unmet need and product opportunity could be identified.

分析不只是记录用户“说了什么”，还进一步区分：

* 发生了什么沟通情境；
* 什么事件触发了困难；
* 用户产生了什么情绪；
* 用户实际做了什么；
* 可能存在什么心理机制；
* 用户目前如何解决这个问题；
* 其中暴露出什么核心痛点和产品机会。

## Tagging Framework

After the initial structured analysis, three fields were further tagged:

* Emotion
* Behavior
* Current Coping Strategy

在完成初步结构化分析后，我进一步对三个字段进行标签化：

* 用户情绪
* 用户行为
* 当前解决方式

The taxonomy was developed to distinguish patterns that may look similar but represent different psychological states or behavioral functions.
建立这套标签体系，是为了区分表面相似、但实际心理状态或行为功能不同的模式。

For example, Behavior describes the user’s immediate reaction after communication anxiety is triggered, while Current Coping Strategy describes the way the user consciously tries to manage the difficulty.
例如，用户行为描述沟通焦虑发生后的即时反应，而当前解决方式描述用户有意识采取的应对方法。

The two categories can overlap. For example, delaying a reply may simultaneously be an immediate behavior and a deliberate coping strategy.
两者可以重叠。例如，“延迟回复”既可能是焦虑发生后的即时行为，也可能是用户主动采用的应对策略。

The complete taxonomy contains 54 tags.

[View Tag Taxonomy](./tag-taxonomy.md)￼

## What the Corpus Revealed

The corpus revealed that communication anxiety was not expressed as a single type of problem. Different users developed different ways of dealing with uncertainty, interpersonal risk, and communication pressure.

语料显示，沟通焦虑并不是一种单一的问题。不同用户会针对沟通中的不确定性、人际风险和表达压力，发展出不同的应对方式。

Users often construct their own communication systems

Users did not simply “do nothing” when communication became difficult. Many developed informal systems to make communication possible.

当沟通变得困难时，用户并不是简单地什么都不做，而是会主动建立各种非正式的沟通机制。

Examples found in the corpus included:

* asking friends to review messages;
* asking friends to interpret messages;
* asking friends to send messages on their behalf;
* drafting messages in a memo before sending;
* searching for communication templates or advice;
* delaying replies;
* replying late at night;
* muting notifications;
* avoiding opening the conversation;
* deliberately ending conversations.

语料中出现了多种方式，例如：

* 找朋友审稿；
* 找朋友代看；
* 找朋友代回；
* 先在备忘录中起草；
* 搜索沟通攻略或模板；
* 延迟回复；
* 半夜回复；
* 设置免打扰；
* 回避打开聊天框；
* 强行结束对话。

These workarounds became an important source of evidence for identifying unmet needs.
这些 Workaround 后来成为判断用户未满足需求的重要证据。

Some users externalize communication judgment

A recurring pattern was asking another person to confirm whether a message was appropriate before sending it.
一个反复出现的模式是：用户在发送前需要让另一个人确认“这样说有没有问题”。

In some cases, friends were not only used for proofreading, but also for interpreting the other person’s message or making the communication decision.
在一些情况下，朋友承担的不只是审稿角色，还包括解读对方消息，甚至代替用户进行沟通判断。

This pattern became an important clue behind the later product insight that the problem may not simply be “I don’t know how to write,” but “I don’t trust my own judgment in this situation.”
这一模式后来成为一个重要线索，并进一步形成了产品洞察：用户面对的可能不只是“不会写”，而是“在这个情境下不相信自己的判断”。

Workarounds vary with the type of communication pressure

The corpus contained different patterns around authority relationships, intimate relationships, initiating contact, waiting for replies, and depleted social energy.
不同沟通压力下出现的 Workaround 也不同，包括权威关系、亲密关系、主动发起联系、等待回复以及社交精力耗竭等场景。

These patterns later became the basis for identifying different user profiles and prioritizing psychological mechanisms and communication scenarios.
这些模式后来成为划分不同用户画像，以及确定心理机制和核心沟通场景优先级的基础。

## From Corpus to User Insights

The corpus analysis was used to produce the first version of the User Insights Report.
基于语料分析，我进一步形成了第一版用户洞察报告。

The report synthesized the corpus into:

* three core user profiles;
* prioritized psychological mechanisms;
* five core communication scenarios;
* existing solutions and workarounds;
* product boundaries;
* interview hypotheses;
* initial principles for AI behavior and product design.

最终的用户洞察报告进一步形成了：

* 三类核心用户画像；
* 心理机制优先级；
* 五个核心沟通场景；
* 用户现有解决方式与 Workaround；
* 产品边界；
* 后续访谈假设；
* AI 行为与产品设计的初步原则。

[View User Insights Report](./user-insights-report.md)