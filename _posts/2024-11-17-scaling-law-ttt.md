## Can Test-Time-Training (TTT) fix the Scaling law ceiling

Here is the translation:

This article mainly discusses the method and application of training-through-test-time (TTT) and how to improve the accuracy of an 8B parameter GPT-3 model on the ARC dataset.

The TTT method involves two-layer voting, namely internal voting and global voting, which combines multiple transformations and prediction results to obtain a more accurate final output.

Experimental results show that by adding the TTT method, the GPT-3 model's accuracy on the ARC dataset was improved from 18.3% to 47.1%, an increase of 157%.

Additionally, the research team also tested the TTT method for different-sized models (1B and 8B) on the ARC dataset. The results showed that the TTT method achieved better performance on the 1B model and narrowed the gap.

Furthermore, researchers compared and combined the TTT method with the previously excellent BARC method, achieving a State-Of-The-Art (SOTA) score of 61.9%.

In summary, this article emphasizes the importance of the TTT method, which allows models to be updated through explicit gradient steps based on test-time input, enabling adaptive ability. This may play a crucial role in promoting the development of next-generation large language models.

#### Translation 

这篇文章主要讨论了推理时训练（TTT）的方法和其应用，以及如何提升8B参数的GPT-3模型在ARC数据集上的准确率。 

TTT的方法涉及两层投票，即内部投票和全局投票，这样可以结合多种变换和预测结果，从而更准确地得到最终输出。

实验结果表明，通过加入TTT方法，GPT-3模型在ARC数据集上的准确率从18.3%提升到了47.1%，增幅达到157%。

另外，研究团队还测试了TTT方法对不同规模的模型（1B和8B）在ARC数据集中的表现效果。结果表明，TTT方法在1B模型上可以获得更好的结果，并且缩小了原有的差距。

此外，研究人员也将TTT方法与之前取得优异成绩的BARC方法进行了比较和结合，取得了61.9%的SOTA成绩。

总之，这篇文章强调了TTT方法的重要性，它可以让模型通过基于测试时输入的显式梯度步骤来进行更新，从而实现自适应的能力。这对推动下一代大语言模型的发展过程中可能会起到关键作用。