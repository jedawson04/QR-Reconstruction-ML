# A Brief Explanation of Locations and Contents of Models, Files, and Plots

## QR Code Files - see `QR_README.md`
All QR Code generation files are found outside all folders, with their own readme titled `QR_README.md`.

## Important Folders/Files

### `no_hidden_layers_dense/torchFF.ipynb` - 
No hidden layers dense was our simplest and best performing model. This folder contains many plots and notebooks of attempts of different models with no hidden layers and a dense architecture. Three files are written using tensorflow, where we attempt the problem in different ways, but the most notable notebooks are our pytorch ones: `torchFF.ipynb` and `torchFF-bigcodes.ipynb`.

`torchFF.ipynb` is used to load the training data from CSV into a DataFrame, make transformations based on fixed pixels and the format of the Feed Forward model, and then predict original QR's based on a subset of the DFT. Loops for training on a single L value with testing across different epochs, and for varying L with a given number of epochs are present. At the end of the file is code to generate graphs based on the results of testing. `torchFF-bigcodes.ipynb` contains similar contents, but written for 41 x 41 QR Codes instead of 29 x 29.

### `curated_graphs`
As the name suggests, this folder contains some hand picked plots and important results. We specifically picked plots from our three main successful projects, the simple feed forward model (represented in `no_hidden_layers_dense`), with 29 x 29 size, and 41 x 41 size, as well as the row_sums problem (represented in `row_sums`). Each folder contains a plot across several L values with fewer epochs, and a plot across a middling L value with many epochs.

### `autoencoder`
This folder contains all our work on the autoencoder on the original problem. This project could theoretically have been expanded towards 'w-net,' in which we train an encoder and a decoder and join them together, but was not finished in time. All plots upto 5000 epochs are shown here, as well as the fully trained model.

### `row_sums`
This contains all work on the separate row sums problem, where we train on the fourier coefficients that encode the row sums, and try to guess the 29 x 1 vector of row sums. Included are our attempts at the overall problem as well as an autoencoder of it, both with plots.

## Less Important Folders (What are they? Why are they here?)

### `ift_null`
This folder just has code to check the performance of our so called 'null model.' In this case, we don't do any machine learning, and simply fourier transform the QR code, center the coefficients, take our L-submatrix, apply the IFT, and round our numbers to 0 or 1.

### `ift_convo`
Here, we put all our attempts at using convulution in our networks. Since spactial relations are mapped differently in the complex plane, none of our attempts were very successful. 

