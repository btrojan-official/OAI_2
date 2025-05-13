## Task 1
You got pointclouds of 3D person position and your goal is to reduce the dimensionality of this data (from 75 features per pose (25 xyz points)) and classify the movement type
by this.
#### Solution:
Leave only points of hand ends, legs ends and two points for core. Apply Random Forest on it

## Task 2
You got images with noise applied to them, which is sampled from normal distribution or uniform distribution and you have to for each image:
1. Classify the type of distribution, that noise comes from
2. Esitmate the noise
3. For noise sampled from normal distribution estimate the parameters: mean and std

#### Solution:
**Conv2d backbone + linear heads for noise estimation, noise classification and params prediction** 

## Task 3
Your task is to represent sentences and articles (text) as embeddings using special type of GPT model, to then find most accuracte article for each sentence.
#### Solution:
**Weighted mean pooling** from last hidden layer of GPT model. Weights are based on order of tokens in sequence (later tokens embeddings are more valuable)

## Task 4
You have a model that decides wheather to give a person a debt or not. Your task is to explain this model by proposing the change in perons feature vector.
#### Solution:
This is too hard to explain in few frases. I encourage you to take a look at my notebook :)