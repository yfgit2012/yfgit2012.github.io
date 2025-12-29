## LangChain 2025 report

### AI Agent Development Status and Trend Summary

#### I. Enterprise Deployment Status
1. **Model Selection and Multi-Model Strategy**
   - **Mainstream Models**: OpenAI's GPT series (67.8%) dominates, but enterprises widely adopt multi-model strategies (>75%) to balance performance, cost, compliance, etc.
   - **Other Models**: Google Gemini (37.4%), Anthropic Claude (36.6%), open-source models (34.2%), etc., are supplementary choices, especially in industries with high data residency requirements (e.g., finance, healthcare), where locally deployed open-source models are preferred.
   - **Low Fine-Tuning Usage**: Only 13.8% of enterprises extensively use fine-tuned models in production due to high fine-tuning thresholds (require annotated data, training resources) and limited ROI.

2. **Model Deployment Methods**
   - **Self-Built Models**: About a third of enterprises choose self-built models, mainly for cost optimization (high usage scenarios), data compliance (cross-border data restrictions), and customization needs.
   - **Commercial API Dependence**: Although convenient, some enterprises shift to self-built models due to compliance or customization requirements.

3. **Evaluation and Testing Practices**
   - **Offline Evaluation Dominates**: 52.4% of enterprises perform offline evaluation on test sets, 37.3% conduct online evaluation based on production data.
   - **Hybrid Evaluation Model**: Nearly a quarter of teams combine offline and online evaluation to cover validation needs across development and production stages.
   - **Innovative Evaluation Metrics**: Human review (59.8%) and large language model judges (53.3%) have become mainstream, while traditional NLP metrics (e.g., similarity) are marginalized due to low applicability in open-ended scenarios.

#### II. Personal Usage Trends
1. **Coding Agent Dominates Development Processes**
   - **High-Frequency Tools**: Claude Code (120+ mentions), Cursor (110+), GitHub Copilot (80+), etc., have become essential tools for developers, covering code generation, debugging, test case writing, etc.
   - **Efficiency Gains**: Significantly shorten development cycles and reduce code error rates.

2. **Research-Driven Agent Enhances Knowledge Exploration**
   - **Tool Application**: ChatGPT, Claude, Gemini, Perplexity, etc., are used for long-document summarization, cross-source information integration, and technical document retrieval.
   - **Collaboration with Coding Agents**: Developers often first use research agents to gather technical resources before employing coding tools to implement functionalities.

3. **Customized Agents Rise**
   - **Scenario-Specific Customization**: Enterprises build internal agents using LangChain/LangGraph, such as QA engineers' automated testing agents or customer service knowledge base query agents, precisely matching business needs.
   - **Limitations**: Some users still rely on basic model chatting or coding assistance, not expanding into complex scenarios, indicating that "agentifying everything" remains in its early stages.

#### III. Technical Challenges and Future Directions
1. **Reconstructing Evaluation Systems**
   - The open-ended interaction of AI agents (e.g., creative generation, tone adaptation) relies on human review, making traditional NLP metrics unsuitable and driving evaluation standards toward human-machine integration.

2. **Balancing Cost and Compliance**
   - Enterprises must balance performance, cost, and compliance in multi-model strategies, especially in data-sensitive sectors, where local deployment becomes a critical choice.

3. **Deepening Customization Capabilities**
   - Lightweight optimization solutions based on prompt engineering and retrieval-augmented generation (RAG) are more favored compared to fine-tuning, offering better cost-effectiveness.

#### IV. Data Sources and Sample Bias
- **Survey Scope**: A public survey in November-December 2025 with 1,340 valid responses, covering enterprises of different sizes across tech, finance, healthcare, and other industries.
- **Sample Limitations**: Respondents predominantly come from the LangChain ecosystem, potentially leading to higher awareness of agent engineering than industry averages, with some data (e.g., LangChain/LangGraph adoption rates) showing bias.

