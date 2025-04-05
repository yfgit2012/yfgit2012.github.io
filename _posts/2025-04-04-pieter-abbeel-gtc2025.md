## Pieter Abbeel Keynote at GTC2025: AI for Humanoid Robots

Here are the contents of the <document> XML tags translated into English:

The Abbeel team is working to make robot bodies more modular, allowing for faster learning and efficiency. They use a localized Transformer architecture that leverages inductive bias to speed up model training. This approach effectively views a robot's skeleton and provides local credit assignment, making reinforcement learning more efficient.

Abbeel also mentioned the common challenge of black boxes in reinforcement learning, where it is difficult to understand why a robot succeeded or failed at a task. Body Transformer can analyze what hands and feet did, providing more specific reasons for success or failure.

Based on the locality of robots, this approach is called sparse attention (Masked Attention). It is much more efficient than full connected attention and works well even with limited data. Abbeel believes that only a good GPU is needed to train a robot.

Finally, Abbeel mentioned the goal-setting problem. He thinks that robotic capabilities should be maximized while staying within physical limits. This is an ideal state where safety and lightweight are prioritized. This approach has been integrated into the humanoid bench benchmark test.

The Abbeel team also developed a simulation environment called MuJoCo Playground, an open-source platform for batch GPU rendering, which can be used to test various algorithms. At the end of the presentation, Abbeel showed a robot trained using MuJoCo Playground that could still effectively walk even with remote control interference and recover from errors.

#### Translation 

Abbeel团队致力于将机器人的身体设计得更加模块化，以便实现更快的学习和效率。他们使用局部连接的Transformer架构，利用归纳偏置来加速模型的训练。这种方法可以有效地查看机器人的骨架，并且能够提供局部化的信用分配，使得强化学习更加高效。

Abbeel也提到了强化学习中的一个常见挑战：黑箱问题，即当机器人完成一个任务后，难以理解导致成功或失败的原因。Body Transformer可以分析出手和脚都做了什么，从而提供更具体的原因。

基于机器人的局部性，这种方法被称为具有稀疏注意力（Masked Attention）。这种方法比全连接式Attention要高效得多，并且在数据较少的情况下也能工作得很好。Abbeel认为，只需要一块不错的GPU，就可以训练出一个机器人。

最后，Abbeel提到了目标设定问题。他认为，应该将机器人的能力最大化，而不是让它们超越物理极限。这是一个理想的状态，将安全性和轻便性作为首要目标。这种方法已被整合到了humanoid bench基准测试中。

阿比尔团队还研发了一个名为MuJoCo Playground的模拟环境，这是一个开源的仿真平台，支持批量GPU渲染，可以用于测试多种算法。在演讲结束时，Abbeel展示了一个基于MuJoCo Playground训练的机器人，在有遥控手柄干扰的情况下仍然能有效地行走，并且在出现错误时能够进行恢复。

#### Reference: 

https://www.nvidia.com/en-us/on-demand/session/gtc25-s73182/