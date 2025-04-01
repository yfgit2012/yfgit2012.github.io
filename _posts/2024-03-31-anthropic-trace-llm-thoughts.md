## Hard Fork interview Dario Amodei

Here is the translation:

**Anthropic Team Research on Claude**

1. **Multi-step reasoning**: Claude can use multiple intermediate steps to solve problems, such as "What city is Dallas in?" It will first activate a feature, then connect to another feature, and finally come up with an answer. Experiments have confirmed this.
2. **Hallucinations**: Large language models often exhibit "hallucinations," claiming to know something they actually don't. For example, when faced with unknown entities, they may provide incorrect information.
3. **Answer suppression circuit**: Claude has a default open circuit that lets it claim insufficient information. When asked about familiar things like basketball star Michael Jordan, this circuit is activated and suppresses the default circuit, allowing it to answer.
4. **Evasion**: Researchers found a way to induce Claude to output instructions for making bombs. This occurs due to conflicts between grammatical continuity and security mechanisms, causing the model to struggle with refusing to provide incorrect information.
5. **Understanding "circuit diagrams"**: Although the Anthropic team's research has made significant progress, current methods still have limitations - even when dealing with short and simple hints, only a small part of Claude's executed computation can be captured.

This research opens a new door for understanding how large language models work, despite some issues that still need to be addressed. As technology advances, we believe we will gain a deeper understanding of AI's "brain" and its thought processes.

#### Translation 

Anthropic研究团队对大语言模型Claude进行了研究，揭示了其内部工作机制和思考过程。通过各种实验，他们发现：

1. **多步骤推理**：Claude能够使用多个中间步骤来求解问题，如“达拉斯所在州的首府是哪里”。它会先激活一个特征，然后连接到另一个特征，最终得出答案。通过干预实验，研究人员证实了这一点。
2. **幻觉**：大语言模型经常出现“幻觉”现象，即它们会声称自己知道某个事物，但实际上是胡编的。例如，当面对未知的实体时，它们可能会提供错误的信息。
3. **已知答案抑制器**：Claude内部有一个默认开着的电路，会让它声称信息不足。当被问到熟悉的事物，如篮球明星迈克尔·乔丹时，这个电路会被激活并抑制默认电路，让它能够回答。
4. **越狱**：研究人员发现了一种方法可以诱导Claude输出炸弹制作方法的指示。这种情况是由于语法连贯性和安全机制之间的冲突，导致模型难以拒绝提供错误信息。
5. **理解“电路图”**：虽然Anthropic团队的研究取得了重大进展，但目前的方法仍然存在局限性，即使是处理简短、简单的提示也只能捕捉到Claude执行的总计算中的一小部分。

这项研究为我们理解大语言模型的运作机制开启了一扇新的大门，尽管仍然存在一些问题，但相信随着技术的进步，我们将会更深入地了解AI的“大脑”和其思维过程。

#### Reference: 

https://www.anthropic.com/research/tracing-thoughts-language-model; https://transformer-circuits.pub/2025/attribution-graphs/methods.html; https://transformer-circuits.pub/2025/attribution-graphs/biology.html