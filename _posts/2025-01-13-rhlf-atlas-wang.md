## Why RLHF is not True RL - Atlas Wang

Here is the translation of the contents from the `<document>` XML tags into English:

1. Does the model have a true objective, or is it merely driven by prompt tokens?
2. If there is no true objective, what consequences would follow?

Consequences mentioned include:

* Simplified alignment (the model may not bypass limitations or autonomously plan non-compliant behavior)
* Difficulty in delegating open-ended tasks (because the model lacks persistent intrinsic motivation)
* Missed potential innovations (because the model relies solely on surface-level feedback for one-step text generation)

However, the author also highlights the positive aspects of methods such as RLHF, which make models more transparent because they are guided by instantaneous feedback signals rather than complex hidden objectives.

The author emphasizes the difference between RLHF and true RL, particularly in terms of time horizon and reward concepts. They point out that fine-tuning large language models is often considered short-term optimization rather than long-term optimization, and that RL typically assumes a well-defined action space, whereas in fine-tuning LLMs, "actions" are fuzzy.

In summary, the paper highlights the challenges and limitations of fine-tuning large language models. The author reminds professionals to be aware of these limitations and policymakers and ethicists to recognize that models cannot autonomously plan or deceive to achieve hidden objectives.

Looking ahead, the development direction of RLHF may have three aspects: higher sample complexity, longer-term multi-step tasks, and transmitting human subtle goals to artificial intelligence systems through structured, symbolic feedback.

#### Translation 

本文讨论了对大语言模型进行微调的方法，尤其是强化学习（RL）-驱动的方法。作者提出了几个问题：

1. 模型是否有真正的目标？或是仅仅被提示词驱动？
2. 如果没有真正的目标，会带来什么后果？

作者列举了几种后果，如被简化的对齐（模型可能不会绕过限制或自主计划非法行为），更难委派开放式任务（因为模型缺乏持续内驱力），错失潜在的创新（因为仅仅依赖于表面反馈的单步文本生成）。

然而，作者也提出了RLHF等方法的积极方面，即它们使模型更加透明，因为它们由即时反馈信号引导，而不是有复杂的隐藏目标。

最后，作者强调了RLHF等方法与真正的RL之间的区别，特别是时间跨度和奖励的概念。他们指出，大语言模型的微调通常被视为短期优化，而不是长期优化。此外，RL通常假设有一个定义明确的行动空间，而在大语言模型的微调中，“动作”的概念是模糊的。

总之，本文强调了对大语言模型进行微调所面临的挑战和局限性。作者提醒，从业者应该意识到这些局限性，政策制定者和伦理学家应该认识到模型不可能自发地策划或撒谎来达到隐藏目的。

展望未来，RLHF的发展方向可能有三个：更高的样本复杂度、更长期的多步骤任务，以及通过结构化、符号化的反馈将人类的细微目标传达给人工智能系统。

#### Reference: 

https://www.linkedin.com/pulse/why-rlhf-other-rl-like-methods-dont-bring-true-rl-llmsand-atlas-wang-s1efc/