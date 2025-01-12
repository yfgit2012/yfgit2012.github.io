## Nvidia Cosmos: WFM platform 

Here are the contents translated into English, excluding any preambles and other content:

1. **Performance**: Its performance is superior to all known word processors, running 12 times faster.
2. **Generating High-Quality Videos**: Can generate detailed videos from text/image input data.
3. **Predicting Scene Evolution**: Can predict the evolution of a scene, helping developers imagine and simulate future scenarios.
4. **Security System**: Provides a powerful security system to protect developers from harmful inputs or outputs.

Additionally:

1. **Instruction-Based Video Prediction**: Researchers demonstrated two tasks: instruction-based video prediction and action-based next-frame prediction.
2. **Cosmos-1X Dataset**: Created a dataset with approximately 200 hours of first-person videos, including navigation, folding clothes, and cleaning a desk.
3. **Bridge Dataset**: Used a public dataset containing approximately 20,000 third-person perspective videos, showing a robotic arm performing various tasks in a kitchen environment.
4. **Real-World Driving Scene (RDS) Dataset**: Created an internal dataset with approximately 360 million 20-second ring-camera video clips.
5. **Multi-Angle World Model**: Fine-tuned the Cosmos-1.0-Diffusion-7B-Text2World model using RDS data and created a multi-angle world model.

In summary, everything in the physical simulation world can be generated through NVIDIA's Cosmos.

#### Translation 

本文讨论了一种新型分词器，称为Cosmos，其性能远超目前所有已知的分词器。研究人员在Cosmos上进行微调并创造了一个能够适用于各种物理AI任务的后训练模型，WFM（World Foundation Model）。该模型可以从文本/图像输入生成详细的视频，并预测场景的演变。

Cosmos及其WFM模型在以下方面表现出色：

1. **性能**: 它的性能比目前所有已知的分词器都要好，运行速度快达12倍。
2. **生成高质量的视频**: 可以从文本/图像输入数据生成详细的视频。
3. **预测场景的演变**: 能够预测场景的变化，帮助开发人员想象和模拟未来的场景。
4. **防护系统**: 提供了一个功能强大的防护系统，以保护开发人员免受有害输入或输出的影响。

此外，本文还讨论了以下内容：

1. **基于指令的视频预测**：研究人员在论文中展示了两个任务，分别是基于指令的视频预测以及基于动作的下一帧预测。
2. **Cosmos-1X数据集**: 创建了一个包含大约200小时第一视角视频的数据集，包括导航、折叠衣物、清洁桌面等任务。
3. **Bridge数据集**: 使用了一个公开数据集，包含大约20,000个第三人称视角的视频，展示了机器人手臂在厨房环境中执行不同任务的过程。
4. **真实驾驶场景RDS数据集**: 创建了一个内部数据集，包含大约360万个20秒的环视视频片段。
5. **多视角世界模型**: 使用RDS数据集对Cosmos-1.0-Diffusion-7B-Text2World模型进行微调，并打造出了一个多视角的世界模型。

总之，物理模拟世界的一切都可以通过英伟达Cosmos来生成出来。

#### Reference: 

https://arxiv.org/pdf/2501.03575