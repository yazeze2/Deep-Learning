# Deep-Learning for Natural Language Processing:

### Convolutional Neural Networks (CNN) and Multi-layer perceptron (MLP) Models for twitter sentiment analysis - without using NLTK's built-in sentiment analysis engine

The dataset for this project can be acquired [here](https://datahack.analyticsvidhya.com/contest/practice-problem-twitter-sentiment-analysis/). Moreover, the GloVe word vector is provided by Stanford NLP group and can be downloaded [here](https://nlp.stanford.edu/projects/glove/)

## Contents

### Tools Required
The general requirements for this project are as follows:
- numpy
- regex
- tensorflow
- keras

### Preprocessing
Process data to remove and replace characters and words irrlevant for analysis to create a processed training and testing .csv file.
- **Process characters/words of each tweet with regex**: Remove punctuations, Convert more than 2 letter repetitions to 2 letter, Check if word begins with an alphabet, and lowercase all the words
- **Process Emoticons using regex**: Replace emoticons with strings 'positive' or negative'
- **Process Tweet with regex:** Remove twitter usernames beginning with @, remove URLs, and replace #hashtag with hashtag


### Model Building & Validation Accuracy
- **Feature Extraction** - namely, unigrams and bigrams
- **Feature Representation** - Dense Word Embedding - **GloVe** word vector provided by StanfordNLP group
- **Weight Update scheme** - Adam (experimented with SGD + Momentum updating scheme but observed to take longer(100 epochs more) to produce a comparable validation loss.
- **Classifiers**:
  - **Multi-layer Perceptron**
      - Layers: 1 hidden layer with 500 neurons
      - Activation function: sigmoid
      - Loss metrics: binary cross_entropy
      - Accuracy = 81.7%
  - **Convolutional Neural Network**
      - **Embedding layer (9000 x 200) ---> dropout(0.4) ---> conv_1(600 filters) ---> relu ---> con_2(300 filters) ---> relu ---> con_3(150 filters) --->rely--->flatten----dense(600)---> relu ----> dropout(0.5) ----> dense(1)------> sigmoid**
      - Accuracy = 83.4%
      
