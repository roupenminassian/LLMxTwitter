## Data Visualization

### Introduction

The Data Visualization section aims to bring all the prior components together into an interactive, intuitive, and informative graphical representation. This interactive visualization serves as the final deliverable, allowing users to explore the relationship between tweets based on their embeddings, clusters, and SHAP values.

### Embedding and Clustering

Before the visualization process, the tweets go through an embedding phase where each tweet is converted into a high-dimensional vector using a DistilBERT-based Sentence Transformer model. These embeddings capture the semantic content of the tweets.

The high-dimensional embeddings are then clustered using the HDBSCAN algorithm. The algorithm groups similar tweets together based on their embeddings. These clusters are essential in the subsequent color-coding in the scatter plot.

For the complete code and implementation details, refer to the [Data Visualization Notebook](https://github.com/roupenminassian/LLMxTwitter/blob/main/Data%20Visualisation/Data_Embedding.ipynb).

### Design Choices

The interactive visualization is implemented as a scatter plot, allowing users to understand the relationships between different tweets intuitively. The scatter plot is a result of dimensionality reduction techniques applied to the high-dimensional embeddings of the tweets.

- **Color-Coding**: The points in the scatter plot are color-coded based on their cluster labels, helping in the visual identification of distinct groups.
- **Interactivity**: Clicking on a point reveals additional details like the username, the text of the tweet, and a bar chart representation of SHAP values explaining the model's prediction for that particular tweet.
- **Dynamic Scaling**: The visualization is designed to be responsive, adjusting its dimensions based on the size of the user's screen.

### User Interface Elements

- **Information Button**: An information button (ℹ) is available, providing users with a walkthrough of the visualization features and how to interpret them.
- **Filter View**: A drop-down menu allows users to filter the scatter plot based on different features, providing more focused insights.

### Backend Implementation

The data for the visualization is fetched asynchronously from an API, ensuring a smooth and responsive user experience. A loading animation is shown while the data is being fetched.

### Error Handling

In case of any issues during data fetch, an error message is displayed, guiding the user on what went wrong and how to proceed.

For a live demonstration of this interactive visualization, visit the [Deployed Webpage](https://ll-mx-twitterx-visualisation.vercel.app/).
