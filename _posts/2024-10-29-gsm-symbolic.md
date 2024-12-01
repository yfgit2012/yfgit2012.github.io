## Apple paper: GSM-Symbolic: Understanding the Limitations of Mathematical Reasoning in Large Language Models

Here is the translation of the contents:

This article describes a study in which large language models (such as Apple models) were used to standardize multiplication algorithms. Researchers helped the model break down multiplication problems into smaller tasks by providing example diagrams, and then described the multiplication algorithm as a directed graph containing basic operations such as addition and multiplication.

The results show that the model cannot generalize from small multiplication problems in the training set to larger ones, indicating that it simply memorizes answers rather than actually reasoning. When comparing the correctness rates of main problems and sub-problems, if the main problem is correct but all sub-problems are incorrect or vice versa, it means that the model does not solve math problems by reasoning.

Researchers concluded some interesting conclusions: whether large models can successfully solve a problem depends on whether they have seen related sub-problems before. In other words, large models cannot solve big problems because they can only solve parts of them. If they succeed in solving more frequent or accurate sub-problems in the training data, it means that they simply memorize answers and solve by recall.

Researchers suggest viewing large models as a search engine that first retrieves similar examples for a specific problem, then combines these approximations to form an answer. Therefore, large models achieve partial success by only completing parts of the overall problem, and more often break down problems in a more intuitive, superficial, and practical way rather than systematically thinking through the specified multiplication algorithm.

The conclusion of this study is that currently no large model can escape the problems pointed out in these papers, not even in common cases, and may not run safely at all. In some extreme cases, it's difficult to abstractly reason enough.

#### Translation 

这篇文章描述了一项研究，在该研究中，大型语言模型（如苹果模型）被用于标准乘法算法。研究者通过提供思维图示例帮助模型把乘法问题分解为更小的任务，然后将乘法算法描述为一个包含加法和乘法等基本操作的定向图。

结果显示，模型无法从训练集中的小乘法问题推广到更大的乘法问题。这表明模型仅仅通过记忆答案，而不是真正进行推理。在对比主要问题和子问题的正确率时，如果主问题答对了，但子问题全错，或反过来，则意味着模型不是通过推理解决数学题。

研究者们总结出了一些有趣的结论：大模型是否能成功解决问题取决于它们之前是否见过相关的子问题。换句话说，大模型无法解决大型问题，因为它们只能解决大型问题中的部分子问题。如果它们在解决训练数据中频率更高或者更精确的子问题上成功了，那就表明它们只是记住了答案，通过回忆的方式来解决。

研究者们建议将大模型视为一个搜索引擎，它会先召回与特定问题部分大致匹配的例子，然后再将这些近似回忆拼接起来。因此，大模型通过仅仅完成整体问题的一部分来取得部分的成功，更多的是在以自己更直觉、更肤浅、更实际的方式来分解问题，而不是系统性地思考指定的乘法算法。

这篇研究的结论是：目前市面上没有一个大模型能逃过这些论文指出的问题，即使是在常见的情况下也可能无法安全运行。在某些极端情况下，难以足够抽象地进行推理。