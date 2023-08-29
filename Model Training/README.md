## Model Training:

[Model_Training_and_Validation.ipynb](https://github.com/roupenminassian/LLMxTwitter/blob/main/Model%20Training//Model_Training_and_Validation.ipynb)

After data preparation, the core of this project lies in training a machine learning model that can accurately classify tweets as factual or misinformation. Below is an outline of the model training process.

### Model Architecture: Transformers Library

We use a pretrained model from Hugging Face's Transformers library, specifically `Twitter/twhin-bert-large`.

- **Model Type**:
  - BERT (Bidirectional Encoder Representations from Transformers)
- **Tokenizer**:

  - AutoTokenizer from Hugging Face Transformers

- **Configuration**:
  - Number of Labels: 2 (factual, misinformation)

### Training Process

#### Tokenization

- Utilizes the `AutoTokenizer` to tokenize the text data into a format suitable for BERT.
- Padding, truncation, and tensor conversion are performed.

#### Model Compilation

- The model is an instance of `AutoModelForSequenceClassification` from the Transformers library.
- Label to ID and ID to label mappings are specified.

#### Metrics

- F1 score is used as the evaluation metric, calculated using a custom `compute_metrics` function.

#### Training Configuration

- Batch Size: 16
- Learning Rate: 2e-5
- Weight Decay: 0.01
- Number of Epochs: 3
- Logging Steps: 250

### Libraries and Tools

- Transformers for model and tokenizer
- Hugging Face's Trainer for training pipeline
- Custom metric evaluation
