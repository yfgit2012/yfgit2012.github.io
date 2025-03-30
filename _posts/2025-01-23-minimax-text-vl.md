## Minimax-Text-01 and Minimax-VL-01

Here is the translation of the contents into English:

MiniMax-Text-01 is a powerful language model based on self-supervised learning that has achieved excellent results in multiple benchmark tests, including GPQA Diamond dataset, MMLU, IFEval and Arena-Hard. It not only demonstrates strong knowledge application abilities and understanding of human preferences but also performs exceptionally well in long context understanding tasks.

The advantages of MiniMax-Text-01 are as follows:

1. On the GPQA Diamond dataset, MiniMax-Text-01 achieved a score of 54.4, surpassing most open-source pre-trained large models and even the latest version of GPT-4o.
2. In MMLU, IFEval and Arena-Hard tests, MiniMax-Text-01 also ranked among the top three.
3. In long context understanding tasks, MiniMax-Text-01's performance is particularly outstanding. On Ruler and LongBench v2 benchmarks, when context length is 64k or shorter, MiniMax-Text-01 performs comparably to other SOTA models; when context length exceeds 128k, MiniMax-Text-01's superiority becomes apparent.
4. In long text learning ability, MiniMax-Text-01 has achieved SOTA level performance on MTOB benchmark.

In practical application cases, for instance, in translating a minority language from New Guinea called Kalamang, MiniMax-Text-01 can provide translation results that are almost identical to standard answers given the provided instructions, grammar book, word list and contrastive examples. In long dialogue memory tasks, MiniMax-Text-01 can accurately remember details from conversations and respond accordingly.

Moreover, MiniMax has developed a multimodal version of the model, called MiniMax-VL-01. This model integrates an image encoder and an image adapter to convert images into token form that can be understood by large language models. The overall architecture of MiniMax-VL-01 follows the ViT-MLP-LLM paradigm, using a 303M-parameter ViT model as the base model, along with a randomly initialized two-layer MLP projector.

Ultimately, MiniMax-VL-01 performs comparably to other SOTA models on various benchmarks and even surpasses them in certain metrics. However, MiniMax also pointed out limitations of the 01 model: one is long context evaluation; two is model architecture; three is complex programming tasks.

In conclusion, this time's MiniMax-01 series has showcased exceptional performance in handling long contexts, as well as potential in processing even longer contexts.

#### Translation 

MiniMax-Text-01是一款基于自我监督学习的强大语言模型，它在多个基准测试中取得了优异的成绩，包括GPQA Diamond数据集、MMLU、IFEval和Arena-Hard。它不仅表现出强大的知识应用能力和对人类偏好的理解能力，而且在长上下文理解任务方面也非常突出。

MiniMax-Text-01的优势体现在以下几个方面：

1. 在GPQA Diamond数据集上，MiniMax-Text-01取得了54.4的成绩，这高于大多数开源指令微调的大模型，以及最新版本的GPT-4o。
2. 在MMLU、IFEval和Arena-Hard测试中，MiniMax-Text-01也取得了前三名的成绩。
3. 在长上下文理解任务上，MiniMax-Text-01的表现更为突出。在Ruler和LongBench v2这两个常见基准上，当上下文长度在64k或者更短的时候，MiniMax-Text-01与其他SOTA模型表现相当；当上下文长度超过128k时，MiniMax-Text-01的优势就明显体现出来了。
4. 在长文本学习能力方面，MiniMax-Text-01也达到了SOTA水平。在MTOB基准上，MiniMax-Text-01的表现也同样出色。

在实际应用案例中，比如，在翻译一门新几内亚的小众语言Kalamang时，MiniMax-Text-01能够根据提供的指令、语法书、单词表和对照例句给出与标准答案基本一致的翻译结果。在长对话记忆任务中，MiniMax-Text-01能够准确地记住对话中的细节，并且做出相应的回应。

此外，MiniMax还开发了一个多模态版本的模型，即MiniMax-VL-01。这款模型整合了图像编码器和图像适配器，将图像转换为大语言模型能够理解的token形式。MiniMax-VL-01的整体架构符合ViT-MLP-LLM的范式，它作为基础模型使用了一个303M参数的ViT模型， 以及一个随机初始化的两层MLP projector。

最终，MiniMax-VL-01在各个基准上的表现可以与其他SOTA模型媲美，并且在某些指标上达到最佳。然而，MiniMax也提出了01模型的局限性：一是长上下文评估；二是模型架构；三是复杂的编程任务。

总之，这次MiniMax-01系列的两个模型展示了处理长上下文方面的卓越性能，以及处理更长上下文上的潜力。

#### Reference: 

https://www.minimaxi.com/news/minimax-01-%E7%B3%BB%E5%88%97