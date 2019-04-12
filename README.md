# Daltix Test

## Instructions

The notebook jupyter is organized as follows:

1 - Load file: In this step it is necessary to set the path where it contains the file with the list of products (data/dataset.jsonl.gz)

2 - Process and clean the features: This is the part where we create and treat the variables chosen for modeling;

3 - Functions and measures: Here it was necessary to create some functions to calculate Cosine Similarity

4 - Output: Generation of the data frame for analysis of the results and also the process to treatment extract the data as requested in the test
      
      daltix_id_1,daltix_id_2
      aaff0aa6db24814ad25d5cb410ded08361ab32bcb953e1f81fd4f77affe7fe35,480e353eb638dbe8be37d04cf28b3b801eadccbd0ffaddec4f9bed10996d901f
      
5 - Validation: the same evaluation measure, provided by Daltix, was used. 


      len_validation = len(validation_set)
      len_submission = len(submission_set)
      tp = len(submission_set.intersection(validation_set))
      fp = len(submission_set - validation_set)
      recall = tp/len_validation
      precision = tp/len_submission
      fpr = fp/len_submission

      f1 = 2/((1/recall) + (1/precision))

## Requirements
    import pandas as pd
    import numpy as np
    import os
    import sparse_dot_topn
    import re
    import sklearn
    import scipy

 
