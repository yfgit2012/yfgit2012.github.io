## Thinking Machines: On-Policy Distillation

Online Policy Distillation (OPD) Summary

---

#### **Core Concepts**  
Online Policy Distillation is an efficient large model training method that combines the advantages of online training and offline distillation. Its core idea is: **using a fixed teacher model (such as a large model optimized through reinforcement learning) to densely supervise the student model's policy, enabling the student model to quickly learn and achieve performance close to the teacher in specific tasks**, without requiring large amounts of data or high computational costs.

---

#### **Key Advantages**  
1. **Performance Improvement**  
   - **Scenario Relevance**: Combining the dynamic adaptation capability of online training, the model achieves large model-level performance in specific domains (such as healthcare, internal company knowledge).  
   - **Dense Feedback**: Achieving 7-10 times faster training speed than reinforcement learning (RL) through per-token scoring (e.g., solving math problems step-by-step).  
   - **Continuous Learning**: Solving the performance degradation caused by SFT (supervised fine-tuning), the fixed teacher model ensures the student model retains old capabilities when facing new tasks.

2. **Cost Efficiency**  
   - **Computational Efficiency**: Compared to reinforcement learning (requiring 17,920 GPU hours), Online Policy Distillation only needs 1,800 hours (about 1/10), saving 9-30 times in FLOPs.  
   - **Data Reuse**: No need for massive data; high-quality data + repeated training can be migrated to other tasks (e.g., achieving teacher-level performance with just one math problem).  
   - **Compatibility with LoRA**: Under lightweight fine-tuning (LoRA), the performance gap narrows from 13 points to 6 points, significantly reducing deployment costs.

3. **Practical Application Value**  
   - **Personalized Scenarios**: Solving the problem of instruction-following capability degradation in enterprise AI assistants during internal knowledge training, restoring instruction capabilities while retaining knowledge (e.g., internal QA scores rise from 36% to 41%).  
   - **Fast Deployment**: Achieving continuous learning and efficient deployment through a phased strategy of "first learning new knowledge, then using Online Policy Distillation to restore old capabilities."

---

#### **Experimental Results**  
- **Math Problem Solving**:  
  - Reinforcement learning requires 70 gradient steps, while Online Policy Distillation only needs 7-10 steps.  
  - With 77,000 samples trained, the student model achieves scores close to the teacher's level (70 → 74.4 on AIME24).  
- **Internal Company Knowledge**:  
  - After mid-training, internal QA scores rise from 36% to 41%, and IF-eval scores recover to 83%.  
- **Data Efficiency**:  
  - Training with just one math problem repeated 20 times achieves performance close to the teacher model.

---

#### **Application Scenarios**  
1. **Personalized AI Assistants**:  
   - Enterprise internal models need to simultaneously master company knowledge and instruction-following capabilities to avoid training degradation.  
2. **Data-Sparse Fields (e.g., Medical/Financial)**:  
   - Achieving model capability transfer with minimal high-quality data + dense supervision.  
3. **Continuous Learning**:  
   - After monthly industry data updates, using 1-2 days of Online Policy Distillation to balance old capabilities and new knowledge.

---

#### **Challenges and Future Directions**  
1. **Teacher Model Accuracy**:  
   - How to improve the accuracy of the scoring mechanism to avoid student performance degradation caused by teacher model biases.  
2. **Multi-Task Adaptation**:  
   - Exploring the universality and optimization strategies of Online Policy Distillation in multi-task scenarios.  
3. **Reducing Teacher Dependency**:  
   - Reducing reliance on large models by developing lighter teacher models or distributed distillation schemes.

---

#### **Summary**  
Online Policy Distillation addresses the pain points of traditional methods in efficiency, cost, and continuous learning through dense supervision and a fixed teacher model, becoming an efficient tool for large model training and fine-tuning. Its core value lies in: **achieving high-performance, low-cost AI deployment using small-to-medium models combined with Online Policy Distillation**, providing developers and enterprises with flexible and practical solutions. In the future, with algorithm optimization and data innovation, its potential in more vertical fields and complex scenarios will be further unleashed.

#### Translation 

### 在线策略蒸馏（Online Policy Distillation）总结

---

#### **核心概念**  
在线策略蒸馏是一种结合在线训练与离线蒸馏优势的高效大模型训练方法。其核心思想是：**通过固定教师模型（如经过强化学习优化的大模型）对学生的策略进行密集监督，使学生模型在特定任务中快速学习并达到接近教师的性能**，而无需大量数据或高昂的计算成本。

---

#### **关键优势**  
1. **性能提升**  
   - **场景相关性**：结合在线训练的动态适应能力，使模型在特定领域（如医疗、企业内部知识）达到大模型级性能。  
   - **反馈密集性**：通过逐token评分（如数学题解题过程），实现比强化学习（RL）快7-10倍的训练速度。  
   - **持续学习**：解决SFT（监督微调）导致的性能退化问题，固定教师模型确保学生模型在新任务中不丢失旧能力。

2. **成本效率**  
   - **计算效率**：相比强化学习（需17920 GPU小时），在线策略蒸馏仅需1800小时（约1/10），FLOPs节省9-30倍。  
   - **数据复用**：无需海量数据，高质量数据+反复训练即可迁移至其他任务（如仅用一道数学题训练，AIME24得分接近教师水平）。  
   - **兼容LoRA**：在轻量微调（LoRA）下，性能差距从13分缩小至6分，显著降低部署成本。

3. **实际应用价值**  
   - **个性化场景**：解决企业AI助手在训练内部知识时指令遵循能力退化的问题，恢复指令能力的同时保留知识（如内部QA得分从36%提升至41%）。  
   - **快速部署**：通过“先学新知识，再用在线策略蒸馏恢复旧能力”的阶段交替策略，实现模型的持续学习与高效落地。

---

#### **实验结果**  
- **数学题解题**：  
  - 强化学习需70梯度步，而在线策略蒸馏仅需7-10步。  
  - 7.7万样本训练下，学生模型AIME24得分接近教师水平（70分→74.4分）。  
- **企业内部知识**：  
  - 中期训练后，内部QA得分从36%提升至41%，IF-eval得分恢复至83%。  
- **数据效率**：  
  - 仅用一道数学题反复训练20步，模型性能接近教师模型。

---

#### **应用场景**  
1. **个性化AI助手**：  
   - 企业内部模型需同时掌握公司知识与指令遵循能力，避免训练退化。  
2. **医疗/金融等数据稀缺领域**：  
   - 通过少量高质量数据+密集监督，实现模型能力迁移。  
3. **持续学习**：  
   - 每月更新行业数据后，用1-2天在线策略蒸馏，保持旧能力与新知识平衡。

---

#### **挑战与未来方向**  
1. **教师模型精准性**：  
   - 如何提升评分机制的准确性，避免因教师模型偏差影响学生性能。  
2. **多任务适配**：  
   - 探索在线策略蒸馏在多任务场景下的通用性与优化策略。  
3. **降低教师依赖**：  
   - 减少对大模型的依赖，开发更轻量的教师模型或分布式蒸馏方案。  

---

#### **总结**  
在线策略蒸馏通过密集监督与固定教师模型，解决了传统方法在效率、成本和持续学习中的痛点，成为大模型训练与微调的高效工具。其核心价值在于：**以中小模型+在线策略蒸馏的方式，实现高性能、低成本的AI落地**，为开发者和企业提供了灵活且实用的解决方案。未来，随着算法优化与数据创新，其在更多垂直领域和复杂场景中的潜力将进一步释放。

#### Reference: 

https://thinkingmachines.ai/blog/on-policy-distillation/