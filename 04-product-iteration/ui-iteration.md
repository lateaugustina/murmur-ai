# UI # UI Iteration

## 1. From User Insights to UI Strategy｜从用户洞察到 UI 策略

User research showed that users were not simply looking for better-written messages.  
用户研究发现，用户并不只是想要一条“写得更好”的消息。

They often wanted to **check whether their intended communication was appropriate and safe to send**.  
他们更常需要确认的是：**自己想表达的内容是否合适，以及这句话是否真的敢发出去**。

This led to three UI design principles:  
这进一步形成了三个 UI 设计原则：

| User Insight | UI Strategy |
|---|---|
| Users need judgment confirmation, not only generation | Make **communication strategy** visible |
| Users have different relationship and risk preferences | Present multiple **strategy-based options** |
| Users hesitate at the moment of sending | Make the output feel like **a message they can actually send** |

The key shift was from **“reading AI suggestions”** to **“choosing the message I am going to send.”**  
核心变化是从**“阅读 AI 建议”**转向**“选择我等会要发送的那句话”**。

---

## UI Evolution｜UI 演进

The interface evolved from an AI suggestion interface to a send-decision interface.  
界面从一个 AI 建议界面，逐渐转向帮助用户做发送决策的界面。

## Final UI｜最终版本

The final UI was adapted for both English and Chinese interfaces, with differences in layout and interaction details.  
最终 UI 分别适配了英文和中文界面，因此在布局和交互细节上存在一定差异。

### English Version｜英文版

![Murmur AI final UI - English](../images/final-ui-en.png)

### Chinese Version｜中文版

![Murmur AI final UI - Chinese](../images/final-ui-zh.png)

## 2. UI Brief｜UI 设计 Brief

### Design Goal｜设计目标

Make Murmur feel like a private communication space rather than a generic AI chat interface.  
让 Murmur 更像一个私密的沟通空间，而不是普通的 AI Chat 界面。

The interface should reduce the psychological distance between **AI-generated text** and **a message the user can actually send**.  
界面需要缩短**AI 生成文本**与**用户真正愿意发送的消息**之间的心理距离。

---

### Core Interaction｜核心交互

The primary interaction is not “read and choose a good answer.”  
核心交互不是“阅读并选择一个好的答案”。

It is:  
而应该是：

```text
Communication Situation
        ↓
User's Rough Thought
        ↓
Communication Strategy
        ↓
3 Sendable Messages
        ↓
Why This Works
        ↓
User Chooses
        ↓
Send
```

Each generated message represents a different communication strategy rather than a simple tone variation.  
每条生成结果代表一种不同的沟通策略，而不是简单的语气变化。

| Strategy | Communication Logic |
|---|---|
| **Conservative** | Avoid conflict, leave room for the relationship, minimize explicit rejection |
| **Natural** | Follow the conversational flow, maintain relationship warmth, reduce awkwardness |
| **Restrained Boundary** | Express the user's intention clearly without unnecessary confrontation |

---

## 3. Information Architecture｜信息结构

The main interaction follows a lightweight three-step structure.  
核心交互采用轻量的三步结构。

```text
Who are you talking to?
        ↓
What do you want to do?
        ↓
Tell Murmur roughly what happened.
```

Users select the relationship and communication intention before entering their rough thought.  
用户先选择沟通对象和沟通意图，再用粗糙的语言描述自己的情况。

The input is intentionally framed as **an intention rather than a polished prompt**.  
输入被设计成**表达意图**，而不是要求用户写出完整 Prompt。

---

## 4. Result Presentation｜结果呈现

Generated messages are presented as **chat bubbles**, making them visually closer to the user's actual communication environment.  
生成结果采用 **Chat Bubble** 呈现，让它更接近用户真实发送消息的场景。

```text
Conservative
"老师，上次的论文方便的时候能麻烦您看一下吗？"

Natural
"老师，上次的稿子您最近有空的时候可以帮我看看吗？"

Restrained Boundary
"老师，想问一下论文有没有最新的修改意见呀？"
```

Users can directly select and copy a message instead of treating the output as a piece of text to read and rewrite.  
用户可以直接选择并复制消息，而不是把生成结果当成一段还需要自己重新加工的文字。

---

## 5. Explanation & Reassurance｜解释与发送确认

Each option includes a short explanation covering:  
每个版本同时提供简短说明：

- **Communication strategy** → why this approach was chosen  
  **沟通策略** → 为什么采用这种方式

- **Expected effect** → what the message is likely to achieve  
  **预计效果** → 这句话主要希望达到什么效果

- **Send reassurance** → why the user can reasonably send it  
  **发送安抚** → 为什么这句话可以放心发送

This makes the explanation part of the product experience rather than an additional AI commentary layer.  
这样，解释就不再是额外附加的 AI 点评，而成为产品核心体验的一部分。

---

## 6. Visual Direction｜视觉方向

The visual system combines a conversational interface with a subtle emotional ambient layer.  
视觉系统将聊天界面与轻量的情绪氛围层结合。

### MOMO Ambient Layer｜MOMO 氛围层

MOMO is treated as an **ambient emotional presence**, rather than a conventional mascot or interactive character.  
MOMO 被设计为一种**情绪氛围存在**，而不是传统意义上的吉祥物或交互角色。

It stays behind the chat content and responds subtly to system states such as generating and completion.  
它始终位于聊天内容之后，只通过轻微的状态变化回应生成、完成等系统状态。

### Chat Layer｜聊天层

The main interface prioritizes:  
主界面优先呈现：

- Relationship and scenario selection  
  沟通对象与场景选择

- Communication intention  
  沟通意图

- Low-pressure rough input  
  低压力的粗略输入

- Strategy-based message options  
  基于策略的消息选项

- Explanation and reassurance  
  解释与发送确认

---

## 7. Design Decision｜设计决策

The UI evolved from an **AI suggestion interface** toward a **send-decision interface**.  
UI 最终从一个**AI 建议界面**转向了一个**发送决策界面**。

The key product question changed from:  
核心产品问题也从：

> “Which answer looks best?”

> “哪个答案看起来最好？”

to:

> “Which message feels like something I can actually send?”

> “哪句话是我真的可以发出去的？”

This became the core principle guiding Murmur's UI design.  
这成为 Murmur 后续 UI 设计的核心原则。