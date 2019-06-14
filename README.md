Readme is a Work in Progress
# RNN Language Model
This is the code associated with @MilkKnight's article [Build your LSTM language model with Tensorflow](Build your LSTM language model with Tensorflow)

Simply modify run.py to build an LSTM model or predict the perplexity of some test corpus with an existing model.

[//]: # (Add explanation of the direcotry structure)

The Language Model's Vocabulary is decided by the file https://github.com/Abhishek-P/RNN_Language_Model/blob/master/data/vocab (It has 9999 unique words. It also contains the labels used for indicating Processing Indicators for ease of use)

## Dataset
The dataset (https://github.com/Abhishek-P/RNN_Language_Model/tree/master/ptb) is PTB corpus from https://github.com/tomsercu/lstm/tree/master/data and used with customer pre-processing

## Pre-processing
Pre-processing is handled by https://github.com/Abhishek-P/RNN_Language_Model/blob/master/data_prepare.py
It takes care of splitting the lines(the PTB corpus is already processed to a significant, eliminating the necessity for cleaning) and storing them in an index based model(based on https://github.com/Abhishek-P/RNN_Language_Model/blob/master/data/vocab)
Line ` aer banknote berlitz calloway centrust cluett fromstein gitano guterman hydro-quebec ipo kia memotec mlx nahb punts rake regatta rubens sim snack-food ssangyong swapo wachter ` is processed to `1 2202 9553 3946 1337 6042 1074 3440 1272 6847 122 704 5423 8233 1624 2709 999 3258 5610 1091 9530 7498 7945 8668 3931 2`
In the vocab 1 s being mapped to \_BOS\_ to indicate beginnning and \_EOS\_ to indicate the end of the line
