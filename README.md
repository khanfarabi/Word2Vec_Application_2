# Word2Vec_Application_2

Word2vec is a two-layer neural net that processes text by vectorizing words. Its input is a text corpus, and its output is a set of vectors: feature vectors that represent words in that corpus. Here the two review data is being used. Hotel Review and IMDB Movie Review data are collected from Kaggle. The data is available here https://drive.google.com/drive/folders/1D9vNJ9O11JOyXo89-Sl2bsguoSxB59nZ?usp=sharing

In IMDB movie data there are 50000 reviews, and in hotel data there are about 5 million reviews.

# Code

The code is available in Word2Vec_Test2_update notebook. Futher the code is available in Google Colab https://colab.research.google.com/drive/1_I0Nj2Wqta0WTImDvLqHzBVDNWN-06km?usp=sharing

# Outcome

In this application, we have checked with the phrase more than one words. For example for movie review data the input phrase is "poor story. not fascinating ". The phrase clearly depicts the negative sentiment. All the words in the phrase are not exressing the sentiment, therfore we have extracted the keywords. In this regard, we have used BERT. We have used Word2Vec to have the embeddings of the keywords. We have extracted the closely related words of the key words based on the cosine similarity. Using BERT the key words in the phrase are:


fascinating, story,  poor. Here the phrase itself is the negative sentiment, the keyword 'poor' represents negative sentiment. 

So the closest words of the keywords are:


fascinating:  ['screenplay', 'davalos', 'solonitsyn', 'selby', 'sander', 'lejla', 'armstrong', 'fjkdfa', 'travolta', 'aoki', 'unkind', 'louisiana', 'hunter', 'bush', 'enbom', 'california', 'horroryearbook', 'solter', 'canada', 'entertainer']


story:  ['story', 'begin', 'jessica', 'show', 'mcdermott', 'cameo', 'film', 'comedy', 'saphirjd', 'awful', 'roloff', 'flick', 'unkind', 'sorbonne', 'brandy', 'passable', 'injustice', 'fenton', 'beautiful', 'value']


poor:  ['poor', 'sander', 'horroryearbook', 'merk', 'travolta', 'none', 'anar', 'text', 'sidney', 'selby', 'virgin', 'locoformovies', 'armstrong', 'blanc', 'screenplay', 'html', 'nelson', 'culp', 'fjkdfa', 'gould']



For the hotel review data, the phrase is "the best quality food. the desert is very sweet. the bathroom  is clean" and it implies to the positive sentiment. Using BERT, we extract the keywords from the phrase. The keywords are:

['best', 'quality', 'desert', 'food', 'sweet', 'bathroom', 'clean'], here we see best ,sweet , and clean are representing positive sentiment. The closest word list for the keywords are:

best: ['best', 'sweet', 'outside', 'sin', 'food', 'westminster', 'studio', 'egg', 'girl', 'big', 'dreadful', 'policy', 'jackson', 'spacious', 'service', 'quality', 'fun', 'classy', 'illegible', 'comfort']


quality: ['quality', 'sweet', 'food', 'illegible', 'overall', 'fun', 'sin', 'window', 'girl', 'location', 'westminster', 'outside', 'ingredient', 'etc', 'water', 'appearance', 'kind', 'bath', 'tasty', 'facility']


desert: ['sweet', 'food', 'window', 'sin', 'quality', 'illegible', 'bath', 'outside', 'claustrophobic', 'bathroom', 'girl', 'etc', 'policy', 'instead', 'classy', 'water', 'patch', 'windowns', 'heat', 'dry']


food: ['food', 'sweet', 'quality', 'policy', 'sin', 'girl', 'etc', 'window', 'customer', 'outside', 'bath', 'heat', 'illegible', 'water', 'jackson', 'smell', 'egg', 'claustrophobic', 'best', 'facility']


sweet: ['sweet', 'sin', 'quality', 'westminster', 'food', 'window', 'outside', 'illegible', 'instead', 'claustrophobic', 'policy', 'studio', 'bath', 'girl', 'water', 'appearance', 'heat', 'facility', 'windowns', 'classy']


bathroom: ['bathroom', 'window', 'patch', 'dry', 'bath', 'claustrophobic', 'screen', 'sweet', 'water', 'instead', 'ridiculous', 'thnkssss', 'bed', 'uncomfortable', 'wall', 'space', 'illegible', 'windowns', 'sin', 'quality']


clean: ['clean', 'claustrophobic', 'modern', 'bumpy', 'spacious', 'classy', 'bath', 'egg', 'sweet', 'ridiculous', 'bathroom', 'dry', 'patch', 'bland', 'food', 'window', 'sin', 'girl', 'kind', 'thnkssss']


In the above we have shown the the top 20 closest words for each keywords.


# Obsevation

We can extract the word list from the text that is contextually and semantically similar to the input phrase using the trained Word2Vec model. The input phrase can be a single word or more than one word. We have analyzed two review data: Hotel Review, and IMDB (Movie Review Data). Mainly here we did the sentiment analysis; whether the review is positive or negative. We see that we can extract the words from the text that is in the same sentiment of the input phrase. Using the extracted words similar to the phrase, we can train the unsupervised model along with unseen labels, and classify the text. We will explore Zero-shot-classification in this regard.




# Packages Need to be Installed

Juoyter Notebook

Python (Version >=3.5)

sentence_transformers

transformers
