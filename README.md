# QuestionAnswering_From_FAQ_Tutorial
NLP Tutorial : Automatic Question Answering from information in FAQ

In this notebook we examine the task of automatically retrieving a suitable response to customer questions from FAQs. Often websites have comprehensive FAQs, but manually searching and finding the answer to a specific question from these FAQs is not trivial. The purpose of this exercise is to answer user queries by automatically retrieving the closest question and answer from predefined FAQs when appropriate.

We will use a sample dataset of FAQs extracted from the site https://machinelearninginterview.com for this task. This dataset can be replaced with a more elaborate dataset as appropriate.

Installation and setup
--------------------------

You need to install the following packages. Most are available in conda except for bert-serving-server and bert-serving-client These are required to experiment with bert embeddings) that are not in the conda repository and need to be installed through pip.

Note that : Numpy, scikit-learn need to be installed. If you want to use BERT embeddings detailed at the end, you need to use Numpy 1.14. 

In addition we will use gensim that can be installed as : 

conda install gensim 


The above setup is required to get the basic part of the notebook running. 


For using BERT Embeddings: 

We want to use the following library to get a sentence embedding using BERT: https://pypi.org/project/bert-embedding/
For using the library we need to install the following (with numpy 1.14) : 

conda install tensorflow=1.13

pip install bert-serving-server 
pip install bert-serving-client

You need to start the BERT server as follows to get phrase embeddings using bert. 

bert-serving-start -model_dir /tmp/english_L-12_H-768_A-12/ -num_worker=1 &


#Optionally
conda install nltk
