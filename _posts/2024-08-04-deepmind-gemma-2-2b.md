## DeepMind Gemma-2-2B model

Google has released versions of Gemma 2.2B and 9B's sparse self-encoding tool, called Gemma Scope. This toolkit includes over 400 sparse self-encoders that can break down neural network activations into features and represent them as a few key characteristics, making it easier to understand model decision-making processes and interactions between features.

Gemma Scope uses the latest JumpReLU SAE architecture, which makes it easier to balance the two goals of detecting features and estimating strength, while significantly reducing errors. Training so many sparse self-encoders is a major engineering challenge that requires vast computational resources.

Researchers used about 15% of the training data for Gemma 2.9B to train these sparse self-encoders and saved around 20 Pebibytes of activations to disk. A total of thousands of billions of sparse self-encoder parameters were generated.

Google has open-sourced the Gemma 2.9B and 27B models, which have shown good results in real dialog tasks, even beating larger models. In recent AI development trends, the "big model" halo seems to be fading away, and making models smaller is becoming more important.

Some industry professionals suggest that large language models may follow the same path as CNNs, whose parameters grew rapidly from ImageNet times before shifting towards smaller and more efficient models. Will this trend continue? The audience can discuss in the comments section.

#### Translation 

Google发布了Gemma 2.2B和9B的稀疏自编码器版本，称之为Gemma Scope。这个工具集包含超过400个稀疏自编码器，能够分解神经网络激活中的特征并将其表示为少数几个特征，这样可以更好地理解模型的决策过程和特征之间的相互作用。

Gemma Scope使用了最新的JumpReLU SAE架构，这种架构能够更容易地实现稀疏自编码器在检测特征存在和估计强度这两个目标之间的平衡，并且显著减少误差。训练如此多的稀疏自编码器是一个重大的工程挑战，需要大量的计算资源。

研究人员使用了Gemma 2.9B训练计算量的大约15%来训练这些稀疏自编码器，并将大约20 Pebibytes的激活保存到了磁盘。总共生成了数千亿个稀疏自编码器参数。

Google开源了Gemma 2.9B和27B版本的模型，这些模型在真实对话任务中表现出很好的结果，甚至比较大的模型还要好。在今年AI发展过程中，大模型的光环似乎正在褪去，而如何将模型做小变得越来越重要。

一些业内人士提出了观点，认为大语言模型的模型大小可能正在走CNN的老路，从ImageNet时代开始，参数规模快速增长，然后转向更小、更高效的模型。是否会遵循同样的趋势？各位观众可以在评论区留言讨论。

#### Reference: 

https://www.youtube.com/watch?v=zEwshL84SLs