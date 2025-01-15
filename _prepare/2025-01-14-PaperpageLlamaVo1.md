## Paper page - LlamaV-o1: Rethinking Step-by-step Visual Reasoning in LLMs

Reasoning is a fundamental capability for solving complex multi-step problems, particularly in visual contexts where sequential step-wise understanding is essential. Existing approaches lack a comprehensive framework for evaluating visual reasoning and do not emphasize step-wise problem-solving.

To this end, we propose a comprehensive framework for advancing step-by-step visual reasoning in large language models (LMMs) through three key contributions:

First, we introduce a visual reasoning chain benchmark specifically designed to evaluate multi-step reasoning tasks. The benchmark presents a diverse set of challenges with eight different categories ranging from complex visual perception to scientific reasoning with over 4k reasoning steps in total.

Second, we propose a novel metric that assesses visual reasoning quality at the granularity of individual steps, emphasizing both correctness and logical coherence.

Third, we present a new multimodal visual reasoning model, named LlamaV-o1, trained using a multi-step curriculum learning approach. Extensive experiments show that our LlamaV-o1 outperforms recent models, achieving an average score of 67.3 with an absolute gain of 3.8% across six benchmarks while being 5× faster during inference scaling. Our benchmark, model, and code are publicly available.

#### Translation 

<document>
推理是一项基本能力，用于解决复杂的多步骤问题，尤其是在视觉背景下，其中顺序逐步理解是必不可少的。现有的方法缺乏一个全面框架来评估视觉推理，并且没有强调逐步解决问题。

为此，我们提议了一项综合框架，以通过三项关键贡献来促进大规模语言模型（LMM）的逐步视觉推理：

首先，我们介绍了一个专门设计用于评估多步骰推理任务的视觉推理链条基准。该基准提供了8个不同的类别，涵盖从复杂的视觉感知到科学推理的挑战，并且总共超过4k的推理步骤。

其次，我们提出了一项新指标，用于评估视觉推理质量，强调每一步的正确性和逻辑一致性。

最后，我们呈现了一个新的多模态视觉推理模型，称为LlamaV-o1，它使用逐步学习方法进行训练。广泛的实验表明我们的LlamaV-o1在六个基准测试中平均得分67.3分，相比最近的模型提高了3.8％，而且在推理缩放时速度加快5倍。我们的基准、模型和代码都是公开可用的。
</document>

#### Reference: 

https://huggingface.co/papers/2501.06186