# FabriqueLLM

FabriqueLLM is a compilation of code notebook and educational resources to fine-tune leading open LLMs (Falcon, Llama, MPT…). The project was originally conceived for fine-tuning in French but can be used in other contexts.

The lightest model used (7B parameters in 4-bit) can be used directly on the free version of Google Colab. They provide a good introduction to the fine-tuning LLM. Even a simple fine-tuning on one epoch already satisfies a variety of uses that GPT-4 would not fulfill (historical variants, dialects, sociolects…).

Te code notebooks of FabriqueLLM can be used in combination with the datasets made available in the **InstructionFr** repository: https://github.com/opinionscience/InstructionFr

## Falcon
FabriqueLLM include a documented code notebook in French and English to fine-tuning Falcon-Instruct-7B quantized at 4bit. This is currently one of the most cost effective model for fine-tuning. The simplest fine-tuning (one epoch) should run in 1h15-1h30 on the free version of Google Colab and in around 15 minutes on Google Colab Pro+ (with a A100 with 40 Go of Vram).

The code notebook comes under two variants:
* Generic example with a French translation of Alpaca instrutions. Probably the best place to start.
* More advanced use with a retraining on 17th century French novels with the original script. Settings have been slightly tweaked as a result (with a highest **learning rate**)

## Llama
To come later.

## MPT
To come later.

## Flan
To come later.
