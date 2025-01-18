# temp_prot123

## Overview

The TiEBe (Timely Events Benchmark) dataset is a comprehensive collection of over 11,000 question-answer (QA) pairs spanning major global events between 2015 and 2024. The dataset covers events from six regions — China, Brazil, Portugal, France, USA, and World — allowing for analysis of geographical performance disparities and temporal trends in LLM capabilities. Benchmarked results include various models, such as GPT-4o, Mistral-large, Sabiá-3, Qwen2-70B, and Llama3-70B, highlighting their factual recall performance.

## Dataset Structure

The dataset is organized into a hierarchical folder structure for clarity and ease of use. At the top level, there is a dataset folder containing subfolders for each evaluated model: gpt4o, llama3-70b, mistral-large, qwen2-70b, and sabia-3-2024-12-11. Inside each model folder, there are two main categories of files: the answers folder, which contains the model's responses for different countries (Brazil, China, USA, France, and Portugal) and the World, and the evaluations folder, which includes the judged responses reviewed by GPT-4o for different countries (Brazil, China, USA, France, and Portugal) and the World.