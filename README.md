# Author Attribution Analysis - README

## Installation
The code was written in Python 3 and requires the following packages: NumPy, Pandas, Chardet, Collections, Seaborn, Matplotlib, String, Time, NLTK, Scikit-Learn (sklearn), Keras and SciPy.

## Project Overview
Author attribution "is the task of identifying the author of a given text from a (given) set of suspects" (Mohsen et al. (2016)). Up until early this century, it was believed that texts had to be a minimum of 250 words in length for the stylometric characteristics to be apparent and for author attribution to be successful. However, recent research has demonstrated the successful application of author attribution techniques to Twitter messages ("tweets"), which "average less than 25 words" in length and are "often less than 10" words long (Green and Sheppard (2013)).

Tweets are currently limited to 280 characters, and prior to November 2017, were limited to 140 characters. As a result, "tweets are relatively self-contained and have smaller sentence length variance compared to excerpts from longer text" (Schwartz (2013)). It is possible that these characteristics are the reason why author attribution techniques, that have previously fallen apart when applied to shorter texts, have succeeded when applied to tweets. It is also possible that, had more modern machine learning algorithms, such as support vector machines (SVMs) and neural networks, been in common usage when the previously mentioned conclusions were drawn about the minimum text length required to successfully identify the author of a text, that different conclusions may have been reached.

In this analysis we explore these hypotheses by applying techniques that have been demonstrated to succeed in determining the authorship of tweets, to short, tweet-length, excerpts of longer works. In performing this analysis, we make use of of a dataset comprising 68,000 sentence-long excerpts from the (fiction) works of eight classic authors (Louisa May Alcott, Jane Austen, Charlotte Bronte, Wilkie Collins, Arthur Conan Doyle, L.M. Montgomery, Bram Stoker and Mark Twain), along with labels identifying the author of each excerpt.

The novels used the create the dataset used in this analysis are:

|Author     | Novels| Genre | Year of Publication|
|---------  |-------|-------|--------------------|
|Louisa May Alcott | *Little Women* |Coming of Age/Romance | 1869 |
|Jane Austen| *Pride and Prejudice* and *Emma*|Romance | 1813/1815 |
|Charlotte Bronte| *Jane Eyre* | Gothic Romance | 1847 |
|Wilkie Collins | *The Woman in White* | Mystery | 1859 |
|Arthur Conan Doyle | *A Study in Scarlet*, *The Sign of the Four* and *The Hound of the Baskervilles*| Mystery |1887/1890/1902| 
|L.M. Montgomery | *Anne of Green Gables* and *Anne of Avonlea* |Coming of Age | 1908/1909 |
|Bram Stoker | *Dracula* | Horror | 1897|
|Mark Twain | *The Adventures of Tom Sawyer* and *The Adventures of Huckleberry Finn*|Coming of Age/Adventure|1876/1884|

## File Descriptions
* **Books**: this folder contains text files of the novels used to create the analysis dataset. Chapter/section headings have been manually removed from the files.
* **create_dataset.ipynb**: the code contained in this Jupyter notebook takes the contents of the Books folder as an input and outputs a processed dataset. To run the code, save the Books folder in the same directory as this notebook. The code will output a csv file named author_data.csv to this directory.
* **analysis.ipynb**: this Jupyter notebook contains all of the analysis for this project. To run this code, first run the code in create_dataset.ipynb to create the author dataset (author_data.csv), then save the author dataset and this notebook in the same directory.

## Results
The main findings of this analysis are summarized in a technical report included in this repository in **Report.pdf** [here](https://github.com/gkhayes/author_attribution/blob/master/Report.pdf).

## Licensing, Authors, Acknowledgements
The novel texts used in this analysis were all sourced from [Project Gutenberg](https://www.gutenberg.org/) and made available for download under the [Project Gutenberg License](https://www.gutenberg.org/wiki/Gutenberg:The_Project_Gutenberg_License). 

The code contained in this repository may be used freely with acknowledgement.

## References
Green, R. and J. Sheppard (2013). Comparing frequency- and style-based features for Twitter author identification. Proceedings of the Twenty-Sixth International Florida Artificial Intelligence Research Society Conference, 64–69.

Mohsen, A., N. El-Makky, and N. Ghanem (2016). Author identification using deep learning. Proceedings of the 15th IEEE International Conference on Machine Learning and Applications, 898–903.

Schwartz, R., O. Tsur, A. Rappoport, and M. Koppel (2013). Authorship attribution of micro-messages. Proceedings of the 2013 Conference on Empirical Methods in Natural Language Processing. Seattle, Washington, USA, 1880–1891.

Shrestha, P., S. Sierra, F. Gonz´alez, P. Rosso, M. Montes-y G´omez, and T. Solorio (2017). Convolutional neural networks for authorship attribution of short texts. Proceedings of the 15th Conference of the European Chapter of the Association for Computational Linguistics: Volume 2, Short Papers. Valencia, Spain, 669–674.
