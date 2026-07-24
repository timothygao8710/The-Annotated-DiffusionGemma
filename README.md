# The Annotated DiffusionGemma 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/17egFGmboDkhU6duNQHvjB1J0oiKslOMl?usp=sharing)

Google recently released [DiffusionGemma](https://deepmind.google/models/gemma/diffusiongemma/), a 26B A4B open-weight uniform state diffusion language model.

We present an annotated, from-scratch implementation reimplementation that attempts to fill in the low-level details that were left out or only briefly covered in Google’s official documentation (e.g., the actual model architecture, partial RoPE, logit softcapping, Google's scalar-weight QK norm) and how exactly they are implemented (e.g., sampling, self-conditioning). We also discuss some implementation and inference ideas for DiffusionGemma: skipping computation on encode, lazy sampling, and RMSNorm fusion.

A working knowledge of vanilla autoregressive LLM implementations (Llama 3.1, MOE) is assumed.



Prompt: What is the meaning of 67?

Model (first canvas): ....


