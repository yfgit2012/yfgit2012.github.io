## DeepSeek Native Sparse Attention (NSA)

Here is the translation of the contents in the <document> XML tags:

NSA (Non-Local Self-Attention) is a sparse attention mechanism that can significantly reduce computational costs and outperform other models on multiple general benchmark tests. NSA helps the model develop specialized attention mechanisms through pre-training, which filters out noise from irrelevant attention paths. This approach excels in long-context tasks, particularly in the 64k context "needle in a haystack" test, where it achieves extremely high retrieval accuracy.

NSA's hierarchical sparse attention design achieves efficient global context scanning using coarse-grained token compression, and then fine-grained selection markers to preserve key information. This is similar to using a wide-angle lens to observe the entire scene, followed by a telephoto lens to focus on specific details, achieving a perfect balance between global awareness and local accuracy.

On LongBench, NSA excels in multiple-hop QA tasks and code comprehension tasks, outperforming all baseline models, demonstrating its advantage in complex long-text reasoning tasks. The NSA mechanism can also be combined with reasoning models for adaptation to advanced post-training methods.

DeepSeek achieved chained mathematical reasoning ability on 32k length mathematical reasoning tasks by distilling knowledge from DeepSeek-R1 and fine-tuning it. In the challenging AIME 24 benchmark test, the sparse attention variant of NSA (NSA-R) was compared with the full attention baseline model (Full Attention-R), showing that NSA-R significantly outperformed Full Attention-R in both 8k and 16k context settings.

In terms of computational efficiency, DeepSeek compared NSA and full attention mechanisms on an 8-GPU A100 system. As context length increased, NSA's acceleration effect became increasingly significant. In 64k context lengths, NSA's forward propagation speed improved by a factor of 9, and backward propagation speed by a factor of 6, mainly due to NSA's hardware-aligned design, block memory access patterns, and merged loading that maximized Tensor Core utilization and fine-grained loop scheduling.

In terms of decoding speed, the attention mechanism is limited by KV cache loading memory bottlenecks. As decoding length increased, NSA's latency showed a significant reduction, achieving up to 11.6 times speedup in 64k context lengths.

Although NSA achieved remarkable results, the DeepSeek research team maintained a rigorous scientific attitude and pointed out potential improvement directions, such as further optimizing the sparse attention pattern learning process to enable models to more intelligently select key information; and exploring more efficient hardware implementation ways to fully tap into hardware potential and make NSA even more effective in the future.

In summary, this paper provides an exhaustive introduction to NSA, with a clear and operable explanation of technical details involved in the mechanism. It showcases DeepSeek's excellent engineering capabilities and contributes significantly to AI research.

#### Translation 

NSA（Non-Local Self-Attention）是一种稀疏注意力机制，其设计可以显著减少计算开销并且在多个通用基准测试中表现优于其他模型。NSA通过预训练机制帮助模型开发专门的注意力机制，从而过滤掉无关注意力路径中的噪声。这种方法能够在长上下文任务中表现出强大的实力，特别是在64k上下文的大海捞针测试中，它实现了超强的检索精度。

NSA的分层稀疏注意力设计通过粗粒度的压缩token来实现高效的全局上下文扫描，再通过细粒度的选择标记来保留关键信息。这就像使用广角镜头先观察整个场景，然后再用长焦镜头聚焦到具体的目标，从而在全局感知和局部精确性之间取得了完美平衡。

在LongBench上，NSA在多跳QA任务和代码理解任务中也表现优异，优于所有的基线模型。这表明了在复杂长文本推理任务上的优势。NSA机制还能与推理模型结合，以适配前沿的后训练方式。

DeepSeek通过从DeepSeek-R1蒸馏知识和监督微调的方式，让采用NSA的模型在32k长度的数学推理任务上获得了链式数学推理能力。在具有挑战性的AIME 24基准测试中，NSA的稀疏注意力变体NSA-R与全注意力的基线模型全注意力-R进行对比，结果显示，在8k和16k上下文设置下，NSA-R均显著优于全注意力-R。

在计算效率方面，DeepSeek在8-GPU的A100系统上，对NSA和全注意力机制进行了对比。在训练速度上，随着上下文长度的增加，NSA的加速效果越来越显著。在64k上下文长度时，NSA的前向传播速度提升了9倍，反向传播速度提升了6倍。这主要得益于NSA的硬件对齐设计，块状的内存访问模式，以及合并加载最大化Tensor Core的利用率和精细的循环调度。

在解码速度方面，注意力机制的解码速度主要受限于KV缓存加载的内存瓶颈。随着解码长度的增加，NSA的延迟表现出了显著的降低。在64k上下文长度时实现了高达11.6倍的速度提升。

尽管NSA取得了显著的成果，但DeepSeek研究团队仍然保持着严谨的科研态度，也指出了一些可能的改进方向，比如进一步优化稀疏注意力模式的学习过程，让模型能够更智能地选择关键信息；还有探索更高效的硬件实现方式，充分挖掘硬件潜力，使NSA能够在未来发挥更大的作用。

总之，这篇介绍NSA的论文内容详实，对NSA机制中涉及的技术细节阐释十分清晰，有很强的可操作性。它让我们再次看到了DeepSeek团队的优秀工程能力，也为AI研究贡献了重要的成果。

#### Reference: 

https://arxiv.org/pdf/2502.11089v1