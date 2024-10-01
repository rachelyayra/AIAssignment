# Overview of Code Implementation for Semeval Tabulur QA-TAPAS notebook
1. Semeval Tabulur QA-TAPAS notebook demonstrates the implementation of a question-answering system over tabular data using just the TAPAS Model. This is a zero-shot used and does not require any training.
This notebook implements a Question Answering (QA) system using the TAPAS model from Hugging Face. It processes tabular data to answer questions based on a dataset of question-answer pairs.

## Key Steps

1. **Setup**: Installs required libraries and loads the QA dataset (`semeval_dev_qa`).
2. **Data Exploration**: Explores the dataset structure and prints sample questions and answers.
3. **Model Preparation**: Defines a `TableDataset` class for tokenization and loads the TAPAS model.
4. **Prediction**: Implements functions to predict answers based on table data and queries, handling both single and multi-cell answers.
5. **Execution**: Generates predictions for the dataset and saves results to text files.

# Overview of Code Implementation for Semeval Tabulur QA-TAPAS notebook
2. Semeval Tabulur QA notebook demonstrates the implementation of a question-answering system over tabular data using the TAPAS and T5 models. The goal is to train a model that can effectively answer questions based on the context provided by structured tables.

## Key Components:

1. **Data Preparation**:
   - The dataset consists of tables that are structured for question-answering tasks.
   - The first 1,000 tables are selected for the training set, while the subsequent 300 tables are designated for validation.

2. **Model Initialization**:
   - Models are initialized using the appropriate architectures (TAPAS and T5) designed for processing tabular data and generating text-based responses.

3. **Training Loop**:
   - The training process includes:
     - Forward pass through the model with input data.
     - Loss computation using the CrossEntropyLoss function.
     - Backpropagation to optimize the model parameters through the AdamW optimizer.
     - Losses are collected for each batch to monitor the training progress.

4. **Validation**:
   - A validation phase is integrated to assess the model's performance on unseen data after each epoch, ensuring that the model generalizes well.

5. **Error Handling**:
   - The implementation includes error handling to gracefully skip batches that encounter issues during processing.

6. **Batch Loss Tracking**:
   - The notebook maintains a list of batch losses, which can be analyzed after training to understand the model's learning behavior over time.
