## Embodied AI: Systems that See, Hear, and Act in the World Alongside Humans

**Article Abstract**  
This article focuses on the development bottlenecks in the field of artificial intelligence (AI), emphasizing the limitations of large language models (LLMs) in physical world tasks, the challenges faced by L5-level autonomous driving, the root causes of AI energy consumption issues, and introducing a deep dialogue by Yann LeCun, the founder of convolutional neural networks, at the Davos Forum. Yann LeCun pointed out that the current AI technical path has fundamental flaws, such as generative models being unable to understand physical laws and the inefficiency of reinforcement learning. He proposed the "Joint Embedding Prediction Architecture" as a new paradigm, emphasizing the realization of intelligence through abstract representations and hierarchical world models, while calling for the use of video data self-supervised learning to replace text data to address the problem of missing physical common sense. The article also analyzes challenges such as hardware energy consumption and algorithm architecture optimization, and looks forward to future application scenarios of embodied intelligence (Embodied Intelligence), such as household robots, L5-level autonomous driving, and humanoid robots.

---

**Key Points Summary**  
- **Definition and Scope of Embodied Intelligence**  
  Embodied intelligence is not limited to robots and includes non-physical systems (such as industrial process optimization). Its core lies in processing high-dimensional, continuous, and noisy physical world data.  
- **Limitations of Large Language Models**  
  LLMs excel in the language domain but cannot handle uncertainties in the physical world, as they rely on discrete, symbolic rules and lack the ability to address complex real-world problems.  
- **Mistakes in the Generative AI Path**  
  Generative models (e.g., diffusion models) attempt to reconstruct details but fail to grasp physical laws, leading to short-term accuracy but long-term failure, along with high energy consumption and large training costs.  
- **Joint Embedding Prediction Architecture**  
  Prediction is achieved through abstract representation spaces, hierarchical modeling (low-level details, high-level planning), mimicking human hierarchical decision-making processes to solve the issue of current AI lacking world models.  
- **Self-Supervised Learning with Video Data**  
  Video data surpasses text data in directly training physical common sense (e.g., gravity, object permanence). Yann LeCun's team's V-JEPA 2 model validates this method by simulating the learning process of infants.  
- **Hardware and Energy Consumption Challenges**  
  Current AI hardware relies on data movement, leading to high energy consumption; new technologies such as spintronics and optical devices need to be explored to achieve low-power, high-parallel computing architectures.  
- **Optimization of Learning Paradigms**  
  Emphasizes self-supervised learning (cake body) as the core, combined with supervised learning (cream) and reinforcement learning (cherry), avoiding reliance on massive reinforcement training data.  
- **Implementation Path of Embodied Intelligence**  
  Through phased pre-training (V-JEPA 2.1) and fine-tuning, models can adapt to different environments and devices, reducing deployment costs and achieving a balance between generality and specialization.  
- **Vision for the Next AI Revolution**  
  Based on a non-generative paradigm, AI will shift from language imitation to world understanding, gaining the ability to predict the consequences of actions, driving the practical application of household robots, L5 autonomous driving, etc.

---

**References and Links**  
1. **Davos Forum Dialogue** (Yann LeCun and Mark Pfeifer discussing)  
2. **V-JEPA 2 Model** (the video self-supervised learning model developed by Yann LeCun's team)  
3. **ConvNext Research** (Soumith Chintala's paper comparing convolutional networks and Transformers)  
4. **Cake Analogy** (Yann LeCun's metaphor for the division of self-supervised, supervised, and reinforcement learning)  

(Note: The mentioned literature and model names in the text are from the article's content; actual links need to be supplemented based on specific research materials.)

#### Translation 

**文章摘要**  
本文围绕人工智能（AI）领域的发展瓶颈展开，重点探讨了大语言模型（LLM）在物理世界任务中的局限性、L5级自动驾驶的困境、AI能耗问题的根源，并引入了卷积神经网络奠基人杨立昆在达沃斯论坛的深度对话。杨立昆指出，当前AI技术路径存在根本性缺陷，如生成式模型无法理解物理规律、强化学习效率低下等。他提出“联合嵌入预测架构”作为新范式，强调通过抽象表示和分层世界模型实现智能，同时呼吁以视频数据自监督学习替代文本数据，解决物理常识缺失问题。文章还分析了硬件能耗、算法架构优化等挑战，并展望了具身智能（Embodied Intelligence）的未来应用场景，如家务机器人、L5级自动驾驶和人形机器人。

---

**关键点总结**  
- **具身智能的定义与范畴**  
  具身智能不仅限于机器人，还包括非实体系统（如工业流程优化），其核心在于处理高维、连续、带噪声的物理世界数据。  
- **大语言模型的局限性**  
  LLM在语言领域表现优异，但无法处理物理世界的不确定性，因其依赖离散、符号化的规则，缺乏对现实复杂问题的应对能力。  
- **生成式AI的路径误区**  
  生成式模型（如扩散模型）试图还原细节，但无法把握物理规律，导致预测短期精准却长期失效，且能耗高、训练成本大。  
- **联合嵌入预测架构（Joint Embedding Prediction）**  
  通过抽象表示空间进行预测，分层建模（低层细节、高层规划），模仿人类分层决策过程，解决当前AI缺乏世界模型的问题。  
- **视频数据的自监督学习**  
  视频数据优于文本数据，能直接训练物理常识（如重力、物体恒存），杨立昆团队的V-JEPA 2模型通过模拟婴儿学习过程验证了这一方法。  
- **硬件与能耗挑战**  
  当前AI硬件依赖数据搬运，能耗高；需探索自旋电子学、光学器件等新型技术，以实现低功耗、高并行的计算架构。  
- **学习范式的优化**  
  强调自监督学习（蛋糕主体）为核心，结合有监督学习（奶油）和强化学习（樱桃），避免依赖海量强化训练数据。  
- **具身智能的落地路径**  
  通过分阶段预训练（V-JEPA 2.1）和微调，使模型适应不同环境和设备，降低部署成本，实现通用性与专用性的结合。  
- **未来AI革命的愿景**  
  基于非生成式范式，AI将从语言模仿转向世界理解，具备预测行为后果的能力，推动家务机器人、L5自动驾驶等应用落地。  

---

**参考文献与链接**  
1. **达沃斯论坛对话**（杨立昆与马克·波莱菲斯讨论）  
2. **V-JEPA 2模型**（杨立昆团队开发的视频自监督学习模型）  
3. **ConvNext研究**（Soumith Chintala关于卷积网络与Transformer性能对比的论文）  
4. **蛋糕类比**（杨立昆提出的自监督、有监督、强化学习的分工模型）  

（注：文中提及的文献和模型名称为文章内容，实际链接需根据具体研究资料补充。）

#### Reference: 

https://www.youtube.com/watch?v=pJyoqapCRZE