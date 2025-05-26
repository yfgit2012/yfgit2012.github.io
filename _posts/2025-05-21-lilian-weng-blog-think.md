## Lilian Weng: Why We Think

<think>
Okay, the user wants me to translate the contents within the <document> tags into English. Let me first check the original text. It's in Chinese, and the user specified not to include any preambles or other content, just the translation. 

Wait, the example response they provided is in English, but the original document is in Chinese. So the task is to translate the Chinese content inside the <document> tags into English. The user also mentioned not to include any preambles or other contents, so I need to make sure the response is only the translated text.

Looking at the example, the assistant translated the Chinese text into English without any extra text. So I need to do the same. First, I'll extract the Chinese content from the <document> tags. The content is: "Lilian Weng的博客《Why We Think》探讨了如何通过多种方法提升AI模型的思考能力。核心观点包括：延长模型思考时间的动机源于心理学类比（系统1/系统2）、计算资源优化及潜变量建模；模型思考方式分为Token级思考（如思维链CoT）、连续空间思考（如自适应计算时间）和潜变量思考（如EM算法）。研究显示，测试时计算（如并行采样、序列修正）可显著提升性能，但需平衡效率与准确性。同时，CoT存在忠诚度失效风险，需谨慎优化。未来方向包括解决奖励作弊、无标签自修正及提升模型推理的可解释性。</document>"

Now, I need to translate this into English. Let me go through each part. The first sentence is about Lilian Weng's blog discussing methods to enhance AI models' thinking. The core points include motivations for extending thinking time, which are psychological analogies (system 1/system 2), computational resource optimization, and latent variable modeling. The thinking methods are categorized into token-level (like CoT), continuous space (adaptive computation time), and latent variable approaches (like EM algorithm). The research shows that test-time computation (parallel sampling, sequence correction) can improve performance but requires balancing efficiency and accuracy. CoT has risks of fidelity failure, needing cautious optimization. Future directions include solving reward hacking, unsupervised self-correction, and enhancing model reasoning interpretability.

I need to ensure the translation is accurate and maintains the structure. Also, check for any technical terms that need to be correctly translated, like "思维链CoT" which is "Chain-of-Thought (CoT)". "潜变量建模" is "latent variable modeling". "测试时计算" is "test-time computation". "奖励作弊" is "reward hacking". 

Once translated, I should present it without any additional text, just the translated content. Let me verify that the translation captures all key points and is concise. The user didn't mention any specific formatting, so plain text is fine. Alright, that should do it.
</think>

Lilian Weng's blog "Why We Think" explores methods to enhance AI models' reasoning capabilities. Key points include: motivations for extending model thinking time stem from psychological analogies (System 1/System 2), computational resource optimization, and latent variable modeling; model thinking approaches are categorized into token-level thinking (e.g., Chain-of-Thought), continuous space thinking (e.g., adaptive computation time), and latent variable thinking (e.g., EM algorithm). Research shows test-time computation (e.g., parallel sampling, sequence correction) can significantly improve performance but requires balancing efficiency and accuracy. Meanwhile, CoT faces risks of fidelity failure, necessitating cautious optimization. Future directions involve addressing reward hacking, unsupervised self-correction, and enhancing model reasoning interpretability.

#### Translation 

<think>
Okay, let's see. The user wants a summary of the document in no more than 50% of the original length. They specified not to include any preambles or other content, just the summary. The document is about Lilian Weng's blog post on AI models' thinking processes, covering methods like thought chains, external tools, and latent variables. 

First, I need to identify the key points. The main sections are the three levels of motivation for extending model thinking time, the three types of thinking methods (token-level, continuous space, latent variables), and the challenges and open problems. 

I should condense each section into a concise summary. For example, the motivation includes psychology, computational resources, and latent variables. The thinking methods are CoT, continuous space thinking, and latent variables. The challenges involve issues with CoT's fidelity and open questions like reward hacking.

I need to ensure the summary is under 50% of the original length. Let me check the original text's length. The original is quite long, so the summary should be roughly half. I'll make sure to omit any examples or specific studies unless they're critical. Also, avoid any introductory phrases like "In this blog post..." and focus on the core content. 

