## DeepSeek: Engram architecture

**Summary:**  
The DeepSeek team proposed a novel architecture called Engram, aiming to enhance the efficiency and performance of large-scale models by decoupling local pattern reconstruction from global reasoning tasks. Engram introduces a Conditional Memory Module, storing static knowledge in a parameterized memory table, thereby reducing the routing costs and training instability of traditional MoE models at ultra-large scales. Experiments show that Engram outperforms traditional MoE models in long-context processing and complex retrieval tasks (such as the RULER benchmark), with significant advantages in inference efficiency and parameter scalability. This architecture not only supports efficient pre-training and deployment but also enables future knowledge updates and dynamic learning.

---

**Key Points:**  
1. **Core Idea of Engram Architecture**  
   - Decoupling local pattern reconstruction (static knowledge) from global reasoning tasks to reduce computational burden on the Transformer backbone.  
   - Utilizing a parameterized memory table (Memory Table) to store static knowledge, enabling O(1) time complexity for direct retrieval.  

2. **Technological Innovations**  
   - **Memory Module**: Transferring local dependency modeling tasks to a dedicated memory module, freeing the attention mechanism for global processing.  
   - **Context-Aware Gating**: Dynamically activating memory modules based on input, for example, when encountering proper nouns (e.g., "Alexander the Great") or fixed titles (e.g., "Princess of Wales"), the gating value significantly increases.  
   - **Lightweight Optimization**: Enhancing efficiency through components like tokenizer compression and branch-specific fusion, reducing validation loss.  

3. **Performance Advantages**  
   - **Training Efficiency**: Engram-27B achieves MoE-27B performance with only 82% of the pre-training computational resources, even surpassing it on the RULER benchmark.  
   - **Inference Efficiency**: Even after offloading a 1000-billion-parameter memory table to host memory, the inference throughput on H800 hardware decreases by less than 3%.  
   - **Long-Context Processing**: Engram outperforms traditional architectures in tasks with 32,768 token long-context.  

4. **Experimental Results**  
   - **Model Comparison**: Engram-27B significantly outperforms MoE-27B in multi-query tasks on the RULER benchmark.  
   - **Knowledge Storage**: Shielding the Engram module reduces factual knowledge task performance to 29-44%, proving its critical role as a parameterized knowledge repository.  
   - **Scalability**: Engram-40B further reduces pre-training loss, with the training loss gap still widening, indicating the memory capacity has not fully unleashed its potential.  

5. **Engineering and Application Value**  
   - **Deployment Advantages**: The deterministic access pattern of the memory module supports efficient pre-fetching and hardware optimization, suitable for large-scale deployment.  
   - **Knowledge Updating**: Future knowledge errors can be corrected by directly modifying the memory table, eliminating the need for costly fine-tuning.  
   - **Future Directions**: Exploring online learning or dynamic updating memory modules to enable models to acquire new knowledge in real time.  

---

**References/Technologies**  
1. **RULER Benchmark**: Used to evaluate models' ability to handle long-range dependencies in complex retrieval tasks.  
2. **DeepSeek-V3 and YaRN Technology**: Expanding context windows to 32,768 tokens enhances models' understanding of long texts.  
3. **Comparison with Traditional MoE**: Engram addresses MoE's high routing costs and training instability at ultra-large scales.  
4. **Comparison with RAG (Retrieval-Augmented Generation)**: Engram internalizes knowledge into parameter tables, offering lower latency and stronger knowledge consistency compared to external database retrieval.  

---  

**Note:** This is an interpretation of the DeepSeek paper, not directly citing the original references, but covering its core innovations and experimental conclusions.

#### Translation 

**总结：**  
DeepSeek团队提出了一种名为Engram的新型架构，旨在通过解耦局部模式重建与全局推理任务，提升大规模模型的效率与性能。Engram通过引入条件记忆模块（Conditional Memory Module），将静态知识存储在参数化的记忆表中，从而减少传统MoE模型在超大规模下的路由成本和训练不稳定性。实验表明，Engram在长上下文处理、复杂检索任务（如RULER基准）中表现优于传统MoE模型，且在推理效率和参数扩展性上具有显著优势。该架构不仅支持高效预训练和部署，还为未来知识更新和动态学习提供了可能性。

---

**关键点：**  
1. **Engram架构的核心思想**  
   - 通过解耦局部模式重建（静态知识）与全局推理任务，减少Transformer骨干网络的计算负担。  
   - 利用参数化记忆表（Memory Table）存储静态知识，实现O(1)时间复杂度的直接检索。  

2. **技术创新**  
   - **记忆模块**：将局部依赖建模任务转移至专门的记忆模块，释放注意力机制的全局处理能力。  
   - **上下文感知门控**：根据输入动态激活记忆模块，例如专有名词（如“亚历山大大帝”）或固定称谓（如“威尔士王妃”）时，门控值显著提升。  
   - **轻量级优化**：通过分词器压缩、分支特定融合等组件提升效率，减少验证损失。  

3. **性能优势**  
   - **训练效率**：Engram-27B仅需82%的预训练计算量即可达到MoE-27B的性能，甚至在RULER基准上实现超越。  
   - **推理效率**：即使卸载1000亿参数的记忆表至主机内存，H800硬件的推理吞吐量下降不足3%。  
   - **长上下文处理**：在32768个token的长上下文任务中，Engram比传统架构表现更优。  

4. **实验结果**  
   - **模型对比**：Engram-27B在RULER基准的多查询任务中准确率显著领先于MoE-27B。  
   - **知识存储**：屏蔽Engram模块后，事实性知识任务性能下降至29-44%，证明其作为参数化知识仓库的关键作用。  
   - **扩展性**：Engram-40B进一步降低预训练损失，且训练损失差距仍在扩大，表明记忆容量尚未完全释放潜力。  

5. **工程与应用价值**  
   - **部署优势**：记忆模块的确定性访问模式支持高效预读取和硬件优化，适合大规模部署。  
   - **知识更新**：未来可通过直接修改记忆表修正模型知识错误，无需昂贵微调。  
   - **未来方向**：探索在线学习或动态更新的记忆模块，使模型实时获取新知识。  

---

**参考文献/技术**  
1. **RULER基准**：用于评估模型在复杂检索任务中的长程依赖处理能力。  
2. **DeepSeek-V3与YaRN技术**：通过扩展上下文窗口至32768个token，增强模型对长文本的理解。  
3. **传统MoE对比**：Engram解决了MoE在超大规模下的路由成本高、训练不稳定问题。  
4. **RAG（Retrieval-Augmented Generation）对比**：Engram内化知识至参数表，相比外部数据库检索具有更低延迟和更强知识一致性。  

--- 

**注**：本文为对DeepSeek论文的解读，未直接引用原文参考文献，但涵盖其核心创新点与实验结论。

#### Reference: 

https://github.com/deepseek-ai/Engram