# Text-Generation-using-VAE-Beta-VAE

There are several research papers showing that the results of beta-VAE on image encoding is much far better than that of VAE. But, there are uncertainity regarding the performance of beta-VAE and VAE on the task of text generation.
So, this project was an attempt to see and compare the preformance of beta-VAE and VAE on text encoding task.

Two datasets were used for this task: -
  1) Quora question-pair dataset https://www.kaggle.com/c/quora-question-pairs/data (this dataset is not considered good for text generation as sentences are very vague)
  2) Keras Moview review dataset with Sentiment Analysis.

Grid Search was used to set find a suitable beta (or kl-weight) for beta-VAE. The range of grid search was \[20, 250\]. `Beta = 100` was found to provide the best fit 
