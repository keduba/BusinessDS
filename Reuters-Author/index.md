       
# Text Mining NLP
# *Introduction*
This notebook contains code examples to get you started with Natural Language Processing (NLP) / Text Mining for Research and Data Science purposes.  ,

In the large scheme of things there are roughly 4 steps:  ,

1. Identify a data source  ,
2. Gather the data  ,
3. Process the data  ,
4. Analyze the data  

## Note: companion slides

# *Elements / topics that are discussed in this notebook: *,
,
,
<img style=\float: left src=\https://i.imgur.com/c3aCZLA.png width=\50% />


# *Table of Contents*  <a id='toc'></a>


* Primer on NLP tools(#tool_primer)     ,
* Process + Clean text(#proc_clean)   ,
   * Normalization(#normalization),
       * Deal with unwanted characters(#unwanted_char),
        * Sentence segmentation(#sentence_seg)   ,
        * Word tokenization(#word_token),
        * Lemmatization & Stemming(#lem_and_stem),
    * Language modeling(#lang_model),
        * Part-of-Speech tagging(#pos_tagging),
        * Uni-Gram & N-Grams(#n_grams),
        * Stop words(#stop_words),
* Direct feature extraction(#feature_extract),
    * Feature search(#feature_search),
        * Entity recognition(#entity_recognition),
        * Pattern search(#pattern_search),
    * Text evaluation(#text_eval),
        * Language(#language),
        * Dictionary counting(#dict_counting),
        * Readability(#readability),
* Represent text numerically(#text_numerical),
    * Bag of Words(#bows),
        * TF-IDF(#tfidf),
    * Word Embeddings(#word_embed),
        * Word2Vec(#Word2Vec),
* Statistical models(#stat_models),
    * \Traditional machine learning(#trad_ml),
        * Supervised(#trad_ml_supervised),
            * Naïve Bayes(#trad_ml_supervised_nb),
            * Support Vector Machines (SVM)(#trad_ml_supervised_svm),
        * Unsupervised(#trad_ml_unsupervised),
            * Latent Dirichilet Allocation (LDA)(#trad_ml_unsupervised_lda),
            * pyLDAvis(#trad_ml_unsupervised_pyLDAvis),
* Model Selection and Evaluation(#trad_ml_eval),
* Neural Networks(#nn_ml)

There are many tools available for NLP purposes.
The code examples below are based on what I personally like to use, it is not intended to be a comprehsnive overview.

Besides build-in Python functionality I will use / demonstrate the following packages:,

**Standard NLP libraries**:,
1. `Spacy` and the higher-level wrapper `Textacy`
2. `NLTK` and the higher-level wrapper `TextBlob`

*Note: besides installing the above packages you also often have to download (model) data . Make sure to check the documentation!*

**Standard machine learning library**:

1. `scikit learn`

**Specific task libraries**:

There are many, just a couple of examples:,

1. `pyLDAvis` for visualizing LDA),
2. `langdetect` for detecting languages,
3. `fuzzywuzzy` for fuzzy text matching,
4. `textstat` to calculate readability statistics,
5. `Gensim` for topic modelling


There are many example datasets available to play around with, see for example this great repository:
https://archive.ics.uci.edu/ml/datasets.html?format=&task=&att=&area=&numAtt=&numIns=&type=text&sort=nameUp&view=table


The data that I will use for most of the examples is the Reuter_50_50 Data Set that is used for author identification experiments.,

See the details here: https://archive.ics.uci.edu/ml/datasets/Reuter_50_50  
