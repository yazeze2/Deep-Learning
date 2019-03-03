# Deep-Learning for Natural Language Processing:

### Convolutional Neural Networks (CNN) and Multi-layer perceptron (MLP) Models for twitter sentiment analysis - without using NLTK's in-built sentiment analysis engine

## Contents

### Tools Required
The general requirements for this project are as follows:
- numpy
- matplotlib
- tensorflow
- keras

### Preprocessing
Process data to remove and replace characters and words irrlevant for analysis to create a processed training and testing .csv file.
- **Process characters/words of each tweet with regex**: Remove punctuations, Convert more than 2 letter repetitions to 2 letter, Check if word begins with an alphabet, and lowercase all the words
- **Process Emoticons using regex**: Replace emoticons with strings 'positive' or negative'
- **Process Tweet with regex:** Remove twitter usernames beginning with @, remove URLs, and replace #hashtag with hashtag


### Models Building & Validation Loss
- **Feature Extraction** - namely, unigrams and bigrams
- **Feature Representation** - Sparse Vector Representation for word presence and frequency feature types
- **Classifiers**:
  - **Multi-layer Perceptron**
      - Layers: 1 hidden layer with 500 neurons
      - Activation function: sigmoid
      - Loss metrics: binary cross_entropy
      - Validation Loss = 1.042%
  - **Convolutional Neural Network**
      - **Embedding layer (9000 x 200) ---> dropout(0.4) ---> conv_1(600 filters) ---> relu ---> con_2(300 filters) ---> relu ---> con_3(150 filters) --->rely--->flatten----dense(600)---> relu ----> dropout(0.5) ----> dense(1)------> sigmoid**
      - Validation Loss = 0.155%
      
