# LLM-Sentiment-Analysis
Sentiment Analysis on Amazon Product Reviews using BERT

Voice of the Customer (VOC)
This project focuses on understanding the Voice of the Customer (VOC) by analyzing product reviews from Amazon. VOC is about capturing what customers are really saying about a product or service. By analyzing review data, I aimed to extract both functional and non-functional feedback such as performance, usability, and cost-related concerns that customers express through their reviews.

Project Overview
I built and fine-tuned a pre-trained transformer model (bert-base-uncased) to classify Amazon reviews into three sentiment categories:

Negative 😠

Neutral 😐

Positive 😊

The goal was to extract meaningful insights from customer feedback to support better product decisions and experience improvements.

What I Did
 I studied foundational papers like Attention is All You Need and BERT: Pre-training of Deep Bidirectional Transformers to understand the theory.

 I explored and cleaned the Amazon reviews dataset, focusing on reviewText and overall rating fields.

 I mapped ratings into sentiment classes and cleaned the text using regex-based preprocessing.

 I fine-tuned BERT using Hugging Face’s Trainer API with an 80/20 train-validation split.

 I evaluated the model with metrics like Accuracy, F1-score, and Confusion Matrix.

 I built a custom prediction function that returns sentiment and confidence scores for any input text.

 Model Details
  Parameter	Value
  Model	bert-base-uncased
  Sequence Length	256 tokens
  Epochs	3
  Batch Size	16
  Sentiment Classes	3 (Neg, Neu, Pos)

  Results
I achieved an overall accuracy of ~89%, with high precision for Positive and Negative classes. Neutral class performance was lower due to its ambiguous nature and limited samples in the dataset.
The model accurately predicted real-world review sentiments and returned confidence scores. I tested it with multiple sample texts, showing high confidence for clearly expressed opinions.

Future Work
Improve Neutral class with class balancing or data augmentation

Experiment with alternative models like RoBERTa or DistilBERT

Deploy the model via Flask or Streamlit for user interaction


License

This project is licensed under the MIT License.


