# Acme-Corp_SentimentAnalysis

A Deep Learning model for classifying semtiments

## Business Scenario
In today's competitive e-commerce environment, understanding customer sentiment is more crucial than ever. With the rise of online reviews, social media feedback, and customer interactions, businesses are inundated with data that can significantly impact their strategies. However, manually sifting through this information can be overwhelming and inefficient.

To tackle this challenge, Acme Corp, a leader in the online retail sector, recognizes the need for an innovative solution to streamline sentiment analysis. By leveraging advanced artificial intelligence techniques like Natural Language processing (NLP), the company aims to automate the process of analyzing customer reviews and transforming raw feedback into valuable insight by leveraging the power of transformers.

This AI model will provide significant support in:

- Real-time Insights: Gain immediate understanding of customer sentiment, enabling proactive responses to feedback.
- Data-Driven Decisions: Inform product development and marketing strategies based on comprehensive analysis of customer opinions.
- Enhanced Customer Engagement: Identify and address negative sentiments quickly, improving overall customer satisfaction and loyalty.
- Operational Efficiency: Reduce the manual effort required for sentiment analysis, allowing team members to focus on higher-value tasks.
Through this project, Acme Corp will harness the power of AI to turn customer feedback into actionable insights, driving business growth and improving customer experiences.

## Dataset
The dataset used in this project is SST2 Dataset by Stanford university **hosted on Hugging face**, it contains 70,042 sentiments classified to 67349 for training , 872 for validation and 1821 for testing.


## Model Architecture
The model used in this project is DistilBERT, a smaller, faster, and cheaper variant of BERT, designed to retain much of BERT’s accuracy while being more efficient. It is fine-tuned on the sentiment dataset, making it capable of predicting sentiment with high accuracy.

Key features of the architecture:

- Pre-trained DistilBERT model from Hugging Face’s transformer library.
- Fine-tuned using a sentiment analysis dataset.
- Integrated with linear layers for classification tasks.


## Training
The model is trained using the following configuration:

- Optimizer: AdamW
- Loss Function: CrossEntropyLoss
- Learning Rate: Dynamically adjusted using a linear learning rate scheduler with warmup.
  
Training Process:
- Loading the training and validation sets.
- Training over 2 epochs (can be extended based on the dataset and performance).
- Evaluation on the validation set after each epoch.
- Early stopping to avoid overfitting, though not used in this example as the training process is quick.

## Results
The final model achieved the following performance:

Train Accuracy: 97.34%
Validation Accuracy: 91.28%

These results demonstrate the model's effectiveness in classifying sentiments to either positive or negative.

