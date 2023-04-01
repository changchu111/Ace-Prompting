# Tooling

There are some tools that can help you with LLM application development and prompting. This section introduces such tools.

Topics:

- [LangChain](#LangChain)
- [Dust.tt](#Dust.tt)
- [GPT Index](#GPT-Index)
- [PromptPerfect](#PromptPerfect)

## [LangChain](https://github.com/hwchase17/langchain/)
Simply calling LLM APIs has limitations:

- LLMs are unable to connect to external resources, such as search engines, APIs, or databases.
- LLMs have token limits (4096 for ChatGPT) that prevent you from providing sufficient context or data for the LLM to work with.

LangChain was launched to solve these problems. It is launched by Chase Harrison, a former machine learning engineer at Robust Intelligence, in late October 2022. It is an open-source Python library that encapsulates a large amount of LLM application development logic and tool integration. It has the potential to become the first widely recognized LLM application development framework.

With Harrison adding many practical abstractions to LangChain, and many AI Hackathon finalist projects using LangChain in January 2023, its Github stars quickly exceeded 10,000. It has become the first choice for LLM application developers when choosing middleware.

## [Dust.tt](https://dust.tt/)

Dust is designed to provide a flexible framework to define and deploy **[large language model apps](https://docs.dust.tt/introduction#large-language-model-apps)** without having to write any execution code. It is specifically intended to ease:

- Working on multiple examples at the same time while designing a large language model app.
- Introspecting model outputs produced by intermediary steps of large language model apps.
- Iterating on the design of large language model apps by providing a granular and automated versioning system.

## [GPT Index](https://gpt-index.readthedocs.io/en/latest/)
LlamaIndex (GPT Index) is a project that provides a central interface to connect your LLM’s with external data.

### **Context**

- LLMs are a phenomenonal piece of technology for knowledge generation and reasoning. They are pre-trained on large amounts of publicly available data.
- How do we best augment LLMs with our own private data?
- One paradigm that has emerged is *in-context* learning (the other is finetuning), where we insert context into the input prompt. That way, we take advantage of the LLM’s reasoning capabilities to generate a response.

To perform LLM’s data augmentation in a performant, efficient, and cheap manner, we need to solve two components:

- Data Ingestion
- Data Indexing

### **Proposed Solution**

That’s where the **LlamaIndex** comes in. LlamaIndex is a simple, flexible interface between your external data and LLMs. It provides the following tools in an easy-to-use fashion:

- Offers [data connectors](http://llamahub.ai/) to your existing data sources and data formats (API’s, PDF’s, docs, SQL, etc.)
- Provides **indices** over your unstructured and structured data for use with LLM’s. These indices help to abstract away common boilerplate and pain points for in-context learning:
    - Storing context in an easy-to-access format for prompt insertion.
    - Dealing with prompt limitations (e.g. 4096 tokens for Davinci) when context is too big.
    - Dealing with text splitting.
- Provides users an interface to **query** the index (feed in an input prompt) and obtain a knowledge-augmented output.
- Offers you a comprehensive toolset trading off cost and performance.

## [PromptPerfect](https://promptperfect.jina.ai/)

PromptPerfect is a cutting-edge prompt optimizer designed for large language models (LLMs), large models (LMs) and LMOps.

Prompt engineering can be tough - a perfect prompt is the key for great AI-generated content. But don't worry, PromptPerfect has got you covered! Our cutting-edge tool streamlines prompt engineering, automatically optimizing your prompts for ChatGPT, GPT-3.5, DALL-E 2, StableDiffusion and MidJourney. Whether you're a prompt engineer, content creator, or AI developer, PromptPerfect makes prompt optimization easy and accessible. With its intuitive interface and powerful features, PromptPerfect unlocks the full potential of LLMs and LMs, delivering top-quality results every time. Say goodbye to subpar AI-generated content and hello to prompt perfection with PromptPerfect!