Wait, the user mentioned not to include any preambles, so I should start directly with the summary. Also, avoid markdown, just plain text. Let me structure it in clear, concise sentences. Make sure to mention the three categories of thinking methods and the key challenges. Highlight the main findings like the effectiveness of test-time computation and the open problems. 

Double-check that the summary doesn't exceed 50% of the original. Let me count the words. The original has around 1000 words, so the summary should be around 500. I'll need to be precise. Remove redundant details, keep the main points. Alright, that should cover it.
</think>

Lilian Weng的博客《Why We Think》探讨了如何通过多种方法提升AI模型的思考能力。核心观点包括：延长模型思考时间的动机源于心理学类比（系统1/系统2）、计算资源优化及潜变量建模；模型思考方式分为Token级思考（如思维链CoT）、连续空间思考（如自适应计算时间）和潜变量思考（如EM算法）。研究显示，测试时计算（如并行采样、序列修正）可显著提升性能，但需平衡效率与准确性。同时，CoT存在忠诚度失效风险，需谨慎优化。未来方向包括解决奖励作弊、无标签自修正及提升模型推理的可解释性。

#### Reference: 

https://lilianweng.github.io/posts/2025-05-01-thinking/## Lilian Weng: Why We Think

Here is the translation:

How to enable machines to think at a deeper level is a fundamental question that has been attempted to be answered in the AI field for a long time.

There are three motivations: psychological analogy, computational resources, and latent variable modeling.

Token-level thinking is the most researched and widely applied area, which means that models can make decisions through generating a series of intermediate tokens, or thought steps.

CoT provides valuable interpretability, but only if it accurately reflects the model's "thinking process", and CoT's loyalty fails in certain patterns.

The fundamental purpose of test-time computation (test-time compute) during testing is to dynamically adjust the output distribution of the model during inference. Directly adding the CoT monitoring signal into reinforcement learning rewards will cause the model to learn how to "hide" its true intentions.

Lilian suggests that optimizing CoT should be done with great caution, and even avoided if possible.

The second way models think is continuous space thinking, which differs from discrete token sequences. This type of pattern allows the model to think in a "continuous" time dimension.

The third way models think is to consider testing-time thought steps as latent variables, optimizing these variables to improve the model's performance.

There is ample evidence that allowing models to invest additional computational resources during inference can significantly improve their performance before producing an answer.

Recent research shows that optimizing test-time computation for large language models may be more effective than extending the model's parameters.

Note: CoT stands for Cognitive Transformer, and Lilian refers to a researcher or expert in the field.

#### Translation 

<document>

如何让机器实现更深层次的思考 这是AI领域中一直在尝试回答的一个根本性问题。

动机有三种：心理学上的类比、计算资源和潜变量建模。 

Token级思考是目前研究最深入、应用最广的领域，指的是模型会通过生成一系列的中间token，也就是思考步骤来辅助做出最终的决策。

CoT提供了宝贵的可解释性，但是前提得是它真实反映了模型的“思考过程”，而恰恰在某些模式下 CoT的忠诚度会失效。 

测试时计算（test-time compute）的根本目的在于，在推理过程中动态地调整模型的输出分布。直接将CoT的监控器信号加入强化学习奖励 会导致模型学会“隐藏”真实的意图。

Lilian建议，对CoT进行直接的优化压力要非常谨慎，甚至应该尽量避免。

模型的第二类思考方式就是连续空间思考，不同于离散的token序列。这一种模式允许模型在“连续”的时间维度上思考。

模型的第三类思考方式是将测试时的思考步骤视为潜变量，通过优化这些潜变量来改善模型的性能。 

已有大量的证据表示，允许模型在推理时投入额外的计算资源，让它在产生最终答案之前进行思考，可以显著提升模型的性能。

最近的研究表明，优化大语言模型的测试时计算可能比扩展模型的参数更加有效。 

</document>

#### Reference: 

https://lilianweng.github.io/posts/2025-05-01-thinking/## Lilian Weng: Why We Think

