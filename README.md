# AI-Powered-Multilingual-Detection-with-Neural-Networks

This project aims to develop a neural network-based system capable of detecting the language of a given text input from a set of 20 languages. The languages include Arabic, German, French, English, Hindi, Chinese, and many others. The neural network models used for this task capture the complexities and patterns within different languages and predict the language of each input text with high accuracy.

#### Key Features:
- **Dataset**: The dataset is sourced from Hugging Face, containing balanced samples of 3,500 texts per language, resulting in 70,000 total samples for training and 10,000 samples each for validation and testing. The dataset includes languages such as English, French, Arabic, Japanese, and more, ensuring wide coverage for multilingual classification.
  
- **Preprocessing**: Text data is transformed into numeric embeddings using the XLM-RoBERTa model. Principal Component Analysis (PCA) is then applied to reduce the dimensionality of the embeddings, improving computational efficiency while preserving 98.6% of the variance. The final dataset is scaled and prepared for input into neural networks.

- **Model Architectures**: Several models were employed to perform language classification:
  - GRU (Gated Recurrent Units)
  - LSTM (Long Short-Term Memory)
  - BiLSTM (Bidirectional LSTM)
  - 1D CNN (Convolutional Neural Network)
  - A hybrid CNN-BiLSTM model

  The CNN-BiLSTM model outperformed the others, achieving the highest accuracy of **93.91%** and a high F1-score across most language categories.

- **Performance**: The project compares various neural network models based on accuracy, loss, and F1-scores. Techniques like early stopping, dropout layers, and class weight adjustments were used to improve model generalization and avoid overfitting. Additionally, a fine-tuned large language model, XLM-RoBERTa, was also tested using zero-shot learning, achieving an impressive F1-score of 99.5%.

#### Results:
- **CNN-BiLSTM**: The best performing model with 93.91% accuracy and robust performance across all language classes.
- **1D-CNN**: Second-best model with 88.38% accuracy, demonstrating CNN's ability to efficiently extract language features.
- **GRU & LSTM**: Provided solid baseline results with accuracies of over 80%, but struggled with specific language classes like Russian.

#### Learnings:
- Incorporating BiLSTM helps in understanding languages written in both left-to-right and right-to-left formats.
- Regularization techniques, such as dropout and batch normalization, significantly help reduce overfitting and speed up convergence.
- CNN combined with BiLSTM proved to be the most effective in extracting features and capturing the sequential nature of languages.

This project demonstrates the power of neural networks in handling multilingual text classification and provides a solid foundation for future improvements in the field.

