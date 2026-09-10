# Decision Log

## 1. Target brand selection
I selected AmazonHelp as the target brand because it provides a large collection of customer-support conversations.

## 2. Golden-set size
I created a 196-example hand-labelled golden set, keeping the evaluation set within the required 150–250 example range.

## 3. Intent taxonomy
I used a compact set of support intents rather than attempting to model every possible customer issue.

## 4. Hand labelling
I used human labelling for the golden set so that evaluation would not depend entirely on model-generated labels.

## 5. Text representation
I used TF-IDF features because they provide a simple and interpretable baseline for short customer-support messages.

## 6. N-grams
I used unigram and bigram features to capture both individual keywords and short phrases.

## 7. Classifier
I used Logistic Regression because it is efficient, reproducible, and appropriate for sparse TF-IDF features.

## 8. Baseline comparison
I included a majority-class baseline and a keyword baseline to determine whether the trained classifier provides meaningful improvement.

## 9. Historical reply grounding
I used historical AmazonHelp replies as grounding material for generating support drafts rather than relying only on unconstrained generation.

## 10. Similarity retrieval
I used TF-IDF cosine similarity to retrieve relevant historical customer/reply examples.

## 11. Escalation
I included an explicit escalation decision rather than assuming every request should be automatically handled.

## 12. Escalation reason
The system records a reason for escalation so that the decision is explainable.

## 13. LLM judge
I used an LLM judge to evaluate reply quality in addition to classification metrics.

## 14. Human agreement
I compared LLM-judge scores with human scores using Cohen's kappa.

## 15. Failure analysis
I examined classification errors to identify weaknesses and potential improvements.
