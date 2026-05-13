# ChatbotLLM
# README.md

## AI-Powered E-commerce Complaint Resolution Bot using Fine-Tuned LLM

### Project Overview

This project focuses on developing an industry-specific AI chatbot for the Retail and E-commerce domain using a fine-tuned Large Language Model (LLM). The chatbot is capable of understanding customer complaints, identifying the complaint category, and predicting urgency levels automatically.

The project was developed using TinyLlama, Hugging Face Transformers, LoRA fine-tuning, and deployed using Hugging Face Spaces with Gradio.

---

# Problem Statement

E-commerce companies receive a large number of customer complaints daily related to:

* Payment failures
* Refund delays
* Order tracking issues
* Technical issues
* Product defects
* Shipping problems

Manually handling and prioritizing these complaints is time-consuming and resource-intensive.

This project aims to automate:

* Complaint understanding
* Complaint classification
* Urgency prediction
* Customer support assistance

using an AI-powered Large Language Model.

---

# Features

* Industry-specific AI chatbot
* Complaint category prediction
* Urgency level prediction
* Fine-tuned TinyLlama model
* Real-time chatbot interface
* Public deployment using Hugging Face Spaces
* Lightweight LoRA fine-tuning

---

# Technologies Used

| Technology                | Purpose                         |
| ------------------------- | ------------------------------- |
| Python                    | Programming Language            |
| Pandas                    | Data Processing                 |
| PyTorch                   | Deep Learning Framework         |
| Hugging Face Transformers | LLM Framework                   |
| TinyLlama                 | Pre-trained Language Model      |
| PEFT                      | Parameter Efficient Fine-Tuning |
| LoRA                      | Lightweight Fine-Tuning         |
| Google Colab              | Model Training                  |
| Gradio                    | Chatbot UI                      |
| Hugging Face Spaces       | Deployment                      |

---

# Dataset Information

The dataset contains customer complaints from the e-commerce industry.

## Dataset Columns

| Column    | Description             |
| --------- | ----------------------- |
| Complaint | Customer complaint text |
| Category  | Complaint category      |
| Urgency   | Complaint priority      |
| target    | Combined label          |

---

# Example Dataset Entry

## Complaint

```text
Transaction failed but my card got debited anyway.
```

## Category

```text
Payments
```

## Urgency

```text
Immediate
```

---

# Model Used

## TinyLlama

```text
TinyLlama/TinyLlama-1.1B-Chat-v1.0
```

Reason for selection:

* Lightweight
* GPU efficient
* Suitable for Google Colab T4 GPU
* Faster training
* Good conversational performance

---

# Project Workflow

```text
Dataset Collection
        ↓
Data Cleaning
        ↓
Instruction Dataset Creation
        ↓
TinyLlama Fine-Tuning using LoRA
        ↓
Model Training on Google Colab
        ↓
Model Upload to Hugging Face
        ↓
Gradio Chatbot Deployment
        ↓
Public AI Chatbot
```

---

# Data Preprocessing

The dataset was:

* cleaned,
* duplicates removed,
* null values removed,
* converted into instruction-response format.

Example:

## Instruction

```text
Customer Complaint:
Transaction failed but card got debited.

Identify the issue category and urgency level.
```

## Response

```text
Category: Payments
Urgency: Immediate
```

---

# Fine-Tuning Process

The model was fine-tuned using:

* LoRA (Low-Rank Adaptation)
* PEFT (Parameter Efficient Fine-Tuning)

Benefits:

* Reduced GPU memory usage
* Faster training
* Efficient fine-tuning on free T4 GPU

Training was performed using:

* Hugging Face Transformers
* SFTTrainer
* PyTorch

---

# Deployment

The chatbot was deployed using:

* Hugging Face Model Hub
* Hugging Face Spaces
* Gradio

The deployment allows users to interact with the chatbot through a web interface.

---

# Example Output

## Input

```text
My order arrived empty.
```

## Output

```text
Category: Order Issues
Urgency: High
```

---

# Challenges Faced

* CUDA memory issues
* bitsandbytes dependency conflicts
* Gradio timeout errors
* Hugging Face deployment configuration issues

These were resolved through:

* LoRA optimization
* batch size tuning
* lightweight deployment setup
* adapter-based model loading

---

# Future Improvements

Possible future enhancements:

* Sentiment analysis
* Multi-turn conversations
* Auto-generated support responses
* CRM integration
* Multilingual support
* Retrieval-Augmented Generation (RAG)

---

# Business Impact

This system can help e-commerce companies:

* automate customer complaint analysis,
* reduce support workload,
* prioritize urgent tickets,
* improve response speed,
* enhance customer experience.

---

# Live Demo

## Hugging Face Space

```text
https://huggingface.co/spaces/Kashfur/ecommerce-llm-chatbot
```

## Hugging Face Model Repository

```text
https://huggingface.co/Kashfur/ecommerce-llm-bot
```

---

# Author

Kashfur Rahman Khan

---

# Final Summary

This project demonstrates the complete end-to-end implementation of an industry-specific Large Language Model chatbot, including dataset preprocessing, LLM fine-tuning, GPU-based training, cloud deployment, and real-world AI application development for the Retail and E-commerce industry.
