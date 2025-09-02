# Zero Shot Text Classification with Explainability

This project shows how to classify text into categories **without any training data** using Hugging Face transformers.  
Instead of building a dataset and training a model, you can simply provide:
- A piece of text (e.g., a news headline, product review, or support ticket)  
- A list of candidate labels in plain English  

The model then scores each label and predicts the most relevant one - a process known as **zero-shot classification**.

## What You’ll Find in the Notebook
- **Zero-Shot Classification**  
  Uses [`facebook/bart-large-mnli`](https://huggingface.co/facebook/bart-large-mnli) to map text to user-defined labels.  

- **Confidence Scoring & Visualization**  
  Displays probabilities for each label and plots them using Matplotlib for easy interpretation.  

- **Explainability**  
  Generates short natural-language explanations for predictions using [`tiiuae/falcon-rw-1b`](https://huggingface.co/tiiuae/falcon-rw-1b).  

## Technologies Used
- [Transformers](https://huggingface.co/docs/transformers) (BART & Falcon models)  
- [PyTorch](https://pytorch.org/)  
- [Matplotlib](https://matplotlib.org/)  

## Example

**Input text:**  

A new drug trial shows promising results in treating early-stage Alzheimer's disease.

**Candidate labels:**  

["technology", "finance", "health", "sports", "politics"]

**Model prediction:**  

health → 0.60,
technology → 0.34,
finance → 0.02,
sports → 0.02,
politics → 0.01

The model correctly identifies the text as related to **health**, even though it was never trained on this label.


This notebook is a simple, end-to-end example of how **pretrained language models** can be applied for text classification and explanation, without fine-tuning or labeled datasets.
