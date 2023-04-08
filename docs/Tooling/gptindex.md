---
sidebar_position: 3
---
# [GPT Index](https://gpt-index.readthedocs.io/en/latest/)
LlamaIndex(GPT Index)是一个提供中央接口将您的LLM与外部数据连接起来的项目。

## 背景
- LLM是知识生成和推理的非凡技术，在大量公开数据上进行了预训练
- 我们如何利用我们的私人数据增强LLM的能力？
- 一种范例是上下文学习（另一种是微调），我们将上下文插入到输入提示中。这样，我们就可以利用LLM的推理能力来生成相应。

为了以高性能、高效和廉价的方式实现LLM的数据扩充，我们需要解决两个问题：
- 数据摄取（Data Ingestion）
- 数据索引（Data Indexing）

## 推荐方案
这些就是LlamaIndex可以发挥作用的地方。LlamaIndex是一个简单灵活的接口，可以连接LLM和您的外部数据。它以易于使用的方式提供了以下工具：

- 为您现有的数据源和数据格式（API、PDF、文档、SQL等）提供[数据连接器](https://llamahub.ai/)
- 为您的非结构化和结构化数据提供索引，以便与LLM一起使用。这些索引有助于抽象出上下文学习的常见样板和痛点
    - 以易于访问的格式存储上下文以便快速插入
    - 当上下文太大时解决提示词字数限制
    - 处理文本拆分
- 为用户提供查询索引（输入提示）和获得知识增强输出的界面
- 为您提供全面的工具集，权衡成本和性能

## Reference
1. https://gpt-index.readthedocs.io/en/latest/