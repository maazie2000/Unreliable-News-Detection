# Fake News Detection 🕵️🗞️

Fake news is everywhere today, and studies show that humans cannot compare real news from fake news. This can create huge misunderstanding of many political and social issues. 
This project works on developing a model that can detect if news can be unreliable at times. 

## Dataset

The dataset used for this can be found here : https://www.kaggle.com/competitions/fake-news/data
This dataset was preprocessed into training and testing files that were imported at the start of the notebook. Here' information on the dataset

- id: unique id for a news article
- title: the title of a news article
- author: author of the news article
- text: the text of the article; could be incomplete
- label: a label that marks the article as potentially unreliable
   - 1: unreliable
   - 0: reliable
   
 
 ## Modelling Experiments
 
 Here's all the models that were created and their accuracy scores on the test set.

- Model 0 : a baseline naive bayes model
- Model 1 : A Conv1D layer with a global maxpooling layer
- Model 2 : A LSTM
- Model 3 : A GRU
- Model 4 : A Bidirectional RNN
- Model 5 : Using a universal sentence encoder

```
Model 0: 0.8521634615384616
Model 1: 0.9855769276618958
Model 2: 0.8805288672447205
Model 3: 0.920192301273346
Model 4: 0.9519230723381042
Model 5: 0.8812500238418579
```

Model 1 which was a model with a 1D Convolution layer performed the best with a high accuracy of about 99% 

## Conclusion

> Note : Any predictions made my the model to flag news as unreliable should not be taken as serious advice.
