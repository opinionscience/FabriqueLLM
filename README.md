# FabriqueLLM

FabriqueLLM is a compilation of code notebook and educational resources to fine-tune leading open LLMs (Falcon, Llama, MPT…). The project was originally conceived for fine-tuning in French but can be used in other contexts.

The lightest model used (7B parameters in 4-bit) can be used directly on the free version of Google Colab in 1h15-1h30. They provide a good introduction to the fine-tuning LLM. Even a simple fine-tuning on one epoch already satisfies a variety of uses that GPT-4 would not fulfill (historical variants, dialects, sociolects…).

Te code notebooks of FabriqueLLM can be used in combination with the datasets made available in the **InstructionFr** repository: https://github.com/opinionscience/InstructionFr

## Falcon
FabriqueLLM include a documented code notebook in French and English to fine-tuning Falcon-Instruct-7B quantized at 4bit. This is currently one of the most cost effective model for fine-tuning. The simplest fine-tuning (one epoch) should run in 1h15-1h30 on the free version of Google Colab and in around 15 minutes on Google Colab Pro+ (with a A100 with 40 Go of Vram).

The code notebook comes under two variants:
* **Fine_tune_avec_falcon_4bit.ipynb**: Generic example with a French translation of Alpaca instrutions. Probably the best place to start ([https://colab.research.google.com/drive/1wu56PqmFDb-zJlIxk_ypbdiuYwrkVJH9?usp=sharing](Google Colab))
* **Fine_tune_avec_falcon_4bit_novel17.ipynb**: More advanced use with a retraining on 17th century French novels with the original script. Settings have been slightly tweaked as a result (with a highest **learning rate**) ([https://colab.research.google.com/drive/1grBHTUuYdodLZFnV0ehUFSUoa4DJkgA2?usp=sharing](Google Colab))

Generation is slow but should be significantly enhanced in future versions. The sample outputs in both code notebooks provide a good illustration of the different capacity of fine-tuning.

With a standard approach (fine-tuning on Vicogne) you get chatGPT-like results:

> **Instruction**: Peux-tu m'expliquer en détail comment je pourrais me rendre sur la Lune ?
> 
> **Output (Falcon-Vicogne)**: Pour se rendre sur la Lune, une personne devrait embarquer sur un vaisseau spatial en orbite autour de la Terre, puis parcourir environ 384 400 miles (643 200 kilomètres) pour se rendre à la surface de la Lune. Le vaisseau spatial doit être conçu pour être capable de voyager dans l'espace et devrait être propulsé par un moteur à combustion pour le faire fonctionner. Le vaisseau spatial doit également être conçu pour protéger les passagers contre les effets de l'environnement extérieur, tels que la gravité, les radiations et les températures extrêmes. Une fois que le vaisseau spatial atteint la Lune, il se pose sur la surface lunaire et le passager sort du vaisseau pour explorer le terrain. Une fois que le vaisseau spatial est parti, il orbite la Lune jusqu'à la prochaine nuit terrestre.

With a very specific dataset of French 17th century novel the model will assimilate specific forms of writing that chatGPT is unable to reproduce:

> **Instruction**: Pourrois-tu me iustifier le moyen le plus ſimple & le plus aisé que j'ay par lequel je pourrois me rendre sur la Lune ?
> 
> **Output (Falcon-Novel17)**: Le moyen le plus aisé pour aller sur la Lune que je connois & pour lequel j'en ai l'honneur de vous le dire est celui qui consiste à nous rendre dans les airs en nous tirant par un canon. Cette machine ſe trouve dans les airs & les nuages de tous les pays. Il nous faut seulement faire un trou dans le vaisſe & nous placer dedans pour être tirés plus haut que la Montagne & dans lequel nous pouvons nous reprendre en toute liberté. Ce moyen convient à tout le monde.

## Llama
FabriqueLLM include a series of documented code notebook in French and English to fine-tune Llama 1 and the the newest version released on July, 18th 2023, Llama 2. Both are quantized at 4bit. The simplest fine-tuning (one epoch) should run in 1h15-1h30 on the free version of Google Colab and in around 15 minutes on Google Colab Pro+ (with a A100 with 40 Go of Vram).

The three variants are
* **Fine_tune_llama_7b.ipynb**: Fine-tuning on the lightest version of Llama-1 (7B) Probably the best place to start ([https://colab.research.google.com/drive/1NQ30BCuOTXtUZ14tbqmW13-ZZ6SPyg1L?usp=sharing](Google Colab))
* **Fine_tune_llama_13b.ipynb**: Fine-tuning of the most advanced version of Llama-1 (13B) that can still easily run on Colab. It will likely requires Google Colab pro due to the memory requirements ([https://colab.research.google.com/drive/1YWuSd82QyrjWtsAOGCsacWa87SVqzZK3?usp=sharing](Google Colab))
* **Fine_tune_llama_2_7b_fr**: Fine-tuning of the lightes version of Llama-2 (7B). For now it will likely requires Google Colab pro but the script is still new, experimental and very likely to improve in the coming weeks. ([https://colab.research.google.com/drive/1l1s00SNwx_S-XmTPoFNhx2LVxi-6v0hB?usp=sharing](Google Colab))

## MPT
To come later.

## Flan
To come later.
