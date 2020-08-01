# Sentiment-Analysis of IMDB reviews

The following is a Sentiment Analysis for the reviews of movies from the IMDB dataset. 
The aim of this analysis is to create a model which will be able to distinguish between positive and negative reviews. To accomplish this, we be creating a Recurrent Neural Network in Keras.

The dataset contains a collection of 50 000 reviews, evenly split between positive and negative reviews (25,000 positive and 25,000 negative reviews). A negative review is defined as having a score of less than 4 (out of 10), and a positive review has a score of more than 7 out of 10. Neutral reviews (scores  between 4 and 7) have not been included in the datatset. All words in the review has already been mapped to integers. The label, which is also an integer, represents whether the review was negative(0) or positive(1). 

We included an Embedding layer in our RNN, which turns positive integers (indexes) into dense vectors of fixed size. This layer requires input data of equal size. To done this, we limited each review to 500 words. For reviews that had less than 500 words, we padded those reviews with zeros using Keras' pad_sequence() function.

Using a batch size of 35 and epoch of 10, our train accuracy was about 89% and our test accuracy was about 85%. The time it took to train our model was about 161 minutes.
When using our model to predict the sentiment of 3 reviews, it predicted all 3 correctly.



