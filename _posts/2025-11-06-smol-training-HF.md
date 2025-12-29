## HF: The Smol Training Playbook

This guide reveals the core trends and key challenges in the training of current large language models. Here is a systematic summary of the key points:

---

### **I. Core Strategies for Model Training**
1. **Rise of Small Models**  
   - **Balance of Parameters and Performance**: SmolLM3 (3B parameters) outperforms Qwen3-1.7B and Qwen3-4B in multilingual, mathematical, and coding benchmarks, proving that small models can achieve large model performance through systematic optimization.  
   - **Edge Deployment Friendliness**: Models with 3B parameters offer advantages in resource consumption and inference speed, making them suitable for deployment on edge devices.  

2. **Evolution of Training Strategies**  
   - **Staged Post-Training**:  
     - **Supervised Fine-Tuning (SFT)**: As a foundation, enhances instruction-following capability (improves by 12%).  
     - **Preference Optimization (APO)**: Optimizes model selection ability based on generated preference data (e.g., Qwen3-32B vs Qwen3-0.6B), improving performance by 15-20%.  
     - **Reinforcement Learning (RL)**: Further optimizes reasoning chains through real-time feedback (e.g., length penalty), improving AIME25 by 8%.  
   - **Avoid Skipping SFT**: Reinforcement learning must be based on SFT baseline; otherwise, it may lead to divergence or performance degradation.  

---

### **II. Hidden Costs of Infrastructure**
1. **Storage Efficiency**  
   - **Local NVMe RAID**: An 8-drive 3.5TB NVMe RAID 0 achieves a throughput of 26.59 GB/s, 6 times faster than network storage.  
   - **Storage Strategy**: Train data is stored locally, with local Checkpoints saved every 2 hours and uploaded to S3 backup to avoid storage space exhaustion.  

2. **GPU Communication Optimization**  
   - **NVLink**: Uses NVLink 4.0 (bidirectional 786 GB/s) within the same node, avoiding PCIe latency (55 times slower).  
   - **EFA Network**: Cross-node communication uses AWS EFA (42 GB/s bandwidth), 14 times faster than TCP.  
   - **PCIe Limitations**: Only used for data loading between GPU and CPU, avoiding GPU-to-GPU communication.  

3. **Memory and Compute Matching**  
   - **BF16 Training**: H100's Tensor Core optimizes BF16 exceptionally well (utilization 72-77%), while FP8 faces memory bottlenecks due to HBM3 bandwidth limitations (utilization 31-37%).  
   - **Flash Attention**: Caches attention computation results in L1/shared memory, boosting throughput by 2-4 times.  

---

### **III. Key Details in the Training Process**
1. **Rigorous Ablation Studies**  
   - **Feature Validation**: Any changes must be validated through ablation studies (e.g., APO vs DPO).  
   - **Hyperparameter Design**: SFT learning rate 1e-5, batch size 128, user round masking (only calculates model output loss).  

2. **Importance of System Capabilities**  
   - **Strategic Decision-Making**: Clearly define training goals to avoid redundant model creation.  
   - **Debug Process**: Prioritize storage/loader issues before analyzing code logic.  
   - **Time Allocation**: In actual training, 30% time is for decision-making, 50% for debugging, and 20% for observing loss curves.  

---

### **IV. Deep Optimization of Post-Training**
1. **Preference Data Generation**  
   - **Generate Adversarial Samples**: Qwen3-32B generates high-quality responses, while Qwen3-0.6B generates low-quality ones, creating over 250,000 preference samples.  
   - **Advantages of APO**: Compared to DPO, APO enables more precise control over optimization magnitude, avoiding overemphasis on preference data.  

2. **Practical Reinforcement Learning**  
   - **GRPO + Length Penalty**: In inference mode, controls response length (around 2k) via length penalty (2.5-3k), improving AIME25 scores.  

---

### **V. Summary and Insights**
- **From Hardware Stacking to System Optimization**: Small model training no longer relies on parameter count or GPU quantity but competes in system capabilities (e.g., ablation studies, infrastructure design, debugging efficiency).  
- **Key Success Factors**:  
  - **Clear Strategic Decisions** (avoid redundant models)  
  - **Rigorous Experimental Validation** (ablation studies)  
  - **Efficient Infrastructure** (storage, communication, memory optimization)  
  - **Fast Debugging Process** (hardware-to-software troubleshooting)  
- **Future Directions**: Integration of reinforcement learning and preference optimization, along with more granular reward function design, will be critical for enhancing model performance.  

---

### **Appendix: Recommended Practices**
- **Ablation Study Configuration**: Record performance comparisons of different hyperparameters and architectural changes during training.  
- **nanotron Usage**: Focus on its communication optimization capabilities in distributed training.  
- **APO Implementation**: Reference Qwen3's preference data generation and optimization strategies.  
- **Storage and Communication Tools**: Prioritize NVMe RAID, EFA network, and NVLink to avoid PCIe and network storage.  

