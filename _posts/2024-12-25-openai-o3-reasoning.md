## OpenAI o3 model for reasoning

Here is the translation of the contents into English, excluding preambles and other contents:

This article discusses ChatGPT UI, o3-mini, and recent updates from OpenAI.

The author first mentions developing a ChatGPT UI that sends requests to call APIs and converse with themselves. The author then used o3-mini to write and execute a script within this UI, which correctly returned a value of 61.62%, similar to the formal evaluation results. Additionally, the low reasoning ability model ran extremely fast, completing the entire evaluation process in just one minute.

The author also mentions that OpenAI has opened up access to o3 and is now allowing security researchers to access it, with an application deadline of January 10th. In their official blog, OpenAI revealed more technical details about the new alignment strategy used by o3.

The author notes that modern large language models typically use supervised fine-tuning (SFT) and human feedback-based reinforcement learning (RLHF) for security training, but still have many security vulnerabilities. According to OpenAI researchers, these failures are due to two limitations: one, the model must respond immediately to user requests, leaving insufficient time for complex and edge-case reasoning; two, large models infer desired behavior from a vast number of labeled samples indirectly, rather than directly learning basic safety standards from natural language.

Finally, the author mentions OpenAI's new training method, Deliberative Alignment (DA), which combines process- and result-based supervision to let large models reason about security rules explicitly before generating answers. This approach overcomes the aforementioned limitations by involving the reasoning of safety norms in learning directly and allowing the model to better understand and apply security knowledge more effectively than other optimization strategies.

#### Translation 

这篇文章介绍了ChatGPT UI、o3-mini和OpenAI最近的一些动态。

首先，作者提到了自己开发的一个ChatGPT UI，通过发送请求来调用API与自己对话，然后让o3-mini在这个UI中编写并且执行一个脚本。结果脚本正确返回了61.62%的数值，与正式的评估结果相近。此外，这个低推理能力的模型运行极快，整个评估过程只用了一分钟。

接着，作者提到了OpenAI开放了o3的访问权限，并且已经开始向安全研究人员开放了o3的访问权限。申请截止日期是1月10日。在官方博客中，OpenAI还透露了o3使用的、新的对齐策略的更多技术细节。

作者也介绍了现代大语言模型基本都会使用监督微调（SFT）和基于人类反馈的强化学习（RLHF）来进行安全训练，但是仍然存在很多安全缺陷。OpenAI研究人员认为，这些失败是由于两个限制造成的：一、模型必须立即响应用户的请求，导致没有足够时间来推理复杂和边缘的安全场景；二、大模型必须从大量标注样本中间接推断出所需的行为，而不是直接学习自然语言中的基本安全标准。

最后，作者提到了OpenAI提出的审议对齐（Deliberative Alignment）的新训练方法。结合基于过程和结果的监督，让大模型在产生答案之前明确地通过安全规范来进行复杂推理，从而克服前面说的两个问题。这比其他优化响应的策略更有效，因为它直接涉及对学习的安全规范的推理，并且可以让模型更好地理解和应用安全知识。