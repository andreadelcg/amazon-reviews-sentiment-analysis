amazon-reviews-sentiment-analysis
-----------

Project Title: Amazon Reviews Sentiment Analysis and Clustering

Introduction:
This project focuses on analyzing and classifying sentiments in Amazon reviews from the Electronics category for the year 2023. The goal is to employ advanced natural language processing (NLP) techniques, particularly using a BERT model, to accurately determine the sentiment of the reviews. Clustering methods are also used to group similar reviews and identify common themes and opinions.

Problem Statement:
- Traditional sentiment analysis methods often fail to capture nuanced sentiments in large datasets.
- Accurate sentiment analysis is crucial for understanding customer feedback, improving products, and enhancing customer satisfaction.
- There is a need for a robust and scalable solution to analyze large volumes of review data efficiently.

Solution Outline:
1. **Data Collection and Filtering**
   - Load the dataset from the McAuley-Lab/Amazon-Reviews-2023. (https://huggingface.co/datasets/McAuley-Lab/Amazon-Reviews-2023/tree/main) the name of the file is asin2category.json
   - Filter reviews to include only those from the year 2023.

2. **Preprocessing**
   - Tokenize, remove stop words, and lemmatize the text using NLTK.
   - Combine the title and text of each review for analysis.

3. **Sentiment Analysis**
   - Initialize a BERT-based sentiment analysis pipeline.
   - Split text into manageable chunks and compute sentiment scores for each chunk.
   - Aggregate sentiment scores for each review.

4. **Clustering**
   - Perform KMeans clustering on sentiment scores.
   - Classify clusters into Positive, Negative, and Neutral sentiments based on cluster centers.

5. **Evaluation**
   - Create true sentiment labels based on review ratings.
   - Calculate evaluation metrics: accuracy, precision, recall, and F1-score.
   - Generate a confusion matrix for visualizing model performance.

6. **Visualization**
   - Histograms for sentiment score distribution.
   - Bar plots for common words and phrases in positive and negative reviews.
   - Analysis of products with the highest and lowest mean sentiment scores.

Examples of Input and Output:
- **Input:** 
  - Amazon review data including title, text, and rating.
- **Output:**
  - Sentiment scores for each review.
  - Clusters of reviews labeled as Positive, Negative, or Neutral.
  - Evaluation metrics and visualizations.

Setup and Run Instructions:

1. **Clone the Repository:** git clone https://github.com/andreadelcg/amazon-reviews-sentiment-analysis.git --- cd amazon-reviews-sentiment-analysis
2. **Install Required Packages:**
3. **Download Dataset:**
- Ensure you have access to the McAuley-Lab/Amazon-Reviews-2023 dataset.
- Modify the script to point to your local or remote dataset source.

4. **Run the Analysis:**
- Open the Python script or Jupyter notebook.
- Follow the steps to load, preprocess, and analyze the data.
- Visualizations will be generated at the end of the script.

Dataset:
- The dataset used in this project is sourced from McAuley-Lab/Amazon-Reviews-2023, specifically the raw_review_Electronics subset.
- Ensure proper access and download permissions for the dataset.

Future Developments:
- Scaling the analysis to process the entire dataset for more comprehensive insights.
- Exploring different NLP models and techniques to improve sentiment classification accuracy.
- Integrating additional features such as product metadata to enhance clustering and analysis.
- Developing a web-based interface to visualize and interact with the analysis results.

Contributors:
- Andrea Del Carpio
- Ryan Eakins
