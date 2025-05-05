# Introduction to LLMs and GenAI

## Session Overview

In this session, we'll explore the fundamentals of Large Language Models (LLMs) and Generative AI (GenAI). Understanding these concepts is essential before we dive into deploying and working with these technologies on Nutanix infrastructure.

## Why Now and What Are LLMs?

Large Language Models (LLMs) are a type of AI model trained on vast amounts of text data to understand and generate human-like text. Their recent growth has been driven by:

- Breakthroughs in transformer architecture
- Massive increases in available training data
- Advancements in computing power, particularly GPUs
- Open-source model research and development

LLMs can perform various tasks without specific training for each task, including:

- Text generation and completion
- Question answering
- Summarization
- Translation
- Code generation
- Logical reasoning

## Open-Source LLMs and Model Architectures

The landscape of open-source LLMs has expanded dramatically, with models like:

- Llama 2 and Llama 3 (Meta)
- Mistral and Mixtral (Mistral AI)
- Falcon (Technology Innovation Institute)
- Gemma (Google)
- MPT (MosaicML)

From an architecture perspective, most modern LLMs are based on the transformer architecture with variations like:

- Decoder-only models (GPT-style)
- Encoder-decoder models (T5-style)
- Sparse mixture of experts (Mixtral, GPT-4)

## Tokens vs. Words

LLMs process text as tokens, not words. Understanding tokenization is important for:

- Calculating context window limitations
- Estimating processing costs and latency
- Designing effective prompts

A general rule of thumb:
- 1 token ≈ 4 characters or ¾ of a word in English
- 100 words ≈ 75-150 tokens (depending on complexity)

## Benchmarking LLMs

Models are evaluated on various benchmarks to measure capabilities:

- MMLU (general knowledge and reasoning)
- HellaSwag (common sense reasoning)
- GSM8K (math problem solving)
- HumanEval (code generation)
- MT-Bench (instruction following)

## Infrastructure Requirements for Inferencing

Running LLMs requires substantial computational resources:

- **GPU Memory**: Primary determinant of which models you can run
  - 7B parameter models: ~14GB VRAM
  - 13B parameter models: ~26GB VRAM
  - 70B parameter models: ~140GB VRAM

- **Optimization Techniques**:
  - Quantization (reducing precision from FP16 to INT8 or INT4)
  - Model sharding across multiple GPUs
  - Attention mechanisms (Flash Attention, xFormers)
  - KV cache optimization

## Embedding, Prompting, Training, and Fine-Tuning

### Embeddings
- Vector representations of text for semantic search
- Used for RAG (Retrieval-Augmented Generation)
- Enable "memory" in LLM applications

### Prompting
- The art of instructing LLMs effectively
- Techniques like few-shot learning, chain-of-thought, and ReAct
- Prompt engineering as a critical skill

### Training and Fine-Tuning
- Pre-training: Learning language patterns from massive datasets
- Fine-tuning: Adapting pre-trained models to specific tasks
- Parameter-Efficient Fine-Tuning (PEFT) methods
  - LoRA (Low-Rank Adaptation)
  - QLoRA (Quantized LoRA)
  - Adapters

## Moving to Practice

With this foundation in place, we'll now move to the hands-on lab where you'll get experience with basic prompting and context manipulation.

Let's proceed to the [lab on prompting and context](lab-prompting.md).
