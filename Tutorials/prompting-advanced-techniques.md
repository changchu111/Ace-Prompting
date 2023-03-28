# Advanced Techniques

## Chain of Thought

Chain of Thought (CoT) refers to a coherent series of intermediate reasoning steps that lead to the final answer for a problem. Including chain-of-thought reasoning in the exemplars for few-shot prompting can significantly improve the ability of large language models to perform complex reasoning.

### Tasks and Performance

Experiments has shown that chain-of-thought prompting improves performance on a range of arithmetic, commonsense, and symbolic reasoning tasks.

#### Arithmetic Task

#### Commonsense Task

#### Symbolic Task

### Limitations

Chain-of-thought prompting is an emergent ability of model scale. That is, chain-of-though prompting does not positively impact performance for small models, and only yields performance gains when used with models of ~100B parameters.

## Zero Shot Chain of Thought

## Reference
1. Wei, J., Wang, X., Schuurmans, D., Bosma, M., Chi, E., Le, Q., & Zhou, D. (2022). Chain of thought prompting elicits reasoning in large language models. arXiv preprint arXiv:2201.11903.
