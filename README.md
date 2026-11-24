# Review sentiment analysis

Four pipelines on 3.6m training and 400k test product reviews: VADER on raw text, VADER after stopword removal, and Multinomial Naive Bayes on bag-of-words and on TF-IDF. Naive Bayes on bag-of-words reached 85% accuracy; VADER reached 72%, and stopword removal made no difference to it.

Known issue: the TF-IDF cell fits `classifier2` on an undefined `train_small` and predicts with the bag-of-words model, so the TF-IDF result needs re-running.
