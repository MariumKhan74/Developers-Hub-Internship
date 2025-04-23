# Report on Summarization Using CNN/Daily Mail Dataset

## 1. Dataset Description and Preprocessing Steps

The **CNN/Daily Mail** dataset is a collection of news articles paired with corresponding human-written summaries, commonly used for text summarization tasks. This dataset is particularly useful for evaluating **abstractive** summarization models, as it contains a diverse set of topics, including politics, business, health, and international affairs.
Dataset: https://www.kaggle.com/datasets/gowrishankarp/newspaper-text-summarization-cnn-dailymail
The dataset was too large to upload on github even after zipping.

### Dataset Description:
- **Content**: The dataset contains news articles from CNN and Daily Mail websites, each paired with a human-written summary.
- **Size**: It contains over 300,000 articles with corresponding summaries, making it a large-scale dataset suitable for training deep learning models.
- **Splits**: The dataset is divided into:
  - **Training set**: Used for training models.
  - **Validation set**: Used for tuning hyperparameters and preventing overfitting.
  - **Test set**: Used for final evaluation after training.

### Preprocessing Steps:
To prepare the dataset for model training, the following steps were carried out:
1. **Text Cleaning**: Articles and summaries were cleaned by removing special characters, excessive whitespace, and unwanted symbols.
2. **Tokenization**: Articles and summaries were tokenized using the **T5 tokenizer** to convert text into numerical tokens that can be processed by the model.
3. **Padding and Truncation**: Sentences longer than the model’s maximum input length (512 tokens for T5) were truncated, while shorter sentences were padded to the required length to ensure uniform input sizes.
4. **Format Conversion**: Text data was converted into tensors, and attention masks were applied to handle padding tokens during model training.

The preprocessed dataset is now ready to be used for training summarization models.

---

## 2. Models Implemented with Rationale for Their Selection

### Models Used:
1. **T5 (Text-to-Text Transfer Transformer)**:
   - **Rationale for Selection**: T5 is a powerful transformer-based model specifically designed for text-to-text tasks, making it ideal for summarization. It can perform a wide range of tasks by framing them as text generation problems, including summarization, translation, and question answering.
   - **Pre-trained Version**: For this task, the **T5-small** version was chosen due to its smaller size, which allows for quicker experimentation and resource efficiency, though larger versions like T5-base or T5-large could be used for improved performance.

2. **BART (Bidirectional and Auto-Regressive Transformers)** (Optional for future comparison):
   - **Rationale for Selection**: BART is another popular model for summarization tasks, particularly for abstractive summarization. It combines the strengths of BERT and GPT, allowing for bidirectional context encoding and autoregressive generation.

Both models are capable of performing abstractive summarization, where the generated summary is not simply a subset of the original text but a paraphrased version that captures the essence of the article.

---

## 3. Key Insights and Visualizations

### Key Insights:
- **Pre-trained Models Are Effective**: Using pre-trained models like T5 significantly reduces the training time and resources required for summarization tasks. Fine-tuning such models on the CNN/Daily Mail dataset allows them to generate high-quality summaries.
- **Challenges in Abstractive Summarization**: Abstractive summarization is challenging because it requires models to understand the context of the article and generate coherent, meaningful summaries that are not just direct extracts from the article.
- **Performance**: The fine-tuned T5 model was able to generate summaries that were meaningful and captured the essence of the articles. However, further fine-tuning on a larger dataset or using a larger version of T5 could improve summary quality.

### Visualizations:
- **Training Loss Curves**: A plot of training and validation loss over epochs helps to visualize the model's convergence and performance.
- **ROUGE Score Comparison**: A bar chart comparing ROUGE scores (e.g., ROUGE-1, ROUGE-2, and ROUGE-L) between different models (T5 vs. BART or other baselines) helps evaluate model performance quantitatively.
- **Word Cloud for Summaries**: A word cloud generated from the summaries produced by the model can help visualize the most common terms in the generated summaries.

---

## 4. Challenges Faced and Solutions

### 1. **Data Preprocessing**:
   - **Challenge**: The CNN/Daily Mail dataset contains long and complex news articles, which required efficient tokenization and truncation to fit within the model’s input limits.
   - **Solution**: Implemented tokenization and padding with truncation to ensure that all input articles fit within the model’s 512-token input limit while retaining important content in the summaries.

### 2. **Model Overfitting**:
   - **Challenge**: Fine-tuning the pre-trained T5 model on the CNN/Daily Mail dataset led to overfitting, where the model performed well on the training set but poorly on the validation and test sets.
   - **Solution**: Employed early stopping during training to prevent overfitting and adjusted the batch size and learning rate for better generalization. Additionally, used data augmentation techniques like random shuffling of sentences in the articles.

### 3. **Coherence of Generated Summaries**:
   - **Challenge**: Generating coherent and concise summaries was difficult, especially for articles that contained diverse information.
   - **Solution**: Fine-tuned the T5 model with careful attention to the training process and used ROUGE scores to evaluate the quality of summaries. Furthermore, manual evaluation was carried out to ensure the generated summaries were relevant, clear, and concise.

### 4. **Computational Constraints**:
   - **Challenge**: The large size of the CNN/Daily Mail dataset and the complexity of transformer-based models made the training process resource-intensive.
   - **Solution**: Utilized the **T5-small** model for quicker experimentation and to reduce computational load. Training was done on GPUs to speed up the process.

---

## 5. Conclusion

This project demonstrates the power of transformer-based models, such as T5, in performing abstractive summarization on large-scale datasets like CNN/Daily Mail. By preprocessing the data, fine-tuning the model, and evaluating it using both automated metrics (like ROUGE) and manual assessments, we were able to generate meaningful summaries. While challenges such as overfitting and coherence were encountered, solutions like early stopping, hyperparameter tuning, and careful model evaluation helped mitigate these issues. Future improvements could include using larger models, such as T5-base or BART, and further refining the summarization process for better coherence and fluency.
