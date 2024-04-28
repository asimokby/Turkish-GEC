# Turkish-GEC

This repository contains all the related artifacts (models, datasets, code) of the currently under review paper: **Organic Data-Driven Approach for Turkish Grammatical Error Correction and LLMs**


## Datasets

| Dataset Name                   | Split  | Sentences | Tokens  | Error Types | Domain        |
|--------------------------------|-------|-----------|---------|-------|---------------|
| [OSCAR GEC (ours)](https://huggingface.co/datasets/asimokby/Turkish-OSCAR-GEC)              | Train  | 2.3m       | 213.2m  | ERRANT | Web            |
| [GPT GEC (ours)](https://huggingface.co/datasets/asimokby/Turkish-GPT-GEC)                 | Train  | 100k       | 3.6m    | ERRANT | Web            |
| GECTurk (Kara et al, 2023)     | Train  | 138k       | 5.8m    | 25      | Newspapers     |
| [OSCAR GEC (ours)](https://huggingface.co/datasets/asimokby/Turkish-GEC-Evaluation)               | Test   | 2.4k       | 142k    | ERRANT | Web            |
| Movie Reviews (Kara et al, 2023)     | Test   | 300        | 2.7k    | 25      | Movie Reviews  |
| Turkish Tweets (Koksal et al, 2020a) | Test   | 2k         | 116.2k  | 13      | Tweets          |


## Models

Fine-tuned mT5 models for the Turish Grammatical Error Correction task on our two datasets: OSCAR GEC and GPT GEC. The models are available on HuggingFace:

Model 1: [Turkish-OSCAR-GEC](https://huggingface.co/asimokby/Turkish-OSCAR-GEC-v0)

Model 2: [Turkish-GPT-GEC](https://huggingface.co/asimokby/Turkish-GPT-GEC-v0)

The following are the results of Turkish GEC models on 3 evaluation sets: 

Eval set 1: **OSCAR GEC (ours)**

| Model                                     | P                  | R     | F0.5 |
|--------------------------------------------|--------------------|--------|-------|
| GPT GEC (mT5)                             | 69.8               | 44.9  | **62.8**  |
| OSCAR GEC (mT5)                           | 68.7               | 31.2  | 55.4  |
| GECTurk (mT5)                             | 42.5               | 5.7   | 18.2  |
| GECTurk (Seq Tagger) (Kara et al., 2023)  | 49.0               | 3.9   | 14.7  |

Eval set 2: **Turkish Tweets** (Koksal et al, 2020a)

| Model                                     | P                  | R     | F0.5 |
------- | -------- | -------- | --------
OSCAR GEC (mT5) | 85.1 | 61.3 | **79.0**
GPT GEC (mT5) | 77.7 | 68.9 | 75.8
GECTurk (Seq Tagger) (Kara et al, 2023) | 64.7 | 19.8 | 44.5
GECTurk (mT5) | 57.2 | 20.7 | 42.3

Eval set 3: **Movie Reviews** (Kara et al, 2023)

| Model                                     | P                  | R     | F0.5 |
|---|---|---|---|
| GECTurk (Seq Tagger) (Kara et al., 2023) | 86.5 | 76.2 | **84.2** |
| GECTurk (mT5) | 73.1 | 71.8 | 72.8 |
| GPT GEC (mT5) | 36.0 | 46.3 | 37.6 |
| OSCAR GEC (mT5) | 30.0 | 22.5 | 28.1 |






