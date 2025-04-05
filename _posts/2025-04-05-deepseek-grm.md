## DeepSeek-GRM: Generalist Reward Modeling

Here is the translation of the contents into English:

This paper explores a model called DeepSeek-GRM that can improve the quality and efficiency of reward models by reasoning at scale. The model combines ideas from reinforcement learning (RL) and meta-learning, allowing it to perform well on different tasks and evaluation metrics.

Researchers evaluate DeepSeek-GRM using various benchmark tests and compare it with other publicly available baseline methods. The experimental results show:

1. Even without scaling during reasoning, the DeepSeek-GRM model trained with SPCT outperforms various baseline reward models of the same size and can compete with some large closed-source models.
2. The effectiveness of SPCT training is verified, with significant performance improvements over RFT cold start alone, and a consumption experiment also proves the contribution of key steps in the process.
3. DeepSeek-GRM exhibits excellent reasoning-at-scale properties, with model performance steadily improving as the sampling number k increases, especially when guided by meta-reward models.
4. In some tasks, DeepSeek-GRM can achieve even better performance through reasoning-at-scale than increasing the model parameters several times, indicating that reasoning-at-scale may have higher computational efficiency.

However, this study also has some limitations:

1. The efficiency of GRM is inherently behind that of Scalar RM of the same size, limiting its large-scale use in online reinforcement learning pipelines.
2. In certain verifiable tasks' specific domains, DeepSeek-GRM still lags behind Scalar RM, which may be because Scalar RM captures hidden features of query and answer reasoning while GRM needs stronger reasoning power to fully check answers.

In summary, this paper presents a promising new model that can improve the quality and efficiency of reward models through reasoning-at-scale. Although there are limitations, the study remains an important contribution, showing that GRM may have higher computational efficiency and less domain bias.

#### Translation 

这篇论文探讨了一个名为DeepSeek-GRM的模型，它能够通过推理时Scaling提高奖励模型的质量和效率。该模型结合了强化学习（RL）和元学习（Meta Learning）的思想，允许它在不同的任务和评价维度上表现良好。

研究人员使用多种基准测试评估DeepSeek-GRM，并与其他公开的基线方法进行比较。实验结果表明：

1.  即使在不进行推理时Scaling的情况下，经过SPCT训练的DeepSeek-GRM模型已经优于同等规模的各种基线奖励模型，并且表现出与一些大型闭源模型竞争的实力。
2.  SPCT训练方法有效性得到证实，与只进行RFT冷启动相比，完整的SPCT流程带来了显著的性能提升，消融实验也证明了其中关键步骤的贡献。
3.  DeepSeek-GRM展现出优秀的推理时Scaling特性，随着采样次数k的增加模型性能持续稳定提高，尤其是在元奖励模型的引导下提升效果更为明显。
4.  在某些任务上，DeepSeek-GRM通过推理时Scaling可以达到甚至超过把模型参数增加几倍所带来的性能提升，这表明推理时Scaling可能具有更高的计算效率。

然而，该研究也存在一些局限性：

1.  GRM的效率本质上落后于同等规模的Scalar RM，这限制了它在在线强化学习管道中的大规模使用。
2.  在某些可验证任务的特定领域，DeepSeek-GRM仍然落后于Scalar RM，这可能是因为Scalar RM捕获了推理查询和回答的隐藏特征，而GRM需要更强的推理能力来全面检查回答。

总之，這篇论文提出了一个有潜力的新模型，它能够通过推理时Scaling提高奖励模型的质量和效率。虽然存在局限性，但该研究仍然是一个重要的贡献，向我们展示了GRM可能具有更高的计算效率和更少的领域偏见。

#### Reference: 

https://arxiv.org/pdf/2504.02495