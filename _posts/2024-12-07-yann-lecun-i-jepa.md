## I-JEPA: A Human-Like world Model by Yann Lecun

Here is a summary of the contents in no more than 20% of the total contents length:

I-JEPA is an open-source computer vision model from Meta AI that aims to improve the semantic level of representations without using prior knowledge. It uses a self-supervised learning approach that predicts missing information in abstract representation space.

There are two common approaches for self-supervised learning: invariance-based and generative. I-JEPA's approach is more human-like, predicting embeddings that grasp the semantics of an image rather than predicting explicit pixels.

I-JEPA has three components: a context encoder, a target encoder, and a predictor. The target encoder converts an input image into a sequence of non-overlapping patches, and the context block is sampled from the original image. The predictor then predicts the representations of the target blocks based on the context block.

The loss is calculated by the average L2 distance between the predictions and the actual representations, and the trained context encoder generates highly semantic representations for input images.

#### Translation 

<document>
I-JEPA是一种由Meta AI开源的计算机视觉模型，旨在通过不使用先前的知识来改善语义表示水平。它采用自我监督学习方法，在抽象表示空间中预测缺失信息。

有两种常见的自我监督学习方法：基于不变性的和生成性的。I-JEPA的方法更像人类，预测嵌入，这里包含了图像语义，而不是预测显式像素。

I-JEPA共有三个组件：上下文编码器、目标编码器和预测器。目标编码器将输入图像转换为一个非重叠块的序列，而上下文块则是从原始图像中采样得到的。然后，预测器根据上下文块来预测目标块的表示。

损失函数通过在预测值和实际表示之间的平均L2距离来计算得出。训练好的上下文编码器为输入图像生成高度语义化的表示。
</document>

#### Reference: 

https://arxiv.org/abs/2301.08243, https://www.youtube.com/watch?v=xL6Y0dpXEwc