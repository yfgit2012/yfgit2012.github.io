## Deepseek-OCR2

**Article Summary**  
This article introduces the technical report on DeepSeek-OCR 2 released by the DeepSeek team, which proposes an innovative method called "Visual Causal Flow" aimed at addressing the inefficiency of traditional visual models in processing structured images such as tables and formulas. By applying the language model architecture to the visual encoder and introducing a causal attention mechanism, DeepSeek-OCR 2 significantly improves performance on the OmniDocBench benchmark test while optimizing the efficiency of visual information compression and reorganization. This method not only enhances the effectiveness of OCR tasks but also provides new insights for the unified architecture design of future multimodal models.

---

**Key Points Summary**  
- **Limitations of Traditional Visual Models**  
  Traditional models process images using a raster scan approach, ignoring the semantic logical structure of images, leading to inefficiency in handling structured data such as documents and tables.  
- **Concept of Visual Causal Flow**  
  DeepSeek-OCR 2 proposes reconstructing visual information through causal reasoning, enabling the model to parse visual data like humans by following semantic logic rather than pixel positions.  
- **Innovation of DeepEncoder V2 Architecture**  
  - Abandoning traditional CLIP/ViT structures, adopting a small language model as the visual encoder.  
  - Introducing "Causal Flow Query" (Causal Flow Query), dynamically capturing visual information through causal attention mechanisms.  
  - Achieving a 16x token compression rate, controlling visual token numbers within 256-1120, significantly reducing computational costs.  
- **Three-Stage Training Process**  
  1. **Encoder Pretraining**: Training the model to learn visual rules and optimize the semantic reorganization capability of causal query tokens.  
  2. **Query Enhancement**: Jointly optimizing the encoder and decoder to improve alignment between visual features and the language model's semantic space.  
  3. **Decoder Specialized Training**: Freezing the encoder to strengthen the model's transcription capabilities for text, formulas, and tables.  
- **Performance Improvements and Challenges**  
  - In the OmniDocBench v1.5 test, the total score increased to 91.09%, and the reading order metric (R-order) dropped to 0.057.  
  - Limitations remain, such as higher edit distance for newspaper-like text (0.13), requiring additional local view samples.  
- **Practical Application Value**  
  - Reducing OCR repetition rate (from 6.25% to 4.17%) and improving production environment stability.  
  - Providing a paradigm for multimodal model design, potentially enabling cross-modal fusion through unified encoders and diverse queries in the future.  

---

**References and Links**  
- **OmniDocBench v1.5**: Document parsing benchmark test (no specific link provided).  
- **DeepSeek-OCR 2 Paper**: No specific URL mentioned; obtain through the DeepSeek official channel.  
- **DeepEncoder V2 Architecture**: Design of a visual encoder based on a Transformer language model.

#### Translation 

**文章摘要**  
本文介绍了DeepSeek团队发布的DeepSeek-OCR 2技术报告，提出了一种名为“视觉因果流”（Visual Causal Flow）的创新方法，旨在解决传统视觉模型在处理结构化图像（如表格、公式）时的效率问题。通过将语言模型架构应用于视觉编码器，并引入因果注意力机制，DeepSeek-OCR 2在OmniDocBench基准测试中显著提升了性能，同时优化了视觉信息的压缩与重组效率。该方法不仅改进了OCR任务的效果，还为未来多模态模型的统一架构设计提供了新思路。

---

**关键点总结**  
- **传统视觉模型的局限性**  
  传统模型采用光栅扫描方式处理图像，忽略图像的语义逻辑结构，导致在处理文档、表格等结构化数据时效率低下。  
- **视觉因果流（Visual Causal Flow）概念**  
  DeepSeek-OCR 2提出通过因果推理重构视觉信息，使模型能像人类一样根据语义逻辑而非像素位置进行视觉解析。  
- **DeepEncoder V2架构创新**  
  - 弃用传统CLIP/ViT结构，改用小型语言模型作为视觉编码器。  
  - 引入“因果流查询”（Causal Flow Query），通过因果注意力机制动态抓取视觉信息。  
  - 实现16倍的Token压缩率，将视觉Token数量控制在256-1120范围内，显著降低计算成本。  
- **三阶段训练流程**  
  1. **编码器预训练**：训练模型学习视觉规则，优化因果查询Token的语义重组能力。  
  2. **查询增强**：联合优化编码器与解码器，提升视觉特征与语言模型语义空间的对齐。  
  3. **解码器专项训练**：冻结编码器，强化模型对文字、公式、表格的转写能力。  
- **性能提升与挑战**  
  - 在OmniDocBench v1.5测试中，总分提升至91.09%，阅读顺序指标（R-order）下降至0.057。  
  - 仍存在局限，如报纸类文本的编辑距离较高（0.13），需增加局部视图样本。  
- **实际应用价值**  
  - 降低OCR重复率（从6.25%降至4.17%），提升生产环境稳定性。  
  - 为多模态模型设计提供范式，未来可能通过统一编码器与不同Query实现跨模态融合。  

---

**参考文献与链接**  
- **OmniDocBench v1.5**：文档解析基准测试（未提供具体链接）。  
- **DeepSeek-OCR 2论文**：未提及具体URL，需通过DeepSeek官方渠道获取。  
- **DeepEncoder V2架构**：基于Transformer语言模型的视觉编码器设计。

#### Reference: 

https://github.com/deepseek-ai/DeepSeek-OCR-2/blob/main/DeepSeek_OCR2_paper.pdf