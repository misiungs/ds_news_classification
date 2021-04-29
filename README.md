# Natural language processing: news classification
NLP project about news classification

<img src="https://github.com/misiungs/readme_images/blob/master/news.jpg?raw=true" alt="drawing" width="500"/>

# Problem
AG news is a subdataset from AG dataset corpus.
Data has been gathered from more than 2000 news sources and it consists of 120000 training examples and 7600 test examples categorized into one of four classes: “World”, “Sports”, “Business”, “Sci/Tech”.
Each example consists of news content and its corresponding label.
The goal is to identify news category based only on its description.

# Approach
As a starting point routines that are necessary for text classification are developed.
They consists of string encoding, string cleaning, lower casing and stemming.
After the data exploration text classification is performed.
First, text classification is done by means of Naive Bayes method with multinomial event model.
Word frequencies are calculated and based on them log-probabilities of each word per class and of each class are calculated.
They are next used for predictions on the test dataset.
Second used approach are recurrent neural networks (RNN) with long short-term memory (LSTM) units.
Model architecture is built in tensorflow and the whole model is trained from scratch.
Improvement compared to Naive Bayes approach is observed.
Finally, the same model architecture is used but this time with transfer learning.
For that word embeddings from GloVe data are used to featurize corpus vocabulary.
Applied transfer learning further improved accuracy of the model.

# Conclusions
Best result from our approach achieved 91.5% accuracy, whereas the best noted score is 95.5%.
It has to be stated that Naive Bayes approach yielded 88.8% of accuracy with use of relatively simple techniques that require much less computational resources.

