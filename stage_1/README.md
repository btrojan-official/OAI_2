## Task 1
You got few photos with polish coins on them and your task is to detect them and classify to one into 9 classes.\
#### Solution:
** 3x convolutional networks**: background detector, coin classifier, bouding box size regressor. Augumentations are cropping coins with random offset and few more.

## Task 2
You got as a single sample: question, answer, 4 supporting answers and probabilities for those supporting answers tokens. Your goal is to classify those samples as halucinations, or not halucinations, but you have to achieve this with only numpy, sklearn and xgboost (torch/tensorflow and no pretrained weights)\
#### Solution:
**Xgboost classifier** trained on **tf-idf** features extracted from question+answer+all supporting answers that <answer></answer> tag contains words that appear in main answer.

## Task 3
You get lists of points that are heartrates of healthy/ill people and your task is to classify them into 5 classes where one is for health and other are some illnesses with random forest classifier, but you could only extract from those charts four features per chart.\
#### Solution:
Features: mean absolute difference between point and previous point, energy of the wave, two other more complicated features: **aggregated information about height of highest peeks on the left and on the right of QRS group** (this one is the most important) and information about flateness of the highest peek on the right of the QRS group - 100

## Task 4
Implement function that takes labels and losses for samples passed throught two models with the same architectures. You have to decide which examples to use in training which not, because some of the samples are misslabeled.\
#### Solution:
**Co-learning** (I fed into model_1 some percent of samples with lowest loss score from model_2, and similarly for model_1)  with balanced label distribution.

## Task 5
You have strings with zeros and ones (for example: 1000101001110) and you have three unknown substrings that determine the value of those strings. Your task is to train model to approximate those values.\\
#### Solution:
**Conv1d layers + MLP trained with BCELoss** (separate output logit for each possible substring)