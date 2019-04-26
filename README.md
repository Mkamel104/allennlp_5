# Training a Sentiment Analyzer using AllenNLP
We will be building and training a  sentiment Analyzer using AllenNLP. Sentiment analysis is a popular text analytic technique used in the automatic identification and categorization of subjective information within text. In this repo we used three different method to train and predict for sentiment, baseline (no ELMO/BERT), ELMO, BERT. We need to build three config files one for each method.

# Training: 
1. We will run below command for three different config files. (replace (name) with the name of config file)

          allennlp train config/name.json -s ./output/name --include-package model
          
          
# Evaluation: 
1. By runing below command and using test.txt file we can evaluate each model. (replace (name) with the correct name of the output folder)

          allennlp evaluate output/name/model.tar.gz  test.txt --include-package model
          
          
          
# Prediction:
          
          allennlp predict output/name/model.tar.gz test.txt --include-package model --predictor predictor
          


