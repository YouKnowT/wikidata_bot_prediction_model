See the paper for full details of this work: https://www-users.cs.umn.edu/~hall1467/wikidata_bot_prediction.pdf

Our bot prediction results dataset can be found here: https://analytics.wikimedia.org/datasets/archive/public-datasets/wikidatawiki/bot_likelihood/



This combines results from anonymous and registered user datasets up to the beginning of May 2017.

The file has three columns. 
The first is a Wikidata revision id. 
The second is a boolean representing whether or not the revision was explicitly flagged as a bot (e.g. a bot user account). 
The third is based on the results of the application of our prediction model. 

Some values for this last column may be “\N” since we could only run our model on user “editing sessions” containing more than 2 edits (see the bot prediction paper forwarded earlier for more details — it has to do with model features that looked at times between edits. For example, the standard deviation of such times).

The likelihood estimates that I provide are not direct probabilities that a given edit is from a bot. Rather they correspond to what is considered to be a bot as the recall of the model is “shifted” in intervals of .1. This procedure is described in section 4.2 of the paper. See section 4.2.1 for recommendations as to what threshold is appropriate for your analyses.