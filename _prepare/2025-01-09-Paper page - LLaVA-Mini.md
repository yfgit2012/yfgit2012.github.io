## Paper page - LLaVA-Mini: Efficient Image and Video Large Multimodal Models with One Vision Token

Here is a summary of the contents in about half of the total length:

LLaVA-Mini: Efficient Image and Video Large Multimodal Models with One Vision Token

Abstract:
The advent of real-time large multimodal models (LMMs) like GPT-4o has sparked interest in efficient LMMs. Previous efforts focus on replacing the LLM backbone, neglecting token quantity. We introduce LLaVA-Mini, an efficient LMM that fuses visual information into text tokens in advance, reducing vision tokens to one.

LLaVA-Mini is a unified large multimodal model supporting images, high-resolution images, and videos efficiently. Experiments demonstrate LLaVA-Mini outperforms LLaVA-v1.5 with just 1 vision token instead of 576. Efficiency analyses reveal:

* Computational effort: 77% FLOPs reduction
* Response latency: reduce from 100 milliseconds to 40 milliseconds
* VRAM memory usage: reduce from 360 MB/image to 0.6 MB/image, support 3-hour video processing

Code, Model, and demo of LLaVA-Mini are available now!

#### Translation 

<document>
LLaVA-Mini：高效图像和视频大型多模态模型，仅需一张视觉通道

摘要：
LMM（Large Multimodal Model）的大型模型如GPT-4o的出现，激发了人们对高效LMM的兴趣。之前的努力主要集中在替换LLM的骨干网络，而忽略了token数量的减少问题。我们引入了LLaVA-Mini，这是一种高效的LMM模型，它将视觉信息融合到文本通道中，减少了视觉通道数量至一张。

LLaVA-Mini是一个支持图像、高清图像和视频处理的大型多模态模型。实验结果表明，与仅使用576张视觉通道的LLA-VA-v1.5相比，LLaVA-Mini在效率方面表现出明显优势：

* 计算开销：77% FLOPs（浮点运算）减少
* 回复延迟：从100毫秒降至40毫秒
* VRAM内存使用量：图像处理时从360MB/image降至0.6MB/image，可支持3小时视频处理

代码、模型和LLaVA-Mini的演示已在此处发布！</document>

#### Reference: 

https://huggingface.co/papers/2501.03895