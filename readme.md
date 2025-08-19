# VulScribeR

Official repository for our [paper](https://doi.org/10.1145/3760775):
> *VulScribeR: Exploring RAG-based Vulnerability Augmentation with LLMs*

If you find this project useful in your research, please consider citing:

```
@article{VulScribeR,
author = {Daneshvar, Seyed Shayan and Nong, Yu and Yang, Xu and Wang, Shaowei and Cai, Haipeng},
title = {VulScribeR: Exploring RAG-based Vulnerability Augmentation with LLMs},
year = {2025},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
issn = {1049-331X},
url = {https://doi.org/10.1145/3760775},
doi = {10.1145/3760775},
abstract = {Detecting vulnerabilities is vital for software security, yet deep learning-based vulnerability detectors (DLVD) face a data shortage, which limits their effectiveness. Data augmentation can potentially alleviate the data shortage, but augmenting vulnerable code is challenging and requires a generative solution that maintains vulnerability. Previous works have only focused on generating samples that contain single statements or specific types of vulnerabilities. Recently, large language models (LLMs) have been used to solve various code generation and comprehension tasks with inspiring results, especially when fused with retrieval augmented generation (RAG). Therefore, we propose VulScribeR, a novel LLM-based solution that leverages carefully curated prompt templates to augment vulnerable datasets. More specifically, we explore three strategies to augment both single and multi-statement vulnerabilities, with LLMs, namely Mutation, Injection, and Extension. Our extensive evaluation across four vulnerability datasets and DLVD models, using three LLMs, show that our approach beats two SOTA methods Vulgen and VGX, and Random Oversampling (ROS) by 27.48\%, 27.93\%, and 15.41\% in f1-score with 5K generated vulnerable samples on average, and 53.84\%, 54.10\%, 69.90\%, and 40.93\% with 15K generated vulnerable samples. Our approach demonstrates its feasibility for large-scale data augmentation by generating 1K samples at as cheap as US$ 1.88.},
note = {Just Accepted},
journal = {ACM Trans. Softw. Eng. Methodol.},
month = aug,
keywords = {Vulnerability Augmentation, Deep Learning, Vulnerability Generation, Program Generation, Vulnerability Injection}
}
```

## Datasets

### Primary Datasets
[Bigvul_train](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/bigvul_train.zip),\
[Bigvul test](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/bigvul_test.zip),\
[Bigvul_val](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/bigvul_val.zip)\
\
[Reveal](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/reveal_ds.zip),\
[Devign](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/devign_ds.zip),\
[PrimeVul (RQ4 only)](https://github.com/DLVulDet/PrimeVul) 


### VGX and Vulgen (used as baselines)
[VGX Full dataset](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/vgx_full.zip),\
[Vulgen Full dataset from VGX paper](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/vulgen_full.zip)

### Retriever's output
[All pair matching (except for RQ4), including for mutation and random ones for RQ2](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/Retriever_Results.zip)\
[RQ4's pair matching/retriver output](https://github.com/shayandaneshvar/VulScribeR/releases/download/RQ4/RQ4-unfiltered.zip)

### Our Generated Vulnerable Samples
[Filtered Datasets for RQs(1-3)](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/generated_filtered.rar),\
[Unfiltered Datasets for RQs(1-3)](https://github.com/shayandaneshvar/VulScribeR/releases/download/Dataset/generated_raw.zip),\
[Unfiltered Datasets for RQ4](https://github.com/shayandaneshvar/VulScribeR/releases/download/RQ4/RQ4-unfiltered.zip) \
\
The unfiltered dataset contains samples from the Generator and hasn't gone through the Verification phase. They also include extra metadata that shows which clean_vul pair was used for generation, plus the vul lines.

## How to use?
[See here](https://github.com/shayandaneshvar/VulScribeR/blob/main/code/readme.md)

## How to train DLVD models
Go to the [models](https://github.com/shayandaneshvar/VulScribeR/tree/main/models) directory, the readme for each model explains how to use each of the models
