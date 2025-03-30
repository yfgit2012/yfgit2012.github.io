## Deepseek open-source-week summary

Here are the contents translated into English, excluding any preambles and other contents:

DeepSeek is a company that specializes in developing artificial intelligence (AI) reasoning systems. They recently published a series of open-source content related to their V3 and R1 systems, which includes information on hardware configuration, resource scheduling strategies, model costs, etc.

In terms of hardware configuration, DeepSeek uses H800 GPU and preserves consistent precision policies during training. Matrix multiplication and data transmission are executed in FP8 format, while core MLA computations and combiner transmissions use BF16 format.

For resource scheduling, they employ a dynamic resource allocation strategy that adjusts node numbers based on daytime and nighttime load differences to minimize resource utilization.

To address the challenges of increasing throughput and reducing latency, DeepSeek's V3 and R1 systems both adopt large-scale cross-node expert parallelism (EP) techniques in the MoE architecture. Each layer has 256 experts, but only 8 are activated for each token.

DeepSeek also employs preloading and decoding strategies with different parallel approaches based on scenarios.

To mitigate the huge communication overhead introduced by large-scale cross-node EP, DeepSeek adopts a double-batch overlap processing load balancing strategy. This divides a large request batch into two micro-batches that alternate execution to achieve excellent reasoning performance under hardware constraints.

Finally, they calculate the total cost of their reasoning system and report an average daily usage of 226.75 nodes per day, each with 8 H800 GPUs. With a rental fee per GPU of $2 per hour, the estimated daily cost is approximately $87,072. However, considering that the web version is free, API discounts at night, and V3 being more affordable than R1, their actual revenue is lower.

Despite this, the estimated daily revenue is around $562,027, with a profit margin of 545%.

#### Translation 

DeepSeek是一家专注于人工智能（AI）推理系统开发的公司，他们近期公布了一系列开源内容，这些内容涵盖了他们所开发的V3和R1系统背后的秘密。这些信息包括硬件配置、资源调度策略、模型的成本利润率等。

在硬件配置方面，DeepSeek使用H800 GPU，并且保留了与训练一致的精度策略，以FP8格式执行矩阵乘法和分发传输，同时核心MLA计算和组合传输使用BF16格式。 

资源调度方面，他们采用动态资源调度策略，根据白天和夜间负载差异动态调整节点数量，最小化资源的利用率。

为了应对系统的提高吞吐量和降低延迟这两大挑战，DeepSeek V3和R1都采用了大规模跨节点专家并行技术，即EP，在MoE架构中，每层有256个专家，但每个token只激活其中的8个。这需要通过专家并行来提高效率。

预填充和解码阶段，DeepSeek针对不同场景采用不同的并行策略。 

为了解决大规模跨节点EP引入的巨大的通信开销，DeepSeek还采用了双批次重叠处理负载均衡策略。这让一个大的请求批次分成两个微批次交替执行，从而在硬件受限的情况下实现出色的推理性能。

最后，他们计算整个推理系统的成本，平均每天使用226.75个节点，每个节点8个H800 GPU。按照每GPU租金每小时2美元计算，成本大约为87072美元/天。但是由于Web版目前是免费的、API夜间打折，以及V3比R1更便宜，因此实际收入没有这么多。

但是，这个收益率已经足够令人震撼，因为理论上日收入大约562027美元/天，而成本利润率为545%。

#### Reference: 

https://github.com/deepseek-ai; https://x.com/deepseek_ai