---
layout: post
title: "Daj Się Poznać/Get Noticed! 2017. Week 2"
date: "2017-03-19 19:11:30 +0100"
tags: DSP2017
categories: coding deep-learning
---

# Update
This week comprises most of cleaning up my notebook and making sure I actually got my Kaggle submission file generation right.
If you compare my notebook to what was there for the first week, you will notice that my method of aligning image IDs with the
order they are processed by the network has changed; you will see that I check against the output given by `filenames()` method
of the generator (which is returned by `flow_from_directory()`), because it actually gives you the order in which images are sorted,
if you don't shuffle them of course.

Another thing is that I made a script to "clip" probabilities returned by my network to fit into [0.05, 0.95] range.
This is a trick to not get on the "bad side" of this competition's scoring function - it will punish you hard if you answer wrong
and are confident at it.

### [Week 2 notebook](https://github.com/danlupei/fastai-dl1-coursework/blob/master/nbs/week2.ipynb)