### Summary
Currently, AI agents have formed a mature ecosystem in enterprises, characterized by multi-model collaboration, self-built deployment, and hybrid evaluation, simultaneously driving efficiency improvements in coding, research, and other scenarios. However, innovation in evaluation systems, balancing cost and compliance, and deepening customization capabilities remain core challenges. Looking ahead, with technological advancements and expanded applications, AI agents are expected to further penetrate more domains, but potential biases in samples should be cautiously addressed.

#### Translation 

### AI Agent发展现状与趋势总结

#### 一、企业层面的部署情况
1. **模型选择与多模型策略**  
   - **主流模型**：OpenAI的GPT系列（67.8%）占据主导地位，但企业普遍采用多模型策略（>75%），以平衡性能、成本、合规性等需求。  
   - **其他模型**：谷歌Gemini（37.4%）、Anthropic Claude（36.6%）、开源模型（34.2%）等成为补充选择，尤其在数据驻留要求高的行业（如金融、医疗）中，本地化部署的开源模型更受青睐。  
   - **微调使用率低**：仅13.8%的企业在生产中广泛使用微调模型，因微调门槛高（需标注数据、训练资源）且ROI有限。

2. **模型部署方式**  
   - **自建模型**：约三分之一企业选择自建模型，主要出于成本优化（高使用量场景）、数据合规（跨境数据限制）和定制化需求。  
   - **商业API依赖**：尽管便捷，但部分企业因合规或定制需求转向自建。

3. **评估与测试实践**  
   - **离线评估为主**：52.4%的企业在测试集上进行离线评估，37.3%基于生产数据进行在线评估。  
   - **混合评估模式**：近四分之一团队结合离线与在线评估，以覆盖开发与生产阶段的验证需求。  
   - **评估指标创新**：人工审核（59.8%）和大语言模型裁判（53.3%）成为主流，传统NLP指标（如相似度）因开放性场景适用性低而被边缘化。

#### 二、个人使用趋势
1. **Coding Agent主导开发流程**  
   - **高频工具**：Claude Code（120+提及）、Cursor（110+）、GitHub Copilot（80+）等成为开发者必备工具，覆盖代码生成、调试、测试用例编写等场景。  
   - **效率提升**：显著缩短开发周期，降低代码错误率。

2. **研究型Agent助力知识探索**  
   - **工具应用**：ChatGPT、Claude、Gemini、Perplexity等被用于长文档总结、跨源信息整合、技术文档检索等任务。  
   - **与Coding Agent协同**：开发者常先通过研究Agent获取技术资料，再用编码工具实现功能。

3. **自定义Agent兴起**  
   - **场景化定制**：企业基于LangChain/LangGraph构建内部Agent，如QA工程师的自动化测试Agent、客服的知识库查询Agent等，精准匹配业务需求。  
   - **局限性**：部分用户仍依赖基础模型聊天或编码辅助，未拓展至复杂场景，表明“代理化一切”仍处于早期阶段。

#### 三、技术挑战与未来方向
1. **评估体系重构**  
   - AI Agent的开放性交互（如创意生成、语气适配）需依赖人工审核，传统NLP指标难以适用，推动评估标准向人机结合方向演进。

2. **成本与合规平衡**  
   - 企业需在多模型策略中权衡性能、成本与合规性，尤其在数据敏感领域，本地化部署成为关键选择。

3. **自定义能力深化**  
   - 基于提示工程和检索增强生成（RAG）的轻量级优化方案更受青睐，相比微调更具性价比。

#### 四、数据来源与样本偏差
- **调查范围**：2025年11-12月的公开调查，共1340份有效回复，覆盖科技、金融、医疗等行业的不同规模企业。  
- **样本局限性**：受访者多来自LangChain生态，可能对代理工程认知度高于行业平均水平，部分数据（如LangChain/LangGraph采用率）存在偏差。

### 总结
当前AI Agent在企业中已形成多模型协作、自建部署与混合评估的成熟生态，同时推动编码、研究等场景的效率提升。然而，评估体系创新、成本合规平衡及自定义能力深化仍是核心挑战。未来，随着技术迭代与场景拓展，AI Agent有望进一步渗透至更多领域，但需警惕样本偏差对结论的潜在影响。

#### Reference: 

https://www.langchain.com/state-of-agent-engineering