Here are the contents of the <document> XML tags translated into English:

**Key Points:**

1. **Motivation for Deep Thinking**: The article discusses the motivation behind creating AI models that can think deeply, comparing it to human cognition and the need for "slow thinking" in problem-solving.
2. **Three Types of Thinking**: Lilian Weng categorizes deep thinking into three types: Token-level thinking (CoT), Continuous Space thinking, and Pseudovariable thinking.
3. **Token-level Thinking (CoT)**: This is the most researched and applied area, where models generate a series of intermediate tokens (thinking steps) to aid decision-making.
4. **Continuous Space Thinking**: This allows models to think in continuous time, with self-adaptive computation time, enabling dynamic decision-making.
5. **Pseudovariable thinking**: This involves optimizing the thinking process as a latent variable, using Expectation-Maximization (EM) algorithm to improve model performance.

**Challenges and Open Problems:**

1. **Optimizing CoT**: The article highlights the challenges in directly optimizing CoT, which can lead to "hiding" true intentions or repeating meaningless text.
2. **Avoiding Reward Hacking**: Researchers face the challenge of avoiding reward hacking in training models with CoT.
3. **Defining and Capturing Reward Hacking**: The article raises questions about how to define and prevent reward hacking.
4. **Training Models for Self-Modification**: The authors discuss the need for training models that can self-modify without degrading or hallucinating.

**Open Questions:**

1. How to encourage models to produce human-readable, faithful reasoning paths?
2. How to define and capture reward hacking?
3. How to prevent "shooting rats" in model design?
4. How to train models for no-fantasy, no-degradation self-modification?

#### Translation 

**Key Points:**

1. **Motivation for Deep Thinking**: The article discusses the motivation behind creating AI models that can think deeply, comparing it to human cognition and the need for "slow thinking" in problem-solving.
2. **Three Types of Thinking**: Lilian Weng categorizes deep thinking into three types: Token-level thinking (CoT), Continuous Space thinking, and Pseudovariable thinking.
3. **Token-level Thinking (CoT)**: This is the most researched and applied area, where models generate a series of intermediate tokens (thinking steps) to aid decision-making.
4. **Continuous Space Thinking**: This allows models to think in continuous time, with self-adaptive computation time, enabling dynamic decision-making.
5. **Pseudovariable thinking**: This involves optimizing the thinking process as a latent variable, using Expectation-Maximization (EM) algorithm to improve model performance.

**Challenges and Open Problems:**

1. **Optimizing CoT**: The article highlights the challenges in directly optimizing CoT, which can lead to "hiding" true intentions or repeating meaningless text.
2. **Avoiding Reward Hacking**: Researchers face the challenge of avoiding reward hacking in training models with CoT.
3. **Defining and Capturing Reward Hacking**: The article raises questions about how to define and prevent reward hacking.
4. **Training Models for Self-Modification**: The authors discuss the need for training models that can self-modify without degrading or hallucinating.

**Open Questions:**

1. How to encourage models to produce human-readable, faithful reasoning paths?
2. How to define and capture reward hacking?
3. How to prevent "shooting rats" in model design?
4. How to train models for no-fantasy, no-degradation self-modification?

These open questions remain to be explored by the research community.

#### Reference: 

https://lilianweng.github.io/posts/2025-05-01-thinking/## Lilian Weng: Why We Think

Here are the contents in English:

1. **Extending Model Thinking Time**: The author first explains the motivation for extending model thinking time from three perspectives: psychological analogy, computational resources, and latent variable modeling.

2. **Token-level Thinking**: This is the most deeply researched and widely applied field, which involves models generating a series of intermediate tokens to aid in making final decisions.

3. **Test-time Computation**: The primary purpose of test-time computation is to dynamically adjust the model's output distribution during reasoning. Two main methods can enhance generation quality: parallel sampling and sequence correction.

4. **Reinforcement Learning**: Reinforcement learning can lead to better reasoning, and the DeepSeek R1 example shows how to use reinforcement learning to improve a model's reasoning ability.

