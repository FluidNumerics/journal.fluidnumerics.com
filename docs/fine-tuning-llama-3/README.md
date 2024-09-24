---
blogpost: true
date: 15 October 2024
author: Garrett Byrd, Joe Schoonover
tags: LLM, AI/ML, PyTorch, Installation
category: Applications & models
language: English
myst:
  html_meta:
    "description lang=en": "Fine-Tuning Llama 3 on AMD Radeon GPUs"
    "keywords": "Llama, Llama 3, PyTorch, LLM, Transformer, Attention, ROCm, large language model, AI/ML, Generative AI, Installation"
    "property=og:locale": "en_US"
---

# Fine-Tuning Llama 3 on AMD Radeon GPUs
<span style="font-size:0.7em;">15, October 2024 by {hoverxref}`Garrett Byrd<garrettbyrd>`, {hoverxref}`Joe Schoonover<joeschoonover>`. </span>



## Introduction
### Source code and Presentation
This blog is a companion piece to the [ROCm Webinar of the same name](UPDATE THIS) presented by Fluid Numerics, LLC on 15 October 2024. The source code for these materials is provided on [GitHub](https://github.com/FluidNumerics/amd-ml-examples).

## What is Fine-Tuning?



## Quantization



## IEEE 754 / FP8 / FP4

Exponent and mantissa stay the same. NF8 maps to int8 (quantile quantization)

## Installation

### Requirements


### Install Steps





## Hugging Face



## Llama 3
Llama 3 likely needs no introduction, and it should be clear that this is the model that we're using in this example. The Llama family, developed by Meta Platforms, Inc., is a collection of some of the most popular open-weight models available today. Meta offers 8 billion, 70 billion, and now even 405 billion parameter versions. Llama 3 was trained with 15 trillion tokens, and can digest an impressive 8K tokens. Llama 3 also achieves consistently high scores on a variety of LLM benchmarks, such as MMLU, HumanEval, and GSM8K. At the time of publication, the Llama family has approximately 15 million downloads on the Hugging Face Hub. Today, we'll be using the `Llama-3-8B-Instruct` version, an 8 billion parameter version that has been fine-tuned for instructional speech patterns, i.e., answering questions.



## Example




## Acknowledgments
Special thanks to [Garrett Byrd](https://github.com/garrettbyrd) and [Dr. Joe Schoonover](https://github.com/fluidnumerics-joe) at [Fluid Numerics, LLC](https://www.fluidnumerics.com/) for contributing this blog. The ROCm software ecosystem is strengthened by community projects that enable you to use AMD GPUs in new ways. If you have a project you would like to share here, [please raise an issue or PR](https://github.com/ROCm/rocm-blogs).

**Find Fluid Numerics online at:**
- [fluidnumerics.com](https://www.fluidnumerics.com)
- [Reddit](https://www.reddit.com/r/FluidNumerics/)
- [GitHub](https://github.com/FluidNumerics)
- [YouTube](https://www.youtube.com/@FluidNumerics)
- [LinkedIn](https://www.linkedin.com/company/fluidnumerics)

## References
### Source Code
[Available on GitHub](https://github.com/FluidNumerics/amd-ml-examples)

### Papers
Vaswani, A. "Attention is all you need." Advances in Neural Information Processing Systems (2017).

Dettmers, Tim, Mike Lewis, Sam Shleifer, and Luke Zettlemoyer. "8-bit optimizers via block-wise quantization." arXiv preprint arXiv:2110.02861 (2021).

Dettmers, Tim, Artidoro Pagnoni, Ari Holtzman, and Luke Zettlemoyer. "Qlora: Efficient finetuning of quantized llms." Advances in Neural Information Processing Systems 36 (2024).

Micikevicius, Paulius, Dusan Stosic, Neil Burgess, Marius Cornea, Pradeep Dubey, Richard Grisenthwaite, Sangwon Ha et al. "Fp8 formats for deep learning." arXiv preprint arXiv:2209.05433 (2022).

### Installation Pages
[ROCm quick start installation guide](https://rocm.docs.amd.com/projects/install-on-linux/en/latest/install/quick-start.html)

[Miniconda Quick Command Line Install](https://docs.anaconda.com/miniconda/#quick-command-line-install)

[PyTorch Installation Configurator](https://pytorch.org/get-started/locally/)

[git-lfs](https://git-lfs.com/)



## Disclaimers
Third-party content is licensed to you directly by the third party that owns the content and is not licensed to you by AMD. ALL LINKED THIRD-PARTY CONTENT IS PROVIDED “AS IS” WITHOUT A WARRANTY OF ANY KIND. USE OF SUCH THIRD-PARTY CONTENT IS DONE AT YOUR SOLE DISCRETION AND UNDER NO CIRCUMSTANCES WILL AMD BE LIABLE TO YOU FOR ANY THIRD-PARTY CONTENT. YOU ASSUME ALL RISK AND ARE SOLELY RESPONSIBLE FOR ANY DAMAGES THAT MAY ARISE FROM YOUR USE OF THIRD-PARTY CONTENT.