## Defeating Nondeterminism in LLM Inference

<think>
Okay, I need to process this article and create a summary. Let me start by reading through the document carefully. The article is about why large models sometimes give different outputs even when the input is the same and the random seed is fixed. The main focus is on the issue of non-determinism in model inference.

The key points mentioned are the research by Thinking Machines Lab, led by Mira Murati. They identified that the root cause is "batch invariance missing" due to floating-point non-associativity. Different batch sizes during inference lead to varying results because the order of operations in matrix multiplications and other operations changes. The solutions involve making the kernel operations batch-invariant, like RMSNorm, matrix multiplication, and attention mechanisms, by fixing the reduction order regardless of batch size. This ensures consistent outputs. They tested this with a model, and the results were consistent across 1000 samples. The implications include enabling online policy reinforcement learning and improving reliability in critical areas like finance and healthcare.

Now, I need to summarize this in the same language as the article, which is Chinese, keeping it within 50% of the original length. The summary should be in a few paragraphs, followed by key points. I should avoid any preambles and stick strictly to the content. Let me make sure I don't include any extra information and that the summary is concise. Also, the key points need to be bullet points. Let me check the original text again to ensure I haven't missed any critical details. Yes, the main elements are the problem, the research team, the cause, the solutions, the experiments, and the implications. I'll structure the summary and key points accordingly.
</think>

**总结：**  
大模型在输入相同且随机种子固定的情况下仍可能输出不一致，主要源于推理过程中的“批次不一致性”问题。Thinking Machines Lab（由Mira Murati领导）发现，浮点数的非结合性导致不同批次大小下数值计算顺序变化，从而引发输出差异。他们通过固定操作顺序（如RMSNorm、矩阵乘法、注意力机制）实现“批次不变内核”，确保结果可重复。实验表明，该方案在保持性能可接受的前提下（如推理速度下降约2倍但优化后可控），可彻底消除非确定性，为强化学习在线策略、金融、医疗等场景提供可靠性保障。研究还揭示了“联结主义”（Connectionism）的学术背景，强调底层计算确定性对AI技术发展的重要性。

**关键点：**  
1. **问题根源**：浮点数非结合性导致不同批次大小下数值计算顺序变化，引发输出不一致。  
2. **解决方案**：  
   - 固定RMSNorm、矩阵乘法、注意力机制的归约顺序，确保批次不变。  
   - 优化内核配置（如禁用Split-K策略、固定张量指令尺寸）。  
3. **实验验证**：  
   - 使用Qwen3-235B模型测试，启用批次不变内核后1000次采样结果完全一致。  
   - 强化学习中，无批次不变内核时训练崩溃，启用后奖励稳定性显著提升。  
4. **应用价值**：  
   - 支持在线策略强化学习，提升AI在金融、医疗等领域的可靠性。  
   - 为AI“可重复性”提供科学方案，弥补性能与严谨性之间的平衡。  
5. **学术背景**：  
   - “联结主义”（Connectionism）是1980年代AI子领域，旨在模拟人脑神经网络，与Thinking Machines Lab的使命契合。</document>

#### Translation 

<think>
Okay, I need to process this article and create a summary. Let me start by reading through the document carefully. The article is about why large models sometimes give different outputs even when the input is the same and the random seed is fixed. The main focus is on the issue of non-determinism in model inference.

The key points mentioned are the research by Thinking Machines Lab, led by Mira Murati. They identified that the root cause is "batch invariance missing" due to floating-point non-associativity. Different batch sizes during inference lead to varying results because the order of operations in matrix multiplications and other operations changes. The solutions involve making the kernel operations batch-invariant, like RMSNorm, matrix multiplication, and attention mechanisms, by fixing the reduction order regardless of batch size. This ensures consistent outputs. They tested this with a model, and the results were consistent across 1000 samples. The implications include enabling online policy reinforcement learning and improving reliability in critical areas like finance and healthcare.

Now, I need to summarize this in the same language as the article, which is Chinese, keeping it within 50% of the original length. The summary should be in a few paragraphs, followed by key points. I should avoid any preambles and stick strictly to the content. Let me make sure I don't include any extra information and that the summary is concise. Also, the key points need to be bullet points. Let me check the original text again to ensure I haven't missed any critical details. Yes, the main elements are the problem, the research team, the cause, the solutions, the experiments, and the implications. I'll structure the summary and key points accordingly.
</think>

**总结：**  
大模型在输入相同且随机种子固定的情况下仍可能输出不一致，主要源于推理过程中的“批次不一致性”问题。Thinking Machines Lab（由Mira Murati领导）发现，浮点数的非结合性导致不同批次大小下数值计算顺序变化，从而引发输出差异。他们通过固定操作顺序（如RMSNorm、矩阵乘法、注意力机制）实现“批次不变内核”，确保结果可重复。实验表明，该方案在保持性能可接受的前提下（如推理速度下降约2倍但优化后可控），可彻底消除非确定性，为强化学习在线策略、金融、医疗等场景提供可靠性保障。研究还揭示了“联结主义”（Connectionism）的学术背景，强调底层计算确定性对AI技术发展的重要性。

**关键点：**  
1. **问题根源**：浮点数非结合性导致不同批次大小下数值计算顺序变化，引发输出不一致。  
2. **解决方案**：  
   - 固定RMSNorm、矩阵乘法、注意力机制的归约顺序，确保批次不变。  
   - 优化内核配置（如禁用Split-K策略、固定张量指令尺寸）。  
3. **实验验证**：  
   - 使用Qwen3-235B模型测试，启用批次不变内核后1000次采样结果完全一致。  
   - 强化学习中，无批次不变内核时训练崩溃，启用后奖励稳定性显著提升。  
4. **应用价值**：  
   - 支持在线策略强化学习，提升AI在金融、医疗等领域的可靠性。  
   - 为AI“可重复性”提供科学方案，弥补性能与严谨性之间的平衡。  
5. **学术背景**：  
   - “联结主义”（Connectionism）是1980年代AI子领域，旨在模拟人脑神经网络，与Thinking Machines Lab的使命契合。

#### Reference: 

https://thinkingmachines.ai/blog/defeating-nondeterminism-in-llm-inference/