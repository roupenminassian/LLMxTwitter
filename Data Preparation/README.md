## Data and Preprocessing

Understanding the complex dynamics of misinformation on social media platforms requires a robust and methodologically sound approach to data collection and preprocessing. In this project, we focus on two distinct datasets to achieve our objectives.

### Dataset for Model Fine-Tuning: `[FineTuning_Dataset.ipynb](./Code/FineTuning_Dataset.ipynb)`

The first dataset serves as the foundation for training a machine learning model capable of discerning factual information from misinformation. This dataset comprises a balanced mix of factual and misleading tweets, articles, and other forms of text data.

- **Data Sources**:

  - Verified News Portals
  - Fact-Checked Tweets
  - Academic Journals

- **Preprocessing Steps**:
  - Text Cleaning: Removal of irrelevant characters, links, and formatting.
  - Tokenization: Breaking down text into individual words or phrases.
  - Labeling: Tagging each data point as 'Factual' or 'Misinformation'.

### Dataset for Model Application: `[Classification_Dataset.ipynb](https://github.com/roupenminassian/LLMxTwitter/blob/main/Data Preparation/Classification_Dataset.ipynb)`

The second dataset consists of raw tweets collected during the period of the Nagorno-Karabakh conflict. The purpose of this dataset is for the model to apply its learned knowledge in classifying tweets as either factual or misinformation.

- **Data Sources**:
  - Twitter API: Tweets containing specific hashtags or mentions related to the conflict.
- **Preprocessing Steps**:
  - Data Extraction: Collecting tweets via API calls.
  - Text Normalization: Standardizing text for uniform analysis.
  - Feature Engineering: Extracting relevant features like hashtags, mentions, and sentiment.
