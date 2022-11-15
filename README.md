# Tutorial of Collaborative Filtering in R (Community Contribution for EDAV)

## Motivation
For data science students, machine learning is always a potential career path they can take. Either work as a machine learning engineer or apply some machine learning techniques to their work. So this tutorial is meant to introduce a technique in machine learning, more specifically in the recommendation system, named collaboratively filtering. 

Collaboratively filtering uses algorithms to filter data from user reviews to make personalized recommendations for users with similar preferences, and it is widely being used by big companies. Netflix uses it to recommend movies or shows that you may like and Amazon uses it to match products to users based on past purchases.

## Need to Address
For this tutorial, I will walk through how to apply this technique in r by investigating the effects of three general parameters on accuracy and run time of collaborative filtering methods, which are n: number of users, m: number of items, and d: proportion of non-NA values.

I use four packages for this tutorial. rectools is a feature-filled packages of tools for recommendation system. qeML is a "quick and easy" wrapper for machine learning. Both pacakges are developed by professor Matloff at UC Davis. Then ggplot2 for plot visualization, and recosystem is a wrapper for "libmy" linrary for recommendation system using matrix factorization. Note: since rectools and qeML are not on CRAN yet, there two packages need to be installed through github repo: install_github('matloff/rectools') and install_github('matloff/qeML'). 

For this tutorial, I will use MovieLens 100k dataset and InstEval dataset, which contains 100000 movie ratings from 1000 users and 1700 movies and university lecture evaluations by students at ETH Zurich from 2972 students and 2160 lecturers or professors respectively. The rating has scale from 0 to 5 for both dataset. One can download the MovieLens dataset here https://grouplens.org/datasets/movielens/ and download the InstEval dataset here https://rdrr.io/cran/lme4/man/InstEval.html. Also, both dataset can be found under data directory. Then, I will use two models to do predictions for these dataset, one is linear model, and another one is matrix factorization.

## What I leanred
While both number of users and items have positive relationship with model accuracy, number of items affect the accuracy more. Also, a higher proportion of non-NA values results in better accuracy.

Note: all plots can be found under result directory for both datasets and both models.
