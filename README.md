# Fighting Fire with Fire: Can Language Models Detect Misinformation Better Than Customized Detectors?

## Abstract
Recent ubiquity and disruptive impacts of large language models (LLMs) have raised concerns due to their potential to be misused (i.e., generating harmful and misleading contents). In response to this challenge, we propose the Fighting Fire with Fire (F3) strategy, employing emergent abilities of LLMs to combat human-written and AI-generated misinformation through prompt engineering. First, we leverage GPT-3.5-turbo to create synthetic real and fake newsusing paraphrase-based and perturbation-based prefix-style prompts, respectively. Next, we utilize cloze-style prompts to detect synthetic and human-written real vs. fake news. Given LLMs' known propensity to hallucinate, we apply Natural Language Inference (NLI) techniques with GPT-3.5-turbo and FLAN-T5 to detect and remove hallucinated synthetic news. Finally, we observe GPT-3.5-turbo's zero-shot superiority, compared to FLAN-T5 and SOTA detectors, for both in-distribution and out-of-distribution datasets.


## Description
This repository contains the codebase and dataset for the paper "Fighting Fire with Fire: Can Language Models Detect Misinformation Better Than Customized Detectors?". The codebase will be available once accepted. 

