# Code for ProbingRankLlama 
1. Install all requirements in requirements.txt.
2. Generate and save all desired Activations by running rankllama-activation.py.
3. Update Queries and Documents as desired in sequences.py.
4. Find context neurons by running context_neurons.py.

Remember to update the hugging face login keys in above files. Also you need access to LLaMa models using this key.



# Fine-Grained Checkpoint Experiments for Ranking LLMs

This repository hosts the checkpoints for various fine-tuned LLMs used in probing and interpretability experiments on ranking tasks. T
These models have been trained using the [Tevatron ranking framework](https://github.com/texttron/tevatron/tree/main/examples/rankllama), as suggested in the [RankLLaMA paper](https://arxiv.org/pdf/2310.08319)

---

## Available Fine-Tuned Models

The following model checkpoints are publicly available on [HuggingFace](https://huggingface.co/AtharvaNijasureUMass):

- **RankLLaMA3**  
  - [RankLLaMA3](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_llama3)
  - [RankLLaMA3 R2](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_llama3_r2)
  - [RankLLaMA3 R8](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_llama3_r8)
  - [RankLLaMA3 R8 LoRA MLP](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_llama3_r8_lora_mlp)
  - [RankLLaMA3 R32 LoRA MHA](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_llama3_r32_lora_mha)
- **RankLLaMA2**  
  - [RankLLaMA2-7B (via paper)](https://huggingface.co/castorini/rankllama-v1-7b-lora-passage) *(link placeholder)*  
  - [RankLLaMA2-13B (via paper)](https://huggingface.co/castorini/rankllama-v1-13b-lora-passage) *(link placeholder)*

- **RankMistral**  
  - [RankMistral](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_rankmistral)
  - [RankMistral R8](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_rankmistral_r8)
  - [RankMistral R8 MLP Only](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_rankmistral_r8_mlp_only)

- **RankPythia**  
  - [RankPythia](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_pythia)
  - [RankPythia R8](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_pythia_r8)
  - [RankPythia R8 MLP Only](https://huggingface.co/AnonymousForReview2/finegrained_checkpoint_experiment_rankpythia_r8_mlp_only)

---

## Experiments

You can run all probing and interpretability experiments described in our paper using any of the above fine-tuned checkpoints. The experiments are designed to measure the alignment of IR feature representations with intermediate layers of these ranking LLMs.

> 🧪 **Note:**  
> The experiments presented in the paper were conducted on **full LoRA fine-tuned Rank-8 and Rank-32** models of **Pythia**, **LLaMA3**, and **LLaMA2** (7B and 13B). These configurations provide optimal probing fidelity for feature tracking and layerwise interpretability.



