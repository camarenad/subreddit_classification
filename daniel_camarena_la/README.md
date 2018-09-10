Background:
I scraped 400k total reddit comments. 200k from r/Libertarian which is 
a subreddit where folks discuss articles and ideas driving libertarian philosophy.
The other 200k come from r/LateStageCapitalism where folks go to discuss articles and idea's driving socialist philosophy. I chose these subreddit because both are populist 
movements but differ fundementally. LSC skews hard left, Libertarian skews hard right. These subs were interesting because I was able to pull an even amount of data from each and both had a similar number of subscribers which ensured rich dialogue.

Problem Statement:
The goal was to build a model with the ability to predict with resonable certainty which sub a comment originated from. This type of modeling has very important real world applications like topic modeling or spam filtering. 

Approach:
I used 4 models:
1. Logistic Regression 
2. Naive Bayes Multinomial - Production Model
3 Random Forrest
4.Descision Tree with and Ada boost

Results:
I was able to achieve decent results with all of my models. The simpler models acutally performed much better on this volume of data. By that I mean that my 
Logistic Regression and Naive Bayes had a much higher accuracy(>75%). My other classifiers still beat the mean but only by 10-12 points. This could just mean 
that I need to continue to refine those models.

In general all of the models do an ok job given the training data. When presented with data from either sub 3/4 of the time it predicts where it came from. With some further tuning this could be used to help flag spammy type posts from propaganda bots on reddit.

Future Considerations:
I would start training this model with articles and headlines commonly associated with each subreddit. I might also try to identify junk bot posts. During my eda I deleted posts made by bots. On the next go I would delete everything but posts made by bots, explore the word densities there and model on that to identify spammy keywords or identify topics of interest in each sub.

Sentiment analysis on the style of writing and comments from each subreddit would be an interesting addition. Paired with my current production model I might be able to identify spammy or propaganda based on a combination of keywords and sentiment. 

