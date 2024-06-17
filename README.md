# Comparative analysis of LoRA fine-tuned BERT and DistilBERT for detecting AI-generated texts

📝 Classify the essay to AI-generated and human texts. <br>
🤖 Investigate the performance of BERT with its lighter variation, DistilBERT, when fine-tuning using the LoRA method.

<img src="https://github.com/phanuphatsrisukhawasu/detecting-ai-generated-texts-with-distilbert/blob/b8bb600488d3ef0108c355936d2ebdf4154cf534/thumbnail.jpg" alt="Graphical Abstract">

[![Python](https://img.shields.io/static/v1?message=Python&logo=python&labelColor=5c5c5c&color=3776AB&logoColor=white&label=%20)](https://www.python.org/)
[![PyTorch](https://img.shields.io/static/v1?message=PyTorch&logo=pytorch&labelColor=5c5c5c&color=EE4C2C&logoColor=white&label=%20)](https://pytorch.org/)
[![Jupyter](https://img.shields.io/static/v1?message=Jupyter&logo=jupyter&labelColor=5c5c5c&color=F37626&logoColor=white&label=%20)](https://jupyter.org/)
[![Hugging Face](https://img.shields.io/static/v1?message=Hugging%20Face&logo=huggingface&labelColor=5c5c5c&color=FF6F00&logoColor=white&label=%20)](https://huggingface.co/)

Note: I provided all codes used in this project on the Jupyter Notebook [here](https://github.com/phanuphatsrisukhawasu/detecting-ai-generated-texts-with-distilbert/blob/76f7ea5319a5ff65f0ceda2200ca353bda064fc9/distilbert_lora_ft.ipynb).

## 🔎 Motivation

The recent advancement in generative AI has significantly impacted every industry. However, concerns about the ethical usage of AI-generated texts also arose. In light of these concerns, developing a tool to detect AI-generated texts is crucial and imperative to prevent AI from being utilized for fraud. As a result, most online tools need to be more accurate, reliable, and lightweight.

## 🛠️ Methods

In this project, I investigate the performance of fine-tuned BERT with its lighter variation, DistilBERT, for classifying human and AI texts. Both models were carried out by the Hugging Face Transformers. They were fine-tuned using LoRA (Low-Rank Adaptation) for the binary classification tasks.

The dataset used in this project was compiled from Kaggle (see the reference). In this dataset, there are almost 27k instances of essays written by humans and LLM. The training was done on Google Colab using T4 GPU. I evaluate the performance of both models using simple accuracy metrics.

## 📊 Key Findings

The findings indicate that after training for one epoch, the performance of both models is comparatively the same. However, I found that DistilBERT's training time (12 minutes 13 seconds) was much faster than that of BERT (23 minutes 45 seconds). The detailed performance, including training and validation losses, are shown in the table below. Despite its fewer parameters, the results suggest that DistilBERT could be as good as BERT for this task.

## **🧑🏻‍🏫 References**

LLM - Detect AI Generated Text Dataset. (2023, November 8). Kaggle. https://www.kaggle.com/datasets/sunilthite/llm-detect-ai-generated-text-dataset
