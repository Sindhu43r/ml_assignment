Project Title

RNN vs LSTM on a Synthetic Long-Memory Task: A Controlled Comparison

Project Overview

This project compares a vanilla Recurrent Neural Network (RNN) and a Long Short-Term Memory network (LSTM) on a controlled synthetic sequence classification task. The goal is to test how sequence length affects the ability of each model to retain useful information from the beginning of a sequence.

The experiment is designed so that the class label depends only on the first token, while all later tokens are noise. This creates a clear long-term dependency problem and allows the effect of increasing sequence length to be studied directly.

The tutorial focuses on two questions:

Why are long-term dependencies difficult for recurrent models?
How do RNNs and LSTMs behave as the required memory span increases?
What this repository contains

This repository includes:

the tutorial write-up
the code used to generate the synthetic dataset
the training and evaluation code for the RNN and LSTM models
the figures and results used in the tutorial
the references used to support the explanation
Main idea of the experiment

Each sequence begins with a signal token that determines the class label. The rest of the sequence is made of random noise. A model can only solve the task if it preserves the information from the first token until the end of the sequence.

Sequence lengths tested:

10
30
60
100

The main evaluation measure is test accuracy. Validation accuracy and validation loss are also used to examine training behaviour.

How to install dependencies

Create and activate a Python environment, then install the required packages.

pip install torch numpy matplotlib

If you prefer, you can install dependencies from a requirements list if you create one for the repository.

How to run the project
Open the 24164952_ml_code.ipnyb or Python script in your preferred environment.
Run the cells or script from top to bottom.
The code will:
generate the synthetic dataset
train a vanilla RNN and an LSTM
evaluate both models across different sequence lengths
print the final accuracy results
generate the plots used in the tutorial

To reproduce the tutorial correctly, run everything from a fresh session so the results and figures are generated in order.
