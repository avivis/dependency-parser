Avighna Suresh (as6469)

A feed-forward neural network to predict the transitions of an arc-standard dependency parser. Model in model.h5 file, and training and evaluation code in .py files

Installing TensorFlow and Keras: 
`$ python -m pip install tensorflow`

`conll_reader.py` - data structures to represent a dependency tree, as well as functionality to read and write trees in the CoNLL-X format (explained below). 
`get_vocab.py` - extract a set of words and POS tags that appear in the training data. This is necessary to format the input to the neural net (the dimensionality of the input vectors depends on the number of words). 
`extract_training_data.py` - extracts two numpy matrices representing input output pairs.
`train_model.py` - specify and train the neural network model. This script writes a file containing the model architecture and trained weights. 
`decoder.py` - uses the trained model file to parse some input. For simplicity, the input is a CoNLL-X formatted file, but the dependency structure in the file is ignored. Prints the parser output for each sentence in CoNLL-X format. 
`evaluate.py` - this works like `decoder.py`, but instead of ignoring the input dependencies it uses them to compare the parser output. Prints evaluation results. 
