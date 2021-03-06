See the paper for full details of this work: https://www-users.cs.umn.edu/~hall1467/wikidata_bot_prediction.pdf

A bot prediction results dataset can be found here: https://analytics.wikimedia.org/datasets/archive/public-datasets/wikidatawiki/bot_likelihood/

This dataset actually combines two datasets: 1) results from application of the model to anonymous user edits and 2) results from application of the model to registered user edits. In both cases, the model was applied to revisions through the beginning of May 2017.

The file has three columns. The first column is a Wikidata revision id. The second column is a boolean representing whether or not the revision was explicitly flagged as a bot (e.g. a bot user account). The third/last column is based on the results of the application of our prediction model. 

Some values for this last column may be “\N” since we could only run our model on user “editing sessions” containing more than 2 edits (see the paper for more details).

The last column provides likelihood estimates. These are not direct probabilities that a given edit is from a bot. Rather they correspond to what is considered to be a bot as the recall of the model is “shifted” in intervals of .1. This concept is described in section 4.2 of the paper. See section 4.2.1 for recommendations as to what threshold is appropriate for your analyses.


Additionally, MODEL_TESTING_I2_FILTERED_predictors_and_labelled_data.tsv provides the testing data used on our completed model. predictors_and_labelled_data.tsv is our corresponding training datset.
