## LLM powered autonomous agents - by Lilian Weng

Here are the contents translated into English:

The article by Lilian Weng explores the potential and challenges of building AI entities based on large language models. The article first introduces the HuggingGPT framework, which uses ChatGPT as a task planner that can select models from the HuggingFace platform and induce a summary response based on execution results.

The HuggingGPT system consists of four stages: task planning, model selection, task execution, and response generation. In the first stage, large language models parse user requests into multiple tasks with four associated attributes: task type, task ID, dependencies, and parameters. In the second stage, the model selects a model from a list, assigns tasks to expert models, considering the limited context length and filtering based on task types.

The third stage is the task execution phase, where expert models execute specific tasks and record results. The fourth stage is response generation, where the large language model receives execution results and provides an overall result to users.

Lilian also mentioned several challenges: improving efficiency, stability of large language model outputs and external service models, and limitations of building intelligent entities based on large language models, such as limited context length, long-term planning, task decomposition challenges, and reliability of natural language interfaces.

The article also introduces a testing tool - the Enhanced Large Language Model Performance Benchmark API Bank, which includes 53 common API tools. Lilian also provides an example - a chemical entity ChemCrow designed by large language models to perform tasks such as organic synthesis, drug discovery, and material design.

Finally, Lilian mentions the concept of generative entities and a project called AutoGPT based on GPT models that combines memory and body - a self-sustaining system that can complete tasks autonomously, with internet access, long-term and short-term memory management, text generation, etc.

In summary, this article provides an overview of the potential and challenges of building AI entities, particularly in the direction of developing intelligent entities based on large language models.

#### Translation 

Lilian Weng 的文章探讨了基于大语言模型构建 AI 智能体的潜力和挑战。文章首先介绍了 HuggingGPT 框架，该框架利用 ChatGPT 作为任务规划器，可以选择 HuggingFace 平台上的模型，并根据执行结果归纳总结出响应。

HuggingGPT 系统由四个阶段组成：任务规划、模型选择、任务执行和响应生成。第一个阶段大语言模型将用户请求解析为多个任务，每个任务有四个关联的属性：任务类型、任务 ID、依赖项和参数。第二个阶段大语言模型从一个模型列表中选择模型，将任务分配给专家模型，考虑到上下文长度有限，需要进行基于任务类型的过滤。

第三个阶段是任务执行阶段，专家模型执行具体的任务，并记录任务结果。第四个阶段是响应生成阶段，大语言模型接收执行结果并向用户提供总体的结果。

Lilian 还提到了几个挑战：提高效率、大语言模型输出和外部模型服务的稳定性，以及基于大语言模型构建智能体的一些限制，如有限的上下文长度、长期规划和任务分解的挑战，以及自然语言接口的可靠性。

文章还介绍了一个评估工具——增强型大语言模型性能的基准 API Bank，包含了 53 个常用的 API 工具。Lilian 还提供了一个案例——用来进行科学发现的智能体 ChemCrow，它是一个由大语言模型设计的化学智能体，可以完成有机合成、药物发现和材料设计方面的任务。

最后，Lilian 提到了生成式智能体的概念，以及基于 GPT 的模型的一个内存和身体的结合——AutoGPT。该项目能够自主完成任务，并具有互联网访问、长期和短期的内存管理、文本生成等功能。

总之，这篇文章提供了一个全面了解 AI 智能体构建的潜力和挑战的概述，特别是基于大语言模型的智能体的发展方向。

#### Reference: 

https://lilianweng.github.io/posts/2023-06-23-agent/