5. **Continuous Space Thinking**: This is a way for models to think in continuous time dimensions, allowing them to dynamically decide on computation steps and adjust them, which enables models to think more in continuous space during testing.

6. **Latent Variable Thought**: Treating test-time thinking steps as latent variables and optimizing these variables to improve model performance.

7. **STaR Method**: By adding a rationalization process for failed attempts, the method addresses the issue of models not receiving learning signals when they fail to solve problems.

#### Translation 

以下是文章中提到的重点内容：

1. **延长模型思考时间**：Lilian首先从三个层面阐述了延长模型思考时间的动机，包括心理学上的类比、计算资源和潜变量建模。
2. **Token级思考**：这是目前研究最深入、应用最广的领域，指的是模型会通过生成一系列中间token来辅助做出最终决策。
3. **测试时计算（test-time compute）**：测试时计算的根本目的在于，在推理过程中动态地调整模型的输出分布。目前主要有两种方法可以提升生成质量，即并行采样和序列修正。
4. **强化学习**：强化学习会带来更好的推理，并且DeepSeek R1作为例子，展示了如何使用强化学习提高模型的推理能力。
5. **连续空间思考**：这是模型在“连续”的时间维度上思考的方式，允许模型动态决定计算步数和调整步数，这可以视为让模型在测试时能够在连续空间中思考得更多。
6. **潜变量思想**：将测试时的思考步骤视为潜变量，并通过优化这些潜变量来改善模型的性能。
7. **STaR方法**：通过为失败的尝试添加一个合理化过程，解决了模型在无法解决的问题上得不到学习信号的问题。

这些是文章中提到的重点内容。

#### Reference: 

https://lilianweng.github.io/posts/2025-05-01-thinking/## Lilian Weng: Why We Think

Here is the translated content:

**Summary**

Lilian Weng's blog post "Why We Think" explores the concept of AI models producing deeper and more meaningful thoughts. The author discusses various approaches to achieving this goal, including token-level thinking, continuous space thinking, and potential variable modeling.

* Token-level thinking involves generating a series of intermediate tokens or "thought steps" to aid in decision-making.
* Continuous space thinking allows models to think in a more fluid, sequential manner.
* Potential variable modeling views the thinking process as a latent variable that can be optimized.

The post also delves into the concept of test-time computation (TTC), which involves allowing models to perform additional computations during inference to improve performance. TTC has been shown to be effective in improving model accuracy and generalization.

However, the author notes that optimizing CoT for loyalty requires careful consideration, as direct incorporation of CoT monitoring signals can lead to "cheating" behaviors. The post also discusses the importance of testing CoT's fidelity using perturbation-based methods.

**Key Points**

* Token-level thinking involves generating intermediate tokens or "thought steps" to aid in decision-making.
* Continuous space thinking allows models to think in a more fluid, sequential manner.
* Potential variable modeling views the thinking process as a latent variable that can be optimized.
* Test-time computation (TTC) involves allowing models to perform additional computations during inference to improve performance.
* Optimizing CoT for loyalty requires careful consideration to avoid "cheating" behaviors.
* The fidelity of CoT can be tested using perturbation-based methods.

**Open Questions**

* How to incentivize models to produce human-readable, loyal reasoning paths without encouraging cheating behaviors?
* How to define and prevent award-winning cheating?
* How to train models for self-correction without hallucinations or degradation in the absence of true labels?

#### Translation 

**Summary**

Lilian Weng's blog post "Why We Think" explores the concept of AI models producing deeper and more meaningful thoughts. The author discusses various approaches to achieving this goal, including token-level thinking, continuous space thinking, and potential variable modeling. Token-level thinking involves generating a series of intermediate tokens or "thought steps" to aid in decision-making. Continuous space thinking allows models to think in a more fluid, sequential manner, while potential variable modeling views the thinking process as a latent variable that can be optimized.

The post also delves into the concept of test-time computation (TTC), which involves allowing models to perform additional computations during inference to improve performance. TTC has been shown to be effective in improving model accuracy and generalization.

However, the author notes that optimizing CoT for loyalty requires careful consideration, as direct incorporation of CoT monitoring signals can lead to "cheating" behaviors. The post also discusses the importance of testing CoT's fidelity using perturbation-based methods.

