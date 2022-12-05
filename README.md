# Machine Learning Class Project (Fall 2022)

Hashtag semantic mapping via dimensionality reduction.

[](images/profile_tags_50_umap_2_dimensions.png)

## Background

This project builds upon previous research ([Bots, Disinformation, and the First Trump Impeachment](https://arxiv.org/abs/2204.08915)), where we collected social media data from Twitter relating to the impeachment discussion.

Of the 3.6M users collected in this process, around 250K included at least one hashtag in their profile (~450K hashtags in total).

In this project, the goal is to use unsupervised machine learning techniques, such as dimensionality reduction, to compare the similarity of different hashtags.

We only care about the top hashtags, and can only practically plot around 100 or less at a time without the chart getting too crowded.

## Methods

See the [notebooks](notebooks/) directory for Python notebooks used to perform the analysis.

  1. First we fetch data from BigQuery, where we have a row per user per hashtag.
  2. Then we one-hot encode the raw data, using one row per hashtag and a column per user id.
  3. Then we apply dimensionality reduction to the one-hot encodings to shrink the number of dimensions from around ~200K users into the given number of dimensions (i.e. two or three).
  4. Finally, we plot these embeddings for visual comparison.

Attempted dimensionality reduction techniques include PCA, T-SNE, and UMAP, but only UMAP seemed to produce interesting results.



## Slides

Link TBA

## Website

https://s2t2.github.io/ml-project-2022/
