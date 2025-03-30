## Huggingface ultrascale playbook

Here is the translation:

This report provides a detailed introduction to the experiments and results conducted by Hugging Face when preparing a training guide for large language models. They utilized 512 GPUs to conduct over 4000 distributed training experiments, exploring the impact of various distributed training architectures and model sizes on training outcomes. This guide provides a comprehensive and practical manual for large-scale language model training, covering aspects such as parallelization techniques, computational efficiency, communication overhead, etc.

The report summarizes key steps and strategies involved in the large language model training process, including:

1. **Adapting models to memory**: Selecting suitable parallelization techniques based on model size, such as data parallelism, tensor parallelism, or sequence parallelism, to maximize GPU resource utilization.
2. **Meeting target global batch sizes**: Combining techniques like activation value re-computation, gradient accumulation, and data parallelism to set up mini-batch sizes and gradient accumulation steps that meet the target global batch size.
3. **Optimizing training throughput**: Selecting suitable combinations of parallelization strategies based on model scale and hardware resources, such as using pipeline parallelism or inter-stage interleaving, to improve GPU utilization and boost training throughput.

This guide provides a practical manual for large language model training for a wide range of AI developers, researchers, and industry professionals.

#### Translation 

这篇报告详细介绍了Hugging Face在制作大语言模型训练手册时所进行的实验和成果。他们利用512个GPU进行超过4000次分布式训练实验，探索不同分布式训练架构和模型大小对训练效果的影响。这份手册为大规模语言模型训练提供了一个全面且实用的指南，涵盖了多种并行技术、计算效率、通信开销等方面。报告总结了一些在大语言模型训练过程中的关键步骤和策略，包括：

1. **将模型适配到内存中**：根据模型大小选择合适的并行技术，如数据并行、张量并行或序列并行，以尽可能地充分利用GPU资源。
2. **满足目标全局批大小**：结合激活值重计算、梯度累积和数据并行等技术，设置微批次大小和梯度累积步数，以达到目标全局批大小。
3. **优化训练的吞吐量**：根据模型规模和硬件资源选择合适的并行策略组合，如使用流水线并行、交错阶段等技术，以提高GPU利用率并提升训练吞吐量。

这本手册为广大的AI开发者、研究人员以及相关企业提供了一个实用的大语言模型训练指南，希望能帮助读者在实际应用中选择合适的技术和配置。

#### Reference: 

https://huggingface.co/spaces/nanotron/ultrascale-playbook