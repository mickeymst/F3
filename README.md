# Fighting Fire with Fire: The Dual Role of LLMs in Crafting and Detecting Elusive Disinformation

## Abstract
Recent ubiquity and disruptive impacts of large language models (LLMs) have raised concerns about their potential to be misused (i.e., generating large-scale harmful and misleading content). To combat this emerging risk of LLMs, we propose a novel "Fighting Fire with Fire" (F3) strategy that harnesses modern LLMs' generative and emergent reasoning capabilities to counter human-written and LLM-generated disinformation. First, we leverage GPT-3.5-turbo to synthesize authentic and deceptive LLM-generated content through paraphrase-based and perturbation-based prefix-style prompts, respectively. Second, we apply zero-shot in-context semantic reasoning techniques with cloze-style prompts to discern genuine from deceptive posts and news articles. In our extensive experiments, we observe GPT-3.5-turbo's zero-shot superiority for both in-distribution and out-of-distribution datasets, where GPT-3.5-turbo consistently achieved accuracy at 68-72%, unlike the decline observed in previous customized and fine-tuned disinformation detectors. 


## Description
This repository contains the codebase and dataset for the paper "Fighting Fire with Fire: The Dual Role of LLMs in Crafting and Detecting Elusive Disinformation."

## F3 Dataset 
Certainly! Here's a descriptive overview of the structure for use on GitHub:

---

## F3_Dataset Structure Overview

The `F3_Dataset` repository is organized to facilitate easy access and understanding of our diverse datasets, particularly focusing on the differentiation between pre- and post-GPT datasets, as well as various sources and types of data. It's structured to support machine learning tasks, especially for projects dealing with fake and real news detection in both news articles and social media posts.

### Structure Breakdown

- **Train-Test-Split**: This primary directory contains split datasets used for training and testing models. It's crucial for ensuring model robustness and generalization. The directory is subdivided as follows:

  - **pre_post_GPT: post-GPT**
    - **dataset_source: F3**
      - **article_type: news article**
        - `label: fake` - Contains post-GPT fake news articles from the F3 source.
        - `label: real` - Contains post-GPT real news articles from the F3 source.
      - **article_type: social media post**
        - `label: fake` - Contains post-GPT fake social media posts from the F3 source.
        - `label: real` - Contains post-GPT real social media posts from the F3 source.

  - **pre_post_GPT: pre-GPT**
    - **dataset_source: CoAID**
      - Similar structure as above for CoAID source.
    - **dataset_source: FakeNewsNet**
      - Similar structure as above for FakeNewsNet source.
    - **dataset_source: F3**
      - Similar structure as above for F3 source, but for pre-GPT datasets.

- **Full Clean (PURIFY) Dataset**: This directory contains datasets that have undergone a comprehensive cleaning and purification process. It's ideal for users who require high-quality, clean data for advanced analytics and machine learning applications.

### Usage

This structured repository is designed for researchers and developers working in the domain of misinformation detection and natural language processing. Users can navigate through the categories based on their requirement of pre- or post-GPT data, the source of the data, and the type (news article or social media post). The labels `fake` and `real` provide a clear demarcation for supervised learning tasks.


## Codebase
The codebase repo folder consists of three Jupyter Notebooks that can be easily run through Google Colab: F3 Data Generation IPYNB, F3 Data Generation IPYNB, and PURIFY Framework IPYNBs. Notebooks are structured intuitively, making it easy for users to follow along and modify according to their specific needs.

#### Getting Started
To use this notebook:
1. Clone the repository.
2. Ensure you have Jupyter Notebook installed, or use Google Colab for an online experience.
3. Follow the instructions within the notebook to mount your Google Drive and access your datasets.

### [F3] Fighting Fire With Fire Generation IPYNB
[IPYNB Notebook](https://github.com/mickeymst/F3/blob/main/F3_Codebase/%5BF3%5D_Fighting_Fire_With_Fire_Data_Generation.ipynb)

#### Overview
This Jupyter Notebook provides code for generating synthetic text data using OpenAI's GPT-3.5 Turbo language model. It focuses on creating fake news articles and social media posts by perturbing real news content.
The code mounts Google Drive to access the dataset and loads requirements like OpenAI Python API, Pandas, UUID, etc. It contains prompt engineering functions to create perturbation-based prompts to generate fake content and paraphrasing functions to rewrite real news.

#### Key functions include:

- **ai_text_generator**: Takes in parameters like prompt type, human text, and article type and calls ChatGPT API to generate synthetic text.
- **process_row**: Helper function processes single rows from the dataset using ai_text_generator.
- **Main generation logic**: Iterates over prompt types like "Minor," "Major," and "Critical" using process_row in ThreadPoolExecutor to generate synthetic datasets in a multi-threaded manner. Saves output content incrementally.

The pipeline allows configuring different perturbation intensities, content types, and output folders. The notebook showcases sample output data, including DataFrame summaries. It aims to provide a template for researchers to configure and execute automated mass-scale synthetic text generation for various research objectives."

### [F3] Fighting Fire With Fire Detection IPYNB
[IPYNB Notebook](https://github.com/mickeymst/F3/blob/main/F3_Codebase/%5BF3%5D_Fighting_Fire_With_Fire_Detection.ipynb)

#### Overview
"Fighting Fire With Fire Detection" is a comprehensive Jupyter notebook designed for advanced data analysis and machine learning inference tailored to binary classification tasks. This notebook is an essential tool for researchers and data scientists aiming to leverage external datasets, particularly those stored on Google Drive, for insightful data exploration and model inference.

#### Key Features
- **Google Drive Integration**: Seamlessly connect and access data stored in Google Drive, facilitating easy data management and retrieval.
- **Classification Prompt Engineering**: Specialized focus on crafting effective prompts for classification problems, enhancing model performance and accuracy.
- **Main detection logic**: Iterates over prompt types that use In-context learning and semantic reasoning, such as Chain-of-Thoughts (CoT)






