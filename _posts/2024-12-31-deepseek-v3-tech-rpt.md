## DeepSeek V3 Tech Report

Here is the translation:

<document>This text appears to be a technical report, describing a model called DeepSeek V3. Here are some key points:

1. **Learning Rate Adjustment**: The learning rate of the model is adjusted in four stages using different strategies, ultimately reaching a minimum constant learning rate.
2. **Dynamic Batch Size**: The batch size increases gradually during training from 3072 to 15360 and then remains unchanged.
3. **Load Balancing**: The model uses an unbiased load balancing strategy without additional loss, adjusting the update speed of bias terms to achieve load balancing.
4. **Sequence-Level Balance Loss Factor**: Set to 0.0001 to help optimize the model's performance in handling long contexts.
5. **Multi-Head Ken Prediction MPT Loss Weight Lambda**: Adjusted this value to control the impact of multi-head KEN prediction.
6. **Two-Phase Training Strategy**: The model is trained gradually by extending its context window from 4K to 128K, adjusting batch size and learning rate.
7. **Post-Training Phase**: Includes supervised fine-tuning (SFT) and reinforcement learning (RL) to further optimize the model's performance.

These details show that DeepSeek V3 is a carefully designed model aiming to improve its performance in handling long text tasks.</document>

#### Translation 

此文本似乎是一份技术报告，描述了一个叫做DeepSeek V3的模型。这里是其中一些主要点：

1. **学习率调整**：模型的学习率经过四个阶段进行调整，每个阶段使用不同的策略，最终达到最小常数学习率。
2. **动态批次大小**：批次大小在训练过程中逐步增加，从3072增加到15360，然后保持不变。
3. **负载均衡**：模型使用无额外损失的负载均衡策略，调整偏置项更新速度来实现负载均衡。
4. **序列级平衡损失因子**：设置为0.0001，以帮助优化模型在处理长上下文时的表现。
5. **多头肯预测MPT损失的权重拉姆达**：调整了这个值来控制多头KEN预测的影响。
6. **两阶段训练策略**：模型通过两步训练逐渐扩展其上下文窗口，从4K增长到128K，调整批次大小和学习率。
7. **后训练阶段**：包括监督微调（SFT）和强化学习（RL），以进一步优化模型的性能。

这些信息表明DeepSeek V3是一个经过精心设计的模型，旨在提高其在处理长文本任务中的表现。

#### Reference: 

https://github.com/deepseek-ai/DeepSeek-V3/blob/main/DeepSeek_V3.pdf