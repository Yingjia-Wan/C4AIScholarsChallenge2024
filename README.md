# C4AIScholarsChallenge2024

📌 Submission for the **C4AI Scholars Program Take-Home Challenge** (Sept 2024)

## Project Notes
The project covers building, training, and aligning a LLAMA-like SmolLM-135M model. 

The challenge is divided into three parts:
1. **Model Architecture Bug Fixing**: Identify and fix 10 bugs in the provided implementaton of building a [SmolLM-135M](https://huggingface.co/HuggingFaceTB/SmolLM-135M) model from scratch in PyTorch.
    - The model structure is close-sourced, but there's some remotely relevant info from its [blog post](https://huggingface.co/blog/smollm). In general, it is a LLAMA-like model architecture for causal generation.
    - The fixed model, when loaded with the provided trained weights, will generate the same output as the provided checkpoint.
    - (Personally speaking, this part is the hardest as many bugs are quite elusive, requiring proficiency in implementation of each module e.g., ROPE, multi-head attention, causal mask, SwiGLU, etc. SOTA AI is mostly useless here.)
2. **SFT + DPO**:
    - Fine-tune the provided SmolLM checkpoint on the Grammarly CoEdIT dataset for grammatical error correction;
    - Created datasets for DPO. I created annotated pairs based on decoding strategy variation and BLEU;
    - Implement DPO to further optimize the model.
3. **DPO Variants Exploration**:
    - Implement and evaluate an alternative Direct Preference Optimization (DPO) variant to improve model performance;
    - Discuss the alignment strategies and evaluation metrics.
