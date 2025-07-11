# LLM-Sentiment-Analysis
Sentiment Analysis on Amazon Product Reviews using BERT

<img width="422" height="180" alt="image" src="https://github.com/user-attachments/assets/f82a7764-41c5-4e55-8c82-d04af5203abc" />


In this project, I built a sentiment analysis model using the pre-trained transformer bert-base-uncased. My goal was to extract the Voice of the Customer (VOC) from Amazon product reviews capturing what users are really saying about a product’s performance, cost, and usability. VOC is vital in customer experience management and helps drive product improvements, making it a meaningful real-world application of NLP.
To tackle this, I fine-tuned BERT to classify reviews into Negative 😠, Neutral 😐, and Positive sentiment 😊, using the star ratings provided by customers. Since BERT understands word meaning in full context by reading text bidirectionally, it is well-suited for interpreting real-world customer opinions.


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


<img width="539" height="273" alt="image" src="https://github.com/user-attachments/assets/f32ca9c1-e766-4d2a-b294-6968e5438af5" />


The model accurately predicted real-world review sentiments and returned confidence scores. I tested it with multiple sample texts, showing high confidence for clearly expressed opinions.

Future Work
Improve Neutral class with class balancing or data augmentation

Experiment with alternative models like RoBERTa or DistilBERT

Deploy the model via Flask or Streamlit for user interaction


License

This project is licensed under the MIT License.


