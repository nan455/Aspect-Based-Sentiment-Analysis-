==>Aspect-Based Sentiment Analysis

Enhancing Aspect-Based Sentiment Analysis Using Large Language Models and Dependency Parsing

==>Abstract

Sentiment analysis is a pivotal task in Natural Language Processing (NLP) that identifies sentiment polarity in textual data. Traditional sentiment analysis mainly focuses on binary classification (positive/negative). However, real-world reviews and social media content often contain multiple sentiments within a single sentence. This complexity necessitates Aspect-Based Sentiment Analysis (ABSA), which identifies aspect terms and their corresponding sentiments.

Despite advancements, existing ABSA models often struggle to capture the intricate interdependencies between aspect-opinion pairs, leading to misclassifications in multi-aspect scenarios. To address these challenges, we propose an enhanced ABSA model that integrates dependency parsing with Large Language Model (LLM)-based learning to incorporate structured semantic knowledge for more effective aspect-opinion relationship extraction.

The proposed approach leverages structured feature engineering and domain-specific vocabulary filtering, ensuring more precise sentiment classification. Experimental evaluations based on average metrics from 5-fold cross-validation demonstrate that the model significantly outperforms existing baselines. 

==>Results show:

3.4% improvement in Precision

4.9% improvement in Recall

3.8% boost in F1-Score

5.6% increase in Matthews Correlation Coefficient (MCC)

3.3% reduction in False Discovery Rate
                                                      
1.7% reduction in Hamming Loss

These findings highlight the value of integrating structured semantic knowledge into ABSA, substantially improving accuracy and consistency for real-world sentiment analysis applications.

==>Dataset

This project uses the SemEval 2014 Task 4 - Aspect-Based Sentiment Analysis dataset, specifically focused on the Restaurants domain. The dataset contains customer reviews annotated with aspect terms and their sentiment polarities.

Source: Kaggle

Link: SemEval 2014 ABSA Dataset - Restaurants( https://www.kaggle.com/datasets/charitarth/semeval-2014-task-4-aspectbasedsentimentanalysis?select=Restaurants_Train_v2.csv)

==>Modules

1.Data Pre-processing
Standardizing input text: tokenization, lowercasing, noise removal.

2.Data Augmentation Using LLM
Expanding training data with synthetic samples generated via prompt-based LLM querying.

3.Adversarial Sample Generation Using LLM
Creating challenging adversarial examples to improve model robustness.

4.Dependency Parsing Using spaCy
Extracting syntactic relations between aspects and opinions.

5.Context-Based Filtering Using LLM
Enhancing aspect-opinion extraction by context validation through LLMs.

6.LLaMA-LoRA Fine-tuning with Integrated K-Fold Cross-Validation
Fine-tuning a lightweight LLaMA model using Low-Rank Adaptation (LoRA) across 5 folds to ensure model generalization and stability.
