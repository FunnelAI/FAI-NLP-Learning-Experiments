# FunnelAI Machine Learning Experiments

Code &amp; notebooks for ML Experiments


# Data

`labeled_dataset.csv` contains a small labeled dataset of forum posts. The relevant columns are `body` and `label_*`, where `*` is a training objective such as `intent`. Note that `condition`, `industry` and `credit` have only two types of labels and could therefore be considered as a binary or multi-label prediction problem, while `intent` has 4 possible labels / classes, which means it could be considered as a mullti-label or multi-class objective.

# Things to explore

* Data visualization
* Text representation strategies
    * Cleaning (removing unwanted characters)
    * Tokenization
        * Per-word tokenization
        * Character n-grams
    * Vectorization
        * Token histograms
        * Normalized token histogram
        * TF-IDF
        * Random embeddings
        * Pretrained embeddings (word2vec)
    * Dimensionality reduction
* Models
    * Decision tree
    * Random forest
    * Gradient boosted trees
    * SVM
    * Logistic regression
    * 1-layer neural net
    * 2-layer neural net
    * 3-layer neural net
    * LSTM
    * BERT
* Effect of training objective
    * 2-class problems: multi-label vs binary optimization
    * 2+-class problems: multi-label vs multi-class optimization
    * Multi-objective vs single-objective optimization of deep models

# Task description

1. Load in the dataset to a Jupyrer notebook or an interactive session in your editor (e.g. VSCode, Atom)
2. Explore the data. Build histograms of class labels. Which training objectives have most data? Are all objectives usable?
3. Experiment with different text representation techniques. Explore the result of tokenization by building histograms, etc. Explore what kinds of tokenization lead to what kind of vocabulary sizes. Try to find reasonable configurations that result in a not-too-large vocab size.
4. Implement functionality to convert tokenized text to vector representations. Explore how to normalize, reduce dimensionality, and perform other transformations in this vector representation. Can you also visualize the documents in this vectorspace with e.g. t-SNE or similar approaches?
5. Train and tune individual models. Selection of models is up to you. For deep learning models, I recommend using Pytorch. The most natural fit for this dataset is considering outputs as multi-label classification, but you can also experiment with multi-class and binary classification to see the comparison.
6. Tune each model to the extent you feel is necessary.
7. Write up your experiences and observations in a form you find most useful - Google Docs, Jupyter notebooks, markdown.
