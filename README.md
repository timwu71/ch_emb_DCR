# A Dynamic Chunk Reader with Character Level Embeddings for Question Answering

In 2016, Yu et. al. proposed an end-to-end neural reading comprehension model, know as a Dynamic Chunk Reader (DCR), for question answering. In this model they chose to input word embeddings as well as several other semantic and linguistic features such parts of speech and capitalization into their initial encoding layer. A natural follow-up to this is to experiment with different inputs to the encoding layer. One possibility is to input character embeddings in addition to the word embeddings. This project describes a model that re-creates the DCR model from scratch and the creation of a character level embedding using CNNs to feed into the DCR model.

Link to the paper: 
http://web.stanford.edu/class/cs224n/reports/final_reports/report235.pdf 