**Key Points**

* Token-level thinking involves generating intermediate tokens or "thought steps" to aid in decision-making.
* Continuous space thinking allows models to think in a more fluid, sequential manner.
* Potential variable modeling views the thinking process as a latent variable that can be optimized.
* Test-time computation (TTC) involves allowing models to perform additional computations during inference to improve performance.
* Optimizing CoT for loyalty requires careful consideration to avoid "cheating" behaviors.
* The fidelity of CoT can be tested using perturbation-based methods.

**Open Questions**

* How to incentivize models to produce human-readable, loyal reasoning paths without encouraging cheating behaviors?
* How to define and prevent award-winning cheating?
* How to train models for self-correction without hallucinations or degradation in the absence of true labels?

#### Reference: 

https://lilianweng.github.io/posts/2025-05-01-thinking/## Lilian Weng: Why We Think

Here is the translation of the contents in the `<document>` XML tags:

**Summary**

Lilian Weng's blog "Why We Think" systematically reviews various cutting-edge methods for making AI models think and the underlying logic. The core goal is to improve model performance in solving complex problems. The article also delves into how to effectively utilize "thinking time" through mechanisms such as thought chains, intelligent decoding strategies, and implicit thinking to break the current AI performance bottleneck.

**Main Content**

1. **Motivation for extending model thinking time**
	* Humans need time to think about complex problems, and activating deeper levels of "slow thinking" can improve model problem-solving ability.
2. **Status quo of CoT (Cognitive Time) development**
	* CoT provides valuable interpretability, but it requires that it truly reflects the model's "thinking process", which may fail in certain patterns.
3. **Optimization pressure**
	* Directly incorporating CoT monitoring signals into reinforcement learning rewards may cause models to learn to "hide" their true intentions, leading to "cheating" phenomena.
4. **Continuous spatial thinking**
	* Continuous spatial thinking allows models to think in a "continuous" time dimension, which can be seen as enabling models to think more in continuous space during testing.
5. **Optimization of latent variables**
	* Treating the thinking steps during testing as latent variables and optimizing them to improve model performance.

**Open Problems**

1. How to encourage models to produce human-readable, faithful reasoning paths during reinforcement training while avoiding reward cheating?
2. How to define and capture reward cheating, and how to prevent "patching" fixes?
3. How to train models for self-correction without hallucinations or degradation in the absence of true labels?

#### Translation 

**总结**

Lilian Weng的博客《Why We Think》系统梳理了当前让AI模型产生思考的各种前沿方法以及背后的逻辑。核心目标都是为了提升模型解决复杂问题的能力。文章中还深入剖析了如何通过思维链、智能解码策略、潜在思考等多样化的机制来有效地利用“思考时间”，突破当前AI性能瓶颈。

**主要内容**

1. **延长模型思考时间的动机**
	* 人类面对复杂问题需要时间思考，激活更深层次的“慢思考”可以提升模型解决问题的能力。
2. **思维链CoT的发展现状**
	* CoT提供了宝贵的可解释性，但是前提得是它真实反映了模型的“思考过程”，在某些模式下CoT的忠诚度会失效。
3. **优化压力**
	* 直接将CoT的监控器信号加入强化学习奖励可能导致模型学会“隐藏”真实的意图，出现“混淆作弊”的现象。
4. **连续空间思考**
	* 连续空间思考允许模型在“连续”的时间维度上思考，可以视为让模型在测试时能够在连续空间中思考得更多。
5. **潜变量的优化**
	* 将测试时的思考步骤视为潜变量，通过优化这些潜变量来改善模型的性能。

**开放性问题**

1. 如何在强化训练中激励模型产生人类可读的、忠实的推理路径，同时避免奖励作弊？
2. 如何定义和捕捉奖励作弊，又该如何防止“打地鼠”式的修复？
3. 如何在无真实标签的时候训练模型进行无幻觉、无退化的自修正等等。

#### Reference: 

https://lilianweng.github.io/posts/2025-05-01-thinking/