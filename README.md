# Fighting Fire with Fire: The Dual Role of LLMs in Crafting and Detecting Elusive Disinformation

## Abstract
Recent ubiquity and disruptive impacts of large language models (LLMs) have raised concerns about their potential to be misused (i.e., generating large-scale harmful and misleading content). To combat this emerging risk of LLMs, we propose a novel "Fighting Fire with Fire" (F3) strategy that harnesses modern LLMs' generative and emergent reasoning capabilities to counter human-written and LLM-generated disinformation. First, we leverage GPT-3.5-turbo to synthesize authentic and deceptive LLM-generated content through paraphrase-based and perturbation-based prefix-style prompts, respectively. Second, we apply zero-shot in-context semantic reasoning techniques with cloze-style prompts to discern genuine from deceptive posts and news articles. In our extensive experiments, we observe GPT-3.5-turbo's zero-shot superiority for both in-distribution and out-of-distribution datasets, where GPT-3.5-turbo consistently achieved accuracy at 68-72%, unlike the decline observed in previous customized and fine-tuned disinformation detectors. 


## Description
This repository contains the codebase and dataset for the paper "Fighting Fire with Fire: The Dual Role of LLMs in Crafting and Detecting Elusive Disinformation."

## Code
The codebase repo folder consists of three Jupyter Notebooks that can be easily run through Google Colab: F3 Data Generation IPYNB, F3 Data Generation IPYNB, and PURIFY Framework IPYNBs

### F3 Data Generation IPYNB
This Jupyter Notebook provides code for generating synthetic text data using OpenAI's GPT-3.5 Turbo language model. It focuses on creating fake news articles and social media posts by perturbing real news content.

The code mounts Google Drive to access the dataset and loads requirements like OpenAI Python API, Pandas, UUID, etc. It contains prompt engineering functions to create perturbation-based prompts to generate fake content and paraphrasing functions to rewrite real news.

Key functions include:

* ai_text_generator: Takes in parameters like prompt type, human text, and article type and calls ChatGPT API to generate synthetic text.

* process_row: Helper function to process single rows from the dataset using ai_text_generator.

* Main generation logic: Iterates over prompt types like "Minor," "Major," and "Critical" using process_row in ThreadPoolExecutor to generate synthetic datasets in a multi-threaded manner. Saves output content incrementally.

The pipeline allows configuring different perturbation intensities, content types, and output folders. The notebook showcases sample output data, including DataFrame summaries.

It aims to provide a template for researchers to configure and execute automated mass-scale synthetic text generation for various research objectives."
