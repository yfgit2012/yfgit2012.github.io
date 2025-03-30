## Google's Titans vs Transformers

Here is the translation of the contents into English:

This research demonstrates the superior ability of Titans architecture in tasks such as language modeling, common sense reasoning, and DNA modeling. Three variants of Titans (MAC, MAG, and MAL) outperform baseline models, with MAC showing the best performance.

In the BABILong benchmark test, Titans (MAC) exhibits excellent performance, scaling up to over 2 million context windows without sacrificing efficiency, surpassing GPT-4, Llama3 + RAG, and Llama3 - 70B, which have much larger parameter sizes. 

The researchers also found that increasing the depth of memory can improve model performance on longer sequences but decrease training speed, indicating a trade-off between performance and efficiency.

In experiments within the Simba framework, replacing Mamba modules with neural memory modules outperformed all baseline models on ETT, ECL, Traffic, and Weather datasets. 

Furthermore, in DNA modeling tasks, Titans architecture demonstrated strong sequence handling capabilities.

Ablation studies were conducted, which showed that all components of the neural memory module contributed positively to model performance, particularly weight decay and momentum. MAC and MAG performed similarly in language modeling and common sense reasoning tasks but MAC outperformed others in long context tasks.

#### Translation 

这个研究中， Titans 架构在语言建模、常识推理和 DNA 模型等任务中表现出色的能力被展示了。 Titans 的三个变体（MAC、MAG 和MAL）都比基线模型表现得更好，在 S-NIAH 任务中，神经记忆模块相较于基线模型具有显著的优势。特别是 MAC 的性能最佳。

在 BABILong 基准测试中，Titans (MAC) 展现出了卓越的性能，可以有效扩展到超过 200 万的上下文窗口，这超出了 GPT-4、Llama3 + RAG 和 Llama3 - 70B 等大模型。 Titans (MAC) 的参数量远少于这些基线模型，充分展示了在长序列推理方面的高效性和强大能力。

研究人员还发现增加记忆的深度能够提升模型在较长序列上的性能，并且改善困惑度，但这也会导致训练的速度降低。这说明性能与效率之间需要权衡。

此外，在 Simba 框架中进行的实验里，通过替换 Mamba 模块并且在 ETT、ECL、Traffic 和 Weather 等基准数据集上进行测试，神经记忆模块超越了所有的基线模型。在 DNA 建模任务中，Titans 架构同样展示了强大的长序列处理能力。

研究人员还进行了消融研究，结果表明神经记忆模块的所有组件对模型性能都有积极的贡献，特别是权重衰减和动量。在语言建模和常识推理任务中 MAC 和 MAG 表现相近，但是MAC 在长上下文任务中表现最佳。

最后，这项研究得到了康奈尔大学计算机科学系的二年级博士生阿里·贝鲁兹、谷歌算法与优化团队的研究科学家Peilin Zhong以及纽约大学库朗研究所兼职副教授瓦哈卜·米罗克尼等人联合完成。

#### Reference: 

https://arxiv.org/abs/2501.00663