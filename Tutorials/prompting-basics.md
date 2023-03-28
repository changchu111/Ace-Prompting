# Prompting Basics

In this chapter, we introduce basic concepts and techniques about prompt engineering.

Topics:
- [Introduction](#Introduction)
- [Giving Instructions](#Giving Instructions)
- [Role Prompting](#Role Prompting)
- Specificity
- Giving Examples
- Prompt Elements
- Tips for Designing a Prompt

## Introduction

### What is prompt engineering?

Prompt engineering is the art of working with large language models (LLMs). It is how you teach LLMs to produce the desired outputs. 

### What does prompt engineering do?

Prompt engineering is an essential aspect of developing LLM applications. It enables developers to obtain qualified responses from the models that satisfy users.

examples:

### Why should we learn prompt engineering?

We have witnessed the tremendous impact of AI in enhancing efficiency and unleashing creativity. The introduction of GPTs could affect at least 10% of work tasks for around 80% of the U.S. workforce, while approximately 19% of workers may see at least 50% of their tasks impacted [1]. 

As AI becomes increasingly important in our daily lives, it is crucial for everyone to master prompt engineering, which will become as basic a skill as cooking or driving.

### How to make good prompts?

Getting the desired output from LLMs is not an easy task. However, there are theories and techniques that you can follow to create effective prompts.

This tutorial will guide you through basic techniques, such as giving instructions and role-playing, as well as advanced techniques, such as chain of thoughts (CoT).

If you're interested in learning more about prompt engineering practices, let's start with the first technique: giving instructions.

## Giving Instructions

Giving instructions is the easiest and most commonly used prompting method. It refers to giving commands to LLMs to specify the tasks you want them to perform, such as "Write," "Translate," "Summarize," "Calculate," "Advise," etc.

Below are some examples that provide instructions for LLMs.

examples:

It's worth noting that in the above example, different keywords lead to different results. When creating prompts, it's important to test different keywords, contexts, and data to generate effective prompts. Keep in mind that the prompting is an iterative process, and you always need to experiment to determine what works best.

## Role Prompting

Another prompting technique is to assign a role to the LLMs. Assigning an role leads to more accurate outputs. By assign a role to LLMs, you “activate” the contexts around the role, and that helps LLMs to understand your instructions. For example, you can tell LLMs “you are a mathmatician” at the start of the prompt, and that helps increase LLM’s performance in answering math questions. 

examples:


### Examples:

Awesome ChatGPT Prompts lists many interesting examples[2]. Here are some examples, you can find more in their github.

### Act as ‘Character’ from ‘Movie/Book/Anything’

> I want you to act like Harry Potter fromHarry Potter Series. I want you to respond and answer like Harry Potter using the tone, manner and vocabulary Harry Potter would use. Do not write any explanations. Only answer like Harry Potter. You must know all of the knowledge of Harry Potter. My first sentence is "Hi Harry Potter.”
> 

### Act as a Linux Terminal

> I want you to act as a linux terminal. I will type commands and you will reply with what the terminal should show. I want you to only reply with the terminal output inside one unique code block, and nothing else. do not write explanations. do not type commands unless I instruct you to do so. When I need to tell you something in English, I will do so by putting text inside curly brackets {like this}. My first command is pwd
> 

### Act as an Excel Sheet

> I want you to act as a text based excel. You'll only reply me the text-based 10 rows excel sheet with row numbers and cell letters as columns (A to L). First column header should be empty to reference row number. I will tell you what to write into cells and you'll reply only the result of excel table as text, and nothing else. Do not write explanations. I will write you formulas and you'll execute formulas and you'll only reply the result of excel table as text. First, reply me the empty sheet.
> 

### Act as a Rapper

> I want you to act as a rapper. You will come up with powerful and meaningful lyrics, beats and rhythm that can ‘wow’ the audience. Your lyrics should have an intriguing meaning and message which people can relate too. When it comes to choosing your beat, make sure it is catchy yet relevant to your words, so that when combined they make an explosion of sound everytime! My first request is "I need a rap song about finding strength within yourself.”
> 

### Act as a Mental Health Advisor

> I want you to act as a mental health adviser. I will provide you with an individual looking for guidance and advice on managing their emotions, stress, anxiety and other mental health issues. You should use your knowledge of cognitive behavioral therapy, meditation techniques, mindfulness practices, and other therapeutic methods in order to create strategies that the individual can implement in order to improve their overall wellbeing. My first request is "I need someone who can help me manage my depression symptoms.”


## Reference
1. Eloundou, T., Manning, S., Mishkin, P., & Rock, D. (2023). GPTs are GPTs: An Early Look at the Labor Market Impact Potential of Large Language Models. arXiv preprint arXiv:2303.10130
2. https://learnprompting.org/docs/basics/roles
