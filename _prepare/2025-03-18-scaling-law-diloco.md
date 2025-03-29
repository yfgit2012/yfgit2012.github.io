## Scaling Laws for DiLoCo by Google

Here is the translation of the contents into English:

This study found that DiLoCo has a significant improvement in scalability. Researchers evaluated loss and zero-shot accuracy on different model sizes with varying batch sizes to validate this conclusion. In almost all cases, DiLoCo outperformed data parallel training, especially when the model size was large.

Researchers also found that the best external learning rate is roughly independent of the model size N but varies with the number of replicas M. For sufficiently large models (N ≥ 3.35 billion parameters), the best external learning rate is fixed and increases with M, consistent with previous federated learning research.

This suggests that the external learning rate should be increased as the number of clients, equivalent to the number of model replicas in DiLoCo, grows, making DiLoCo more natural for horizontal extension and reducing overall training time. In addition to its excellent performance during normal training, DiLoCo also has a unique advantage in handling overfitting problems.

The study showed that using DiLoCo typically enables 4 times as much overfitting on the same amount of data as data parallel training, providing a stronger tool for researching the performance bounds of models.

#### Translation 

这个研究发现 DiLoCo 在横向扩展能力上有了很大的提升，研究人员通过对不同规模模型在不同批大小下的评估损失和零样本准确率进行测试，验证了这一结论。在几乎所有情况下，DiLoCo在较大批大小下的表现都优于数据并行训练，尤其是在模型规模较大的时候，这种优势更加明显。

研究人员还发现最佳外部学习率基本上与模型的规模N无关，但会随着副本数M的变化而变化，对于足够大的模型，也就是N≥3.35亿参数，每个M的最佳外部学习率是固定的，而且M越大，最佳外部学习率似乎也越大，这个结果与之前联邦学习的研究是一致的。

这表明外层学习率应该随着客户端的数量，也就是DiLoCo中模型的副本数量的增加而增加，使得DiLoCo在水平扩展上更加自然，缩短总训练时间。除此之外，DiLoCo不仅在正常训练中表现出色，在处理过度训练的问题上也有独特的优势。

研究表明，使用DiLoCo通常可以在相同时间内进行4倍于数据并行训练的过度训练，这为研究模型的性能边界提供了更有力的工具。

#### Reference: 

https://arxiv.org/pdf/2503.09799