# Hiver Customer Support AI Agent

## 1. Project Overview

This project builds a customer-support AI agent for AmazonHelp.

The system:
1. Classifies customer-support messages into support intents.
2. Retrieves relevant historical AmazonHelp replies.
3. Produces a grounded draft reply.
4. Decides whether the case can be auto-handled or should be escalated.
5. Evaluates the classifier and reply-quality process.

## 2. Dataset

Dataset:
Customer Support on Twitter

Target brand:
AmazonHelp

The project uses a hand-labelled golden evaluation set of 196 examples.

## 3. Intent Taxonomy

The intent categories used are:

- delivery_issue
- refund_issue
- payment_issue
- order_issue
- account_issue
- technical_issue
- other

## 4. System Pipeline

Customer message
→ Intent classification
→ Historical reply retrieval
→ Grounded draft reply
→ Escalation decision

## 5. Model

The intent classifier uses:

- TF-IDF features
- unigrams and bigrams
- Logistic Regression

## 6. Evaluation

The evaluation includes:

- held-out accuracy
- weighted precision
- weighted recall
- weighted F1
- majority-class baseline
- keyword baseline
- confusion matrix
- LLM-as-judge
- human-vs-LLM agreement using Cohen's kappa

## 7. Failure Analysis

The five main failure modes are discussed in the project report.

## 8. Reproduction

Open the notebook in Google Colab and run the cells from top to bottom.

The notebook downloads the dataset, prepares the golden set, trains the classifier, generates predictions, retrieves historical replies, performs escalation decisions, and runs evaluation.

## 9. Output Files

- customer_support_predictions.csv
- customer_support_intent_model.pkl
- customer_support_evaluation.csv

## 10. Limitations

The golden set is relatively small and may not represent every possible customer-support conversation.

Classification accuracy alone does not measure reply helpfulness or escalation quality.

## 11. Future Work

With additional development time, the system could be improved with a larger golden set, better intent boundaries, stronger reply evaluation, and more robust escalation policies.
