# 工具篇

有一些工具可以帮助你更好的开发基于大语言模型的应用，或者帮你写出更好的提示词。这一章节我们介绍这样的工具。

内容：
- [LangChain](#LangChain)
- [Dust.tt](#Dust.tt)
- [GPT Index](#GPT-Index)
- [PromptPerfect](#PromptPerfect)

## [LangChain](https://github.com/hwchase17/langchain/)
简单的调用大语言模型的API是有局限性的：

- 大语言模型无法连接到外部资源，例如搜索引擎、API以及数据库
- 大语言模型有token限制，这会让你无法为大语言模型提供足够的背景信息和数据

LangChain就是为了解决这些问题而生的。它由Robust Intelligence的前机器学习工程师Chase Harrison于2022年10月下旬推出。它是一个开源的Python库，封装了大量的LLM应用程序开发逻辑和工具集成，有潜力成为第一个被广泛认可的LLM应用程序开发框架。

随着Harrison为LangChain添加了许多实用的抽象，以及2023年1月许多项目在Hackathon上使用LangChain，它在Github上的star数目迅速超过10,000，已然成为LLM应用程序开发人员的中间件首选。

## [Dust.tt](https://dust.tt/)
Dust旨在提供一个灵活的框架来定义和部署[LLM应用程序](https://docs.dust.tt/introduction#large-language-model-apps)，而无需编写任何执行代码。它专门针对以下场景：
- 在设计LLM应用时同时处理多个示例
- 检查由LLM应用中间步骤产生的模型输出
- 通过提供细粒度和自动化的版本控制系统来迭代LLM应用设计

## [GPT Index](https://gpt-index.readthedocs.io/en/latest/)
LlamaIndex(GPT Index)是一个提供中央接口将您的LLM与外部数据连接起来的项目。

### 背景
- LLM是知识生成和推理的非凡技术，在大量公开数据上进行了预训练
- 我们如何利用我们的私人数据增强LLM的能力？
- 一种范例是上下文学习（另一种是微调），我们将上下文插入到输入提示中。这样，我们就可以利用LLM的推理能力来生成相应。

为了以高性能、高效和廉价的方式实现LLM的数据扩充，我们需要解决两个问题：
- 数据摄取（Data Ingestion）
- 数据索引（Data Indexing）

### 推荐方案
这些就是LlamaIndex可以发挥作用的地方。LlamaIndex是一个简单灵活的接口，可以连接LLM和您的外部数据。它以易于使用的方式提供了以下工具：

- 为您现有的数据源和数据格式（API、PDF、文档、SQL等）提供[数据连接器](https://llamahub.ai/)
- 为您的非结构化和结构化数据提供索引，以便与LLM一起使用。这些索引有助于抽象出上下文学习的常见样板和痛点
    - 以易于访问的格式存储上下文以便快速插入
    - 当上下文太大时解决提示词字数限制
    - 处理文本拆分
- 为用户提供查询索引（输入提示）和获得知识增强输出的界面
- 为您提供全面的工具集，权衡成本和性能

## [PromptPerfect](https://promptperfect.jina.ai/)
PromptPerfect是专门为LLM设计的提示词优化器。

PromptPerfect的工具简化了提示词工程，自动优化ChatGPT、GPT-3.5、DALL-E 2、StableDiffusion和Midjourney提示。无论您是提示工程师、内容创作者还是AI开发人员，PromptPerfect都能帮助您优化提示词。

## Reference
1. https://github.com/hwchase17/langchain/
2. https://mp.weixin.qq.com/s/3coFhAdzr40tozn8f9Dc-w
3. https://dust.tt/
4. https://gpt-index.readthedocs.io/en/latest/
5. https://promptperfect.jina.ai/

[上一章节（黑客篇）](prompting-hacking.md)

[下一章节（参考文献）](prompting-bibliography.md)
