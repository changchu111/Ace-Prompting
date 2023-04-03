# 进阶篇
在这一章节，我们介绍提示词工程的高级用法。

内容包括：
- [思维链（Chain of Thought, CoT）](#思维链)
- [零样本思维链（Zero-Shot Chain of Thought）](#零样本思维链)
- [自恰性（Self-Consistency）](#自恰性)

## 思维链
思维链（Chain of Thought, CoT）指的是导向最终答案的一系列连贯的中间推理步骤。在示例中引入思维链举例子可以显著改善大语言模型处理复杂推理任务的能力[1]。
![](../img/CoT.png)

### 任务和表现
实验表明思维链方法可以提升大语言模型在算数类、常识类、以及符号类任务的表现。

#### 算数性任务
![](../img/Examples/CoT_money.png)

#### 常识性任务
![](../img/Examples/CoT_commensense.png)

#### 符号学任务
![](../img/Examples/CoT_symbolic_false.png)
![](../img/Examples/CoT_symbolic_true.png)

### 局限
思维链是模型参数量变大涌现出的能力，也就是说，思维链并不能提升小模型的能力，当模型有100B参数是，思维链提成模型性能的作用才显现出来。

## 零样本思维链
零样本思维链（Zero-shot CoT）是在思维链方法的基础上展开的。研究者们仅仅是在提示词中加入“让我们一步一步的思考”（Let's think step by step），也能大幅提升大语言模型的能力。
![](../img/zero-shot-cot.png)

零样本思维链的原理
![](../img/how-zero-shot-cot-work.png)

### 示例
![](../img/Examples/CoT_money_zero_shot.png)

### 局限
研究者发现大语言模型会捕捉并放大训练数据中的偏差（Bias）。提示词是一种旨在利用语言模型在训练中学到的知识解决各类任务的方法，因此它也具有相同的缺点，会导致偏差。

## 自洽性
自恰性是一种改进语言模型在复杂任务上的推理表现的解码策略[3]。它将思维链中运用的贪心解码策略换成了更多样和灵活的方法。

自恰性方法的灵感来自一个想法：复杂任务常常有多种解法，人们通过不同的推理路径都可以找到最终答案。与其只考虑可能性最大的路径，不如在样本中包括多种路径，然后选择最一致的答案。这个方法允许模型像人一样有更多样的推理方法，并显著提升模型在复杂任务上的表现。

下图展示了自洽行方法和思维链方法的不同：
![](../img/self-consistency.png)

### 示例

### 结果
与思维链相比，自恰性方法在算数类、常识类和符号类任务的众多基准上都有提升，包括GSM8K（+17.9%），SVAMP（+11.0%），AQuA（+12.2%），StrategyQA（+6.4%）以及ARC-challenge（+3.9%）。

### 局限
自恰性的一个局限是它带来了更多的计算成本。在实际使用中，可以少量尝试几条路径（比如5条或者10条）来获取这一方法带来的好处，同时不会产生太多成本，因为在大多数情况下性能提升很快会放缓。

## Reference
1. Wei, J., Wang, X., Schuurmans, D., Bosma, M., Chi, E., Le, Q., & Zhou, D. (2022). Chain of thought prompting elicits reasoning in large language models. arXiv preprint arXiv:2201.11903.
2. Kojima, T., Gu, S. S., Reid, M., Matsuo, Y., & Iwasawa, Y. (2022). Large language models are zero-shot reasoners. arXiv preprint arXiv:2205.11916.
3. Wang, X., Wei, J., Schuurmans, D., Le, Q., Chi, E., & Zhou, D. (2022). Self-consistency improves chain of thought reasoning in language models. arXiv preprint arXiv:2203.11171.

[上一章节（入门应用）](prompting-basic-applications.md)

[下一章节（可靠性）](prompting-reliability.md)
