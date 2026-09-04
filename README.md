# Task-01: Text Generation with GPT-2

## Objective
Fine-tune a GPT-2 model on a custom Python programming dataset and generate text based on a given prompt.

## Model
- GPT-2 (124M)
- Hugging Face Transformers

## Dataset
A custom text dataset focused on Python programming concepts, including:
- Python basics
- Data types and operators
- Control flow
- Functions
- Object-oriented programming
- Data structures
- File handling
- NumPy and Pandas
- Backend and AI concepts

## Process
1. Loaded the custom dataset.
2. Tokenized and divided the text into 512-token training chunks.
3. Fine-tuned GPT-2 for 10 epochs.
4. Generated text using custom prompts.
5. Saved the generated output.

## Generation Settings
- Max new tokens: 120
- Temperature: 0.7
- Top-k: 50
- Top-p: 0.9
- Repetition penalty: 1.15

## Files
- `python_gpt2_custom_dataset_clean.txt` — Custom training dataset
- `generated_output.txt` — Generated text output

## Result
The fine-tuned GPT-2 model generates Python-related text from a given prompt. The generated output demonstrates the model's learned style from the custom training dataset.
