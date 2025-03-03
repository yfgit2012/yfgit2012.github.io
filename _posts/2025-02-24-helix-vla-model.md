## FigureAI' Helix - VLA model

Here is the translation of the contents:

This article describes a robot model called Helix that can be trained and deployed on multiple robots using a single imitation learning strategy. This approach allows different robots to behave and act like humans, with strong object generalization abilities.

The Helix model consists of two sub-models: S2 and S1. S2 runs as an asynchronous background process, processing robot images and states before passing the results to S1. S1 is a real-time visual processing sub-model that uses fully convolutional networks and multi-scale visual backbone networks to process image information.

The training design and deployment strategy of Helix have been optimized for efficient parallel deployment on each robot equipped with dual low-power embedded GPUs. This approach splits the reasoning pipeline into two models, S2 and S1, which run on dedicated GPUs, minimizing distribution discrepancies during training and inference.

This video showcases a scenario where two robots work together to categorize items placed on a table by a human, remembering specific locations such as a basket on the fridge door and cookies in a drawer.

While the model exhibits strong environmental adaptability, it still has limitations, such as slowly closing the fridge door after picking up all items. This suggests further improvement is needed to meet standards for energy awareness, etc.

In summary, this article describes the Helix model that enables robots to exhibit human-like environmental adaptability using a single imitation learning strategy trained and deployed on multiple robots. This approach provides a possibility for future humanoid robot ubiquity, making them an indispensable part of our lives.

#### Translation 

这篇文章描述了一种称为Helix的机器人模型，该模型可以通过单一的模仿学习策略来训练和部署在多个机器人上。这种方法允许不同机器人的行为和动作与人类非常相似，且表现出强大的物体泛化能力，即能够适应新未见过的环境和任务。

Helix模型由两个子模型组成：S2和S1。S2作为异步后台进程运行，它首先对机器人图像和状态进行处理，然后将结果传递给S1。S1是实时视觉处理子模型，使用完全卷积网络和多尺度视觉骨干网络来处理图像信息。

Helix的训练设计和部署策略被优化，以实现高效并行地部署模型，每个机器人都配备了双低功耗嵌入式GPU。这种方法使得推理管道分为S2和S1两个模型，它们在专用的GPU上运行，最大限度地减少了训练和推理时的分布差距。

本期视频展示了一个场景，当人类把Figure机器人从未见过的杂物放置在桌上，并提出整理要求时，两个机器人可以协作，将杂物归类并放置。机器人能够记住具体的位置，如冰箱门上的置物筐和抽屉中饼干的位置。

虽然该模型表现出强大的环境适应性，但仍然存在一些不足之处，例如在收拾完全部物品后才缓缓合上冰箱门。这表明还需要进一步改进，以便达到节能意识等方面的标准。

总而言之，这篇文章描述了一种能够使机器人表现出人类级别环境适应性的Helix模型，该模型通过单一的模仿学习策略来训练和部署在多个机器人上。这种方法为将来的人形机器人普及提供了可能，使其成为我们的生活中不可缺少的一部分。

#### Reference: 

https://www.figure.ai/news/helix