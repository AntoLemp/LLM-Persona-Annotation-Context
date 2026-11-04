# LLM Persona Annotation & Context Study

## Overview
This project investigates whether Large Language Models (LLMs) instructed to adopt specific personas rate the toxicity of online comments similarly to human annotators. Additionally, it explores how providing a conversation as context shifts the model's judgment. 

This repository contains the work for Assignment 1, utilizing the `SynDisco` library to generate synthetic discussions and perform automated annotations using a 4-bit quantized Qwen2.5-3B model.

## Project Structure
The pipeline is divided into seven main parts (A-G):
*   **A & B: Human Baseline** - Manual annotation of 20 online comments on a 1-5 toxicity scale (with evidence extraction).
*   **C: Conversation Generation** - Using a pool of diverse character personas to generate a discussion about each comment.
*   **D & E: Model Annotation** - A structured $2\times2\times2$ persona grid (Gender $\times$ Politics $\times$ Education) rates the 20 comments under two conditions: *With Context* (reading the conversation first) and *Without Context* (reading the comment alone).
*   **F: Agreement Analysis** - Calculating numerical (exact 1-5) and categorical (civil vs. toxic) agreement to compare the models against the baseline, and comparing the personas against one another.
*   **G: Story & Results** - Interpretations of the data, determining which persona aligns closest with human ratings, and measuring the impact of context.

## Technologies Used
*   **Python 3** (pandas, numpy, seaborn, matplotlib)
*   **Google Colab** (T4 GPU)
*   **SynDisco** (Synthetic Discussion)
*   **HuggingFace** (`unsloth/Qwen2.5-3B-Instruct-bnb-4bit`)
