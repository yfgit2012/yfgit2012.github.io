## Context Engineering for Agents

<think>
</think>

文章解析了AI Agent失败的主要原因，指出多数问题源于上下文工程而非模型能力。上下文工程是系统性设计动态上下文组合的学科，与提示词工程和检索增强生成不同，后者侧重单点优化而上下文工程关注全局信息管理。其核心在于通过写入、选取、压缩、隔离四类策略，解决长上下文带来的冗余、冲突和性能问题。例如，邮件响应案例显示有效上下文管理能提升任务执行效率，而长任务案例则揭示无差别上下文注入会导致信息退化。文章强调，随着基础模型能力提升，上下文工程成为工业级应用的关键，需结合多Agent架构和标准化接口实现高效信息处理。关键点：1. 上下文工程是AI Agent性能瓶颈的核心解决方案；2. 区分Prompt Engineering/RAG与上下文工程的系统性差异；3. 四大策略（写入/选取/压缩/隔离）应对上下文管理挑战；4. 多Agent架构与MCP协议支撑稳健的上下文工程实践。

#### Translation 

<think>
Okay, let's tackle this query. The user wants me to analyze the provided article, extract key points, summarize it into a few paragraphs, and list the key points. The summary needs to be in the same language as the article, within 50% of the original length, and without any preambles or other content.

First, I need to read through the article carefully. It's about Context Engineering in AI Agents, explaining what it is, how it differs from Prompt Engineering and RAG, and why it's important. The author uses examples to illustrate the necessity of Context Engineering, like the email response example and the long-term task example. They also mention the four components of Context Engineering: Write, Select, Compress, and Isolate.

Now, I need to identify the main points. The key points are: Context Engineering is crucial for AI Agent performance, it's different from Prompt Engineering and RAG, it involves managing context through four strategies, and it's necessary to avoid issues like context overflow and inefficiency. The examples show how proper context management improves task execution.

Next, the summary should be concise. I need to make sure it's in Chinese, under 50% of the original length. The original article is quite long, so I'll condense it into a few paragraphs. The summary should cover the definition, importance, differences from other methods, and the four strategies. The key points section should list the main ideas clearly.

I need to avoid any markdown and keep the response straightforward. Let me check if I missed any important details. The article also mentions MCP (Model Context Protocol) as part of the infrastructure for Context Engineering. I should include that in the summary and key points.

Finally, ensure that the summary and key points are accurate, concise, and meet the user's specifications. No preambles, just the required content. Let me put it all together now.
</think>

文章解析AI Agent失败原因，指出多数问题源于上下文工程而非模型能力。上下文工程（Context Engineering）是系统性设计动态上下文组合的学科，与提示词工程（Prompt Engineering）和检索增强生成（RAG）不同，后者侧重单点优化而上下文工程关注全局信息管理。其核心在于通过写入、选取、压缩、隔离四类策略，解决长上下文带来的冗余、冲突和性能问题。例如，邮件响应案例显示有效上下文管理能提升任务执行效率，而长任务案例则揭示无差别上下文注入会导致信息退化。文章强调，随着基础模型能力提升，上下文工程成为工业级应用的关键，需结合多Agent架构和标准化接口（如MCP）实现高效信息处理。关键点：1. 上下文工程是AI Agent性能瓶颈的核心解决方案；2. 区分Prompt Engineering/RAG与上下文工程的系统性差异；3. 四大策略（写入/选取/压缩/隔离）应对上下文管理挑战；4. 多Agent架构与MCP协议支撑稳健的上下文工程实践。

#### Reference: 

https://rlancemartin.github.io/2025/06/23/context_engineering/