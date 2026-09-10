# hiver-customer-support-ai-agent
# Hiver Customer Support AI Agent

## Project Overview

This project builds an AI-based customer support intent classification system.

The system classifies customer support messages into:

- delivery_issue
- refund_issue
- payment_issue
- order_issue
- account_issue
- technical_issue
- other

## Dataset

Customer support conversations from the Customer Support on Twitter dataset were used for the project.

## Model

A TF-IDF based text classification model was trained to predict customer support intents.

## Evaluation

The project includes evaluation of model predictions and comparison with human/LLM-based assessment.

## Files

- `your_completed_notebook.ipynb` — complete project implementation
- `customer_support_predictions.csv` — final predictions
- `customer_support_intent_model.pkl` — trained model
