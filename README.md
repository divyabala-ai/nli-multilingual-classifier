# Natural Language Inference - Watson Project

## Overview
This project predicts whether a pair of sentences are in *entailment*, *neutral*, or *contradiction* relationship using the [Contradictory, My Dear Watson dataset](https://www.kaggle.com/competitions/contradictory-my-dear-watson).  
The workflow includes multilingual text preprocessing, exploration, and training multiple NLP models — BERT (XLM-RoBERTa), GPT-2 Medium, and Ollama — to compare their performance.

## Project Workflow
1. **Data Exploration**  
   - Reviewed dataset structure, language distribution, and class balance.  
   - Identified multilingual nature of data and class distribution (~balanced).

2. **Data Preprocessing**  
   - Tokenized text using model-specific tokenizers (BERT, GPT-2).  
   - Encoded labels into numerical format.  
   - Prepared datasets for PyTorch DataLoader.

3. **Model Training**  
   - **XLM-RoBERTa (BERT)**: Fine-tuned multilingual transformer for sequence classification.  
   - **GPT-2 Medium**: Adapted a generative model for classification via token classification head.  
   - **Ollama**: Used local LLM inference API for classification.

4. **Evaluation**  
   - Generated classification reports for each model.  
   - Compared precision, recall, and f1-score across classes.

5. **Model Comparison & Findings**  
   - **BERT** achieved the highest accuracy (75%) with balanced precision and recall.  
   - **GPT-2** achieved 63% accuracy, struggling with the *neutral* class.  
   - **Ollama** achieved 55% accuracy, with high precision for *contradiction* but low recall.

## Technologies Used
- Python  
- Pandas, NumPy  
- PyTorch, Transformers (Hugging Face)  
- Scikit-learn  
- Matplotlib, Seaborn  

## Dataset
Contradictory, My Dear Watson dataset from Kaggle:  
https://www.kaggle.com/competitions/contradictory-my-dear-watson
