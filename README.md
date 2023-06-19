# Databricks FAQ Chatbot

The **Databricks FAQ Chatbot** is a comprehensive AI-based system for answering user queries related to the Databricks platform. It leverages Large Language Models (LLMs) and advanced Natural Language Processing (NLP) techniques to generate human-like responses.

## Table of Contents

- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
- [System Workflow](#system-workflow)
- [How to Use](#how-to-use)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Project Overview

Our project started with the need for automating responses to repetitive customer queries. The end product is a sophisticated FAQ Chatbot that learns from the Databricks FAQ dataset, uses a fine-tuned Wizard-Vicuna model, and integrates seamlessly with any customer service platform. 

## Getting Started

The following instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- [Databricks](https://databricks.com/)
- [Hugging Face](https://huggingface.co/)
- [Google Colab](https://colab.research.google.com/)

### Installing

- Clone the repo
```sh
git clone https://github.com/sumitsahaykoantek/koantekDatabricksHackathon.git

Install necessary libraries
```sh
pip install -r requirements.txt
```
## System Workflow

Our development process involves the following steps:

1. **Data Collection**: Extract FAQ data from the Databricks website.
2. **Topic Modeling**: Use the Hugging Face's ChatGPT model for topic modeling on the collected dataset.
3. **Data Augmentation**: Paraphrase the questions with Hugging Face's Paraphrase models.
4. **Data Classification**: Classify the generated questions using the Databricks AutoML system.
5. **Embeddings Creation**: Create embeddings for questions, answers, and categories using Hugging Face's Sentence Transformers.
6. **Data Storage**: Store these embeddings in a database such as ChromaDB for easy retrieval.

Real-time inferencing involves the following steps:

1. **Input Processing**: Create embeddings for user-input questions.
2. **Query Classification**: Classify the question with the AutoML model.
3. **Similarity Check**: Compare the input question with stored questions in the database.
4. **Answer Retrieval**: If an exact match is found, display the corresponding answer. If not, retrieve similar questions and their answers.
5. **Response Generation**: Feed the input question, similar questions, categories, and answers into the fine-tuned GPT-4 based language model.
6. **Answer Comparison**: Employ fuzzy matching to compare the model's answer with the original answers in the database.
7. **Answer Display**: Display the best-matched answer to the user.

## How to Use
Detailed instructions for usage can be found in our User Guide. It explains how to input a question, interpret the output, and handle errors or issues.

## Future Enhancements
We plan to expand the training dataset continually, ensuring coverage for a wide range of customer queries. We also intend to explore live streaming man-in-the-middle QA systems to correct and improve the chatbot's responses in near-real time.

## Contributing
We welcome contributions to improve this project. Please refer to CONTRIBUTING.md for details on our code of conduct
