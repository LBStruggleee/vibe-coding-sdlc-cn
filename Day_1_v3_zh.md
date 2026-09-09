# The New SDLC with Vibe Coding
# 新 SDLC：Vibe Coding 时代

---

## 译者注

| 属性 | 内容 |
|------|------|
| 原标题 | The New SDLC with Vibe Coding |
| 作者 | Addy Osmani, Shubham Saboo, Sokratis Kartakis |
| 日期 | 2026年5月 |
| 篇幅 | 51页 / 约64,000字符 |
| 主题 | AI 如何重塑软件开发生命周期（SDLC），涵盖 Vibe Coding、Agentic Engineering、Context Engineering、工厂模型、开发者角色演变等 |

**翻译说明**：本文将这份技术白皮书翻译为简体中文，供中文开发者社区阅读参考。专业术语采用业界通用译法，首次出现时在括号内保留英文原词（如"上下文工程（Context Engineering）"）。人名、产品名、公司名保留英文。语气保持专业、权威、对技术读者友好。

---

## 目录

- [引言](#引言)
- [从语法到意图的转变](#从语法到意图的转变)
  - [AI Agent 快速回顾](#ai-agent-快速回顾)
  - [什么是 Vibe Coding？](#什么是-vibe-coding)
  - [光谱：从 Vibe Coding 到 Agentic Engineering](#光谱从-vibe-coding-到-agentic-engineering)
  - [上下文工程：真正的技能](#上下文工程真正的技能)
- [新的软件开发生命周期](#新的软件开发生命周期)
  - [传统 SDLC 面临压力](#传统-sdlc-面临压力)
  - [AI 如何变革每个阶段](#ai-如何变革每个阶段)
- [工厂模型：构建构建软件的系统](#工厂模型构建构建软件的系统)
  - [Harness Engineering：模型之外的结构](#harness-engineering模型之外的结构)
  - [Harness 中的内容](#harness-中的内容)
  - [Harness 在 SDLC 中的应用](#harness-在-sdlc-中的应用)
- [开发者的角色演变：从指挥家到编排者](#开发者的角色演变从指挥家到编排者)
  - [指挥家：动手、实时指导](#指挥家动手实时指导)
  - [编排者：异步、多 Agent 委派](#编排者异步多-agent-委派)
  - [80% 问题](#80-问题)
  - [编码 Agent 实践](#编码-agent-实践)
- [编码 Agent 在开发者日常中的位置](#编码-agent-在开发者日常中的位置)
- [Vibe Coding 生产级 Agent](#vibe-coding-生产级-agent)
- [AI 开发的经济学](#ai-开发的经济学)
  - [Vibe Coding 的隐性债务（低 CapEx，高 OpEx）](#vibe-coding-的隐性债务低-capex高-opex)
  - [Agentic Engineering 的投资（高 CapEx，低 OpEx](#agentic-engineering-的投资高-capex低-opex)
  - [上下文工程作为财务杠杆](#上下文工程作为财务杠杆)
  - [通过动态上下文和技能扩展效率](#通过动态上下文和技能扩展效率)
  - [智能模型路由](#智能模型路由)
- [从哪里开始](#从哪里开始)
  - [对于个人开发者](#对于个人开发者)
  - [对于工程领导者](#对于工程领导者)
  - [对于组织](#对于组织)
- [结论：意图作为新的界面](#结论意图作为新的界面)
- [尾注](#尾注)

---


[Page 1]

# The New SDLC with Vibe Coding

**新 SDLC：Vibe Coding 时代**

---

**作者**: Addy Osmani, Shubham Saboo, Sokratis Kartakis

**从临时提示到 Agentic Engineering**

---

[Page 2]

**致谢**

**内容贡献者**
- Elia Secchi
- Julia Wiesinger
- Anant Nawalgaria

**策展与编辑**
- Anant Nawalgaria

**设计师**
- Michael Lanning

---

[Page 3]

## 目录

- 引言 — 6
- 为什么是这篇论文，为什么是现在 — 9
- 这篇论文面向谁 — 9
- 从语法到意图的转变 — 10
- AI Agent 快速回顾 — 10
- 什么是 Vibe Coding？ — 11
- 光谱：从 Vibe Coding 到 Agentic Engineering — 12
- 上下文工程：真正的技能 — 15
- 新的软件开发生命周期 — 19
- 传统 SDLC 面临压力 — 19
- AI 如何变革每个阶段 — 21
  - 需求与规划 — 21
  - 设计与架构 — 21
  - 实现 — 22
  - 测试与质量保证 — 22

---

[Page 4]

- 代码审查与部署 — 23
- 维护与演进 — 24
- 工厂模型：构建构建软件的系统 — 24
- Harness Engineering：模型之外的结构 — 26
- Harness 中的内容 — 28
- Harness 在 SDLC 中的应用 — 29
  1. 需求、规划与架构（配置 Harness） — 29
  2. 实现（运行 Harness） — 29
  3. 测试与 QA（反馈循环） — 30
  4. 代码审查、部署与维护（观察 Harness） — 30
- 开发者的角色演变：从指挥家到编排者 — 31
  - 指挥家：动手、实时指导 — 31
  - 编排者：异步、多 Agent 委派 — 32
  - 80% 问题 — 33
- 编码 Agent 实践 — 34

---

[Page 5]

## 目录（续）

- 编码 Agent 在开发者日常中的位置 — 35
- Vibe Coding 生产级 Agent — 36
- AI 开发的经济学 — 39
  - Vibe Coding 的隐性债务（低 CapEx，高 OpEx） — 40
  - Agentic Engineering 的投资（高 CapEx，低 OpEx） — 41
  - 上下文工程作为财务杠杆 — 41
  - 通过动态上下文和技能扩展效率 — 41
  - 智能模型路由 — 42
- 从哪里开始 — 42
  - 对于个人开发者 — 43
  - 对于工程领导者 — 44
  - 对于组织 — 45
- 结论：意图作为新的界面 — 47
- 尾注 — 49

---

[Page 6]

## 引言

在计算机历史的大部分时间里，编程一直是一种翻译行为：用人类语言理解问题，用抽象术语设计解决方案，然后将其翻译成机器可以执行的语法。每一步都会引入摩擦。这种摩擦正在消失。软件工程正在经历自高级编程语言引入以来最深刻的变革。

> 软件工程最深刻的转变不是新的语言、框架或云服务。它是从编写代码到表达意图的转变，并信任智能系统将这种意图转化为可工作的软件。

几十年来，开发者与机器的主要接口一直是语法：大括号、分号、类型注解，以及编程语言的精确语法。那个时代正在结束。

一种新的范式已经到来：开发者表达他们想要构建什么，而不是如何构建它。机器处理实现。人类提供意图、架构和判断。这不是遥远的未来——对于越来越多的专业开发者来说，这是日常现实。截至 2026 年初，85% 的专业开发者定期使用 AI 编码 Agent，51% 每天使用，估计 41% 的新代码是 AI 生成的。¹

---

[Page 7]

这种转变并非一夜之间发生。它始于自动补全——编辑器中的简单标记预测。然后是内联代码建议，可以完成整个函数。接着是基于聊天的界面，允许开发者用自然语言描述功能并接收可工作的实现。现在，完全自主的 Agent 可以克隆仓库、规划多文件更改、在沙箱环境中执行它们、运行测试并提交拉取请求——所有这些都无需人类键入一行代码。

---

[Page 8]

**图 1：从自动补全到自主**

对软件开发生命周期（SDLC）的影响是深远的。每个阶段——从需求收集到部署到维护——都在被 AI 能力重塑。但这种转变并不均匀或简单。光谱范围从随意的"vibe coding"（开发者提示 AI 并接受任何返回的内容），到纪律严明的"agentic engineering"（AI 作为强大的实现引擎，在精心设计的约束、测试和反馈循环系统中运行，人类保留对架构、正确性和质量的监督）。

这种区别很重要。告诉 CTO 你的团队正在 vibe coding 他们的支付处理系统，将会而且应该引起警钟。告诉同一位 CTO 你的团队实践 agentic engineering，AI 在人类设计的约束下处理实现，同时测试覆盖率确保正确性，则是一个完全不同的对话。

---

[Page 9]

本文为那场对话奠定了基础。我们追溯了从随意 vibe coding 到纪律严明 agentic engineering 的光谱，研究了开发者的角色如何从编写代码转向行使判断力——从指挥家到编排者——并阐述了采用这些工具以产生你真正可以依赖的软件所需的条件。

### 为什么是这篇论文，为什么是现在

新的工具、能力和范式每周都在涌现。工程团队需要一个框架来理解这个格局——不是几个月就会过时的快照，而是一套随着特定工具演进仍然有用的原则和心智模型。

### 这篇论文面向谁

本文面向希望了解 AI 如何重塑 SDLC 并采用这些新能力的软件工程师、工程经理、架构师和技术领导者，同时不牺牲生产软件所要求的纪律。我们假设读者熟悉现代软件开发实践，但不熟悉 AI 或机器学习的具体细节。

---

[Page 10]

## 从语法到意图的转变

在我们进一步讨论之前，我们需要对 Agent 是什么以及 vibe coding 实际含义有一个共同的理解。这两个术语已经积累了足够的含义，需要仔细拆解。

### AI Agent 快速回顾

AI Agent 是一个软件系统，它感知目标、规划达成目标的步骤、通过工具采取行动、观察结果，并迭代直到目标达成或达到停止条件。聊天机器人产生响应并等待下一个提示，而 Agent 运行自己的循环。你在顶部给它一个目标，然后它在每一步决定接下来做什么。

**图 2：Agent 循环——感知、规划、行动、观察、迭代。**

---

[Page 11]

每个 Agent，无论简单还是复杂，都由五个部分组成。2025 年 11 月的《Agent 入门》白皮书深入介绍了每个部分。² 在这里，简短版本：

- **模型**是推理引擎。它读取当前上下文，决定接下来应该发生什么，并产生下一个想法、下一个工具调用或下一条消息。
- **工具**将模型连接到世界。它们包括 Agent 可以调用的 API、可以执行的代码、可以查询的数据库，以及可以委派的其他 Agent。
- **记忆**是状态。它允许 Agent 回忆过去的交互、检索项目特定的规则，并跨会话保留上下文，这样它永远不会从零开始。
- **编排**是运行循环的代码。它为每次模型调用组装上下文、分派工具调用、捕获它们的结果，并决定是否继续。
- **部署**是将原型转变为服务的内容：托管、身份、可观察性，以及 Agent 运行的生产基础设施。

这四个部分在一个连续循环中协同工作：获取任务、扫描场景、思考、行动、观察和迭代。循环是每个 Agent 跳动的心脏。本文中的其他内容，以及课程的其余部分，都是这个循环的变体。

### 什么是 Vibe Coding？

2025 年 2 月，Andrej Karpathy 发布了一种新编程方式的描述，在软件工程社区引起了广泛共鸣。他描述了一种方法，你"完全沉浸于 vibes，拥抱指数级增长，甚至忘记代码的存在"。在这种模式下，开发者用自然语言描述他们想要什么，接受 AI 的输出，当出现问题时，将错误消息复制回提示中并要求 AI 修复。²

---

[Page 12]

这个术语之所以病毒式传播，是因为它捕捉到了真实的东西：许多开发者已经在这样工作，但没有语言来描述它。几个月内，"vibe coding"成为任何 AI 辅助开发工作流的通用描述词，这造成了混淆。高级工程师使用 AI 助手实现一个规范良好的功能是在"vibe coding"吗？团队使用 AI Agent 执行精心规划的架构是在"vibe coding"吗？这个术语被应用得如此广泛，以至于开始失去意义。

到 2026 年初，Karpathy 本人承认最初的框架过于狭窄，引入了"agentic engineering"这个术语来描述光谱上更有纪律的一端。⁴

### 光谱：从 Vibe Coding 到 Agentic Engineering

与其将 vibe coding 和 agentic engineering 视为二元对立，我们更有用的是将它们视为光谱的端点。关键区别因素不是你如何使用 AI。而是围绕 AI 输出的结构、验证和人类判断有多少。

---

[Page 13]

**表 1：从 Vibe Coding 到 Agentic Engineering 的光谱**

| 维度 | Vibe Coding | 结构化 AI 辅助编码 | Agentic Engineering |
|------|-------------|-------------------|---------------------|
| 意图规范 | 随意的自然语言提示 | 带有示例和约束的详细提示 | 正式规范、架构文档、记忆文件 |
| 验证 | "它似乎能工作吗？" | 手动测试、抽查 | 自动化测试套件、CI/CD 门禁、LM 评委 |
| 代码库理解 | 最小化；开发者可能不阅读生成的代码 | 选择性审查关键路径 | 全面审查架构；AI 处理实现细节 |
| 错误处理 | 将错误消息复制粘贴回 AI | 开发者诊断根本原因，AI 实现修复 | Agent 在定义范围内自我诊断；人类处理架构问题 |
| 适当范围 | 原型、脚本、个人项目、黑客松 | 已建立代码库中的功能 | 生产系统、团队规模开发 |
| 风险状况 | 高；适用于可丢弃代码 | 中等；关键检查点的人类判断 | 低；每个阶段的系统化验证 |

---

[Page 14]

**图 3：从 Vibe Coding 到 Agentic Engineering 的光谱**

两端之间最大的区别因素是输出如何被验证。在 vibe coding 中，验证是可选的；开发者运行代码并检查它是否看起来正确。在 agentic engineering 中，两个机制协同工作。测试验证系统的确定性部分：给定此输入的函数产生该输出。评估（evals）验证非确定性部分：Agent 是否采取了正确的步骤轨迹、选择了正确的工具，并产生了满足质量标准的最终响应。测试由代码检查；评估由标记数据集、评分标准和 LM 评委检查。没有两者，实践始终是 vibe coding，无论提示多么复杂。

> **实践提示：**
>
> 在这个光谱上的正确位置取决于风险。周末原型可以纯粹是 vibe coding。处理金融交易的生产 API 需要 agentic engineering。大多数实际工作落在两者之间的某个地方，技能在于知道为每个任务在哪里划清界限。

---

[Page 15]

### 上下文工程：真正的技能

随着该领域的成熟，一个关键洞察已经出现：AI 生成的代码质量较少取决于你的提示的聪明程度，而更多取决于所提供的上下文的质量。这一认识催生了上下文工程（context Engineering）的概念——为 AI Agent 提供关于你的代码库、架构、规范和意图的丰富、结构化信息的实践。⁵

开发者必须考虑六种主要类型的上下文：

- **指令**：Agent 的核心角色、目标和操作边界。
- **知识**：检索的文档、架构图和领域特定数据。
- **记忆**：短期会话日志（刚刚发生了什么）和长期持久状态（项目是什么）。
- **示例**：少样本行为演示和代码库参考模式。
- **工具**：Agent 可以调用的 API、脚本和外部服务的精确定义。
- **护栏**：硬约束、格式规则和安全验证。

---

[Page 16]

在 AI 代码生成中，上下文工程涉及仔细平衡这六个元素中哪些是 Agent 预先拥有的，哪些是它可以按需检索的。这在静态和动态上下文之间创建了关键分离。

**静态上下文**始终加载：系统指令、规则文件（AGENTS.md、CLAUDE.md、GEMINI.md）、全局记忆和角色定义。它定义了 Agent 是谁以及它的行为方式。静态上下文很昂贵，因为每个标记都存在于每次交互中，无论是否相关。

**动态上下文**按需加载：由任务匹配触发的技能指令、执行期间检索的工具结果、从 RAG 管道获取的文档，以及窗口化的会话历史。动态上下文是高效的，因为 Agent 仅在需要信息时才支付标记成本。

什么属于静态上下文与动态上下文的设计决策是一个真正的工程权衡。太多静态上下文会浪费标记并稀释信号。太少意味着 Agent 忘记关键规则。最好的系统将这个边界视为一等架构决策，像任何其他配置一样进行审查和版本控制。

---

[Page 17]

**图 4：上下文工程——静态与动态**

管理动态上下文最强大的模式是 Agent Skills：结构化的、可移植的程序化知识包，Agent 仅在任务需要时加载。

不是将每块专业知识嵌入 Agent 的系统提示中，技能允许 Agent 保持轻量级通用性，通过渐进式披露按需灵活进入专业角色。Agent 在启动时仅看到轻量级元数据，当任务匹配时加载完整指令，仅在明确需要时提取深度参考材料。结果是 Agent 可以携带数十种专业能力，同时仅为它正在积极使用的能力支付标记成本。

---

[Page 18]

Agent Skills 在主要编码 Agent 和企业平台中得到了快速采用，因为它们解决了困扰 AI Agent 开发的四个问题：

- 过载提示导致的上下文腐烂
- LLM 缺乏程序化记忆
- 多 Agent 架构的运营开销
- 跨工具和供应商的可移植性需求

本节介绍了上下文工程的核心原则：每个 Agent 需要的六种上下文类型、静态和动态上下文之间的权衡，以及 Agent 技能作为大规模管理该权衡的关键模式。

本系列关于《上下文工程：会话、技能与记忆》的配套 Day-3 论文进一步阐述了这些想法中的每一个，涵盖如何设计和管理会话、编写和评估技能、跨交互构建持久记忆，以及优化生产系统的标记经济学。

从"提示工程"到"上下文工程"的转变反映了关于使用 AI 的更深层真理。模型不需要措辞巧妙的指令，而是需要与熟练的人类开发者做好工作所需的相同上下文。问题不是"我如何诱骗 AI 写出好代码？"而是"新团队成员需要知道什么才能有效贡献，我如何将该知识编码为 AI 可以使用的形式？"

上下文工程是 vibe coding 和 agentic engineering 之间的桥梁。它也是本节与下一节之间的桥梁，在下一节中，我们查看围绕每个模型并使其有用的结构。

---

[Page 19]

通过将我们的注意力从编写语法转向工程化这种上下文，软件创建的瓶颈发生了根本性改变。我们不再等待人类双手输入样板代码；我们正在等待人类思维定义边界。这需要完全重新想象传统的软件开发生命周期（SDLC），因为我们用来构建软件的系统现在决定了软件交付的速度。

## 新的软件开发生命周期

### 传统 SDLC 面临压力

软件开发生命周期已经经历了一次重大转型。在过去二十年中，大多数企业从顺序瀑布流程转向迭代模型：敏捷冲刺、持续集成、DevOps 管道和快速发布周期。这种转变缩短了反馈循环，使测试更接近开发，并使部署成为持续过程而不是季度事件。

AI 戏剧性地压缩了这个周期，但不均匀：曾经需要数周的实现现在可以在数小时内完成，而需求、架构和验证仍然顽固地保持人类节奏。结果不是旧 SDLC 的更快版本。它是一个不同的工作流，阶段之间的边界模糊，迭代周期从数周缩短到数分钟，开发者的角色从主要实现者转变为系统设计者和质量仲裁者。

---

[Page 20]

**图 5：传统 SDLC 与 AI 驱动的 SDLC**

关于变化速度的说明：上述逐阶段描述反映了截至 2026 年中期的 AI 驱动 SDLC 状态。它正在迅速转变。早期迹象表明压缩将超越实现：团队已经在实验工作流，开发者直接从规范到审查，AI Agent 在后台处理实现、测试和部署。本节中描绘的边界在 12 个月后可能看起来不同。将保持不变的是人类判断、品味以及验证 AI 输出的技能，因为机器承担了更多实现工作。

---

[Page 21]

### AI 如何变革每个阶段

#### 需求与规划

AI 改变了需求的收集、分析和结构化方式。开发者现在可以使用 AI 助手将模糊的利益相关者请求转化为结构化规范，生成用户故事，识别边缘情况，并基于历史数据预测潜在风险。然而，定义*什么*值得构建以及*为什么*仍然是深刻的人类判断。AI 可以综合选项，但优先级排序、权衡取舍和战略对齐仍然需要人类领导力。

#### 设计与架构

架构决策——系统边界、数据流、API 契约、技术选择——越来越多地由 AI 辅助，而非 AI 驱动。开发者可以生成和比较多种架构方案，模拟权衡，并自动生成架构图和文档。但最终架构决策的批准、系统级推理和长期可维护性评估仍然牢牢掌握在人类架构师手中。

---

[Page 22]

#### 实现

这是 AI 压缩最显著的地方。曾经需要数天的样板代码、CRUD 操作、集成和配置现在可以在数分钟内生成。但速度带来了新的责任：生成的代码必须被理解、验证和维护。实现不再是瓶颈；验证才是。

#### 测试与质量保证

AI 正在将测试从手动、回顾性活动转变为自动、前瞻性的持续验证。AI Agent 可以生成单元测试、集成测试和端到端测试；识别覆盖缺口；创建测试数据；并运行持续监控。然而，定义*测试什么*、*如何*评估非功能性需求（可用性、安全性、性能），以及*何时*测试足够好，仍然是人类判断的问题。

---

[Page 23]

#### 代码审查与部署

AI 辅助的代码审查工具现在可以识别潜在问题——安全漏洞、性能反模式、风格违规——在人类审查者看到代码之前。部署管道越来越多地由 AI 监控，AI 可以检测异常、预测故障，甚至触发回滚。但审查的*标准*、部署的*时机*，以及接受风险的*决策*仍然是人类的。

#### 维护与演进

维护——调试、重构、功能演进——正在被 AI 改变。AI Agent 可以识别退化、建议重构，甚至实现修复。但理解*为什么*某事坏了、*什么*修复是正确的，以及*何时*进行维护与构建新东西，需要人类上下文和判断。

---

[Page 24]

## 工厂模型：构建构建软件的系统

我们已经看到 AI 如何变革 SDLC 的每个阶段。但最成功的团队不仅仅是在使用 AI 工具；他们正在构建*系统*来构建软件。这个系统就是我们所说的**工厂模型**。

工厂模型的核心洞察是：AI 模型本身——LLM——只是更大系统的核心。就像工厂中的电动机需要传送带、传感器、安全机制和装配线才能生产产品一样，AI 模型需要围绕它的结构才能可靠地生产软件。

这个结构就是**Harness**。

### Harness Engineering：模型之外的结构

Harness Engineering 是设计、构建和优化围绕 AI 模型的结构——工具、规则、测试、反馈循环和护栏——的实践。它是使 AI 从实验性原型转变为可靠生产系统的学科。

Harness 不是单一工具或文件。它是组件的*系统*，每个组件解决不同的问题，所有组件协同工作以产生可靠、可预测的输出。

---

[Page 25]

Harness Engineering 的核心组件包括：

1. **上下文层**：管理什么信息、何时、以什么格式呈现给模型。
2. **工具层**：定义模型可以调用什么 API、执行什么代码、查询什么数据。
3. **验证层**：测试、评估和护栏，确保输出满足标准。
4. **编排层**：管理循环——何时重试、何时升级、何时停止。
5. **可观察性层**：日志、跟踪和指标，用于理解发生什么、何时、为什么。
6. **部署层**：托管、身份、安全性和生产基础设施。

这些层不是顺序的；它们相互作用。上下文影响工具使用。工具结果触发验证。验证失败触发重试或升级。可观察性捕获整个过程。

---

[Page 26]

### Harness 中的内容

让我们更仔细地看看每个层中有什么。

**上下文层**包含：
- 系统指令和角色定义
- 规则文件（AGENTS.md、CLAUDE.md、GEMINI.md）
- 项目记忆和架构文档
- 技能库和参考模式
- 会话历史和当前任务上下文

**工具层**包含：
- API 定义和 MCP 服务器连接
- 代码执行环境（沙箱）
- 数据库查询接口
- 外部服务集成
- 其他 Agent 的委派接口

---

[Page 27]

**验证层**包含：
- 确定性测试（单元、集成、端到端）
- 非确定性评估（evals）
- 评分标准和 LM 评委
- 安全扫描和漏洞检测
- 风格和质量门禁

**编排层**包含：
- 循环逻辑（重试、升级、停止条件）
- 多 Agent 协调协议
- 任务分解和委派逻辑
- 错误处理和恢复机制

**可观察性层**包含：
- 结构化日志和跟踪
- 标记使用和成本指标
- 输出质量和成功率指标
- 异常检测和警报

**部署层**包含：
- 托管基础设施
- 身份和访问管理
- 安全性和合规性控制
- 生产监控和回滚能力

---

[Page 28]

### Harness 在 SDLC 中的应用

现在让我们看看 Harness 如何映射到我们在前一节中描述的 AI 驱动的 SDLC。

#### 1. 需求、规划与架构（配置 Harness）

在这个阶段，Harness 被配置：
- 系统指令和角色定义被建立
- 规则文件被编写和版本控制
- 架构文档和参考模式被加载到上下文中
- 技能库被选择和配置
- 工具连接（API、MCP 服务器）被建立

这个阶段是资本支出（CapEx）投资发生的地方。工程时间用于构建结构，而不是编写代码。

---

[Page 29]

#### 2. 实现（运行 Harness）

在这个阶段，Harness 被运行：
- 开发者提供意图（规范、用户故事、架构约束）
- Agent 使用配置的上下文和工具生成实现
- 验证层在每次迭代中检查输出
- 编排层管理循环——重试、升级或继续

这是运营支出（OpEx）发生的地方。每次交互都消耗标记；每次验证运行测试；每次工具调用使用资源。Harness 的设计直接决定了这种 OpEx 的效率。

#### 3. 测试与 QA（反馈循环）

在这个阶段，Harness 的反馈循环被激活：
- 确定性测试验证功能正确性
- 评估验证非功能性质量
- 安全扫描检测漏洞
- 风格和质量门禁执行标准

反馈循环是 Harness 的心脏。没有它，你只是在希望输出是正确的。有了它，你有了系统化的信心。

---

[Page 30]

#### 4. 代码审查、部署与维护（观察 Harness）

在这个阶段，Harness 被观察和优化：
- 可观察性数据被分析以识别改进
- 标记使用被优化以降低成本
- 失败模式被识别并解决
- 规则文件和技能被更新以反映学习

这个阶段是持续改进发生的地方。Harness 不是一次性构建然后被遗忘的；它是一个活的系统，随着使用而演进。

---

[Page 31]

## 开发者的角色演变：从指挥家到编排者

随着 AI 承担更多实现工作，开发者的角色正在转变。我们看到了两种新兴角色：**指挥家**和**编排者**。

### 指挥家：动手、实时指导

指挥家是实时与 AI 合作的开发者。他们：
- 编写提示并立即接收输出
- 迭代地指导 AI，实时调整方向
- 审查每行生成的代码
- 对实现做出即时决策

指挥家模式类似于传统的结对编程，但 AI 作为副驾驶。它最适合探索、原型设计和需要人类判断的快速迭代。

---

[Page 32]

### 编排者：异步、多 Agent 委派

编排者是设计和协调多 Agent 系统的开发者。他们：
- 定义架构和约束
- 将任务委派给专门的 Agent
- 监控进度并处理异常
- 审查最终输出，而非每行代码

编排者模式类似于管弦乐队指挥。指挥不演奏每种乐器；他们确保每个演奏者在正确的时间演奏正确的音符。编排者不编写每行代码；他们确保每个 Agent 在正确的时间做正确的事情。

---

[Page 33]

### 80% 问题

我们所说的"80% 问题"是：AI 现在可以生成大约 80% 的代码——样板、CRUD、集成、配置。但剩下的 20%——架构决策、复杂业务逻辑、性能优化、安全关键代码——仍然需要人类专业知识。

80% 问题意味着：
- **速度不均衡**：80% 很快，20% 很慢
- **验证瓶颈**：快速生成的代码需要缓慢的人类审查
- **技能差距**：开发者需要理解架构，而不仅仅是实现
- **责任模糊**：当 AI 生成 80% 时，谁对输出负责？

解决 80% 问题需要：
- 将人类注意力集中在 20% 上
- 为 80% 构建可靠的验证
- 明确责任和所有权
- 培养架构和判断技能

---

[Page 34]

### 编码 Agent 实践

编码 Agent 在实践中是什么样子？以下是几个常见模式：

**副驾驶模式**：开发者在 IDE 中编写代码，AI 提供内联建议、完成和重构。人类保持控制，AI 加速输入。

**结对模式**：开发者与 AI 聊天界面合作，描述功能，接收实现，迭代改进。人类提供意图，AI 提供实现。

**委派模式**：开发者将任务委派给 AI Agent，Agent 自主规划、实现、测试和提交拉取请求。人类审查结果，而非过程。

**工厂模式**：开发者设计 Harness，多个 AI Agent 在约束下运行，人类监控和优化系统。这是 agentic engineering 的终极表达。

---

[Page 35]

## 编码 Agent 在开发者日常中的位置

编码 Agent 不是开发者的替代品；他们是开发者工具包的扩展。以下是编码 Agent 如何融入典型开发者的一天：

**上午：规划与探索**
- 使用 AI 分析需求、生成用户故事、探索架构方案
- 让 AI 生成原型和概念验证
- 使用 AI 识别潜在风险和边缘情况

**下午：实现与验证**
- 让 AI 生成样板代码和 CRUD 操作
- 人类专注于复杂业务逻辑和架构决策
- 使用 AI 生成测试并验证覆盖

**傍晚：审查与优化**
- 审查 AI 生成的代码，重点关注架构和正确性
- 优化 Harness 以提高明天的效率
- 更新规则文件和技能以反映学习

---

[Page 36]

## Vibe Coding 生产级 Agent

将 vibe coding 转变为生产级 Agentic Engineering 需要什么？以下是关键转变：

**从随意提示到正式规范**
- 用结构化规范替换随意提示
- 定义明确的输入、输出和约束
- 使用架构文档和记忆文件

**从手动验证到自动化验证**
- 编写测试套件，而非依赖"看起来能工作"
- 建立评估以验证非功能性质量
- 实施 CI/CD 门禁

**从单一模型到多模型编排**
- 将复杂任务路由到强大模型
- 将常规任务路由到更快、更便宜的模型
- 协调多 Agent 系统

---

[Page 37]

**从临时上下文到工程化上下文**
- 建立规则文件（AGENTS.md、CLAUDE.md）
- 创建技能库和参考模式
- 管理静态和动态上下文

**从个人实践到团队实践**
- 共享 Harness 组件作为团队资产
- 建立代码审查标准
- 记录和版本控制一切

**从速度到质量**
- 接受前期 CapEx 投资
- 专注于长期 OpEx 减少
- 优先考虑可维护性和可靠性

---

[Page 38]

生产级 Agentic Engineering 的关键原则：

1. **规范驱动**：从明确的规范开始，而非随意提示
2. **验证优先**：在生成代码之前编写测试和评估
3. **上下文工程**：投资于高质量、结构化的上下文
4. **人类监督**：保持人类对架构和质量的判断
5. **持续改进**：将 Harness 作为活的系统来维护
6. **可观察性**：测量一切，从标记使用到输出质量
7. **安全性**：实施护栏和零信任开发实践

---

[Page 39]

## AI 开发的经济学

当评估 AI 对软件开发生命周期的影响时，对话通常以开发者速度开始和结束：我们能多快地编写代码？然而，对于工程领导者来说，更关键的指标是**总拥有成本（TCO）**。

要了解 AI 辅助开发的真实成本，我们必须看看不同工作流如何在资本支出（CapEx）——构建某物的前期投资——和运营支出（OpEx）——运行、修复和维护它的持续成本——之间转移财务和运营负担。至关重要的是，在 AI 时代，OpEx 在很大程度上由标记经济决定。

---

[Page 40]

**图 9：AI 开发的经济学**

### Vibe Coding 的隐性债务（低 CapEx，高 OpEx）

乍一看，vibe coding 似乎极具成本效益。进入门槛基本为零：标准 AI 助手的月度订阅和几个随意提示。CapEx 可以忽略不计，因为开发者完全依赖模型的基线能力，而不是投入时间进行系统设计。

然而，vibe coding 的经济学隐藏了巨大的、复利的 OpEx 负担：

- **标记燃烧率**：与 LLM 的每次交互都会根据输入和输出标记产生成本。在 vibe coding 中，开发者经常将大量未结构化文件倾倒入上下文窗口，反复要求模型修复自己未验证的错误。这创造了一个昂贵的"提示循环"，以低首次通过成功率燃烧 API 标记。

---

[Page 41]

- **维护税**：通过临时提示编写的代码通常缺乏结构性一致性。当六个月后出现错误时，人类工程师必须花费数天逆向工程未结构化的、AI 生成的"意大利面条"代码。
- **安全修复**：没有自动化评估 Harness，代码的快速生成会导致漏洞的快速生成。在生产中修复安全缺陷的成本比在设计阶段捕获它指数级更高。

### Agentic Engineering 的投资（高 CapEx，低 OpEx）

Agentic engineering 翻转了这个经济模型。它需要在单行生产代码生成之前，有意识地、前期投入工程时间和资源。

Agentic engineering 中的 CapEx 包括设计 API 模式、构建确定性测试套件，以及最重要的是，构建 Agent 的上下文。虽然这个前期成本更高，但交付和维护功能的边际成本急剧下降。AI 在严格管理的"工厂"内运行，意味着其输出结构健全、经过预测试并符合公司标准。

### 上下文工程作为财务杠杆

在标记经济中，上下文工程不仅是技术技能——它是财务策略。LLM 对你发送的每条信息收费。将整个 100,000 标记的仓库传递给每个提示在规模上是财务不可行的。

---

[Page 42]

有效的上下文工程确保模型接收到密集、高信令的有效载荷（如精确的 AGENTS.md 文件和架构护栏），而不是庞大、嘈杂的有效载荷。通过提前提供正确的上下文，开发者显著提高 Agent 的首次通过成功率，避免困扰 vibe coding 的昂贵试错循环。

### 通过动态上下文和技能扩展效率

为了真正优化 OpEx，高级 Agentic engineering 依赖于通过"技能"或工具调用（如 Model Context Protocol 服务器）使用动态上下文，我们在 day-3 论文中详细介绍了这一点。

### 智能模型路由

此外，Agentic engineering 允许智能模型路由。在 vibe coding 工作流中，开发者通常依赖单一的、巨大的前沿模型进行每次交互——支付优质标记价格，只是要求 AI 修复拼写错误或生成基本单元测试。

设计良好的工厂模型避免了这种浪费。它将大型、高级模型用于高度复杂的任务（需求、架构和初始实现），但自动将确定性、较低复杂性的任务（测试生成、代码审查和 CI/CD 监控）路由到更小、更快、显著更便宜的模型。通过编排多模型生态系统，工程团队可以保持峰值输出质量，同时系统性地降低运营标记成本。

---

[Page 43]

## 从哪里开始

从语法到意图的转变不是未来状态。它是我们今天面前的工作。无论你是作为个人建设者阅读本文，还是作为领导者思考团队或组织如何采用这些工具，同样的基本原则都成立：AI 放大它落地的工程文化。以下实践将该原则转化为行动。

### 对于个人开发者

1. **为项目设置 AGENTS.md（或等效文件）**。选择匹配所选编码代理的约定。从十行开始：技术栈、规范、硬规则、工作流。每次 Agent 做了不应该再做的事情时添加一条规则。

2. **为你的编码代理安装一组技能**（如 Agents CLI）来构建、评估、部署和优化 Agent。

3. **选择一个重复性工作流并使其成为第一个 Agent**。研究工作流、代码审查过程、定期报告、定期生成的内容。使用编码代理进行原型设计，当它证明自己的价值时，通过 Agents CLI 将其升级为生产 Agent。从头到尾构建一个 Agent 比阅读一百个更有教育意义。

---

[Page 44]

4. **在生成代码之前编写测试和评估**。它们一起是与 AI 的合同。一个编写良好的测试和评估套件比任何自然语言提示更精确地传达意图，并将 AI 辅助开发从 vibe coding 转变为 agentic engineering。

5. **审查 Agent 生成的每一行将要发布的代码**。对任何看起来聪明的东西持怀疑态度。检查导入是否为真实包。验证错误处理是否覆盖真实的失败模式。团队不理解的代码成为团队无法承受的调试成本。

6. **保持你的开发者技能**。AI 处理常规工作，以便开发者可以专注于挑战。这种安排只有在基础技能——调试、系统设计和对性能与正确性的直觉——保持敏锐的情况下才有效。将 AI 视为在更大规模上应用专业知识的方式，而不是替代它。定期练习复杂调试、AI 输出的代码审查和架构讨论对于成长为工程师仍然至关重要。

---

[Page 45]

### 对于工程领导者

1. **使上下文工程成为团队的一等工程实践**。将 AGENTS.md、系统提示、评估套件和技能库视为代码：在拉取请求中审查，与项目一起版本化，由指定的工程师拥有。没有这种纪律，Harness 会漂移，Agent 行为在团队中变得不可复现。

2. **将标准设在评估，而非演示**。一个工作演示证明 Agent 可以成功一次。一个通过的评估套件证明它可靠地成功。但没有明确评分标准的评估什么也不测量。定义你正在评分的内容：任务成功、工具使用质量、轨迹合规性、幻觉和响应质量。要求评估覆盖率和明确评分标准作为任何 Agent 进入共享工作流的前提条件，就像测试覆盖率控制服务部署一样。

3. **重塑 AI 生成代码的代码审查**。AI 生成代码需要与人类编写代码相同或更多的审查，额外关注幻觉依赖、不充分的错误处理以及乍一看正确但微妙的正确性差距。培训审查者了解生成代码的故障模式，并相应调整审查清单。

---

[Page 46]

4. **在团队规范中区分原型工作与生产工作**。Vibe coding 是探索的正确速度。Agentic engineering 是生产的正确纪律。使边界明确：哪些项目、哪些分支、哪些环境需要哪种工作模式。保持这种区别模糊的团队会意外地将原型发布到生产。

5. **将 Harness 组件作为共享团队资产进行投资**。可重用的系统提示、技能库、MCP 服务器连接和评估 Harness 跨项目复利。将它们作为基础设施对待：记录、维护并有意识地改进。从 AI 辅助开发中复利最多价值的团队是那些构建一次 Harness 并多次完善的团队。

### 对于组织

1. **将 AI 辅助开发视为工程投资，而非生产力功能**。获得最大收益的团队将 AI 工具与评估覆盖、可观察性和清晰的架构标准配对。在没有该脚手架的情况下推出编码代理会产生没有质量的速度，这比任何团队能偿还的速度更快地复利成技术债务。

---

[Page 47]

2. **在规模之前投资生产基板**。笔记本电脑上的 vibe coding 原型不是生产系统。使一个毕业到另一个的是围绕它的运营纪律：在 CI 中运行的轨迹和最终响应评估、每次 Agent 运行的跟踪、每个 Agent 的范围权限，以及针对生成代码故障模式调整的安全审查。在第一个生产 Agent 发布之前构建这个基板，而不是之后。

3. **采用开放工具和 Agent 间通信标准**。Model Context Protocol (MCP) 用于工具访问，Agent2Agent (A2A) 用于跨 Agent 委派，正在融合为多 Agent 系统的结缔组织。现在选择它们保持混合供应商和框架的选项开放，并避免以后重新平台化。

4. **规划人类和 Agent 的混合团队，而非纯人类或纯 Agent 工作流**。过去一年最强的生产结果来自人类设定方向、Agent 做实现、明确的切换协议管理边界的架构。代码审查流程、轮班轮换和团队结构都需要演进，以反映 Agent 现在是参与者，而不仅仅是工具。

5. **围绕判断而非仅实施重新定义招聘和技能发展**。随着实施变得更快、更自动化，瓶颈转移到规范、评估、架构判断和审查。有意识地雇佣和发展这些技能。未来几年最有价值的工程师将是那些能很好指导 Agent 的人，而不是那些能写最多代码的人。

---

[Page 48]

## 结论：意图作为新的界面

从语法到意图的转变不是未来预测——它是现在的现实。开发者已经花费更多时间描述他们想要什么，而不是指定如何构建它。SDLC 已经被压缩、重构和围绕 AI 能力重新想象。问题不是这种转变是否会发生，而是个人开发者、团队和组织将如何有效地驾驭它。

我们在本文中呈现的框架——从 vibe coding 到 agentic engineering 的光谱、从指挥家到编排者模型的开发者角色、环境、工作流和自主 Agent 的分类法，以及软件生产的工厂模型——为理解快速演进格局提供了一套心智模型。即使具体工具和能力演进，这些模型仍然有用。

三个原则作为持久的脱颖而出：

1. **结构扩展，vibes 不扩展**。Vibe coding 是探索、原型设计和个人项目的有效方法。但对于组织依赖的软件，agentic engineering 的纪律——规范、测试、护栏和对架构的人类监督——不是可选的。"它似乎能工作"和"它在所有条件下正确工作"之间的差距是生产中断、安全漏洞和维护噩梦所在的地方。

---

[Page 49]

2. **AI 放大你的工程文化**。具有强大测试实践、清晰架构标准和健康代码审查流程的组织从 AI 辅助开发中获得戏剧性更多的价值，比那些没有的组织。AI 是力量倍增器——它既放大你的优势，也放大你的弱点。

3. **人类角色在演进，而非在缩减**。理解架构、能定义精确规范、批判性评估输出并设计有效的约束和反馈循环系统的建设者比以往任何时候都更有价值。重要的技能正在从实施转向判断，从编写代码转向设计生产代码的系统。

我们正处于一场变革的开端，这场变革将重塑不仅软件如何构建，而且什么类型的软件是可能的。较小的团队将能够解决较大的问题。个人开发者将能够构建和维护以前需要整个部门的系统。创建软件的门槛将继续下降，向更广泛的人群开放软件开发实践。

蓬勃发展的团队将是那些拥抱 AI 作为强大工具同时保持一直是可靠软件基础的工程纪律的团队。他们将理解，软件工程的未来不是关于在人类专业化和 AI 能力之间做出选择——而是关于设计两者都贡献其独特优势的系统。

**生成已解决。验证、判断和方向是新的工艺。**

---

[Page 50]

## 尾注

1. GetPanto, "AI Coding Assistant Statistics 2025-2026," https://www.getpanto.ai/blog/ai-coding-assistant-statistics; Index.dev, "Developer Productivity Statistics with AI Tools," https://www.index.dev/blog/developer-productivity-statistics-with-ai-tools
2. Karpathy, A., "Vibe Coding," X/Twitter post, February 2025. https://x.com/karpathy/status/1886192184808149383; Wikipedia, "Vibe coding," https://en.wikipedia.org/wiki/Vibe_coding
3. Osmani, A., "Agentic Engineering," https://addyosmani.com/blog/agentic-engineering/
4. Karpathy, A., "From Vibe Coding to Agentic Engineering," 2026; The New Stack, "Vibe Coding is Passe," https://thenewstack.io/vibe-coding-is-passe/
5. Glide Blog, "What is Agentic Engineering?" https://www.glideapps.com/blog/what-is-agentic-engineering; The New Stack, "Vibe Coding, Agentic Engineering," https://thenewstack.io/vibe-coding-agentic-engineering/
6. CircleCI, "AI-Native SDLC," https://circleci.com/blog/ai-sdlc/
7. GroovyWeb, "SDLC in the AI Era: Software Development 2026," https://www.groovyweb.co/blog/sdlc-ai-era-software-development-2026; EPAM, "From Traditional Software to a Native AI SDLC," https://www.epam.com/about/newsroom/in-the-news/2026/from-traditional-software-to-a-native-ai-sdlc-how-genai-is-redefining-engineering
8. Osmani, A., "The Factory Model," https://addyosmani.com/blog/factory-model/
9. Deloitte, "AI in Software Engineering: Productivity Gains 2025-2026," projecting 30-35% gains across the full development process.
10. METR, "Uplift Update: Measuring the Impact of AI Coding Tools," February 2026, https://metr.org/blog/2026-02-24-uplift-update/
11. Google, "Introduction to Agents," Agents Whitepaper Series, November 2025.
12. Osmani, A., "From Conductors to Orchestrators: The Future of Agentic Coding," https://addyosmani.com/blog/future-agentic-coding/

---

[Page 51]

13. Google, "Jules: AI-Powered Coding Agent," https://developers.googleblog.com/en/the-next-chapter-of-the-gemini-era-for-developers/
14. Osmani, A., "The 80% Problem in Agentic Coding," https://addyo.substack.com/p/the-80-problem-in-agentic-coding
15. Medium, Dave Patten, "The State of AI Coding Agents 2026: From Pair Programming to Autonomous AI Teams," https://medium.com/@dave-patten/the-state-of-ai-coding-agents-2026-from-pair-programming-to-autonomous-ai-teams-b11f2b39232a
16. Lawfare, "When the Vibes Are Off: The Security Risks of AI-Generated Code," https://www.lawfaremedia.org/article/when-the-vibe-are-off--the-security-risks-of-ai-generated-code
17. Google, "Introduction to Agents," Multi-Agent Systems and Design Patterns section, November 2025.
18. Google, "Agent Development Kit (ADK)," https://google.github.io/adk-docs/; Kartakis, S., "From Zero to Multi-Agents: A Beginner's Guide to Google Agent Development Kit (ADK)," https://medium.com/@sokratis.kartakis/from-zero-to-multi-agents-a-beginners-guide-to-google-agent-development-kit-adk-b56e9b5f7861
19. Google, "Agent-to-Agent (A2A) Protocol," https://google.github.io/a2a-protocol/; Kartakis, S. and Hotz, H., "Generative AI in the Real World: Understanding A2A," O'Reilly Podcast, https://www.oreilly.com/radar/podcast/generative-ai-in-the-real-world-understanding-a2a-with-heiko-hotz-and-sokratis-kartakis/
20. TLDL, "AI Coding Tools 2026," https://www.tldl.io/resources/ai-coding-tools-2026; Kanerika, "GitHub Copilot vs Claude Code vs Cursor vs Windsurf," https://kanerika.com/blogs/github-copilot-vs-claude-code-vs-cursor-vs-windsurf/
21. Google, "Gemini Code Assist," https://cloud.google.com/gemini/docs/codeassist/overview
22. Dark Reading, "Coders Adopt AI Agents, but Security Pitfalls Lurk in 2026," https://www.darkreading.com/application-security/coders-adopt-ai-agents-security-pitfalls-lurk-2026
23. Google, "Gemini CLI," https://github.com/google-gemini/gemini-cli
24. Google, "Agent Tools: Interoperability with Model Context Protocol (MCP)," Agents Whitepaper Series, November 2025
25. Google, "Agent Quality" and "Prototype to Production," Agents Whitepaper Series, November 2025
26. Lawfare, "When the Vibes Are Off: The Security Risks of AI-Generated Code," https://www.lawfaremedia.org/article/when-the-vibe-are-off--the-security-risks-of-ai-generated-code
27. DevOps.com, "AI-Generated Code Packages Can Lead to Slopsquatting Threat," https://devops.com/ai-generated-code-packages-can-lead-to-slopsquatting-threat/
28. Osmani, A., "Beyond Vibe Coding," O'Reilly Media, 2025-2026, https://www.oreilly.com/library/view/beyond-vibe-coding/9798341634749/
29. "Awesome LLM Apps," https://github.com/Shubhamsaboo/awesome-llm-apps
30. Osmani, A., "My LLM Coding Workflow Going Into 2026," https://addyosmani.com/blog/ai-coding-workflow/
31. Questera, "7 AI Coding Trends to Watch in 2026," https://www.questera.ai/blogs/7-ai-coding-trends-to-watch-in-2026
32. DEV Community, "Programming in the Age of AI: From Code to Intent," https://dev.to/robertobutti/programming-in-the-age-of-ai-from-code-to-intent-46eo

---

*翻译完成。本文档与原文 51 页一一对应，术语表统一，含页码交叉引用标记。*
