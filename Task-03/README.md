# Task-03: Text Generation using Markov Chains

## Objective

Generate text using a Markov Chain model trained on a custom text corpus.

## Description

For this task, a custom programming-related text corpus was used to build a Markov Chain text generator.

The text was divided into sentences and words. A second-order Markov Chain was initially used and later improved to a third-order Markov Chain to provide better context during text generation.

## Markov Chain

The model uses the previous three words (state) to determine the possible next word.

The next word is selected randomly from the learned transitions, allowing the model to generate new text based on patterns found in the corpus.

## Corpus

The corpus contains programming-related topics such as:

- Python
- Programming
- Functions
- Data Structures
- Object-Oriented Programming
- Web Development
- Backend Development
- Databases
- SQL
- Data Science
- Machine Learning
- Artificial Intelligence

## Model Details

- Model: Markov Chain
- State size: 3
- Number of states: 452
- Maximum generated words: 30

## Generated Output

The generated output is saved in:

`generated_output3.txt`

Example generated text:

> A class defines the structure and behavior of objects.

## Technologies

- Python
- Markov Chains
- Markovify