The core value of this guide lies in revealing the shift from "hardware stacking" to "system engineering" in model training, emphasizing the importance of detail optimization and strategic design, providing reusable paradigms for small model training.

#### Translation 

这份指南揭示了当前大语言模型训练的核心趋势和关键挑战，以下是核心要点的系统性总结：

---

### **一、模型训练的核心策略**
1. **小模型的崛起**  
   - **参数量与性能的平衡**：SmolLM3（3B参数）在多语言、数学、代码等基准测试中超越了Qwen3-1.7B和Qwen3-4B，证明小模型通过系统优化可达到大模型性能。
   - **端侧部署友好性**：3B参数的模型在资源占用和推理速度上更具优势，适合边缘设备部署。

2. **训练策略的演进**  
   - **分阶段后训练**：  
     - **监督微调（SFT）**：作为基础，提升指令跟随能力（提升12%）。  
     - **偏好优化（APO）**：基于生成的偏好数据（如Qwen3-32B vs Qwen3-0.6B），优化模型选择能力（提升15-20%）。  
     - **强化学习（RL）**：通过实时反馈（如长度惩罚）进一步优化推理链（AIME25提升8%）。  
   - **避免跳过SFT**：强化学习需基于SFT的基线，否则易导致发散或性能下降。

---

### **二、基础设施的隐形成本**
1. **存储效率**  
   - **本地NVMe RAID**：8块3.5TB NVMe的RAID 0实测吞吐量达26.59 GB/s，比网络存储快6倍。  
   - **存储策略**：训练数据本地存储，每2小时保存一次本地Checkpoint并上传S3备份，避免存储空间占满。

2. **GPU通信优化**  
   - **NVLink**：同节点内使用NVLink 4.0（双向786 GB/s），避免PCIe延迟（慢55倍）。  
   - **EFA网络**：跨节点通信使用AWS EFA（42 GB/s带宽），比TCP快14倍。  
   - **PCIe的局限性**：仅用于GPU与CPU间的数据加载，避免GPU间通信。

3. **内存与计算匹配**  
   - **BF16训练**：H100的Tensor Core对BF16优化极佳（利用率72-77%），而FP8因HBM3带宽限制（利用率31-37%）存在内存瓶颈。  
   - **Flash Attention**：将注意力计算结果缓存于L1/共享内存，吞吐量提升2-4倍。

---

### **三、训练过程的关键细节**
1. **消融实验的严谨性**  
   - **特性验证**：任何改动前需通过消融实验验证（如APO对比DPO）。  
   - **超参数设计**：SFT学习率1e-5，批大小128，用户轮次掩码（仅计算模型输出损失）。

2. **系统能力的重要性**  
   - **战略决策**：明确训练目标，避免重复已有模型。  
   - **debug流程**：优先排查存储/加载器问题，再分析代码逻辑。  
   - **时间分配**：实际训练中30%时间用于决策，50%用于debug，20%观察损失曲线。

---

### **四、后训练的深度优化**
1. **偏好数据生成**  
   - **生成对抗样本**：Qwen3-32B生成高质量回答，Qwen3-0.6B生成低质量回答，形成25万+偏好样本。  
   - **APO的优势**：相比DPO，APO能更精准控制优化幅度，避免过度偏向偏好数据。

2. **强化学习的实践**  
   - **GRPO+长度惩罚**：在推理模式中通过长度惩罚（2.5-3k）控制回答长度（约2k），提升AIME25分数。

---

### **五、总结与启示**
- **从硬件堆叠到系统优化**：小模型的训练已不再依赖参数量和GPU数量，而是拼系统能力（如消融实验、基础设施设计、debug效率）。  
- **关键成功因素**：  
  - **清晰的战略决策**（避免重复模型）  
  - **严谨的实验验证**（消融实验）  
  - **高效的基础设施**（存储、通信、内存优化）  
  - **快速的debug流程**（硬件到软件的排查）  
- **未来方向**：强化学习与偏好优化的结合，以及更细粒度的奖励函数设计，将是提升模型效果的关键。

---

### **附录：推荐实践**
- **消融实验配置**：在训练过程中记录不同超参数、架构变更的性能对比。  
- **nanotron使用**：关注其在分布式训练中的通信优化能力。  
- **APO实现**：参考Qwen3的偏好数据生成与优化策略。  
- **存储与通信工具**：优先使用NVMe RAID、EFA网络、NVLink，避免PCIe和网络存储。

这份指南的核心价值在于揭示了模型训练从“堆硬件”到“系统工程”的转变，强调了细节优化和策略设计的重要性，为小模型训练提供了可复用的范式。

#### Reference: 

https://huggingface.co/spaces/HuggingFaceTB/smol-training-playbook