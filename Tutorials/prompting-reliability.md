# Reliability
We’ve learned prompting techniques to get more accurate responses from LLMs. Sometimes, there are reliability issues in LLM responses, such as factuality, biases, calibration, math, etc. This section introduces techniques to make LLMs reliable.

Topics:
- [Factuality](#Factuality)
- [Biases](#Biases)
- Calibration
- Math

## Factuality

LLMs tend to generate responses that sound coherent and convincing but can sometimes make things up. Prompt engineering can be used to guide LLMs to generate more factual responses and avoid fabrication.

Effective ways to improve response factuality:

- Providing ground truth context, e.g., Wikipedia paragraph
- Including examples: questions LLMs can answer and questions LLMs cannot.  For those LLMs cannot answer, configure the response to instruct LLMs to admit they don’t know the answer (e.g., replying “I don’t know”).

### Examples

参考prompt engineering guide

## Biases


[Previous Section (Basic Application)](prompting-advanced-techniques.md)

[Next Section (Reliability)](prompting-image-prompting.md)
