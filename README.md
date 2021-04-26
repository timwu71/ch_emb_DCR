# A Dynamic Chunk Reader with Character Level Embeddings for Question Answering

In 2016, Yu et. al. proposed an end-to-end neural reading comprehension model, know as a Dynamic Chunk Reader (DCR), for question answering. In this model they chose to input word embeddings as well as several other semantic and linguistic features such parts of speech and capitalization into their initial encoding layer. A natural follow-up to this is to experiment with different inputs to the encoding layer. One possibility is to input character embeddings in addition to the word embeddings. This project describes a model that re-creates the DCR model from scratch and the creation of a character level embedding using CNNs to feed into the DCR model.
This is my final project for Stanford's CS224N class.

Link to the paper: 
http://web.stanford.edu/class/cs224n/reports/final_reports/report235.pdf 

# Setup

1. To run the code, make sure you have [Miniconda](https://conda.io/docs/user-guide/install/index.html#regular-installation) installed
    1. Conda is a package manager that sandboxes your project’s dependencies in a virtual environment
    2. Miniconda contains Conda and its dependencies with no extra packages by default (as opposed to Anaconda, which installs some extra packages)

2. cd into src, run `conda env create -f environment.yml`
    1. This creates a Conda environment called `squad`

3. Run `conda activate squad`
  
4. Run `python setup.py`
    1. This downloads SQuAD 2.0 training and dev sets, as well as the GloVe 300-dimensional word vectors (840B)
    2. This also pre-processes the dataset for efficient data loading
    3. This may takee around 20 minutes - 1 hour total  

5. Browse the code in `train.py`
    1. The `train.py` script is the entry point for training a model. It reads command-line arguments, loads the SQuAD dataset, and trains a model.
    2. You may find it helpful to browse the arguments provided by the starter code. Either look directly at the `parser.add_argument` lines in the source code, or run `python train.py -h`.

