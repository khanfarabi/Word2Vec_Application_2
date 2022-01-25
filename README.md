# Word2Vec_Application_2

Word2vec is a two-layer neural net that processes text by vectorizing words. Its input is a text corpus, and its output is a set of vectors: feature vectors that represent words in that corpus. Here the two review data is being used. Hotel Review and IMDB Movie Review data are collected from Kaggle. The data is available here https://drive.google.com/drive/folders/1D9vNJ9O11JOyXo89-Sl2bsguoSxB59nZ?usp=sharing

In IMDB movie data there are 50000 reviews, and in hotel data there are about 5 million reviews.

# Code

The code is available in Word2Vec_Test2_update notebook. Futher the code is available in Google Colab https://colab.research.google.com/drive/1_I0Nj2Wqta0WTImDvLqHzBVDNWN-06km?usp=sharing

# Outcome

In this application, we have checked with the phrase more than one words. For example the input phrase is "poor story. not fascinating ". The phrase clearly depicts the negative sentiment. All the words in the phrase are not exressing the sentiment, therfore we have extracted the keywords. In this regard, we have used BERT. We have used Word2Vec to have the embeddings of the keywords. We have extracted the closely related words of the key words based on the cosine similarity. 

# Packages Need to be Installed

Juoyter Notebook

Python (Version >=3.5)

sentence_transformers

transformers
