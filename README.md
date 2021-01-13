#Natural Language Processing  

NLP covers the different way to process, analyse, generate, translate languages using computers, algorithms and machine learning.  

In these two projects on the [taln-corpus](https://www.ortolang.fr/market/corpora/corpus-taln), made of conference papers about NLP, the follwing objectives were :  

1 - Find a creative way to summarize the corpus, analyse it and reveal information about it using the different tools, techniques and algorithms of NLP,  

2 - Predict the year of an article by whatever means you see fit  

###My work

For the first project i went with the tf-idf method, where a corpus is converted into a matrix with columns for words and rows for each document, the values in the matrix are
the relative importance of the word in the document plus the absolute importance in the whole dataset.
This enabled me to further curate the corpus to what carries the most information and relevance in order to summarize it. For this task is used BERT, an industry-wide used
deep learning neural network able to perform multiple different NLP tasks.  
In this case by using the sequence-to-sequence functionnality to produce a summary by concatenating several curates and cleaned documents. They are then compacted into a lower
scale data representation which enables the conservation of only the most relevant informations, and then a shorter sequence is reconstructed from the documents.

The second project has an NLP but also a Machine Learning side, there the articles' content serve as the variable, and the year of publication is the target. The key to this
project is to build a fair algorithm that only takes data that does not make the task too easy or enable overfiting. In order to attain this Data Spliting into training
and testing set is used along with stratification to assure an approximately equal repartition of the target years in both training and test set, which would otherwise
negatively impact prediction performance.
In order to attain this i used the Tf-Idf matrix of earlier, instead of solely curating the text further for high information words, i used the matrix as the input data for linear
regression algorithm and neural networks, this text representation under a numeric matrix form allows for mathematic calculation on each document's information, using each word
as a variable. Thus words more prevalent in some years, strongly linked to a peculiar span of time will have a stronger value for those years/documents, which will enable
prediction of the year.


Repartition of the years


![year distribution](/years_distribution.png)

![train test difference](/train_test_difference.png)

![Bayesian Ridge Prediction](/Bayesian_Ridge_prediction.png)
