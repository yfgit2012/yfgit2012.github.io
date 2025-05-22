## Lilian Weng: Why We Think

Here is the translation of the contents within the `<document>` XML tags into English:

Summary of the status quo on CoT (Chain of Thoughts), including training and inference with added dummy tokens, Quiet-STaR method, token-level reasoning, EM algorithm, etc. It also discusses the advantages and limitations of computing during testing, as well as problems such as defining and catching reward cheating, preventing "whack-a-mole" style repairs, etc.

In terms of training, adding dummy tokens can help the model generate more reasonable CoT, while the Quiet-STaR method uses token-level reasoning to optimize the quality of reasons, significantly improving zero-shot performance. The EM algorithm can be used to optimize parameters of models with hidden latent variables.

During testing, increased computational resources can help improve the quality of CoT, but high-temperature sampling may damage generalizability. In pretraining and inference, the ratio of tokens is crucial, only when the number of inference tokens is significantly less than that during pretraining does computing have an advantage during testing.

Finally, the article mentions several open problems, such as how to encourage models to generate human-readable, faithful reasoning paths, as well as how to define and catch reward cheating, etc. The answers to these questions still need more people to explore.

#### Translation 

本文总结了思维链（CoT）的发展现状，包括训练和推理时追加哑token、Quiet-STaR方法、Token-level推理、EM算法等。它还讨论了测试时计算的优势和局限性，以及如何定义和捕捉奖励作弊、如何防止“打地鼠”式修复等问题。

在训练中，追加哑token可以帮助模型生成更合理的CoT，而Quiet-STaR方法通过引入Token-level推理来优化理由的质量，从而显著提升零样本性能。EM算法可以用来优化具有隐含潜变量的模型参数。

在测试时，计算资源的增加可以帮助模型产生更好的CoT，但高温采样可能会损害泛化性。在预训练和推理中，token预算比例很重要，只有当推理token显著少于预训练token时，测试时计算才更有优势。

最后，文章提到了几个开放的问题，比如如何激励模型产生人类可读的、忠实的推理路径，以及如何定义和捕捉奖励作弊等。这些问题的答案仍然需要更多的人去探索。

#### Reference: 

https://lilianweng.github.io/posts/2025-05-01-thinking/