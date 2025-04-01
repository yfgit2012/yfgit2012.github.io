## Transformers without Normalization by DyT (dynamic Tanh)

This paper mainly discusses a new method of replacing traditional normalization layers in neural networks, called DyT (Dynamic Thresholding) layer. Researchers have shown through experiments that using the DyT layer can achieve similar performance improvement while significantly reducing computational costs. This study has important implications for designing and optimizing deep learning models.

Main Contents:

1.  **Introduction to DyT Layer**: The DyT layer is a new type of neural network layer that achieves normalization function by means of dynamic thresholding.
2.  **Experimental Results**: Researchers have shown through experiments that using the DyT layer can achieve similar performance improvement while significantly reducing computational costs, indicating its potential in practical applications.

Key Points:

*   In most models, the accuracy of DyT layers is higher than traditional normalization layers by 1-2%.
*   In some specific models (such as LLaMA 7B), using DyT layers can achieve more significant performance improvement.
*   Researchers have also found that using DyT layers can significantly reduce computational costs, especially in inference stages.

#### Translation 

这篇论文主要探讨了一种新的神经网络层替代传统归一化层的方法，称为DyT（Dynamic Thresholding）层。研究人员通过实验表明，使用DyT层可以实现类似的性能提升，同时显著降低计算成本。这项研究对于深度学习模型设计和优化具有重要意义。

以下是这篇论文主要内容：

1. **DyT层的提出**: DyT层是一种新的神经网络层，它通过动态阈值来实现归一化功能。
2. **实验结果**: 研究人员通过实验表明，使用DyT层可以实现类似的性能提升，同时显著降低计算成本。这表明DyT层在实际应用中具有很大的潜力。

下面是一些关键点：

*   DyT层的准确率在大多数模型中都比传统归一化层高出1-2个百分点。
*   在某些特定模型中（如LLaMA 7B模型），使用DyT层可以实现更大的性能提升。
*   研究人员还发现，使用DyT层可以显著降低计算成本，特别是在推理阶段。

总的来说，这项研究对于深度学习模型设计和优化具有重要意义，它证明了在不使用传统归一化层的情况下，模型依然可以取得优异的性能。

#### Reference: 

https://arxiv.org/pdf/2503.10622; https://www.youtube.com/watch?v=D-pR7qWuheE