# Text-Generation-using-VAE-and-Beta-VAE

There are several research papers showing that the results of beta-VAE on image encoding is much far better than that of VAE. But, there are uncertainity regarding the performance of beta-VAE and VAE on the task of text generation.
So, this project was an attempt to see and compare the preformance of beta-VAE and VAE on text encoding task.

Two datasets were used for this task: -
  1) Quora question-pair dataset https://www.kaggle.com/c/quora-question-pairs/data (this dataset is not considered good for text generation as sentences are very vague)
  2) Keras Movie review dataset with Sentiment Analysis.

**Grid Search** was used to set find a suitable beta (or kl-weight) for beta-VAE. The range of grid search was \[20, 250\]. `Beta = 100` was found to provide the best fit.

Since Quora question-pair dataset was not labelled, custom labelling of the data was created. The dataset was split into five classes based on the following keywords: \['How', 'Where', 'When', 'Why', None\].

The performance of both were compared by plotting **t-Distributed Stochastic Neighbor Embedding (t-SNE)** plots for the encodings produced of the training dataset. t-SNE is basically a Dimensionality Reduction technique which makes it easier to visualize the results of a dataset having many features.
Additionally, results on Quora dataset were also compared by generating the sentences from the encodings of the sentences used.


