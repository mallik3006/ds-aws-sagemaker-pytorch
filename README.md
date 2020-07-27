# DS-AWS-SageMaker-PyTorch


### Introduction

The goal of this project is to predict the sentiment of the entered movie review via a simple web page which a user can use to enter a movie review which will then sent to a deployed model. The Model will be deployed as an endpoint on AWS which will be invoked via a API Gateway that will trigger the Lambda function containing the inference code.


### Data

Data is downloaded from - [IMDb dataset](http://ai.stanford.edu/~amaas/data/sentiment/)
> Maas, Andrew L., et al. [Learning Word Vectors for Sentiment Analysis](http://ai.stanford.edu/~amaas/data/sentiment/). In _Proceedings of the 49th Annual Meeting of the Association for Computational Linguistics: Human Language Technologies_. Association for Computational Linguistics, 2011.
Dataset contains reviews for 25,000 movies.

### Libraries

* `nltk`
* `numpy`
* `BeautifulSoup`
* `sagemaker`
* `PyTorch`


### Repository Files 

* `SageMaker_sentiment_analysis.ipynb`: Notebook with text pre-processing, build and train PyTorch model with LSTM classifier, deploy model using AWS Lambda and API gateway.
* `train.py`: This has the training method that is called by the PyTorch training script. 
* `predict.py`: The inference script used for the actual prediction.
* `index.html`: Webpage that is utilized for entering a moview review to get the sentiment analysis prediction.
