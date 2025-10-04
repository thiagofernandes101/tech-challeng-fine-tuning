# Fine-Tuning Tech Challenge

## Project Description
This project focuses on fine-tuning a pre-trained language model using the `unsloth` library and Hugging Face's `transformers` framework. The goal is to adapt the model to generate text in the style of specific books or content provided in the dataset.

## Objective
The primary objective of this project is to:
- Fine-tune a pre-trained language model to generate high-quality, contextually relevant text.
- Utilize efficient training techniques, such as LoRA (Low-Rank Adaptation), to optimize resource usage.

## Implementation Key Points
1. **Dataset Preparation**:
   - The dataset is loaded from a JSON file (`datasets/trn.json`) using the `datasets` library.
   - Data is filtered and preprocessed to clean text and format it for training.

2. **Model Selection**:
   - The project uses the `unsloth/Phi-3.5-mini-instruct` model, a lightweight and efficient pre-trained language model.
   - LoRA is applied to the model for parameter-efficient fine-tuning.

3. **Training Pipeline**:
   - The `SFTTrainer` from the `trl` library is used for supervised fine-tuning.
   - Training arguments are configured for efficient GPU usage, including gradient accumulation and mixed-precision optimization.

4. **Evaluation**:
   - The model is tested before and after training using specific prompts to evaluate its text generation capabilities.
   - Training logs and loss curves are visualized to monitor performance.

5. **Tools and Libraries**:
   - `unsloth` for model loading and LoRA integration.
   - `transformers` and `trl` for training and tokenization.
   - `datasets` for data handling and preprocessing.
   - `pandas` and `matplotlib` for logging and visualization.

## Results
- The fine-tuned model demonstrates improved text generation capabilities tailored to the dataset.
- Training statistics and loss curves provide insights into the model's learning process.
