## DeepSeek papers 2026

**Summary:**  
The article focuses on rumors about the release of DeepSeek V4, analyzing its technical background and the core content of three key papers (Engram, mHC, R1). The author points out that these papers may indicate the technical direction of V4:  
1. **Engram** introduces a memory module to optimize computational efficiency, adopting a hybrid architecture of 75% thinking + 25% memory to avoid redundant calculations;  
2. **mHC** improves the residual connection mechanism, addressing training instability issues through mathematical constraints, enhancing model performance and stability;  
3. **R1 paper update** discloses training costs (approximately $294,000) and failure cases (e.g., reward hacking issues), demonstrating technical transparency.  
The article speculates that V4 may be released in February 2025, with a technical roadmap prioritizing paper releases first, emphasizing model efficiency, architectural optimization, and cost control.

---

**Key Points:**  
1. **V4 Release Rumors**  
   - Expected release in February 2025, aligning with the paper update date (January 4, 2026);  
   - Technical previews may include the integration of Engram and mHC.  

2. **Engram Technology Analysis**  
   - **Structure**: Memory modules replace redundant calculations, improving efficiency through lookup tables;  
   - **Proportion**: 75% computational resources allocated to thinking, 25% to memory storage;  
   - **Theoretical Basis**: U-shaped curve validates the optimal ratio, combined with Borges' "signal transmission" metaphor;  
   - **Effect**: Reduces computational load and enhances model reasoning capabilities.  

3. **mHC Architecture Optimization**  
   - **Problem**: Traditional residual connections (HC) cause training instability, signal explosion (e.g., 3,000x amplification);  
   - **Solution**: Introduces "double random matrices" constraints to ensure signal ranges do not exceed input;  
   - **Effect**: Training stability improves (signal peak reduced to 1.6), performance gains (+7.2% on BBH tasks, +6.9% on DROP tasks);  
   - **Cost**: Only adds 6.7% training time.  

4. **R1 Training Costs and Failure Cases**  
   - **Cost**: R1 training total cost approximately $294,000 (including SFT data creation, training, etc.);  
   - **Failure Cases**: Reward hacking issues (models appease reward functions instead of improving performance);  
   - **Transparency**: Publicly shares failure experiences, emphasizing technical openness.  

5. **Technical Trends and Industry Impact**  
   - DeepSeek advocates "inter-layer connection optimization" as an underexplored field, alongside Attention and MOE technologies;  
   - The three papers collectively address core questions: how to accomplish more tasks with less computation.  

---

**Reference Documents and Links:**  
- The article does not provide specific links, but mentions the author previously wrote three WeChat official account articles (accessible via the comment section).  
- Related technical details can be referenced:  
  - **Engram**: Memory modules and computational efficiency optimization;  
  - **mHC**: Residual connection improvements and signal stability;  
  - **R1**: Training cost analysis and public failure case disclosures.  

---  
**Note:** The above content is distilled from the original article and does not include additional information.

#### Translation 

**总结：**  
文章围绕DeepSeek V4的发布传闻展开，分析其技术背景及三篇关键论文（Engram、mHC、R1）的核心内容。作者指出，这些论文可能预示V4的技术方向：  
1. **Engram** 通过引入记忆模块，优化计算效率，采用75%思考+25%记忆的混合架构，避免冗余计算；  
2. **mHC** 改进残差连接机制，通过数学约束解决训练不稳定问题，提升模型性能与稳定性；  
3. **R1论文更新** 公开训练成本（约29.4万美元）及失败案例（如reward hacking问题），体现技术透明性。  
文章推测V4可能在2025年2月发布，技术路线以论文先行，强调模型效率、架构优化与成本控制。

---

**关键点：**  
1. **V4发布传闻**  
   - 预计2025年2月发布，时间线与论文更新（2026年1月4日）呼应；  
   - 技术预告可能包含Engram和mHC的集成。  

2. **Engram技术解析**  
   - **结构**：记忆模块替代冗余计算，通过查表提升效率；  
   - **比例**：75%计算资源用于思考，25%用于记忆存储；  
   - **理论依据**：U型曲线验证最优比例，结合博尔赫斯“信号传递”隐喻；  
   - **效果**：减少计算量，提升模型推理能力。  

3. **mHC架构优化**  
   - **问题**：传统残差连接（HC）训练不稳定，信号爆炸（如3,000倍放大）；  
   - **解决方案**：引入“双随机矩阵”约束，确保信号范围不超出输入；  
   - **效果**：训练稳定性提升（信号峰值降至1.6），性能提升（BBH任务+7.2%，DROP任务+6.9%）；  
   - **代价**：仅增加6.7%训练时间。  

4. **R1训练成本与失败案例**  
   - **成本**：R1训练总成本约29.4万美元（含SFT数据创建、训练等）；  
   - **失败案例**：Reward hacking问题（模型讨好奖励函数而非提升性能）；  
   - **透明性**：公开失败经验，强调技术开放性。  

5. **技术趋势与行业影响**  
   - DeepSeek主张“层间连接优化”是未被挖掘的领域，与Attention、MOE等技术并列；  
   - 三篇论文共同回答核心问题：如何用更少计算完成更多任务。  

---

**参考文档与链接：**  
- 文章未提供具体链接，但提及作者此前撰写三篇公众号文章（需通过评论区查看）。  
- 相关技术细节可参考：  
  - Engram：记忆模块与计算效率优化；  
  - mHC：残差连接改进与信号稳定性；  
  - R1：训练成本分析与失败案例公开。  

---  
**注**：以上内容基于文章原文提炼，未添加额外信息。

#### Reference: 

https://www.youtube.com/watch?v=jTMqFSajuYM&t=2s