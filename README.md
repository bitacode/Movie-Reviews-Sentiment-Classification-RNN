# Sentiment Classification with RNN

## Introduction

A Recurrent Neural Network (RNN) is a type of artificial neural network specifically designed to handle sequential data by maintaining a memory of previous inputs. Unlike traditional feedforward neural networks, where the input moves in one direction (from input to output), RNNs allow information to persist by introducing connections that loop back on themselves.

RNNs are widely used in tasks that require understanding of context and sequence, such as natural language processing, time-series forecasting, and speech recognition.

## Dataset

This experiment employs a dataset that comprises movie reviews. The dataset used for model training is publicly available on Kaggle and accessible for free on the internet. The link to this data is [Kaggle Rotten Tomatoes EDA](https://www.kaggle.com/code/stefanoleone992/rotten-tomatoes-eda). The movie reviews were annotated using [RoBERTa](https://github.com/bitacode/Labeling-Dataset-For-Sentiment-Analysis.git).

## Results

The RNN model training results show a training loss of 1.1826 and a training accuracy of 0.6903, indicating that the model is learning but has not yet achieved high accuracy, with around 69% correct classifications on the training data. However, the validation loss of 1.6149 and validation accuracy of 0.5905 suggest that the model is struggling more on the validation data, with lower performance (about 59% accuracy). The higher validation loss compared to the training loss could indicate overfitting, where the model performs better on the training data but does not generalize well to unseen data.

The RNN model achieved an overall accuracy of 63%. The model performs well in recognizing positive sentiment, with a high recall of 0.91 but relatively low precision of 0.59, leading to an F1-score of 0.71. For negative sentiment, the model achieves a more balanced performance, with both precision and recall around 0.69 and 0.75, resulting in an F1-score of 0.72. However, the model struggles significantly with the neutral sentiment, where the F1-score drops to 0.35, reflecting poor recall (0.24), indicating difficulty in correctly identifying neutral cases. The macro and weighted averages of precision, recall, and F1-score suggest that the model has room for improvement, particularly in handling the neutral class and balancing precision and recall across all classes.

## Prospect

RNN has limitations in handling long sequences due to the vanishing gradient problem, where information from earlier time steps is lost. However, there are other variants of RNN, such as [LSTM](https://github.com/bitacode/Movie-Reviews-Sentiment-Classification-LSTM.git) and [GRU](https://github.com/bitacode/Movie-Reviews-Sentiment-Classification-GRU.git), that overcome this issue. Increasing the model complexity by adding more layers or incorporating an attention mechanism can further improve performance in sentiment analysis tasks.
