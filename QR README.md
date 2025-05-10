# README Documentation for `gen_qr.py` and `gen_set.py` and `gen_set_big.py` 
## (for generating individual QR codes, and groups of QR codes respectively)

## `gen_qr.py` - 
This file generates invididual instances of qr codes using the qrcodegen library.

the generate qr method allow for specification on the message to be encoded, the error correction level (low through high), the type of masking (0-7), and the size to generate and return a QR code object.

the file output method takes in a QR code object, 

## `no_hidden_layers_dense/torchFF.ipynb` - 
This notebook is used to load the training data from CSV into a DataFrame, make transformations based on fixed pixels and the format of the Feed Forward model, and then predict original QR's based on a subset of the DFT. Loops for training on a single L value with testing across different epochs, and for varying L with a given number of epochs are present. At the end of the file is code to generate graphs based on the results of testing.