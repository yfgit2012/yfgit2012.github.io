## The Danger of Overthinking

Here is the translated content:

This paper discusses the "Reasoning-Action Conundrum" problem that occurs in executing AGENTIC tasks with a reinforcement learning-based AGI model. The problem negatively affects the model's performance.

Researchers found that non-reasoning models have lower beta coefficients, indicating that overthinking has a more severe impact on their performance. This is because non-reasoning models lack specialized reasoning training and are limited in handling reasoning chains, leading to poorer performance when overthinking occurs.

The researchers also investigated the relationships between model size, token usage, context window size, and overthinking. They found:

* There is a negative correlation between model size and overthinking behavior: as model size decreases from 32B to 7B, overthinking scores increase.
* The o1 model with low reasoning effort showed a 35% higher overthinking score compared to the high-reasoning effort model: this suggests that increasing token allocation may reduce overthinking in Agent context.
* There is no significant correlation between context window size and overthinking scores: this implies that overthinking behavior is more influenced by model architecture design and training methods than by contextual ability.

Finally, the researchers proposed two potential relief methods:

* Native function calls: using native function calls can efficiently utilize existing resources, avoid excessive internal reasoning, and quickly find solutions.
* Selective reinforcement learning: this can significantly reduce overthinking while improving model performance.

These findings and methods have the potential to solve the overthinking problem in large-scale reasoning models, ultimately reducing computational costs.

#### Translation 

这篇论文主要讨论了基于强化学习的AGI模型在执行AGENTIC任务时出现的“推理-行动困境”（Reasoning-Action Conundrum）的问题，以及该问题对模型性能的负面影响。

研究者们发现，非推理模型的beta系数更低，这意味着过度思考对非推理模型的性能影响更为严重。这是因为非推理模型没有经过专门的推理训练，在处理推理链时的能力有限，所以当出现过度思考的时候，表现会更差。

研究者们还对模型的规模、token使用以及上下文窗口与过度思考的关系进行了研究。他们发现：

* 模型规模与过度思考行为之间存在负相关关系：随着模型规模从32B减小到7B，过度思考得分会逐渐增加。
* 低推理努力程度的o1模型的过度思考得分比高推理尝试程度的模型高出35%：这说明增加token分配可能会减少Agent上下文中的过度思考。
* 上下文窗口大小与过度思考得分之间没有明显相关性：这意味着过度思考行为更多地是受到模型的架构设计和训练方法的影响，而不是模型的上下文能力。

最后，研究者们提出了两种潜在的缓解方法：

* 原生函数调用：通过合理运用原生函数调用，可以更高效地利用已有的资源，避免过度的内部推理，从而更快地找到解决方案。
* 选择性强化学习：这可以显著减少模型的过度思考，同时提高模型的性能。

这些发现和方法都有潜力解决大型推理模型的过度思考问题，进而降低计算成本。

#### Reference: 

https://arxiv.org/pdf/2502.08235