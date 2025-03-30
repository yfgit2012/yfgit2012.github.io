## Transformers without Normalization by DyT (dynamic Tanh)

Here is the translation:

This paper discusses a new type of dynamic regularization layer (DyT) and its applications in large-scale language models. Researchers found that fine-tuning α₀ can significantly improve performance, and larger models require smaller α₀ values. Additionally, they discovered that high-tuning α₀ values in attention layers also helps to boost model performance.

Furthermore, this paper evaluates the computational efficiency of DyT, comparing it with RMSNorm on the LLaMA 7B model. The results show that DyT layer computation is significantly faster than RMSNorm layer. Researchers also found that DyT has great potential for network design optimization focusing on efficiency.

In summary, this paper presents a new type of dynamic regularization layer (DyT) and demonstrates its effectiveness in large-scale language models. Moreover, it challenges the conventional idea that normalization layers are indispensable, considering that model training and inference may require millions of calculations. The high efficiency of DyT can greatly help reduce costs.

This study provides new ideas and methods for future research on optimizing neural network architecture.

#### Translation 

该论文探讨了一个新型的动态正则化层（DyT）的设计及其在大型语言模型中的应用。研究人员发现，对于α₀的精细调整可以带来明显的性能提升，并且，较大的模型需要较小的α₀值。此外，他们还发现，对于注意力层中的α₀值进行高调优，也有助于提升模型的性能。

此外，该论文也对DyT的计算效率进行了评估，在LLaMA 7B模型上，对RMSNorm和DyT进行基准测试，结果显示DyT层的计算时间显著低于RMSNorm层。研究人员还发现，DyT在面向效率优化的网络设计中具有很大的潜力。

总之，该论文展示了一个新型的动态正则化层（DyT），并且，在大型语言模型中的应用中表现出很好的效果。此外，它也打破了人们长期以来对归一化层不可或缺的固有观念，从实际应用角度来看，考虑到模型训练和推理可能需要进行数千万次的计算，DyT的高效性能够极大的帮助降低成本。

这项研究为后续研究如何进一步优化神经网络架构提供了新的思路和方法。

#### Reference: 

https://arxiv.org/pdf/2503.10622; https://www.youtube.com/watch?v=D-pR7qWuheE