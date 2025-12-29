## Agentic Context Engineering 

ACE Framework Summary: Redefining the Self-Improvement Method of Large Language Models

---

#### **Core Value**  
The ACE framework addresses two major pain points of existing methods through a **generate-reflect-organize** closed-loop mechanism:  
1. **Simplicity Bias** (over-reliance on short prompts, losing detail strategies)  
2. **Context Collapse** (knowledge fragmentation caused by frequent updates)  
Without requiring model weight updates, it achieves triple improvements in performance, efficiency, and cost through context optimization.

---

#### **Key Advantages**  
1. **Performance Breakthrough**  
   - **Agent Tasks**: In AppWorld rankings, ReAct+ACE (based on the open-source model DeepSeek-V3.1) achieves an average accuracy of 59.4%, close to GPT-4.1 (60.3%), and performs better in challenging test sets (8.4% higher on TGC).  
   - **Financial Tasks**:  
     - **FiNER** (Entity Recognition): Accuracy improves by 7.6 percentage points (78.3%), capable of distinguishing fine-grained entities (e.g., unrestricted cash vs. restricted cash).  
     - **Formula** (Numerical Reasoning): Accuracy increases by 18 percentage points (85.5%) from the base model, precisely extracting calculation logic (e.g., full steps of diluted EPS).  

2. **Efficiency and Cost Optimization**  
   - **Offline Adaptation**: In AppWorld tasks, adaptation latency drops from 53,898 seconds to 9,517 seconds (82.3% reduction), with rollout frequency reduced by 75.1%.  
   - **Online Adaptation**: In FiNER tasks, latency decreases from 65,104 seconds to 5,503 seconds (91.5% reduction), and token costs drop by 83.6% (from $17.7 to $2.9).  

3. **Potential of Small Models**  
   ACE enables small models (e.g., DeepSeek-V3.1) to approach the performance of large models (e.g., GPT-4.1), significantly reducing deployment costs for Agent applications.

---

#### **Application Scenarios**  
ACE is suitable for scenarios requiring **complex strategy accumulation**:  
- **Agent Tasks**: Multi-turn tool calls, dynamic environment adaptation  
- **Domain Reasoning**: Financial numerical calculations, medical document analysis  
- **Long-Context Needs**: Tasks requiring precise differentiation of fine-grained entities or complex logic (e.g., XBRL parsing)  

---

#### **Limitations**  
1. **Dependence on Strong Reflectors**: If the reflector fails to extract effective insights (e.g., distinguishing DICOM/HL7 formats in medical document analysis), ACE may underperform compared to simple context learning.  
2. **Not All Tasks Are Applicable**:  
   - **Simple Tasks** (e.g., common-sense QA, 24-point game): Short prompts are more efficient; long contexts may increase inference burden.  
   - **No-Feedback Scenarios**: Performance declines without ground truth labels or execution feedback (e.g., FiNER accuracy drops to 71.1% without labels).  

---

#### **Insights for Developers and Enterprises**  
1. **Developers**:  
   - Optimize context design rather than solely pursuing model parameter volume.  
   - Use ACE to achieve efficient adaptation of small models, lowering deployment barriers.  

2. **Enterprises**:  
   - **Cost Advantage**: Combining open-source models with ACE can significantly reduce deployment costs for complex AI systems (e.g., annual savings exceeding $10,000 for financial document processing).  
   - **Explainability**: ACE's editable context (e.g., deleting erroneous entries) meets data privacy regulations.  

---

#### **Future Directions**  
ACE provides new insights for **online learning and continual learning**:  
- **Dynamic Updates**: Adjust strategies in real-time using new execution feedback (e.g., replacing rules when accounting standards change).  
- **Reduce Redundant Inference**: Combine long contexts with KV caching technology to lower computational costs.  

---

**Summary**: The ACE framework redefines the self-improvement path of large language models through context optimization, particularly excelling in complex tasks. Its core value lies in **precise strategy accumulation** and **cost-efficiency balance**, offering developers and enterprises more flexible and economical AI solutions.

#### Translation 

### ACE框架总结：重新定义大语言模型的自我提升方式

---

#### **核心价值**  
ACE框架通过**生成-反思-整理**的闭环机制，将大语言模型的上下文转化为动态演进的知识库，解决了现有方法的两大痛点：  
1. **简洁性偏差**（过度依赖简短提示词，丢失细节策略）  
2. **上下文坍缩**（频繁更新导致知识碎片化）  
无需依赖模型权重更新，通过上下文优化实现性能、效率与成本的三重提升。

---

#### **关键优势**  
1. **性能突破**  
   - **Agent任务**：在AppWorld排行榜中，ReAct+ACE（基于开源模型DeepSeek-V3.1）的平均准确率（59.4%）接近GPT-4.1（60.3%），且在测试挑战集（难度更高）中表现更优（TGC高8.4%）。  
   - **金融任务**：  
     - **FiNER**（实体识别）：准确率提升7.6个百分点（78.3%），能区分细分实体（如无限制现金 vs 受限现金）。  
     - **Formula**（数值推理）：准确率从基础模型提升18个百分点（85.5%），精准提炼计算逻辑（如稀释每股收益的完整步骤）。  

2. **效率与成本优化**  
   - **离线适配**：在AppWorld任务中，适配延迟从53,898秒降至9,517秒（降幅82.3%），rollout次数减少75.1%。  
   - **在线适配**：在FiNER任务中，延迟从65,104秒降至5,503秒（降幅91.5%），token成本降低83.6%（从17.7美元至2.9美元）。  

3. **小模型潜力释放**  
   ACE使小模型（如DeepSeek-V3.1）接近大模型（如GPT-4.1）的性能，显著降低Agent应用的部署成本。

---

#### **应用场景**  
ACE适用于需要**复杂策略积累**的场景：  
- **Agent任务**：多轮工具调用、动态环境适应  
- **领域推理**：金融数值计算、医疗文档分析  
- **长上下文需求**：需精准区分细分实体或复杂逻辑的任务（如XBRL解析）  

---

#### **局限性**  
1. **依赖强反思器**：若反思器无法提炼有效洞察（如医疗文档分析中区分DICOM/HL7格式），ACE效果可能不如简单上下文学习。  
2. **非所有任务适用**：  
   - **简单任务**（如常识问答、24点游戏）：简洁提示词更高效，长上下文反而增加推理负担。  
   - **无反馈场景**：若缺乏真值标签或执行反馈，性能会下降（如FiNER无标签时准确率仅71.1%）。  

---

#### **对开发者与企业的启示**  
1. **开发者**：  
   - 优化上下文设计，而非单纯追求模型参数量。  
   - 利用ACE实现小模型的高效适配，降低部署门槛。  

2. **企业**：  
   - **成本优势**：开源模型+ACE组合可显著降低复杂AI系统的部署成本（如金融文档处理年节省超1万美元）。  
   - **可解释性**：ACE的上下文可编辑（如删除错误条目），满足数据隐私法规要求。  

---

#### **未来方向**  
ACE为**在线学习与持续学习**提供了新思路：  
- **动态更新**：通过新执行反馈实时调整策略（如会计准则变更时替换规则）。  
- **减少重复推理**：长上下文结合KV缓存技术，降低计算成本。  

---

**总结**：ACE框架通过上下文优化，重新定义了大语言模型的自我提升路径，尤其在复杂任务中展现卓越性能。其核心价值在于**精准策略积累**与**成本效率平衡**，为开发者和企业提供了更灵活、经济的AI解决方案。

#### Reference: 

https://arxiv.org/pdf/2510.04618v1