# temp_prot123

## Overview

TiEBe is a benchmark dataset containing over 11,000 question-answer (QA) pairs that evaluate large language models (LLMs) on their ability to recall factual knowledge about globally and regionally significant events from 2015 to 2024. This benchmark addresses critical gaps in existing evaluations by focusing on two main aspects:

1. Temporal Knowledge: How well do LLMs capture knowledge of events that occurred in specific time frames, particularly in a rapidly changing global landscape?

2. Geographic Disparities: How evenly do LLMs perform across different regions, considering significant regional disparities in data representation?

TiEBe was created using structured retrospective data from Wikipedia, making it continuously updateable for the evaluation of evolving knowledge. The benchmark serves as a tool for:

* Assessing LLMs' factual recall capabilities.

* Evaluating strategies for continual learning.

* Identifying and addressing regional biases in knowledge representation.

If you have suggestions or would like to contribute, let us know! We’re excited to expand and improve this dataset together. 🙌

## Dataset Highlights

🕒 **Temporal Coverage:** Events from 2015 to 2024.

🌍 **Geographical Scope:** Six regions are covered—Brazil, China, Portugal, France, USA, and "World" (global events).

📊 **Size:** Over 5,700 distinct events and 11,000 QA pairs.

🌐 **Language:** QA pairs are exclusively in English to minimize translation inconsistencies and ensure clarity during evaluation.

## Dataset Structure
The repository contains three main folders:

`data/` Organized into subfolders for each evaluated model: gpt4o, llama3-70b, mistral-large, qwen2-70b, and sabia-3-2024-12-11.
Each model folder contains:
* answers/: Model responses for specific countries (Brazil, China, Portugal, France, USA) and World.

`results/` Organized into subfolders for each evaluated model: gpt4o, llama3-70b, mistral-large, qwen2-70b, and sabia-3-2024-12-11.
Each model folder contains:
* evaluations/: Judged responses reviewed by GPT-4o for the same regions.

`code/`
Scripts for dataset generation, model evaluation, and result analysis.

## Results Summary

**Top Performer:** GPT-4o consistently outperforms all other models across every region, with Mistral-large securing second place in all regions except China. Meanwhile, Sabiá-3, Qwen2-70B, and Llama3-70B often compete for the bottom three positions.

**Regional Disparities:** The USA had significantly higher average accuracy (~61%) compared to other regions. There is a performance gap of approximately 20\% between the best-performing and worst-performing models across all regions. This highlights that despite the regional disparities in performance observed.

**Temporal knowledge:**  The data reveals that model performance remains relatively consistent between the periods 2015–2018 and 2019–2022, suggesting that the models do not exhibit a strong performance bias toward either older or more recent events within this range. However, a marked decline in performance is observed across all models for the period 2023–2024. This decline is expected, as the questions increasingly require knowledge of events occurring after the models' respective cutoff dates.

**Model specialization:**  Sabiá-3 shows his best relative performance in the Brazil context, and Qwen shows his best relative performance in China-related questions. Mistral performs well in European contexts (France and Portugal) and shows a good overall performance, possibly due to its larger size. If we were to consider only the bottom three models, the language-specialized models would be the best-performing models in their respective countries.

| Model  | France | Portugal |China |Brazil | USA |World | Overall |
| ------------- | ------------- |------------- |------------- |------------- |------------- |------------- |------------- |
|  **GPT-4o** | 39%  |56% |48%  |55%  |70%  |81% | 68%
| **Qwen2-70B**  |29%  |34% |43%  |34%  |58%  |61% | 52%
|  **Sabiá-3**|22%  |35% |38%  |37%  |56%  |61% | 50%
|  **Llama3-70B**|22%  |38% |37%  |35%  |57%  |61% | 51%
|  **Mistral-large**|32%  |46% |42%  |41%  |64%  |69%| 58%


## How to Contribute
We welcome contributions to improve and expand TiEBe! Here’s how you can help:

Improve the dataset: 

* Suggest new events, refine existing QA pairs, or propose additional evaluation criteria.

* Analyze results: Share insights or benchmarks using our dataset.

* Extend the project: Create tools to explore regional or temporal trends.

Feel free to open an issue or submit a pull request. Make sure to follow these guidelines:

* Ensure all files are organized within the appropriate folder (data/, results/, or code/).
* For datasets, provide a clear description of your changes in a README or metadata file.