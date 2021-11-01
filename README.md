# simple word embedding
A very simple word embedding layer for LSTM models. For futher information refer to [A Guide to Word Embedding](https://towardsdatascience.com/a-guide-to-word-embeddings-8a23817ab60f) and [Creating Word Embeddings](https://towardsdatascience.com/creating-word-embeddings-coding-the-word2vec-algorithm-in-python-using-deep-learning-b337d0ba17a8).

## How to do it?
Making a Word Embedding is quite straight forward:
1. Gather some text data, prepare them by some preprocessings and define a window parameter (*embedding_dim*)
2. Create the vocabulary
3. Create the windowed contexts
4. Apply *One-Hot encoding*
5. Create, compile and train a model
    - The model consists of 3 layers: Input, Hidden (Dense layer with *window* for the number of units), Output
    - Model output should have *softmax* activation. Also input and output layers should have the same number of shape as the X matrix
6. Get the weights from the model and map them into a dictionary
