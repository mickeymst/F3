# Fighting Fire with Fire: The Dual Role of LLMs in Crafting and Detecting Elusive Disinformation

## Abstract
Recent ubiquity and disruptive impacts of large language models (LLMs) have raised concerns about their potential to be misused (.i.e, generating large-scale harmful and misleading content). To combat this emerging risk of LLMs, we propose a novel "Fighting Fire with Fire" (F3) strategy that harnesses modern LLMs' generative and emergent reasoning capabilities to counter human-written and LLM-generated disinformation. First, we leverage GPT-3.5-turbo to synthesize authentic and deceptive LLM-generated content through paraphrase-based and perturbation-based prefix-style prompts, respectively. Second, we apply zero-shot in-context semantic reasoning techniques with cloze-style prompts to discern genuine from deceptive posts and news articles. In our extensive experiments, we observe GPT-3.5-turbo's zero-shot superiority for both in-distribution and out-of-distribution datasets, where GPT-3.5-turbo consistently achieved accuracy at 68-72%, unlike the decline observed in previous customized and fine-tuned disinformation detectors. 


## Description
This repository contains the codebase and dataset for the paper "Fighting Fire with Fire: The Dual Role of LLMs in Crafting and Detecting Elusive Disinformation".

