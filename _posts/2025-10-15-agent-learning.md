## Agent Learning via Early Experience 

"早期经验"范式在AI代理开发中的总结  

### **早期经验的核心价值**  
1. **解决无奖励学习挑战**：  
   - 该范式使用**动作-未来状态对**作为监督信号，无需外部奖励。这使其适用于大多数奖励不可用的真实世界环境。  

2. **降低数据依赖性**：  
   - 早期经验能够以**更少专家数据**实现与全模仿学习相当甚至更高的性能。例如，在WebShop中，使用1/8的专家数据表现优于全模仿学习。  

3. **连接模仿与强化学习**：  
   - 它是一种**混合框架**，增强模仿学习并作为强化学习（RL）的强大初始化方法。这弥合了人类数据驱动方法与自我改进系统的差距。  

---

### **关键方法论组件**  
1. **隐式世界建模（IWM）**：  
   - 从动作预测未来状态，使代理学习环境动态。  
   - **性能**：随替代动作数量（分支因子K）增加而提升。  

2. **自我反思（SR）**：  
   - 生成专家动作优于替代方案的原因解释，利用未来状态差异。  
   - **实现**：需结构化提示以确保逻辑且可操作的解释，提升策略优化。  

3. **训练流程**：  
   - 结合**专家数据**和**自我生成的反思**（D_refl）进行训练。  
   - 平衡准确性（专家路线）和泛化能力（自我反思）。  

---

### **实验验证**  
- **测试环境**：8种多样化场景（如WebShop、TravelPlanner、ALFWorld）和3种模型规模（3B、70B）。  
- **评估指标**：  
  - **有效性**：早期经验平均超越模仿学习**+9.6%**，在TravelPlanner（SR）中提升**+15.0%**，在WebShop（IWM）中提升**+9.6%**。  
  - **泛化能力**：早期经验在分布外（OOD）任务中恢复更多性能，部分OOD增益超过分布内得分。  
  - **RL兼容性**：以早期经验初始化的RL模型表现优于模仿学习初始化模型，训练过程中保持持续领先。  

---

### **局限性与未来方向**  
1. **局限性**：  
   - **短序列聚焦**：当前方法优化于短交互（如单次点击），但长序列（如多步任务）需进一步研究。  
   - **安全风险**：在高风险环境（如删除文件）中试错动作可能带来危害，需安全探索策略。  

2. **未来研究**：  
   - **自监督整合**：引入动作一致性或状态预测任务以增强环境理解。  
   - **跨环境迁移**：实现从环境A到环境B的知识迁移以减少冗余训练。  
   - **现实部署**：收集自然用户交互以实现持续学习，推动代理向自主改进发展。  

---

### **结论与影响**  
"早期经验"范式标志着向**自主AI代理**迈出的重要一步，使其无需人工干预即可学习和适应。通过结合模仿学习与强化学习，它解决了无奖励学习和数据效率的关键挑战。尽管实际部署面临挑战，但研究凸显了AI助手通过自我反思和试错演进的潜力，契合Sutton等人提出的"经验时代"愿景。这项工作为现实应用中更智能、自给自足的系统铺平了道路。

#### Translation 

**Summary of the "Early Experience" Paradigm in AI Agent Development**  

### **Core Value of Early Experience**  
1. **Solving the Reward-Free Learning Challenge**:  
   - The paradigm uses **action-future state pairs** as supervision signals, eliminating the need for external rewards. This makes it adaptable to most real-world environments where rewards are unavailable.  

2. **Reducing Data Dependency**:  
   - Early Experience enables **fewer expert data** to achieve performance comparable to or exceeding full imitation learning. For example, in WebShop, using 1/8 of the expert data outperformed full imitation learning.  

3. **Bridging Imitation and Reinforcement Learning**:  
   - It acts as a **hybrid framework**, enhancing imitation learning and serving as a strong initialization for reinforcement learning (RL). This bridges the gap between human data-driven methods and self-improving systems.  

---

### **Key Methodological Components**  
1. **Implicit World Modeling (IWM)**:  
   - Predicts future states from actions, enabling the agent to learn environmental dynamics.  
   - **Performance**: Scales with the number of alternative actions (branch factor K), improving as K increases.  

2. **Self-Reflection (SR)**:  
   - Generates explanations for why expert actions are better than alternatives, using differences in future states.  
   - **Implementation**: Requires structured prompts to ensure logical and actionable explanations, improving strategy optimization.  

3. **Training Workflow**:  
   - Combines **expert data** and **self-generated reflections** (D_refl) for training.  
   - Balances accuracy (expert routes) and generalization (self-reflection).  

---

### **Experimental Validation**  
- **Environments Tested**: 8 diverse scenarios (e.g., WebShop, TravelPlanner, ALFWorld) and 3 model scales (3B, 70B).  
- **Metrics Evaluated**:  
  - **Effectiveness**: Early Experience outperformed imitation learning by **+9.6%** on average, with +15.0% gains in TravelPlanner (SR) and +9.6% in WebShop (IWM).  
  - **Generalization**: Early Experience recovered more performance on out-of-distribution (OOD) tasks, with some OOD gains surpassing in-distribution scores.  
  - **RL Compatibility**: Early Experience-initialized RL models outperformed imitation learning-initialized ones, maintaining a consistent lead throughout training.  

---

### **Limitations and Future Directions**  
1. **Limitations**:  
   - **Short-Sequence Focus**: Current methods are optimized for short interactions (e.g., single clicks), but long sequences (e.g., multi-step tasks) require further research.  
   - **Safety Risks**: Trial-and-error actions in risky environments (e.g., deleting files) may pose hazards, necessitating safe exploration strategies.  

2. **Future Research**:  
   - **Self-Supervised Integration**: Incorporate tasks like action consistency or state prediction to enhance environmental understanding.  
   - **Cross-Environment Transfer**: Enable knowledge migration from one environment (A) to another (B) to reduce redundant training.  
   - **Real-World Deployment**: Collect natural user interactions for continuous learning, advancing agents toward autonomous improvement.  

---

### **Conclusion and Implications**  
The "Early Experience" paradigm marks a significant step toward **autonomous AI agents** that can learn and adapt without human intervention. By combining imitation learning and reinforcement learning, it addresses critical challenges in reward-free learning and data efficiency. While practical deployment faces challenges, the research highlights the potential for AI assistants to evolve through self-reflection and trial, aligning with the vision of a "Experience Era" proposed by Sutton and others. This work paves the way for more intelligent, self-sufficient systems in real-world applications.

#### Reference: 

https://arxiv.org/pdf/2510.08558