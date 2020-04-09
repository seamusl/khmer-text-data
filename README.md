# khmer-text-data
Khmer unicode text data for unsupervised learning language model

This goal of this repos is serve as a collection of Khmer corpus that can be used to train Khmer language model. 
These text are already run through word segmentation to add space between words using Conditional Random Fields ([CRF](https://github.com/phylypo/segmentation-crf-khmer/tree/master/data)).

Corpus so far contains:
- km-wikipedia: Khmer wikipedia downloaded January 2020 (has 7.8 millions words, 110K lines)
- oscar: OSCAR Khmer text (has 10 millions words)
- classification: Khmer news article on traffic accident with labels using Pandas pickle format (has 238K words, 820 articles)

Some of the Khmer news articles can be found here:
https://github.com/phylypo/segmentation-crf-khmer/tree/master/data.
This repo has 2 sets of 1000 articles segmented using CRF from https://niptict.edu.kh/khmer-word-segmentation-tool/. See more detail post [here](https://medium.com/@phylypo/segmentation-of-khmer-text-using-conditional-random-fields-3a2d4d73956a).

It also contains some sample code to train BERT from scratch. 
See this [Python Notebook](https://github.com/phylypo/khmer-text-data/tree/master/bert-pretrain-from-scratch). It contains steps by steps to pretrain BERT on Khmer language.
- use Khmer news articles to pretain BERT using word masking
- use [classification](https://github.com/phylypo/khmer-text-data/tree/master/classifications) data to test the model with 99% accuracy for 2 classes
