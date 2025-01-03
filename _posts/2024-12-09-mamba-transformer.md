## Mamba vs Transformers

Here is the translated content:

This article discusses a neural network architecture called Mamba. It differs significantly from traditional linear RNNs in its core structure. Specifically, Mamba's matrices A, B, and C are distinct from the fixed B and C matrices used in linear RNNs.

Mamba's A matrix acts as a "memory card" that stores historical information as tokens change. The B matrix serves as a filter to select important features from new inputs. The C matrix functions as a decoder to determine which memories to output.

In contrast, the B and C matrices in linear RNNs are fixed. Mamba transforms these matrices into intelligent buckets, allowing it to handle information with both memory and forgetfulness capabilities more effectively.

However, one major drawback of Mamba is its recursive structure, which requires sequential processing and wastes GPU parallel computing power. To mitigate this, Mamba uses a parallel scan operation, enabling the reasoning phase to utilize parallel computation as well. This makes Mamba faster at handling long sequences than Transformer and capable of increasing the throughput of Transformer models by five times.

Despite this optimization, efficiency in training is still limited by the recursive structure. Future architectures may emerge that change the rules and combine old and new architectures to achieve more powerful results. The article concludes by mentioning that Transformer, CNN, and RNN could all be essential pieces of the puzzle towards achieving AGI.

#### Translation 

这篇文章讨论的是一个叫做Mamba的神经网络架构。它与传统的线性RNN（递归神经网络）在核心结构上有很大的不同。具体来说，Mamba架构的三个矩阵A、B和C，不同于线性RNN中不变的B和C矩阵。

Mamba的A矩阵相当于是“储存卡”，随着token（信息单位）的变化，储存的历史信息会越来越多。B矩阵相当于是过滤器，可以从新输入的特征中筛选出重要信息。C矩阵相当于是解码器，可以决定哪些记忆输出。

相比之下，线性RNN中的B和C矩阵是固定的，不变。Mamba通过将这些矩阵转化为灵活的智能漏斗，使得它能够更好地处理信息，有记忆能力也有遗忘能力。

然而，Mamba的一个主要缺点仍然是递归结构导致的，因为递归结构需要按照顺序一步一步来，这会浪费GPU并行计算的能力。为了弥补这一点，Mamba使用了并行扫描操作，让推理阶段也能利用并行计算。这使得Mamba在处理超长序列时比Transformer更快，并且能够以5倍的吞吐量提高 Transformer模型。

然而，这个优化仍然局限于推理层面，训练方面的效率还受递归结构的影响。未来可能会有新的架构出现，改变游戏规则，并融合这些新旧架构，以实现更强大的结果。这篇文章结束时提到了Transformer、CNN和RNN都可能是通往AGI（强人工智能）的必不可少的一块拼图。