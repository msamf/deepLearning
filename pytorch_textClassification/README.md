# PyTorch for Text Classification: Classifying IMDB Movie Reviews with TinyBERT Transformers
This project explores the use of pytorch for text classification, specifically through classifying IMDB movie reviews with TinyBERT transformers. 

NOTE: This project is based on Codecademy's [text classification project](https://www.codecademy.com/content-items/29838c7636654e48ac72458af6373d5d).

## Dataset
The dataset is about movie reviews, and can be found at [Hugging Face](https://huggingface.co/datasets/Lowerated/lm6-movies-reviews-aspects); the given datasets in the `datasets` folder have been already cleaned and preprocessed.

## Methods
The following steps are performed:
* Import and inspect dataset
* Data pre-processing 
    * Create vocabulary from tokenized reviews in the train set (1000 most common words)
    * Tokenize, encode, and express train texts as tensors
    * Tokenize, encode, and express test texts as tensors
* Train a simple neural network (1 hidden layer) + evaluation
* Fine-tune existing TinyBERT model + evaluation

## Results and Discussion
The simple neural network has an accuracy of 68%, while the fine-tuned TinyBERT model has an accuracy of 93% - this shows that TinyBERT is much better at this kind of text classification than a simple neural network. 
Some future steps could be to explore dfference sequence lengths, train for more epochs, etc. 