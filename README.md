# asonam2017


### Collected tweets

The dataset contains twitter posts about two premier UK music festivals: Creamfields 2016 (on August 25th-28th) and VFestival 2016 (on August 20th-21st). 

Both files **creamfields_tweets.json** and **vfestival_tweets.json** contain the ids of the tweets gathered for each festival. 
The tweets were collected using both the Streaming API and REST API provided by Twitter. To obtain tweets related to the
VFestival, we used the terms ‘vfest’ and ‘v21st’ as identifiers, while for the Creamfields event we used its own name. We used the Streaming API from August 10th to September 15th 2016, while the REST API was used to also collect the available past tweets from March 1st to September 15th 2016.


### Supervised dataset

The supervised dataset is split on the basis of their timestamp into three different disjoint sets: posts made before, during or after the event. 
For its generation, we randomly sample (without replacement) 460 distinct tweets for each task from each dataset, thus 1,380 tweets in total for each festival. Then, for each of the three tasks, a binary label is assigned to each tweet (positive class: a user who intends/is/has attended, and vice versa for the negative class).  This human assessment is based on the textual or visual content of the tweet that provide any explicit evidence of attendance at the event to be established.

The **supervised_dataset.csv** contains the following fields. 
* tweet_id. The id of the tweet.
* task. Defined according to the date wich the post was made (i.e. before, during or after the related event).
* label. The class of the labeled-tweet. The value 1 means a positive case of attendance. The value 0 means the opposite, not attendance. 
* event. The event which the post is related to. 
 


For further information, please contact us by email:

vcml@cin.ufpe.br
renso@isti.cnr.it
