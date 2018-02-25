## Data Science Text Generation & Classification Project
#### Using RNN LSTM Network & Logistic Regression Classification Algorithms

> Rotem Shperling - 305699514  
Eitan Shteinberg - 305809535

### File & Directories

| Notebook | Description |
| --- | --- |
| `ds_project.ipynb` | *Main notebook of the project* |
| `colab_gpu.ipynb` | *Contains the phases that were conducted on the Google Colab GPU* |

| Directory | Description |
| --- | --- |
| `models` | *Contains the trained models of the politicians* |
| `history` | *Contains the history & parameters of the trained models* |
| `text_speeches` | *Contains the original raw politicians speeches* |
| `generated_speeches` | *Contains the generated speeches from the models* |
| `dataframe` | *Contains the dataframes that are used for the classification model* |

### Introduction
> __In this assignment we were asked to perform 3 major tasks:__
> 1. Build a classification model based on the speeches of 3 chosen politicians.
> 2. Build a model to predict the speeches of each politician (separate model for each of them).
> 3. Test the trained classification model on the generated speeches.  

> __Technical aspects:__
> 1. We collected **80** speeches from each politician.
> 2. We generated **24** speeches (30%) for each politician using his trained models.
> 3. We trained each model with **200** epochs in order to get better results.
---
### The Use Of Google Colaboratory In This Project
> __What is [Google Colab](https://colab.research.google.com):__  
Colaboratory is a Google research project created to help disseminate machine learning education and research.  
It's a Jupyter notebook environment that requires no setup to use and runs entirely in the cloud.  
Colaboratory notebooks are stored in Google Drive and can be shared just as you would with Google Docs or Sheets.  

> __What was our main benefit from using it:__  
The us of the Tesla K80 GPU, using the Keras library.  
That way we performed very heavy calculations such as training the model & predicting speeches in less time.  
It is FREE.

> __Cons of using it:__  
> 1. The runtime environment collapsed occasionally and we had to start everything  
from the start (__we trained each model ~10 times before the last version__)
> 2. The importing and exporting of files was __incredibly painful__.
> 3. The work with the Google Drive was not convinient.

> __Where did we use it:__  
> 1. Training the RNN LSTM models - 200 epochs
> 2. Generating the speeches of each politician
> 3. Support in generating the generated speeches dataframe
---
### Expansion On The Library 'Textacy'
#### Textacy
> Textacy is a Python library for performing higher-level natural language processing (NLP) tasks, built on the high-performance spaCy library.  
With the basics — tokenization, part-of-speech tagging, dependency parsing, etc. — offloaded to another library, textacy focuses on tasks  
facilitated by the ready availability of tokenized, POS-tagged, and parsed text.

### Expansion On The Recurrent Neural Network
#### LSTM - Long Short-term Memory Networks
> In this code we use an LSTM (Long Short Term Memory) Neural Network which is a special kind of RNN,  
capable of learning long-term dependencies.  
LSTM was introduced by Hochreiter & Schmidhuber (1997), and was refined and popularized by many people afterwards.  
LSTM works tremendously well on a large variety of problems, and are now widely used.
>LSTMs are explicitly designed to avoid the long-term dependency problem.  
Remembering information for long periods of time is practically their default behavior.

### Expansion On The Classification Algorithm
#### Multinomial Logistic Regression
> Multinomial Logistic Regression is a classification method that generalizes logistic regression to multiclass problems,  
i.e. with more than two possible discrete outcomes. That is, it is a model that is used to predict the probabilities of the  
different possible outcomes of a categorically distributed dependent variable, given a set of independent variables,  
which may be real-valued, binary-valued, categorical-valued and more.
