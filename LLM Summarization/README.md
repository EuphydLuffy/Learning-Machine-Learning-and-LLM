# LLM summarization projects

## Contents
- Summarization accuracy comparison: Llama 3.2 1B-instruct vs Flan-t5 large
  - Compares the two models on summarization tasks. Note that these two models have similar number of parameters (1B vs 750 million)
  - Comparison tasks were done on two different huggingface datasets (Samsum and CNN daily), with different prompts considered. 
  - Surprisingly, Flan-t5 large outperforms on the selected summarization tasks, especially on summarizing shorter texts such as samsum.

- Fine-tuning Llama 3.2 1B-instruct with Low Rank Adaptation (LoRA). 
  - The fine-tuning was done on
    - 1000 Samsum texts
    - LoRA setting: r= 8, alpha = 16, dropout = 0.05.
    - Adaptive padding is used. In fact, padding all texts with maximum lengths would negatively impact summarization quality per Rouge scores.
    - The winning prompt from the notebook "Summarization accuracy comparison: Llama 3.2 1B-instruct vs Flan-t5 large" is used for the fine-tuning.
  - The LoRA fine-tuning significantly improved the model performance measured in Rouge scores, and the improvement is observable on out-of-development samples. 
  
## Requirements
Please refer to "requirements.txt".